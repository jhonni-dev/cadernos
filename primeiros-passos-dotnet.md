# Aula .NET do bootcamp Avanade #2
*Primeiros passos com .NET*

## Aula 1
### O que é .NET?
- .Net é uma **infraestrutura** para desenvolvimento de software criada pela Microsoft
- Uma aplicação .NET é desenvolvida para e roda em uma das seguintes **impementações** do .NET:
> .NET Core
> .NET Framework
> Mono
> Universal Windows Plataform (UWP)

### Como
+ Cada implementação inclui um ou mais .NET Runtimes (ambientes de execução)
  + .NET Core: CoreCLR e CoreRT
  + .NET Framework: CLR
  + Mono: Mono Runtime
  + UWP: .NET Native
+ Atualmente a Microsoft desenvolve e suporta 3 linguagens para .NET: **C#, F# e VB**

### Onde
- Desktop: WPF, Windows Forms, UWP
- WEB: ASP.NET
- Cloud: Azure
- Mobile: Xamarin
- Gaming: Unity
- IoT: ARM32, ARM64
- AI: ML.NET, NET for Apacha Spark
- Tools: Visual Studio, Visual Studio for MAC, Visual Studio Code, Comand Line

## Aula 2
### Iniciando com .NET
- dotnet --version (mostra a versão instalada)
- dotnet --help (exibe comandos e sua sintaxe)
- dotnet --info (exibe todas as versões do dotnet instaladas)
- dotnet --add (adiciona um pacote ou uma referência a um projeto .NET)
- dotnet --build (cria um projeto do .NET)
- dotnet --new (cria um novo projeto ou arquivo do .NET)
- dotnet --nuget é um gerenciador de pacotes para .NET

### Criando uma aplicação console
+ **Criar uma aplicação console:** dotnet new console -n <nome da aplicação>  
+ explorer . : abre o local onde o terminal está rodando no windows explorer
+ Ao criar uma aplicação ele cria uma pasta de artefatos, um documento .csproj e um documento cs
+ code . : abre o conteúdo da pasta no VS Code
  + Ao executar este comando, o VS Code cria também uma pasta bin com os binários da aplicação
+ dotnet restore: restaura os pacotes atrelados ao projeto
+ dotnet build: também restaura os pacotes e compila, gera os binários e as dll's
+ dotnet run: restaura os pacotes, excuta o build e executa o main
  + Para funcionar o comando run, é preciso estar no mesmo nível de pastas do arquivo .csproj
+ Para dar um **build** fora do diretório onde está o arquivo .cdproj, é preciso especificar o diretório do arquivo, caso haja apenas um arquivo deste tipo na pasta
+ Para dar um **run** fora do diretório onde está o arquivo .cdproj, é preciso usar a flag -p **(ou --project no caso do .NET 6)** e especificar o diretório do arquivo

## Aula 3
### Conhecendo o C#
+ C# é uma linguagem elegante, orientada a obejtos e fortemente tipada
+ a sintaxe é similar a do C, C++ ou Java
+ Suporta os conceitos de encapsulamento, herança e polimorgismo (oo)
+ Os programas C# são executados no .NET, que inclui:
  + CLR *(Common Language Runtime)
  + Conjunto unificado de bibliotecas de classes
+ Atualmente o compilador do C# é o **Roslyn**

### Como funciona
+ O código-fonte escrito em C# é compilado em uma linguagem intermediária (IL)
+ O código e os recursos de IL sçao armazenados no disco em um arquivo executável chamado **assembly**, geramente com uma extensçai .exe ou .dll
+ Quando o programa C# é executado, o assembly é carregado no CLR
+ Em seguida, o CLR executará a compilação ***just in time*** (JIT) para converter o código IL em instruções de máquina nativas
+ O CLR também fornece outros serviços:
  + *Garbage Collector*
  + *Exception Handler*
  + *Resources Manager*
+ Além dos serviços de tempo de execução, o .NET também inclui uma extensa biblioteca com milhares de classes que fornecem uma ampla variedade de funcionalidades úteis, desde entrada e  saída de arquivos, manipulação de cadeias de caracteres, análise XML, etc...

### Estrutura de programa
+ Os principais conceitos organizacionais em C# são:
  + programas
  + *namespaces*
  + tipos
  + membros
  + *assemblies*
+ Programas C# consistem em um ou mais arquivos
+ Os programas declaram **tipos**, que  contêm **membros** e podem ser organizados em *namespaces*
  + Exemplos de tipos: Classes e interfaces
  + Exemplos de membros: Campos, métodos, propriedades e eventos

## Aula 4
### Tipos e Variáveis
+ Variáveis de tipos de valor contêm diretamente seus dados
+ As variáveis têm sua própria cópia dos dados e não é possível que as operações afetem outra variável (exceto no caso das variáveis de parâmetro *ref* e *out*)
+ Tipos **numéricos**: sbyte, short, int, long, byte, ushort, uint, ulong
+ Tipo **Caractere Unicode**: char
+ Ipos **Pontos Flutuantes**: float, double, decimal
+ Ipo **Booleano**: bool
+ Outros Tipos: enum, struct e nullable (exemplo int?)
+ Tipos de **Referência**: Variáveis de tipos de referência aramazenam referências a seus dados
  + É possível que duas variáveis façam referência ao mesmo objeto em, portanto, que operações em uma variável afetem o objeto referenciado pela outra variável.
  + Tipos **Classe**: class, object, string
  + Tipos **Arrays**: int[], int[,], etc...
  + interface, delegate

### Instruções:
+ Ações de um programa são expressas usando instruções 
+ Um bloco (escrito dentro de chaves {}), permite que várias instruções sejam escritas em contextos
+ Tipos de instruções:
  + Declaração de variáveis e constantes
  + Condicionais: *if, switch*
  + Laços de Repetição: *while, o*, for, foreach*
  + Auxiliares: *break, continue, return*
  + Tratativas de exceções: *throw, try.. catch.. finally*
  + Importar referências de pacotes e *namespaces: using* 
+ Comando *Dispose*: Elimina da memória os objetos não gerenciáveis
+ Para eliminar os objetos gerenciáveis, como classes e objetos, utiliza-se o *garbage collector*

### Array
+ Um **array** é uma estrutura de dados que contém um número X de **elementos**, todos do mesmo **tipo**, que são acessados através de **índices** computados
+ *Arrays* são tipos de referências e a declaração de uma variável *array* simplesmente reserva espaço para uma **referência** de uma instância de *array*
+ Ao criar um *array* é especificado o **tamanho** da nova instância, que é fixo durante todo o tempo de vida da instância
+ Os índices dos elementos de um *array* variam de **0** a **comprimento do array -1**

## Aula 5
### Classes e Objetos
+ Classes são os tipos mais fundamentais de C#
+ Uma classe é uma estrutura de dados que combina estado (campos) e ações (métodos)
+ Objetos são instâncias de uma classe
+ As classes suportam herança e polimorfismo, mecanismos pelos quais as classes derivadas podem estender e especializar as classes-base
+ Instâncias de classes (objetos) são criadas usando o operador new, que aloca memória para uma instância, chama um  construtor para inicializar a instância e retorna uma referência à instância
+ A memória ocupada por um objeto é recuperada automaticamente quando o objeto não estpa mais acessível. Não é necessário nem possível desalocar explicitamente objetos em C#
+ Os membros de uma classe podem ser estáticos ou membros da instância
+ Membros estáticos pertencem a classe e membros da instância pertencem ao objeto
+ São membros: constantes, variáveis, métodos, propriedades, construtores, etc
+ Cada membro de uma classe tem uma acessibilidade associadad, que controla as regiões do texto do programa que podem acessar o membro
+ Os tipos de acessibilidade podem ser: *public, protected, internal, private*
+ Uma declaração de classe pode especificar uma classe base, herdando os membro *public, internal e protected* da classe base
+ Omitir uma especificação de classe base é o mesmo que derivar do tipo object
+ Um método é um membro que implementa uma computação ou ação que pode ser executada por um objeto ou classe
+ Os métodos podem ter uma lista de parâmetros, que representam valores ou referências de variáveis passados para o método, e um tipo de retorno, que especifica o tipo do valor calculado e retornado pelo método

## Aula 6
### Structs
+ Como as classes, as *structs* são **estruturas de dados** que podem conter membros de dados e membros de ação, mas diferentemente das classes, as *structs* são tipos de valor e não requerem alocação de heap
+ Uma variável de um tipo de *struct* armazena diretamente os dados da estrutura, enquanto uma variável de um tipo de classe armazena uma referência a um objeto alocado na memória
+ *Structs* não aceitam herança determinada pelo desenvolvedor
+ São úteis para pequenas estruturas de dados que possuem semântica de valor como: números complexos, pontos em um sistema de coordenadas ou pares de chave-valor em um dicionário são bons exemplos de utilização
+ O uso de *structs* em vez de classes para pequenas estruturas de dados pode fazer uma grande diferença no número de alocações de memória 
+ Construtores de *structs* são chamados com o operador ***new***, semelhante a um construtor de classe, mas em vez de alocar dinamicamente um objeto no *heap* gerenciado e retornar uma referência a ele, um contrutor *struct* simplesmente retorna o próprio valor *struct* (normalmente em um local temporário na stack), e esse valor é copiado conforme necessário
+ www.eximiaco.tech/pt/category/fundamentos

### Interfaces
+ Uma interface define um contrato que pode ser implementado por classes e *structs*
+ Uma interface pode conter métodos, propriedades, eventos e indexadores
+ Uma interface não fornece implementações dos membros que define - apenas suas "assinaturas"
+ As interfaces podem empregar herança múltipla

### Enums
+ Um *enum* é um tipo de valor distinto com um conjunto de constantes nomeadas
+ Você define enumerações quando preciso definir um tipo que pode ter um conjunto de valores discretos. Eles usam um dos tipos de valor integral como armazenamento subjacente. Eles fornecem significado semântico aos valores discretos.
+ Cada tipo de *enum* possui um tipo integral correspondente chamado **tipo subjacente do tipo de *enum***
+ Um tipo de enumeração que não declara explicitamente um tipo subjacente tem um tipo subjacente *int*
