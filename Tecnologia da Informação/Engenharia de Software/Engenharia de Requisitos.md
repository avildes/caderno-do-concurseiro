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

##Gerenciamento de Requisitos

Matriz de Rastreabilidade

