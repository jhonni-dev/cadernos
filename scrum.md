# SCRUM

## Aula 1
### Introdução ao SCRUM
+ **Parte 1 - Conceitos básicos**
  + O **Princípio de Pareto** também se aplica ao desenvolvimento de software, onde 20% das funcionalidades costumam gerar 80 % ou mais do benefício esperado.
  + **Gestão de projetos:**
    + **Resumo:** Em projetos tradicionais você corre o risco de descobrir que estava errado depois de meses. Com o SCRUM você descobre que estava errado em no máximo 30 dias 
    + Tradicional (waterfall): 
      + Só permite que o projeto avance quando uma fase está inteiramente completa
      + Escopo definido na fase inicial do projeto (Preditivo)
      + Projeto é controlado por fases e marcos
      + Cliente só vê o software funcionando na fase final do projeto
      + Resistência a mudanças
    + Ágil: 
      + Software construído por partes (incremental) e cada parte executa-se em um ciclo (iterativo)
      + Escopo definido ao longo do projeto (adaptativo)
      + Projeto écontrolado por funcionalidades entregues
      + Cliente pode ver parte do software funcionando na parte inicial do projeto
      + Mudanças constantes de acordo com feedbacks contínuos
  + **O que é ser ágil:**
    + Rapidez (mudança) e desembaraço, ter capacidade de responder rapidamente a mudanças
    + Fazer coisas complexas de forma simples
    + Equipe comprometida com os objetivos
    + **Maior valor para o cliente**
  + **SCRUM**
    + É um dos frameworks de gerenciamento de projetos ágeis
    + Projetos usando equipes pequenas e multidisciplinares produzem o melhor resultado
    + **Pilares:** Transparência, Adaptação e inspeção
    + Conversar mais e escrever menos (transparência)
    + Demonstrar o software constantemente aos usuários e obter feedbacks constantes (inspeção)
    + Requisitos mudam ao longo do tempo (adaptação)
    + Aprender progressivamente ao longo do tempo (adaptação)
  + **Razões para adotar o SCRUM:**
    + Desenvolvido e entregue em partes menores (2 a 4 semanas) com constante feedback dos usuários
    + Melhor gerenciamento de riscos (redução de incertezas)
    + Comprometimento, motivação e transparência da equipe (Dailly Meeting)
    + **Maior valor para o negócio (priorização do backlog)**
    + Usuários desenvolvidos durante todo o ciclo
    + Aplicação das lições aprendidas (melhoria contínua)
  + **Características do time SCRUM:**
    + Equipes capazes de se auto-organizarem
    + As tarefas são do time e todos são responsáveis
    + Forte comprometimento com os resultados
  + **Por que as Startups utilizam framework ágil?**
    + MVP (Minimum Viable Product), entrega o produto mínimo viável que o usuário consiga fazer uso e evoluir o produto

+ **Parte 2 - Papéis e responsabilidades de cada um do time**
  + **Product Owner (PO)**
    + Representa a área de negócios
    + PO é uma pessoa, não um comitê
    + Define as funcionalidades do software (Product Backlog)
    + Prioriza as funcionalidades de acordo com o valor de negócio
    + garante que o time de DEV entenda os itens do Backlog no nível necessário
  + **Scrum Master (SM)**
    + Garantir o suo correto do SCRUM
    + SM não é gerente de projetos
    + Age como um facilitador
    + Auxilia o PO no planejamento e estimativas do backlog
    + Auxilia a equipe a remover impedimentos
    + Treina o time em autogerenciamento e interdisciplinaridade
  + **Time de Desenvolvimento (DEV)**
    + Possui habilidades suficientes para desenvolver, testar, criar e desenhar, ou seja, tudo que for necessário para entregar o software funcionando

+ **Parte 3 - Cerimônias do SCRUM**
  + **Time Box:** Tempo máximo definido para fazer uma cerimônia ou todo desenvolvimento em uma Sprint
  + **Sprint:** Corrida, arrancada. É o principal evento da SCRUM e tem duração de 30 dias corridos ou menos
    + Composição de uma Sprint:
      + **Planejamento da Sprint(1º dia da Sprint):** 
        + Participa o PO, SM e DEV. 
        + Time box de 8 horas dividas em 2 partes iguais contendo O QUE fazer(4h) e COMO fazer(4h, time DEV)
        + Planning Poker: Cada membro opina com uma estimativa do tempo de cada tarefa e entram num consenso geral do tempo para cada uma delas. O time devolve pro PO o que consegue entregar na Sprint
      + **Reuniões Diárias (Daily Meeting)**
        + Dura no máximo 15 minutos 
        + É uma reunião em pé que ocorre no mesmo horário e local 
        + DEV: diz o que foi feito no dia anterior, o que está programado no dia, o que tem a fazer e se existe algum impedimento
        + Quadro Kanban: feito, em andamento e a fazer
      + **Revisão da Sprint (Review)**
        + No último dia da Sprint ocorre uma revisão onde o time DEV apresenta para o PO o trabalho feito
        + Time box para essa cerimônia é de 4 horas
        + O PO pode levar stakeholders para esse evento
      + **Retrospectiva da Sprint**
        + Também ocorre no último dia
        + Reunião da equipe para lições aprendidas
        + Transparência sobre erros
        + Timebox 3 horas

## Aula 2 - Fundamentos de um projeto ágil
### Papeis e Responsabilidades - Product Owner
+ **Papeis e Responsabilidades do PO**
  + PO representa o profissional que tem a visão do que será desenvolvido, as necessidades a serem atendidas, o público que vai utilizar os serviços e os objetivos a serem alcançados. Na pior das hipóteses, o PO é responsável por cancelar a Sprint quando as atividades planejadas não puderem ser entregues ou enteder que o valor planejado não poderá ser atingido.
  + A característica que melhor define um PO é: entende a demanda e extrai o meior valor possível
  + **Refining:** Onde o PO apresenta previamente pro time as histórias que deverão ser apresentadas na planning, pois até que a planning aconteça qualquer mudança repentina é tolerada. O **objetivo** é informar ao time o que será desenvolvido e poder fazer questionamentos. Nessa cerimônia é permitida a participação dos stakeholders.
  + **Planning** ????
  + **Release Planning:** Liberação ou lançamento de software (em inglês: _release_) é o lançamento de nova versão oficial de produto de software. Cada vez que um produto de software é criado ou modificado, o fabricante e seus desenvolvedores decidem sobre como distribuir ou o novo produto ou a modificação às pessoas que o utilizam
    + **Release Planning de Múltiplas Squads:** são vários times de dev agrupados fazendo várias coisas distintas que podem ou não ter correlação entre as atividades mas que ao final da Sprint devem ser agrupadas em uma única release para serem implementadas em produção.
    + **Release Planning de Projeto:** o PO possui uma demanda muito grande que será necessário quebrar essa entrega em várias histórias e consequentemente quebrar em várias Sprints

### Analisando o Escopo e definindo prioridades
+ A definição do escopo é um dos pontos mais críticos do processo de gestaõ de projetos, pois é neste momento que será definido o que será desenvolvido e é do artefato dessa fase que serão extraídos os benefícios a serem atingidos. Portanto, se a definição de escopo for ruim os benefícios atingidos poderão ser os errados ou menos assertivos
+ O Método mais indicado para definir o escopo do projeto é entender qual o  ganho antes de definir o escopo
+ **Product Backlog** é composto por 
  + **Épicos:** incremento sem muito detalhamento, ajuda a te direcionar dos caminhos que deve seguir
  + **Estórias:** detalhamento dos épicos, um épico normalmente se divide em várias estórias, onde ficam descritos o que deve acontecer e suas regras de negócio
    + **Escrevendo uma estória:** nome da história; Descrição da estória (eu, como, quero, quando); Regras de negócio (Separar regras de Front-end de regras de Back-end); Tela (Link ou imagem das telas a serem desenvolvidas); KPI (Quais os onjetivos/valor a estória precisa atingir); Tagueamento (Como a estória será "tagueada" para mensurar os KPI); Critérios de aceite (qual o passo a passo de todos os caminhos felizes possíveis a estória deve cumprir para que ela seja considerada aceita)
+ **Gestão de riscos**
  + **Positivos:** muito ignorado nos projetos, porém um dos fatores de maiores ganhos no desenvolvimento de sistemas. A importância de mapear os riscos positivos é que isso permite priorizar outros itens no backlog
  + **Negativos:** Itens que podem afetar o prazo, custo ou escopo de um projeto de maneira que pode acabar inviabilizando-o

### Papel do PO na Transformação Digital
+ A transformação digital é um processo no qual as empresas fazem uso da tecnologia para melhorar o desempenho, aumentar o alcance e garantir resultados melhores. É uma mudança estrutural nas organizações dando um papel essencial para a tecnologia
