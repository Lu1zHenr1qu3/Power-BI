# 🚀 Guia para Criar Repositório no GitHub

Siga estes passos para criar e configurar seu repositório no GitHub:

## 📋 Passo 1: Criar Repositório no GitHub

1. Acesse [GitHub.com](https://github.com) e faça login
2. Clique no botão **"+"** no canto superior direito
3. Selecione **"New repository"**
4. Preencha as informações:
   - **Repository name:** `power-bi-projects` (ou o nome que preferir)
   - **Description:** `Coleção de projetos Power BI desenvolvidos durante cursos da Alura`
   - **Visibilidade:** Escolha **Public** ou **Private**
   - **⚠️ NÃO marque** "Add a README file" (já criamos um)
   - **⚠️ NÃO adicione** .gitignore ou licença (já criamos)
5. Clique em **"Create repository"**

## 📋 Passo 2: Inicializar Git Localmente

Abra o PowerShell ou Terminal na pasta do projeto e execute:

```powershell
# Inicializar repositório Git
git init

# Adicionar todos os arquivos
git add .

# Criar primeiro commit
git commit -m "Initial commit: Power BI projects portfolio"

# Renomear branch principal (opcional, mas recomendado)
git branch -M main
```

## 📋 Passo 3: Conectar ao GitHub

No GitHub, após criar o repositório, você verá uma página com comandos. Execute:

```powershell
# Adicionar repositório remoto (substitua SEU_USUARIO pelo seu username do GitHub)
git remote add origin https://github.com/SEU_USUARIO/power-bi-projects.git

# Enviar código para o GitHub
git push -u origin main
```

**Alternativa usando SSH:**
```powershell
git remote add origin git@github.com:SEU_USUARIO/power-bi-projects.git
git push -u origin main
```

## 📋 Passo 4: Verificar

1. Acesse seu repositório no GitHub
2. Verifique se todos os arquivos foram enviados corretamente
3. Confirme que o README.md está sendo exibido

## 🔧 Comandos Úteis Futuros

```powershell
# Ver status dos arquivos
git status

# Adicionar arquivos específicos
git add "caminho/do/arquivo.pbix"

# Fazer commit de alterações
git commit -m "Descrição das alterações"

# Enviar para o GitHub
git push

# Ver histórico de commits
git log

# Criar nova branch
git checkout -b nova-feature

# Voltar para branch principal
git checkout main
```

## ⚠️ Observações Importantes

1. **Arquivos .pbix** são binários e podem ser grandes. O GitHub tem limite de 100MB por arquivo
2. Se algum arquivo for muito grande, considere usar **Git LFS** (Large File Storage)
3. Para usar Git LFS:
   ```powershell
   git lfs install
   git lfs track "*.pbix"
   git add .gitattributes
   git commit -m "Add Git LFS tracking for .pbix files"
   ```

## 🆘 Solução de Problemas

### Erro: "Repository not found"
- Verifique se o nome do usuário está correto
- Confirme que você tem permissão de acesso ao repositório

### Erro: "Authentication failed"
- Use um **Personal Access Token** em vez de senha
- Crie um token em: GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
- Use o token como senha ao fazer push

### Arquivo muito grande
- Use Git LFS para arquivos .pbix grandes
- Ou remova arquivos grandes do histórico se não forem necessários

---

**Boa sorte com seu repositório! 🎉**
