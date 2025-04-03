# Guia Completo de Git

## Introdução ao Git
Git é um sistema de controle de versão distribuído amplamente utilizado para rastrear alterações em arquivos e coordenar o trabalho entre desenvolvedores. Foi criado por Linus Torvalds em 2005 e é essencial para o desenvolvimento moderno de software.

## Instalação do Git
Para instalar o Git, siga os passos abaixo:

### Windows
1. Baixe o instalador em: [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Execute o instalador e siga as instruções na tela.
3. Verifique a instalação executando no terminal:
   ```sh
   git --version
   ```

### Linux (Ubuntu/Debian)
```sh
sudo apt update
sudo apt install git
```

### macOS
```sh
brew install git
```

## Configuração Inicial
Após instalar o Git, configure seu nome e e-mail:
```sh
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```
Verifique as configurações com:
```sh
git config --list
```

## Comandos Básicos do Git
### Criando um Repositório
```sh
git init
```
Cria um novo repositório Git na pasta atual.

### Clonando um Repositório
```sh
git clone URL
```
Baixa um repositório remoto para sua máquina.

### Status do Repositório
```sh
git status
```
Exibe o estado atual dos arquivos no repositório.

### Adicionando Arquivos ao Controle de Versão
```sh
git add nome_do_arquivo
```
Ou para adicionar todos os arquivos:
```sh
git add .
```

### Confirmando Mudanças (Commit)
```sh
git commit -m "Mensagem descritiva do commit"
```
Registra as mudanças no histórico do repositório.

### Visualizando Histórico de Commits
```sh
git log
```
Exibe o histórico de commits do repositório.

## Trabalhando com Branches
### Criando uma Nova Branch
```sh
git branch nome_da_branch
```

### Mudando para uma Branch
```sh
git checkout nome_da_branch
```
Ou:
```sh
git switch nome_da_branch
```

### Criando e Mudando para uma Nova Branch
```sh
git checkout -b nome_da_branch
```
Ou:
```sh
git switch -c nome_da_branch
```

### Mesclando Branches
```sh
git merge nome_da_branch
```

### Deletando uma Branch
```sh
git branch -d nome_da_branch
```

## Trabalhando com Repositórios Remotos
### Adicionando um Repositório Remoto
```sh
git remote add origin URL
```

### Enviando Mudanças para o Repositório Remoto
```sh
git push origin nome_da_branch
```

### Atualizando o Repositório Local
```sh
git pull origin nome_da_branch
```

## Resolvendo Conflitos
Quando dois desenvolvedores modificam o mesmo arquivo, um conflito pode ocorrer. O Git indicará quais arquivos estão em conflito. Para resolvê-los:
1. Edite os arquivos conflitantes e escolha as alterações corretas.
2. Marque os arquivos como resolvidos:
   ```sh
   git add nome_do_arquivo
   ```
3. Finalize o processo com um commit:
   ```sh
   git commit -m "Resolvendo conflito"
   ```

## Usando .gitignore
Crie um arquivo `.gitignore` na raiz do projeto para ignorar arquivos indesejados, como:
```
node_modules/
.env
*.log
```
Isso impede que arquivos desnecessários sejam adicionados ao repositório.

## Git Revert vs. Git Reset
### Revertendo um Commit (Mantendo Histórico)
```sh
git revert ID_DO_COMMIT
```
Cria um novo commit que desfaz as mudanças do commit específico.

### Resetando um Commit (Apagando do Histórico)
```sh
git reset --hard ID_DO_COMMIT
```
Isso remove o commit e todas as alterações subsequentes.

## Conclusão
O Git é uma ferramenta poderosa para gerenciar código-fonte e colaborar em projetos. Este guia cobriu os principais comandos e conceitos para iniciar. Pratique e explore mais funcionalidades para se tornar um especialista!
