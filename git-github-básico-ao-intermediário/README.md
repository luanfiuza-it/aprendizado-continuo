# 🐙 Git e GitHub — Guia Básico ao Intermediário

## 📖 O que é Git?

O **Git** é um sistema de controle de versão distribuído criado para rastrear alterações em arquivos e projetos.

Com ele é possível:
- salvar versões do projeto
- voltar alterações
- trabalhar em equipe
- criar branches
- sincronizar código entre máquinas
- manter histórico completo de desenvolvimento

---

# ☁️ O que é GitHub?

O **GitHub** é uma plataforma online para hospedar repositórios Git.

Com ele é possível:
- armazenar projetos na nuvem
- compartilhar código
- colaborar com outras pessoas
- criar portfólio
- versionar projetos
- utilizar CI/CD
- publicar documentação

---

# ⚙️ Instalação do Git

---

# 🪟 Instalando Git no Windows

## Download oficial

https://git-scm.com/download/win

---

## Verificando instalação

Abrir PowerShell ou CMD:

```powershell
git --version
```

---

# 🐧 Instalando Git no Linux (Ubuntu/WSL2)

Atualizar pacotes:

```bash
sudo apt update
```

Instalar Git:

```bash
sudo apt install git -y
```

Verificar instalação:

```bash
git --version
```

---

# 👤 Configuração inicial do Git

## Configurar nome

```bash
git config --global user.name "SEU_USUARIO"
```

---

## Configurar email

```bash
git config --global user.email "seuemail@exemplo.com"
```

---

## Verificar configurações

```bash
git config --list
```

---

# 🔐 Configurando SSH com GitHub

## Gerar chave SSH

```bash
ssh-keygen -t ed25519 -C "seuemail@exemplo.com"
```

---

## Inicializar SSH Agent

```bash
eval "$(ssh-agent -s)"
```

---

## Adicionar chave SSH

```bash
ssh-add ~/.ssh/id_ed25519
```

---

## Exibir chave pública

```bash
cat ~/.ssh/id_ed25519.pub
```

Copiar e adicionar em:

https://github.com/settings/keys

---

# ✅ Testando conexão com GitHub

```bash
ssh -T git@github.com
```

Primeira conexão:

```text
yes
```

Resultado esperado:

```text
You've successfully authenticated
```

---

# 📂 Conceitos fundamentais do Git

---

# 📁 Repositório

Pasta controlada pelo Git.

Inicializar:

```bash
git init
```

---

# 📌 Staging Area

Área temporária onde arquivos ficam antes do commit.

Adicionar arquivos:

```bash
git add .
```

---

# 💾 Commit

Snapshot/versionamento do projeto.

Criar commit:

```bash
git commit -m "mensagem do commit"
```

---

# 🌿 Branch

Linha paralela de desenvolvimento.

Criar branch:

```bash
git branch nome-da-branch
```

Trocar branch:

```bash
git checkout nome-da-branch
```

Criar e trocar ao mesmo tempo:

```bash
git checkout -b nome-da-branch
```

---

# 🔄 Merge

Une branches diferentes.

```bash
git merge nome-da-branch
```

---

# ☁️ Remote

Ligação entre repositório local e GitHub.

Adicionar repositório remoto:

```bash
git remote add origin git@github.com:USUARIO/REPOSITORIO.git
```

---

# 🚀 Push

Envia commits para GitHub.

```bash
git push
```

Primeiro push:

```bash
git push -u origin main
```

---

# 📥 Pull

Baixa alterações do GitHub.

```bash
git pull
```

---

# 📥 Clone

Baixar um repositório existente.

```bash
git clone git@github.com:USUARIO/REPOSITORIO.git
```

---

# 🔍 Comandos essenciais

## Ver status

```bash
git status
```

---

## Ver histórico

```bash
git log
```

---

## Histórico resumido

```bash
git log --oneline
```

---

## Ver diferenças

```bash
git diff
```

---

## Ver branches

```bash
git branch
```

---

# 🧠 Fluxo básico de trabalho

```text
Editar arquivos
↓
git add .
↓
git commit -m "mensagem"
↓
git push
```

---

# 📂 Estrutura recomendada

## Windows

Projetos normalmente em:

```text
C:\Projetos
```

---

## Linux/WSL2

Projetos preferencialmente em:

```text
/home/usuario/projetos
```

Evitar:

```text
/mnt/c/
```

---

# 🚫 Arquivos que NÃO devem ir para o GitHub

Adicionar no `.gitignore`:
- senhas
- tokens
- `.env`
- builds
- cache
- dependências pesadas

Exemplo:

```gitignore
.env
node_modules/
dist/
__pycache__/
```

---

# 📘 Boas práticas

- fazer commits pequenos
- escrever mensagens claras
- usar branches para features
- não commitar arquivos sensíveis
- utilizar README.md
- manter projetos organizados

---

# 🔥 Conceitos intermediários importantes

## Rebase

Reorganiza histórico de commits.

```bash
git rebase main
```

---

## Stash

Guardar alterações temporariamente.

```bash
git stash
```

Recuperar:

```bash
git stash pop
```

---

## Reset

Voltar commits.

```bash
git reset --hard HEAD~1
```

⚠️ Remove alterações permanentemente.

---

# 📚 Links úteis

## Git Oficial
https://git-scm.com/

## GitHub
https://github.com/

## Documentação Git
https://git-scm.com/doc

## GitHub Docs
https://docs.github.com/

---

# 🎯 Resultado final

Ao dominar Git e GitHub é possível:
- versionar projetos profissionalmente
- colaborar em equipe
- criar portfólio
- trabalhar com DevOps
- utilizar CI/CD
- contribuir em projetos open source
- manter histórico seguro e organizado do código
