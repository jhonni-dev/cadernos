#Comandos GIT

###Branches
+ **git switch -c \<nome da branch>** ou **git checkout -b \<nome da branch>** cria e acessa a branch indicada (ignorar a barra)
+ **git switch \<nome da branch>** ou **git checkout \<nome da branch>**: alterna para a branch indicada (ignorar a barra)
+ **git branch -d \<nome da branch>** remove a branch indicada
+ **git branch:** lista as branches existentes no repositório local
+ 

### git stash
+ **git stash save "nome-da-stash":** salva em um stash os arquivos ainda não comitados. Esses arquivo também ficam no index
+ **git stash list: ** exibe os stashes existentes
+ **git stash pop: ** recupera os arquivos que estão em um stash
+ **git stash delete: ** deleta um stash de acordo com a sua posição no index

