
 Noções sobre metodologias de análise, projeto e desenvolvimento de sistemas.
 UP, RUP, Scrum, XP.
 Engenharia de software: levantamento e gerenciamento de requisitos, análise e projeto orientado a objetos, 
 UML; 
 testes, homologação e implantação de sistemas.

 
Atividades fundamentais em um processo de software:

* **Especificação de software:**
  A funcionalidade do software e as restrições a seu funcionamento devem ser definidas.
* **Projeto e implementação de software:**
  O software deve ser produzido para atender as especificações.
* **Validadação de software**:
  O software deve ser validado para garantir que atenda às demandas do cliente.
* **Evolução de software:**
  O software deve evoluir para atender às necessidades de mudança dos clientes.
  
##Modelos de processo genéricos

###Modelo em cascata

###Modelo incremental

###Modelo orientado a reúso de software
  
##RUP - Rational Unified Process

É um modelo de processo derivado de trabalhos sobre a UML e o Unified Software Development Process. É um processo híbrido que inclui elementos de todos os modelos de processo genéricos. 

O RUP reconhece que os modelos de processo convencionais apresentam uma visão única do processo. Em contrapartida, o RUP é normalmente descrito em três perspectivas:

1. Uma perspectiva dinâmica, que mostra as fases do modelo ao longo do tempo.
2. Uma perspectiva estática, que mostra as atividades realizadas ao longo do tempo.
3. Uma perspectiva prática, que sugere boas práticas a serem usadas durante o processo.

O RUP é constituído de 4 fases que são estritamente relacionadas ao negócio, e não a assuntos técnicos. São elas:

1. Concepção (ou Iniciação)
  O objetivo da fase de concepção é estabelecer um bussiness case para o sistema. Você deve identificar todas as entidades externas (pessoas e sistemas) que vão interagir com o sistema e definir as interações. Então, você deve usar essas informações para avaliar a contribuição do sistema para o negócio. Se essa contribuição for pequena, então o projeto poderá ser cancelado depois dessa fase.
  
2. Elaboração
  As metas da fase de elaboração são desenvolver uma compreensão do problema dominante, estabelecer um framework da arquitetura para o sistema, desenvolver o plano do projeto e identificar os maiores riscos do projeto. No fim dessa fase, você deve ter um modelo de requisitos para o sistema, que pode ser um conjunto de casos de uso da UML, uma descrição da arquitetura ou um plano de desenvolvimento do software.

3. Construção
  A fase de contrução envolve projeto, programação e testes do sistema. Durante essa fase, as partes do sistema são desenvolvidas em paralelo e integradas. Na conclusão dessa fase, você deve ter um sistema de software já funcionando, bem como a documentação associada pronta para ser entregue aos usuários.

4. Transição
  A fase final do RUP implica transferência do sistema da comunidade de desenvolvimento para a cominidade de usuários e em seu funcionamento em um ambiente real. Isso é ignorado na maioria dos modelos de processo de software, mas é, de fato, uma atividade cara e, às vezes, problemática. Na conclusão dessa fase, você deve ter um sistema de software documentado e funcionando corretamente em seu ambiente operacional.
  
É importante ressaltar que dentro de cada fase, um conjunto de iterações, envolvendo **planejamento**, **levantamento de requisitos**, **análise de projeto**, e **implementação** e **testes**, é realizado. Contudo, de uma iteração para outra e de uma fase para a próxima, a ênfase sobre as várias atividades muda. Na fase de concepção, o foco principal recai sobre o entendimento dos requisitos e a determinação do escopo do projeto (planejamento e levantamento de requisitos). Na fase de elaboração, o enfoque está na captura e modelagem dos requisitos (levantamento de requisitos e análise), ainda que algum trabalho de projeto e implementação seja realizado para prototipar a arquitetura, evitando certos riscos técnicos. Na fase de construção  o enfoque concentra-se no projeto e na implementação, visando evoluir e rechear o protótipo inicial, até obter o primeiro produto operacional. Finalmente, a fase de transição concentra-se nos testes, visando garantir que o sistema possui o nível adequado de qualidade. Além disso, usuários dever ser treinardos, características ajustadas e elementos esquecidos adicionados.
  
O RUP promove o uso de seis melhores práticas: 

* desenvolva iterativamente; 
* gerencie requisitos; 
* use arquiteturas de componentes; 
* modele visualmente (UML);
* verifique qualidade de software continuamente;
* e gerencie mudanças.


As disciplinas de suporte (Core Supporting Workflows) são: 

* Gerência de Configuração e Mudanças (Configuration and Change Management); 
* Gerência de Projetos (Project Management); 
* e Ambiente(Enviroment).

Papéis no RUP:

Um papel é uma definição abstrata de um conjunto de atividades executadas e dos respectivos artefatos. 

* Os papéis do Analista organizam os papéis envolvidos principalmente na identificação e na investigação de requisitos (Analista de Sistemas, Designer de Negócios, etc). 

* Os papéis do Desenvolvedor organizam os papéis envolvidos principalmente no design e desenvolvimento de software (Designer de Cápsula, Revisor de Código, etc). 

* Os Papéis do Testador organizam os papéis que lidam com habilidades específicas exclusivas para teste (Testador). 

* Os papéis do Gerente organizam os papéis envolvidos principalmente no gerenciamento e na configuração do processo de engenharia de software (Engenheiro de Processo, Gerente de Projeto, etc). 

* Os papéis adicionais organizam os papéis que envolvem funções diversas ou de suporte no projeto (Desenvolvedor do Curso, Artista Gráfico, Especialista em Ferramentas, etc).

As disciplinas (workflows) do RUP são separadas em dois grupos: **Core Engineering Workflows**(contendo 6 disciplinas) e **Core Supporting Workflows** (contendo 3 disciplinas). Os dois grupos (engineering e supporting) formam um grupo mais generico chamado: **Core Process Workflows** (contendo as 9 disciplinas do RUP)
OBS.: As vezes o grupo Core Engineering Workflow é chamado simplesmente de Core Process WorkFlow.	

Core Process Workflows:	

  Core Engineering Workflows:	
    * Business Modeling (modelo de negócios)	
	* Requirements (requisitos)	
	* Analysis and Design (análise e desenho) 
	* Implementation (implementação)	
	* Test (teste)	Deployment (implantação)	
  
  Core Supporting Workflows:	
    * Configuration and Change Management (Gerência de Configuração e Mudanças)	
	* Project Management (Gerência de Projetos)	
	* Environment (ambiente)

## XP - Extreme Programming

A metodologia XP (Extreme Programming) é destinada a grupos pequenos de desenvolvimento, e em projeto de duração de até 36 meses. Os principais papeis nesta metodologia são: **Programador** - foco da metodologia; **Coach** - responsável por questões técnicas do projeto, maior conhecimento do processo, valores e práticas XP. Verifica o comportamento da equipe; **Tracker** -  Coletar sinais vitais do projeto uma ou 2 vezes por semana e mantem todos informados; **Gerente** - responsável pelos assuntos admnistrativos, mantém um forte relacionamento com o cliente.

Entre as principais características da metodologia XP estão:

1. Metáforas - Utilização de comparações e analogias para facilitar o entendimento;
2. Design Simples do Sistema;
3. Testes Automatizados - Testes de Unidade e de Aceitação;
4. Refactoring - Todo desenvolvedor tem o dever de melhorar um código que esteja funcionando porém mal escrito;
5. Programação de Dupla - Todo código deve ser implementado em dupla;
6. Propriedade Coletiva do Código;
7. Semana de 40 horas - Evitar trabalhar a mais. Inicialmente se obtem resultados, mas depois há o desgaste;
8. Integração contínua - Eliminar erros graves de integração;
9. Releases Curtos - Release é um conjunto de funcionalidades bem definidas e que representam algum valor para o cliente. Um projeto XP pode ter um ou mais releases no seu ciclo;
10. Story Cards - Cartões escritos pelos usuários onde são descritas funcionalidades do sistema;
11. CRC - Linguagem para Modelagem de Classes do XP. Utiliza os Story Cards.

Esta metologia se baseia em 5 valores (já foi questão da CESPE):

* Comunicação
* Simplicidade
* Feedback
* Coragem
* Respeito

## SCRUM


No scrum as funcionalidades a serem implementadas, na forma de histórias de usuários, são mantidas em uma lista denominada Product Backlog. O Product Owner (P.O.) deverá selecionar os itens no backlog e escolher os que mais agregarem valor para serem executados na Sprint.

O Product Owner é a pessoa que define os itens que compõem o Product Backlog e os prioriza nas Sprint Planning Meetings. O Scrum Team olha para o Product Backlog priorizado, seleciona os itens mais prioritários e se compromete a entregá-los ao final de um Sprint (iteração). Estes itens transformam-se no Sprint Backlog. O Product Owner utiliza práticas de estimativa como o burndown e o burnup para acompanhar a quantidade de trabalho que a organização ainda deve realizar para alcançar os seus objetivos. Assim, se o propósito for garantir o alcance de objetivos, o trabalho poderá ser resumido em qualquer ponto do tempo.

O Scrum Master procura assegurar que a equipe respeite e siga os valores e as práticas do Scrum. Ele também protege a equipe assegurando que ela não se comprometa excessivamente com relação àquilo que é capaz de realizar durante um Sprint.

**Sprint**
Uma Sprint é a unidade básica do SCRUM. Dura no máximo um mês e representa o tempo de desenvolvimento  dos itens de história do cliente que foram selecionados pelo Product Owner antes do começo da Sprint na Sprint Planning Meeting.

Reuniões:

* **Sprint Planning Meeting** - Reunião onde o Product Owner vai selecionar itens do Product Backlog para serem executados durante a sprint. Uma vez que as sprints no SCRUM são fixadas em uma time- box de um mês, as reuniões de planejamento das sprints seguem uma time-box de oito horas. Caso o tamanho da sprint seja menor, a duração desta reunião deve ser reduzida proporcionalmente.

* **Daily Meeting** - Reunião diária para revisar o que será feito nas próximas 24 horas e apontar algum possível impedimento. Essa reunião é organizada pelo próprio time, sendo função do Scrum Master apenas garantir que ela aconteça. É um evento time-boxed de 15 minutos, para que a Equipe de Desenvolvimento possa sincronizar as atividades e criar um plano para as próximas 24 horas. 

* **Review Meeting** - Reunião onde o time apresenta todos os entregáveis (itens do product backlog que foram desenvolvidos na sprint) para o Product Owner. Reunião para inspecionar o incremento e adaptar o Backlog do Produto, se necessário. 


* **Retrospective Meeting** - Reunião onde o time coleta lições aprendidas e discute possíveis melhorias para as próximas sprints. É uma reunião time-boxed de 3 horas para uma Sprint de um mês, sendo uma oportunidade para o Time Scrum inspecionar a si próprio e criar um plano para melhorias a serem aplicadas na próxima Sprint. 