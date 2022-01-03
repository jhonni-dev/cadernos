# Programação Orientada a Objetos com C#

## Aula 1

### Conhecendo a POO
+ A **POO é um paradigma de programação**, ou seja, corresponde a uma **técnica de programção para um fim específico**.
+ Dentro desta técnica existem quatro pilares:
  + **Abstração** (aproxima o mundo real com o mundo da programação)
  + **Encapsulamento** 
  + **Herança**
  + **Polimorfismo**
+ O principal conceito da POO são **classes e objetos**
+ **Classe** é uma abstração, um molde de algo do mundo real que você queira **representar**, como a planta de uma casa
+ **Objeto** é a construção dessa classe, é casa em si, que é possível manipular
+ **Método** é a ação(ões) que o objeto pode executar

### Paradigmas de Programação
+ Paradigma de programação é diferente de linguagem de programação
+ Uma linguagem de programação implementa um ou mais paradigmas
+ Um paradigma nada mais é do que um **modelo de técnicas**, estruturas e formas de solucionar um problema
+ Tipos de paradigmas:
  + POO
  + Programação estruturada
  + Programação imperativa
  + Programação procedural
  + Programação orientada a eventos
  + Programação Lógica
  + ETC...

## Aula 2
### Abstração
+ Abstrair um objeto do mundo real para um contexto específico, considerando apenas os atributos importantes
+ Comandos: 
  + dotnet new sln --name "nomeDaSolucao" (criar nova solução)
  + Criar uma pasta para criar o console nela
  + dotnet new console
  + dotnet sln add "diretorio do arq. csproj" (linka a solução com o console).
  
## Aula 3
### Encapsulamento
+ O encapsulamento serve para proteger uma classe e definir limites para alteração de suas propriedades
+ Serve para ocultar seu comportamento e expor somente o necessário
  
## Aula 4
### Herança
+ A herança nos permite reutilizar atributos, métodos  comportamentos de uma classe em outras classes
+ Serve para agrupar objetos que são do mesmo tipo, porém com comportamentos diferentes

## Aula 5
### Polimorfismo
+ Polimorfismo vem do grego e significa "muitas formas".
+ Com o polimorfismo podemos sobrescrever métodos das classes filhas para que se comportem de maneira diferente e ter sua própria implementação
+ Existem dois tipos de polimorfismo:
  + Polimorfismo em **tempo de compilação (Overload/ Early Binding)**
  + Polimorfismo em **tempo de execução (Override/ Late Binding)**

## Aula 6
### Classes Abstratas
+ Uma classe abstrata tem como objeto **ser exclusivamente um modelo para ser herdado**, portanto não pode ser instanciada
+ Você pode implementar métodos (abstratos) ou deixá-los a cargo de quem herdar

### Classes Seladas
+ Uma classe sela tem como objetivo impedir que outras classes façam uma herança dela, ou seja, nenhuma classe pode ser sua derivada.
+ Também existem métodos e propriedades seladas.
+ No C#, se tentar herdar uma classe selada, será apresentado um erro e o programa não será compilado.

### Classe Object
+ A classe **System.Object** é a mãe de todas as classes na hierarquia do .NET
+ Todas as classes derivam, direta ou indiretamente da classe Object e ela tem como objetivo prover serviços de baixo nível para suas classes filhas, principalmente para operações com referência de memória, comparações, etc
+ É possível reescrever os métodos da classe Object usando o comando "public override ..."
