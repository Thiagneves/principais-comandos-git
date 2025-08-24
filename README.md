# 📘 Git – Principais Comandos

## 🔍 Verificar instalação do Git

```bash
git version
```

---

## 📂 Comandos Principais do Git

### 🔹 git clone
Clona um repositório remoto (ex.: GitHub) para a máquina local.

```bash
git clone <url_do_projeto>

# Exemplo:
git clone https://github.com/Thiagneves/Thiagneves.git
```

---

### 🔹 git init
Inicia o Git em um projeto, criando a pasta oculta `.git`.

```bash
git init
```

---

### 🔹 git add
Adiciona arquivos ou pastas à área de *staging* (preparação para commit).

```bash
# Adicionar um arquivo
git add index.html

# Adicionar uma pasta
git add assets

# Adicionar todos os arquivos
git add .
```

---

### 🔹 git status
Mostra o que está no *staging* e o que ainda não foi adicionado.

```bash
git status
```

Remover arquivos do *staging*:

```bash
git rm --cached <arquivo_ou_pasta>
```

---

### 🔹 git commit
Cria um **ponto de salvamento** no histórico do repositório.

```bash
git commit -m "mensagem_do_commit"

# Exemplo
git commit -m "feat(auth): create login screen"
```

📌 Dica: Use padrões como [Conventional Commits Pattern](https://medium.com/linkapi-solutions/conventional-commits-pattern-3778d1a1e657).

Ver commits já realizados:

```bash
git log
```

---

### 🔹 git branch -M main
Renomeia a branch atual para **main** (usada como branch principal no GitHub).

```bash
git branch -M main
```

---

### 🔹 git remote add origin
Conecta o repositório local a um repositório remoto.

```bash
git remote add origin https://github.com/Thiagneves/principais-comandos-git.git
```

Ver remotos configurados:

```bash
git remote -v
```

➡️ Se der erro de remote já existente:

```bash
# Alterar a URL
git remote set-url origin <nova-url>

# Remover e adicionar de novo
git remote remove origin
git remote add origin <nova-url>

# Criar outro remoto
git remote add github <url>
```

---

### 🔹 git push
Envia commits locais para o repositório remoto.

```bash
# Primeiro envio
git push -u origin <nome_da_branch>

# Próximos envios
git push

# Sem -u (precisa informar a branch sempre)
git push origin <nome_da_branch>
```

---

### 🔹 git pull
Atualiza seu repositório local com as mudanças do remoto.

```bash
git pull

# Caso não tenha configurado o upstream
git pull origin <nome_da_branch>
```

---

### 🔹 git checkout
Troca de branch ou cria uma nova.

```bash
# Mudar de branch
git checkout <nome_da_branch>

# Criar e mudar para nova branch
git checkout -b <nome_da_branch>
```

---

### 🔹 git branch
Gerencia branches locais.

```bash
# Listar branches
git branch

# Deletar branch local
git branch -D <nome_da_branch>

# Deletar branch remota
git push --delete origin <nome_da_branch>
```

📌 Saiba mais: [O que é uma branch](https://www.notion.so/Entenda-o-que-uma-branch-259c12cc61c08027b2fcd9679aea84d1?pvs=21)

---

## 🚀 Fluxo Básico de Uso do Git

1. **Inicie o repositório**
   ```bash
   git init
   ```

2. **Adicione os arquivos**
   ```bash
   git add .
   ```

3. **Faça o commit inicial**
   ```bash
   git commit -m "chore: primeiro commit"
   ```

4. **Renomeie a branch para main**
   ```bash
   git branch -M main
   ```

5. **Conecte ao repositório remoto**
   ```bash
   git remote add origin https://github.com/usuario/repositorio.git
   ```

6. **Envie os arquivos para o GitHub**
   ```bash
   git push -u origin main
   ```

7. **Nos próximos commits**
   ```bash
   git add .
   git commit -m "feat: nova funcionalidade"
   git push
   ```

---

Para elaborar este estudo, utilizei cursos e também sites. Para auxiliar na formatação, utilizei o ChatGPT apenas para organizar o conteúdo e deixá-lo esteticamente mais bonito. Obs: abra o index.html
