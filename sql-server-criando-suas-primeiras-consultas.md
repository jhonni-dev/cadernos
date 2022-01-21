## Aula 1

### O que é SQL Server

+ Bancos de dados relacionais (**SQL**): fornecem uma melhor garantia de dados
+ Bancos NoSQL: melhores em performance
+ Um banco SQL possui linhas e colunas
+ Atomicidade: é a garantia de que os dados estão corretos para introduzir no banco de dados
+ Consistência dos dados: é a garantia de que os dados são consistentes em vários bancos
  + Bancos SQL: se preocupam com a consistência de dados
  + Bancos NoSQL: não se preocupam com a consistência de dados

## Aula 3

### Comandos básicos - SQL Server Management Studio

+ **Criar banco de dados:** create database nome-do-banco
+ **Acessar banco de dados:** use *nome-do-banco*
+ **Criar tabela:** create table *nome-da-tabela*(nome-da-coluna tipo-da-coluna null/not null)
  + o *null* ou *not null* a frente do tipo na criação de tabelas indica se aceita ou não o tipo nulo, ou seja, a ausência de valores
+ **Apagar tabela:** drop table *nome-da-tabela*
+ Tipos de dados:
  + **int:**
  + **bigint:**
  + **varchar:**
  + **char:**

## Aula 4

### Comandos *insert, select, update, delete*

+ **Selecionar: ** **select ** *nome-da-coluna ou asterisco para todos* **from** *nome-da-tabela* 
  + **Alt+F1 (com o nome-da-tabela selecionado):** acessa mais informações da tabela
+ **Inserir:** **insert into** *nome-da-tabela*(colunas a serem inseridas) **values** (valores dos atributos);
+ **Atualizar:** **update** *nome-da-tabela* **set** *colunas e valores a serem alterados* **where** *coluna e valor de referência*
  + Se fizer um *update* sem a cláusula *where*, todos os registros da tabela serão afetados
+ **Deletar:** 
  + todos os registros: **delete from** *nome da tabela*
  + campos selecionados: use a cláusula *where*. Exemplo: **delete from** *nome da tabela* **where** *registro(s) a ser(em) alterado(s)*

### Especificidades do comando *select*

+ funções são métodos encapsulados que contêm uma dinâmica própria
+ O ideal é sempre indicar as colunas que você está inserindo
+ Função **isnull:** retorna uma ação caso algum parâmetro seja nulo
+ Função **convert:** convert(*tipo-convertido, nome-da-coluna*)



## Aula 5

### Normalizando dados

+ **Chave primária:** é uma forma de identificar um registro, sendo uma chave única para cada registro e gera uma melhor performance na busca por indexar todos registros
  + única:
  + composta:
+ **Chave estrangeira:** é uma chave que faz a relação de uma tabela com outra tabela
  + Uma chave estrangeira sempre será uma cópia de uma chave primária de mesmo tipo e mesma quantidade

+ alter table Clientes add constraint pk_clientes primary key(Codigo)

### Fases da normalização de dados

+ Não deve haver um conjunto de colunas repetidos ou um conjunto de informações em apenas uma propriedade. Não pode guardar uma coluna multivalorada
+ Não pode haver informações duplicadas que dependam da chave primária
+ Um relacionamento se dá pela forma de identificar as informações e como elas se relacionam



## Aula 6

### Trabalhando com tabelas relacionais

+ **inner join:** analisa linha a linha e retorna os elementos comuns das tabelas
+ **left join:** traz todas informações na tabela a esquerda e se houver elementos comuns ele coloca na tabela a direita. Se não houver elementos comuns, preenche com NULL
+ **right join:** traz todas informações na tabela a esquerda e se houver elementos comuns ele coloca na tabela a esquerda. Se não houver elementos comuns, preenche com NULL
+ **Somar:** select sum (*coluna_1* * *coluna_2*)
+ **Média:** **avg** (*coluna*)
+ **Contar linhas:** **count(*)**
+ **Agrupar:** group by
+ **Ordenar:** order by
+ **having**
