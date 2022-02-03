# Comandos GIT

## Aula 1
### Branches
+ **DICA - VIAULIZING GIT:** ferramenta visual para entender melhor a movimentação dos commits e branches https://git-school.github.io/visualizing-git/
+ **git switch -c \<nome da branch>** ou **git checkout -b \<nome da branch>** cria e acessa a branch indicada (ignorar a barra)
+ **git switch \<nome da branch>** ou **git checkout \<nome da branch>**: alterna para a branch indicada (ignorar a barra)
+ **git branch -d \<nome da branch>** remove a branch indicada
+ **git branch:** lista as branches existentes no repositório local

## Aula 2
### Git Stash
+ **git stash save "nome-da-stash":** salva em um stash os arquivos ainda não comitados. Esses arquivo também ficam no index
+ **git stash list: ** exibe os stashes existentes
+ **git stash pop: ** recupera os arquivos que estão em um stash
+ **git stash delete: ** deleta um stash de acordo com a sua posição no index

### git log
+ **git log:** lista as alterações de um repositório
+ **git log nome-da-pasta: ** lista as alterações na pasta indicada
+ **git log nome-do-arquivo: ** lista as alterações no arquivo indicado
+ **git log --oneline:** traz o histórico de commits de forma resumida
+ **git log --graph:** traz de forma mais visual o histórico de commits realizados
+ **gitk:** inicializa uma ferramenta gráfica que permite visualizar melhor os commits, as branchs e as operações realizadas nelas

## Aula 3
### Revertendo commits - git reset
+ É possível usar o **git reset** orientando pelo sha1 ou a HEAD
+ **git reset --soft:** faz o processo inverso do git add, retornando para o staging/index os arquivos do commit indicado. Ex: git reset --soft HEAD~1
+ **git reset --mixed:** é a operação default do git reset (caso o reset seja omitido, ele executará essa flag) e retorna os arquivos para a working directory, ou seja, a unstaged area.
+ **git reset --hard:** exclui os arquivos existentes no commit indicado

### Revertendo commits - git revert
+ Manipula os commits revertendo as alterações, não arquivos
+ É possível usar o **git revert** orientando pelo sha1 ou a HEAD

## Aula 4
### Revertendo commits
+ 
