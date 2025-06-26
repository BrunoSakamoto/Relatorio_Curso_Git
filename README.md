# Git

```git init```: Inicia o git dentro de um diretório.

```git add```: Prepara mudanças para o próximo commit.

```git add arquivo.txt```: Adiciona apenas as mudanças do arquivo.txt.

```git add .```: Adiciona as mudanças do diretório atual.

```git commit -m "<mensagem do commit>"```: É usado para criar um commit no Git, com uma mensagem associada a ele.

```git log```: Exibe o histórico de commits do seu repositório.

```git --no-pager log -n <número limite>```: Limita a quantidade de commits a serem mostrados.

```git cat-file -p <hash>```: Permite ver o conteúdo de um commit sem precisar mexer diretamente nos arquivos de objeto.

### Entrada
```
git cat-file -p 2b96acc625c268f2655074750d1908f9a97f3388
```
### Saída
```
tree e0bf8212d8e6e1005d5ec2880088b3fa7879b660
author BrunoSakamoto <brunosakar2005@gmail.com> 1750874251 -0300
committer BrunoSakamoto <brunosakar2005@gmail.com> 1750874251 -0300

A: add contents.md
```

## Git Config

git config: comando para interagir com a configuração do git
```git config --list```: Lista todas as configurações ativas

```
git config --add --global user.name "github_username_here"
git config --add --global user.email "email@example.com"
```

### Comando parte por parte

```--add```: Adicionar uma configuração.

```--global```: Essa configuração será adiciconada globalmente em ```~/.gitconfig```.

```--local```: Essa configuração será adiciconada somente no repositório atual.

```user.name```: Adicionar o nome do usuário.

```user.email```: Adiciona o email do usuário .

### GET
```git config --list```: Buscar todos os valores das configurações.

```git config --get <key>```: Buscar um valor em específico.

### UNSET

```git config --unset <key>```: É usado para remover uma configuração.

## Localizações

Sistema: ```/etc/gitconfig``` um arquivo que configura o Git para todos os usuários do sistema.

Global: ```~/.gitconfig``` um arquivo que configura o Git para todos os projetos de um usuário.

Local: ```.git/config``` um arquivo que configura o Git para um projeto específico.

Worktree: ```.git/config.worktree``` um arquivo que configura o Git para parte de um projeto.

![image](https://github.com/user-attachments/assets/a523521d-7e5d-4e5e-846c-e98d8235e3e7)

- As informações adicionadas/alteradas na ***Worktreee*** sobrescrevem a ***Local***

- As informações adicionadas/alteradas na ***Local*** sobrescrevem a ***Global***

- As informações adicionadas/alteradas na ***Global*** sobrescrevem a ***Sistema***

## O que é uma branch?

Uma Git branch permite que você lide com diferentes alterações seperadamente.

```git branch```: Verifica qual é a branch atual.

```git branch -m <oldname> <newname>```: Serve para renomear a branch.

```git switch -c my_new_branch```: O comando ***switch***, permite que altere as branches e o ***-c*** faz com que seja criada uma nova.

## Merge
É usado para fazer mudanças de forma segura sem que afete a branch do seu time.

```
A - B - C    main
   \
    D - E    alteracoes
```

Para fazer o merge de ```alteracoes``` dentro de ```main```, é necessário executar esse comando enquanto estiver rodando a main:

```git merge alteracoes```

### Merge Log

```git log --oneline --decorate --graph --parents```: Este comando mostra o histórico de forma visual e com detalhes extras úteis para inspeções mais técnicas, como genealogia de merges.

## Git Reset

```git reset --soft <commitHash>```: Esse comando é usado para desfazer as mudanças dos últimos commits ou as mudanças do index.

```git reset --hard <commitHash>```: Esse comando é usadoa para desfazer as mudanças de um commit em específico.
## GitHub
### Remote

```git remote add <name> <uri>```: É usado para adicionar um repositório remoto ao seu repositório Git local.

### Git Push

```git push origin main```: Envia as mensagens locais para o repositório remoto.

### Git Pull

```git pull```: É usado para atualizar seu repositório local com as mudanças mais recentes do repositório remoto.

### Pull Request
No GitHub, um Pull Request é uma maneira de propor alterações, normalmente para o resto da sua equipe ou para o mantenedor de um projeto ao qual você está contribuindo.

### Merge Pull Request
Em um fluxo de trabalho de equipe, você pediria a um colega para revisar seu Pull Request. Se ele aprovasse as alterações, você estaria liberado para a mesclagem.

### Git Ignore
O arquivo ***.gitignore*** serve para informar ao Git quais arquivos ou pastas ele deve ignorar — ou seja, não rastrear, não versionar e não enviar ao repositório remoto.
