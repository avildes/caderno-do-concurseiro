#Engenharia de Requisitos

##Processo de Engenharia de Requisitos

Os processos de engenharia de requisitos podem incluir quatro atividades de alto nível. Elas visam avaliar se o sistema é útil para a empresa (estudo de viabilidade), descobrindo requisitos (elicitação e análise), convertendo-os em alguma forma-padrão (especificação), e verificar se os requisitos realmente definem o sistema que o cliente quer (validação).

Essas atividades não são realizadas sequêncialmente, elas são intercaladas e formam um ciclo repetitivo. A quantidade de esforço dedicados a cada atividade em cada iteração depende do estágio do processo como um todo e do tipo de sistema que está sendo desenvolvido. Inicialmente, o esforço maior será a compreensão dos requisitos de negócio e não funcionais em alto nível, bem como dos requisitos de usuário para o sistema. Mais tarde no processo o esforço maior será dedicado a elicitar e compreender os requisitos de sistema em detalhes.

No desenvolvimento ágil, a prototipação pode ser trocada pelo desenvolvimento dos requisitos e da implementação do sistema em conjunto.

##Especificação de Requisitos

A especificação de requisitos é o processo de escrever os requisitos de usuário e de sistema em um documento de requisitos. Idealmente, os requisitos de usuário e de sistema devem ser claros, inequívocos, de fácil compreensão, completos e consistentes. Na prática, isso é difícil de conseguir, pois os stakeholders interpretam os requisitos de maneiras diferentes, e, muitas vezes, notam-se conflitos e inconsistências inerentes aos requisitos.

###Requisitos de Usuário:

Os requisitos de usuário para um sistema devem descrever os requisitos funcionais e não funcionais de modo que sejam compreensíveis para os usuários do sistema que não tenham conhecimentos técnicos detalhados. Idealmente, eles devem especificar somente o comportamento externo do sistema. O documento de requisitos não deve incluir detalhes da arquitetura ou projeto do sistema. Eles são quase sempre escritos em linguagem natural e suplementados no documento de requisitos por diagramas apropriados e tabelas.

###Requisitos de Sistema:

Os requisitos de sistema são versões expandidas dos requisitos de usuário, usados por engenheiros de software como ponto de partida para o projeto do sistema. Eles acrescentam detalhes e explicam como os reqisitos de usuário devem ser atendidos pelo sistema. Eles podem ser usados como parte do contrato para a implementação do sistema e devem consistir em uma especificação completa e detalhada de todo o sistema.

Os requisitos do sistema devem  descrever apenas o comportamento externo do sistema e suas restrições operacionais. Eles não devem se preocupar com a forma como o sistema deve ser projetado ou implementado. No entanto, para atingir o nível de detalhamento necessário para especificar completamente um sistema de software complexo, é praticamente impossível eliminar todas as informações de projeto.

###Requisitos Funcionais:

São declarações de serviços que o sistema deve fornecer, de como o sistema deve reagir a entradas específicas e de como o sistema deve se comportar em determinadas situações. Em alguns casos, os requisitos funcionais também podem explicitar o que o sistema não deve fazer.

###Requisitos Não Funcionais: 

São restrições aos serviços ou funções oferecidas pelo sistema. São aqueles que não dizem respeito diretamente às funções específicas fornecidas pelo sistema. Entre eles destacam-se restrições de tempo de desenvolvimento ou de resposta, restrições sobre o processo de desenvolvimento, padrões, entre outros. Ao contrário das características individuais ou serviços do sistema, os requisitos não funcionais, muitas vezes, aplicam-se ao sistema como um todo.

* Segundo Thayer (1990)  em engenharia de sistemas de software, um requisito não funcional de software é aquele que descreve não o que o sistema fará, mas COMO ele fará.

##Elicitação e Análise de Requisitos

Nessa atividade, os engenheiros de software trabalham com clientes e usuários finais do sistema para obter informações sobre o domínio da aplicação, os serviços que o sistema deve oferecer, o desempenho do sistema, restrições de hardware e assim por diante.

A elicitação e análise de requisitos podem envolver diversos tipos de pessoas em uma organização. Um stakeholder do sistema é quem tem alguma influência direta ou indireta sobre os requisitos do sistema. Os stakeholders incluem usuários finais que irão interagir com o sistema e qualquer outra pessoa em uma organização que será afetada por ele. Outros stakeholders do sistema podem ser os engenheiros que estão desenvolvendo ou mantendo outros sistemas relacionados a esse, como também gerentes de negócios, especialistas de domínio e representantes sindicais.

A imagem abaixo mostra um modelo do processo de elicitação e análise. As atividades do processo são:

1. **Descoberta de Requisitos:**
  Essa é a atividade de interação com os stakeholders do sistema para descobrir seus requisitos. Os requisitos de domínio dos stakeholders e da documentação também são descobertos durante essa atividade. 
  
2. **Classificação e Organização de Requisitos:**
  Essa atividade toma a coleção de requisitos não estruturados, agrupa requisitos relacionados e os organiza em grupos coerentes. A forma mais comum de agrupar  os requisitos é o uso de um modelo de arquitetura do sistema para identificar subsistemas e associar requisitos a cada subsistema. Na prática, a engenharia de requisitos e projeto da arquitetura não podem ser atividades completamente separadas.
  
3. **Priorização e Negociação de Requisitos:**
  Inevitavelmente, quando os vários stakeholders estão envolvidos, os requisitos entram em conflito. Essa atividade está relacionada com a priorização de requisitos e em encontrar e resolver os conflitos por meio da negociação de requisitos. Normalmente, os stakeholders precisam se encontrar para resolver as diferenças e chegar a um acordo sobre os requisitos.
  
4. **Especificação de Requisitos:**
  Os requisitos são documentados e inseridos no próximo ciclo do processo. Documentos formais e informais podem ser produzidos. Nesse estágio, os requisitos que foram elicitados até esse momento são documentados de uma forma completamente diferente (por exemplo uma planilha ou em cartões). Escrever os requisitos em cartões pode ser muito eficaz, pois são fáceis para os stakeholders lidarem, mudarem e organizarem.
  

![Processo de Elicitação e Análise de Requisitos](https://raw.githubusercontent.com/avildes/caderno-do-concurseiro/master/Tecnologia%20da%20Informação/Engenharia%20de%20Software/processodeelicitacao.PNG)

##Validação de Requisitos

A validação de requisitos é o processo pelo qual se verifica se os requisitos definem o sistema que o cliente realmente quer. Ela se sobrepõe à análise, uma vez que está preocupada em encontrar problemas com os requisitos. A validação de requisitos é importante porque erros em um documento de requisitos podem gerar altos custos de retrabalho quando descobertos durante o desenvolvimento ou após o sistema já estar em serviço.

O custo para consertar um problema de requisitos por meio de uma mudança no sistema é geralmente muito maior do que o custo de consertar erros de projeto ou de codificação. A razão para isso é que a ocorrência de mudança dos requisitos normalmente significa que o projeto e a implementação do sistema também devem ser alterados. Além disso, o sistema deve, posteriormente, ser retestado.

Durante o processo de validação de requisitos, diferentes tipos de verificação devem ser efetuados com os requisitos no documento de requisitos. Essas verificações incluem:

1. **Verificações de Validade:**
  Um usuário pode pensar que é necessário um sistema para executar determinadas funções. No entanto, maior reflexão e análise mais aprofundada podem identificar funções necessárias, adicionais ou diferentes. Os sistemas têm diversos stakeholders com diferentes necessidades, e qualquer conjunto de requisitos é inevitavelmente um compromisso da comunidade de stakeholders.

2. **Verificações de Consistência:**
  Requisitos no documento não devem entrar em conflito. Ou seja, não deve haver restrições contraditórias ou descrições diferentes da mesma função do sistema.
  
3. **Verificações de Completude:**
  O documento de requisitos deve incluir requisitos que definam todas as funções e as restrições pretendidas pelo usuário do sistema.

4. **Verificações de Realismo:**
  Usando o conhecimento das tecnologias existentes, os requisitos devem ser verificados para assegurar que realmente podem ser implementados. Essas verificações devem considerar o orçamento e o cronograma para o desenvolvimento do sistema.

5. **Verificabilidade:**
  Para reduzir o potencial de conflito entre o cliente e o contratante, os requisitos do sistema devem ser passíveis de verificação. Isso significa que você deve que você deve ser capaz de escrever um conjunto de testes que demonstrem que o sistema entregue atende a cada requisito especificado.
  
Existe uma série de técnicas de validação de requisitos que podem ser usadas individualmente ou em conjunto:

1. **Revisões de Requisitos:**
  Os requisitos são analisados sistematicamente por uma equipe de revisores que verifica erros e inconsistências.

2. **Prototipação:**
  Nessa abordagem para validação, um modelo executável do sistema em questão é demonstrado para os usuários finais e clientes. Estes podem experimentar o modelo para verificar se ele atende a suas reais necessidades.

3. **Geração de Casos de Teste:**
  Os requisitos devem ser testáveis. Se os testes forem concebidos como parte do processo de validação, isso frequentemente revela problemas de requisitos. Se é difícil ou impossível projetar um teste, isso normalmente significa que os requisitos serão difíceis de serem implementados e devem ser reconsiderados. O desenvolvimento de testes a partir dos requisitos do usuário antes de qualquer código ser escrito é parte integrante do Extreme Programming.
  
Não deve-se subestimar os problemas envolvidos na validação de requisitos. Afinal, é difícil mostrar que um conjunto de requisitos atende de fato às necessidades de um usuário; os usuários precisam imaginar o sistema em operação e como esse sistema se encaixaria em seu trabalho. Até para profissionais qualificados de informática é difícil fazer esse tipo de análise abstrata, e é mais difícil ainda para os usuários do sistema. Como resultado, durante  o processo de validação de requisitos raramente são encontrados todos os problemas de requisitos. Após o ajuste do documento de requisitos, é inevitável a necessidade de mudanças nos requisitos para corrigir omissões e equívocos.

##Gerenciamento de Requisitos

Os requisitos para sistemas de software estão sempre mudando, mudam inclusive, até quando o sistema já esteja sendo utilizado regularmente, pois os usuários passam a ter uma visão diferente do sistema. Isto é inévitavel e parte integrante do desenvolvimento de um sistema pois a compreensão dos stakeholders vai evoluindo a medida que eles vão tendo contato com o sistema.

O gerenciamento de requisitos é o processo de compreensão e controle das mudanças nos requisitos do sistema. É preciso se manter a par das necessidades individuais e manter as ligações entre as necessidades dependentes para conseguir avaliar o impacto das mudanças nos requisitos. É preciso estabelecer um processo formal para fazer propostas de mudanças e a ligação destas às exigências do sistema. O processo formal de gerenciamento de requisitos deve começar assim que uma versão preliminar do documento de requisitos estiver disponível. No entanto, é importante começar a planejar como gerenciar mudanças de requisitos durante o processo de elicitação de requisitos.


###Matriz de Rastreabilidade

A matriz de rastreabilidade é uma ferramenta para facilitar a visualização dos relacionamento entre requisitos e outros artefatos ou objetos. Existem diversos tipos de matrizes de rastreabilidade a depender de que artefatos iremos relacionar com os requisitos. Mas, qualquer que seja o tipo de matriz, ela sempre segue o mesmo modelo. Basicamente, coloca-se os objetos sendo rastreados nos eixos de uma tabela e marca-se os pontos de intersecção. No caso mais comum, da matriz de rastreabilidade entre requisitos ou de dependências, repete-se os requisitos nos eixos horizontal e vertical.

Imagine agora que na metade do desenvolvimento do seu projeto você recebe uma solicitação de mudança que envolve alterar um determinado requisito. Sem uma matriz de rastreabilidade, você pode não perceber todo o impacto dessa mudança no seu sistema e acabar tomando decisões equivocadas por não poder realizar uma análise de impacto completa e confiável. Com a matriz, facilmente conseguimos identificar quantos e quais requisitos são afetados por qualquer alteração no sistema, e assim tornamos nossa avaliação de impacto muito mais eficaz.


#Fontes: 
1. Engenharia de Software - Ian Sommerville
2. EUAX - http://www.euax.com.br/2012/01/matriz-de-rastreabilidade/
3. Handbook de TI para concursos: O guia definitivo - Camatta, Gobira e Melotti








