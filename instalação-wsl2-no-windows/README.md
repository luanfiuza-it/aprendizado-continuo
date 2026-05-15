# 🐧 Instalação e Configuração do WSL2 no Windows

# 🐧 O que é WSL2?

O **WSL2 (Windows Subsystem for Linux 2)** permite rodar uma distribuição Linux diretamente dentro do Windows, sem precisar utilizar máquina virtual pesada ou dual boot.

Com ele é possível:

- utilizar um terminal Linux nativo
- programar em um ambiente Linux real
- usar ferramentas como Git, Docker, Python e Node.js
- estudar desenvolvimento e cibersegurança com mais facilidade
- integrar Linux e Windows no mesmo ambiente de trabalho

Este repositório documenta meu processo de instalação e configuração do ambiente Linux utilizando o WSL2 no Windows.

O objetivo foi criar um ambiente leve e funcional para:
- desenvolvimento
- estudos de Python
- Git/GitHub
- cibersegurança
- terminal Linux

---

# ⚙️ Ambiente utilizado

- Windows 11
- WSL2
- Ubuntu
- Windows Terminal
- ZSH
- Starship Prompt

---

# 🚀 Instalação do WSL2

## 1. Abrindo o PowerShell como administrador

Executar:

```powershell
wsl --install
```

Na primeira execução o Windows apenas habilitou:
- Plataforma de Máquina Virtual
- Subsistema do Windows para Linux

Depois foi necessário reiniciar o computador.

---

## 2. Finalizando instalação

Após reiniciar o sistema:

```powershell
wsl --install
```

O Windows:
- baixou o kernel do WSL2
- instalou o Ubuntu
- configurou automaticamente o ambiente Linux

---

# 🐧 Configuração inicial do Ubuntu

Durante a primeira inicialização:
- criação do usuário Linux
- definição de senha

---

# 📦 Atualização do sistema

```bash
sudo apt update
```

---

# 🔧 Instalação do Git

```bash
sudo apt install git -y
```

Verificando versão:

```bash
git --version
```

---

# 👤 Configuração do Git

## Nome de usuário

```bash
git config --global user.name "luanfiuza-it"
```

## Email

```bash
git config --global user.email "luanfiuza.it@gmail.com"
```

## Verificar configurações

```bash
git config --list
```

---

# 🔐 Configuração SSH para GitHub

## Gerando chave SSH

```bash
ssh-keygen -t ed25519 -C "luanfiuza.it@gmail.com"
```

---

## Inicializando SSH Agent

```bash
eval "$(ssh-agent -s)"
```

---

## Adicionando chave SSH

```bash
ssh-add ~/.ssh/id_ed25519
```

---

## Exibindo chave pública

```bash
cat ~/.ssh/id_ed25519.pub
```

Copiar a chave e adicionar no GitHub:
- Settings
- SSH and GPG keys
- New SSH Key

---

# ✅ Testando conexão com GitHub

```bash
ssh -T git@github.com
```

Na primeira conexão:

```text
yes
```

Se estiver tudo correto:

```text
You've successfully authenticated
```

---

# 💻 Personalização do terminal

## ZSH

Shell utilizado para substituir o Bash padrão.

## Starship

Prompt minimalista e altamente customizável.

## Zinit

Gerenciador de plugins do ZSH.

## Zsh Completions

Autocompletar avançado para comandos no terminal.

---

# 📂 Organização dos projetos

Projetos devem ficar preferencialmente dentro do Linux:

```text
/home/usuario/
```

Evitar trabalhar dentro de:

```text
/mnt/c/
```

pois o desempenho no WSL2 costuma ser inferior.

---

# 📚 Links utilizados

## WSL2
https://learn.microsoft.com/pt-br/windows/wsl/

## Executar aplicativos GUI no WSL2
https://learn.microsoft.com/pt-br/windows/wsl/tutorials/gui-apps

## ZSH
https://github.com/ohmyzsh/ohmyzsh/wiki

## Starship
https://starship.rs/

## Zinit
https://github.com/zdharma-continuum/zinit

## Zsh Completions
https://github.com/zsh-users/zsh-completions

## Vídeo utilizado como base
https://youtu.be/PeiWB1xCS6w?si=6SR9nsMfonTPQ-06

---

# 🎯 Resultado final

Ao final da configuração:
- WSL2 funcionando
- Ubuntu instalado
- Git configurado
- GitHub conectado via SSH
- terminal customizado
- ambiente pronto para estudos e desenvolvimento
