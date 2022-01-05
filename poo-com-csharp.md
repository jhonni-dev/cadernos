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

## Aula 7
### Interfaces
+ Uma interface é um contrato que pode ser implementado por uma classe.
+ É como se fosse uma classe abstrata, podendo definir métodos abstratos para serem implementados.
+ Assim como uma classe abstrata, uma interface **não pode ser instanciada**
+ É possível definir os métodos diretamente na interface, tornando opcional implementar na classe

## Aula 8
### Arquivos
+ O C# nos apresenta algumas **classes estáticas** (não é preciso instaciá-las) que facilitam o trabalho com arquivos, dentre elas
  + **File** (Manipular arquivos)
    + Listar arquivos: Directory.GetFiles()
    + Criar arquivo de texto: File.WriteAllText()
    + Testa se arquivo existe(retorna true ou false): File.Exists()
    + Criar arquivo texto com stream: File.CreateText()
      + Quando se usa uma stream, a gente coloca ela em memória e prepara para ser escrita. Dessa forma, quando termina de usar o arquivo ele tem que ser encerrado para liberar espaço na memória.
      + Para tal usá-se o *using*, que garante o arquivo seja liberado para outro processo poder trabalhar
      + Para criar uma lista de string:List\<string>\ {} // OBS: as barras são para ignorar as tags neste arquivo MD
    + **Adicionar novas linhas em um arquivo:**
      + **Sem stream:** File.AppendAllText()
      + **Com stream:** File.AppendText()
    + **Ler arquivos:** 
      + **Sem stream:** File.ReadAllLines()
      + **Com stream:** (var).ReadLine() //É preciso usar o *using*
    + **Mover arquivos:** File.Move(local, destino)
      + É possível renomear o arquivo ao movê-lo, basta apenas inserir um terceiro parâmetro logo após o destino.
      + Não é permitido sobrescrever um arquivo com o mesmo nome a menos que seja forçado através de um *true* no terceiro parâmetro)
    + **Copiar arquivos:** File.Copy(local, destino)
      + Não é permitido sobrescrever um arquivo com o mesmo nome a menos que seja forçado através de um *true* no terceiro parâmetro)
    + **Deletar arquivo:** File.Delete()
  + **Directory** (Operações com diretórios)
    + Listar diretórios: Directory.GetDirectories()
    + Criar diretórios: Directory.CreateDirectory()
    + Apagar diretório: Directory.Delete()
      + Se tentar apagar um diretório que não está vazio, será apresentado um erro. Para validar que você quer de fato excluir um diretório que contém arquivos é preciso criar uma variável do tipo **bool** dentro do método e setá-la como **true**
      + Nâo é possível recuperar os arquivos depois de apagar um diretório pelo .NET
  + **Path** (Organizar os caminhos de maneira lógica)
    + Organizar os diretórios em pastas e subpastas: Path.Combine()
