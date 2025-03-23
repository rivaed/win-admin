
# Ativar Conta Administrador Oculta no Windows

**⚠️ AVISO LEGAL:**  
Este procedimento é destinado exclusivamente a profissionais de suporte, técnicos de TI, administradores de sistemas e usuários com autorização para realizar manutenção.  
**Não use este método para acessar sistemas sem permissão. O uso indevido pode configurar crime.**

---

## 🎯 Objetivo

Ativar a conta de usuário interno "Administrador" (em inglês: `Administrator`) que vem desativada por padrão nas versões modernas do Windows.

Essa conta possui privilégios totais e é útil para tarefas de recuperação, manutenção e diagnóstico do sistema.

---

## 🛠️ Como Ativar

1. **Abra o Prompt de Comando como Administrador:**
   - Pressione `Win + S`, digite `cmd`
   - Clique com o botão direito em "Prompt de Comando" e escolha **Executar como administrador**

2. **Digite o seguinte comando:**

   ```cmd
   net user administrador /active:yes
   ```

   (Em sistemas em inglês, substitua `administrador` por `administrator`)

3. **(Opcional) Defina uma senha para a conta:**

   ```cmd
   net user administrador *
   ```

   Você será solicitado a digitar a nova senha (duas vezes).

---

## 🔒 Como Desativar a Conta Depois

Se quiser desabilitar a conta novamente:

```cmd
net user administrador /active:no
```

---

## 🧠 Observações

- A conta "Administrador" aparece na tela de login apenas após ser ativada.
- Ela não possui UAC (controle de conta de usuário) habilitado por padrão.
- Recomendado definir senha forte imediatamente após ativação.
- Não use essa conta como login diário – apenas para manutenção.

---

## 🛡️ Ética e Responsabilidade

Este repositório é para **fins educativos e profissionais**.  
Jamais utilize este procedimento em máquinas que não lhe pertencem ou sem autorização expressa.

---

## 📄 Licença

Distribuído sob a licença [MIT](LICENSE).  
Este conteúdo é fornecido "como está", sem garantias.
```
