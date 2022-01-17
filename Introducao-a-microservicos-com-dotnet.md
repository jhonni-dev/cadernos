Introdução a Microserviços com .NET

## Conceitos Iniciais sobre Microserviços e Monolitos
+ Microserviços foram criados com o intuito de agilizar
+ Monolito é uma estrutura geológica, como uma montanha, constituído por uma única e macica pedra ou rocha
  + Rápido e fácil para iniciar
  + Infraestrutura simples
  + Debug fascinante
  + Problema com merge-conflicts
  + Conexão simultânea TCP é limitada
  + Deadlock e concorrência
  + Bugs e defeitos colaterais (único ponto de falha)
  + Build/Deploy longos e pesados
  + **Principal problema: Baixa escalabilidade**
  + Agregação de tecnologia
  + Demora de aculturamento
+ **Greenfield:** Começar um projeto do zero

## Escalabilidade Vertical x Horizontal
+ **Escalabilidade Vertical:** Escalabilidade de lata, comprar hardware
+ **Escalabilidade Horizontal:** Load balancer que funciona também como firewall
+ Referência: Martin Fowler
  + Uma aplicação monolítica coloca todas as funcionalidades dentro de um processo único e escala por replicação dos múltiplos servidores monolíticos
  + Uma arquitetura de microserviços coloca cada elemento de funcioinalidade dentro de serviços separados e escala distribuindo estes serviços através dos servidores, replicando conforme necessário

## Manifesto Ágil e Ciclos de desenvolvimento
+ Microserviço é uma forma de desenvolvimento ágil
+ Recomendação de livro: Desenvolvimento ágil Limpo - De volta às origens de Bob Martin
+ LIN: Desenvolvimento, Aprendizado, Feedback. Tudo em ciclos menores
+ DevOps: Build, Code, Plan, Monitor, Operarat, Deploy, Release, Test

## Ecossistema de microserviços
+ Para cada microserviços é preciso ter um Banco de Dados
+ Domínio: Questões de negócio
+ Escalabilidade
+ Segregação de contexto: apesar de interligados os sistemas precisar ser segregados

## O que é uma API pública e como se itneragem
+ Quando se chama uma API de outro servidor
+ Microserviços podem e DEVEM ser poliglotas em seus stacks
+ A flexibilidade tem que ser baseada numa necessidade de negócio e não técnoloógica
+ Microserviços encapsulam Estado (dados)  e Comportamento (regras de negócios) para resultar na Capacidade de Negócios
+ Microserviços possuem deploy independentes
+ Microserviços devem ter tratamentos isolados à falhas

## Dúvidas
+ A flexibilidade do microserviço se deve ao objeto do negócio
+ Os microserviços são diferentes serviços dentro de um sistema super desmembrado e comunicações esternas com outros sistemas/bancos
+ Microserviços podem comunicar-se internamente ou consumir outros microserviços externos

## Como dividir um monolito em microsserviços
+ **DDD (Domain Drive Design):** 
+ **Bounded Context:** não precisa necessariamente usar o modelo DDD
  + Quando se divide um domínio, os dados e responsabilidades também são divididos
  + Maintaining Model Integrity
    + Mapa de contexto: são todos domínios e todos contextos dentro da aplicação
    + Anticorruption Layer: Importante para a comunicação entre serviços
    + Shared Kernel: 

## Dúvidas
+ Tarefas síncronas são tarefas de leitura de informações
+ Para escrita ou exclusão não precisa ser síncrona
+ Há perda de performance com microserviços
+ Ferramentas de medição de latência existem para monitorar a jorney
+ 
