#Projeto orientado a objetos com UML

Um sistema orientado a objetos é composto de objetos interativos que mantêm seu próprio estado local e oferecem operações nesse estado. A representação do estado é privada e não pode ser acessada diretamente, de fora do objeto. Processos de projeto orientado a objetos envolvem projetar as classes de objetos e os relacionamentos entre essas classes. Essas classes definem os objetos no sistema e suas interações. Quando o projeto é concebido como um programa em execução, os objetos são criados dinamicamente a partir dessas definições de classes.

Sistemas orientados a objetos são mais fáceis de mudar do que os sistemas desenvolvidos com abordagens funcionais. Os objetos incluem os dados e as operações para manipulá-los. Portanto, eles podem ser entendidos e modificados como entidades autônomas. Alterar a implementação de um objeto ou adicionar serviços não deve afetar outros objetos do sistema. Como os objetos são associados com coisas, muitas vezes existe um mapeamento claro entre entidades do mundo real (como componentes de hardware) e seus objetos de controle no sistema, o que melhora a inteligibilidade e, portanto, a manutenibilidade do projeto.

Para desenvolver um projeto de um sistema desde o conceito até o proeto detalhado orientado a objeto, existem várias atitudes que é preciso tomar:

1. Compreender e definir o contexto e as interações externas com o sistema.

2. Projetar a arquitetura do sistema.

3. Identificar os principais objetos do sistema.

4. Desenvolver modelos de projeto.

5. Especificar interfaces.

Como todas as atividades criativas, o projeto não é um processo sequencial claro. O projeto é desenvolvido a partir de idéias, soluções são propostas e refinando essas soluções assim que as informações ficam disponíveis. Quando os problemas surgem, inevitavelmente é preciso voltar atrás e tentar novamente. Às vezes, as opções são exploradas detalhadamente para ver se elas funcionam; em outros momentos, os detalhes são ignorados até o fim do processo, porque isso implicaria a possibilidade de o projeto ser pensado como uma sequência de atividades. Na verdade, todas essas atividades são intercaladas e, assim, influenciam-se mutuamente.

##Contexto e interações do sistema

O primeiro estágio de qualquer processo de projeto de software é o desenvolvimento de uma compreensão dos relacionamentos entre o software que está sendo projetado e seu ambiente externo. Isso é essencial para decidir como oferecer a funcionalidade requerida para o sistema e como estruturar o sistema para se comunicar com seu ambiente. A compreensão do contexto também permite estabelecer os limites do sistema.

Definir os limites do sistema ajuda a decidir quais recursos serão implementados no sistema que está sendo projetado e quais recursos estão em outros sistemas associados. O ponto importante aqui é saber distinguir que funcionalidades estão no sistema que será construído e quais fazem parte dos outros sistemas que interagem com o primeiro.

Modelos de contexto do sistema e modelos de interação apresentam visões complementares dos relacionamentos entre um sistema e seu ambiente:

1. Um modelo de contexto do sistema é um modelo estrutural, que demonstra os outros sistemas no ambiente do sistema a ser desenvolvido. O modelo de contexto pode ser representado por um diagrama de blocos simples mostrando as entidades do sistemas e de suas associações.

2. Um modelo de interação é um modelo dinâmico que mostra como o sistema interage com seu ambiente quando ativo. Quando se modela as interações de um sistema é interessante usar uma abordagem abstrata sem muitos detalhes. Um modelo indicado é o modelo de casos de uso onde cada caso de uso representa uma interação com o sistema.

##Identificação dos objetos de classe

Os casos de uso são usado para aumentar a compreensão do sistema e a medida que o sistema fica mais claro as ideias são refinadas e as classes começam a ser identificadas. A descrição dos casos de uso ajuda a identificar objetos e operações no sistema.

Foram feitas várias propostas sobre como identificar as classes de objetos em sistemas orientados a objetos:

1. Usar uma análise gramatical de uma descrição em linguagem natural do sistema a ser construído. Objetos e atributos são substantivos, operações ou serviços são verbos.

2. Usar uma análise baseada em cenários, na qual diversos cenários de uso do sistema são identificados e analisados separadamente. À medida que cada cenário é analisado, a equipe responsável pela análise deve identificar os objetos necessários, atributos e operações.

##Modelos de projeto

Modelos de projeto ou de sistema mostram os objetos ou classes de objetos em um sistema. Eles também mostram as associações e relacionamentos entre essas entidades. Esses modelos são a ponte entre os requisitos do sistema e a implementação de um sistema. Eles precisam ser abstratos, para que os detalhes desenecessários não escondam os relacionamentos entre eles e os requisitos do sistema. No entanto, também devem incluir detalhes suficientes para que os programadores possam tomar decisões de implementação.

Geralmente, você contorna esse tipo de conflito desenvolvendo modelos em diferentes níveis de detalhe. Sempre que houver links estreitos entre os engenheiros de requisitos, projetistas e programadores, os modelos abstratos podem ser tudo o que é necessário. Decisões específicas de projeto podem ser feitas enquanto o sistema é implementado, com problemas resolvidos por meio de discussões informais. Quando os links entre os especificadores do sistema, projetistas e programadores são indiretos (por exemplo, quando um sistema está sendo projetado em uma parte de uma organização, mas implementado em outros lugares), modelos mais pormenorizados poderão ser necessários.

Portanto, um passo importante no processo de projeto é decidir os modelos de projeto que você precisa e o nível de detalhes para esses modelos. Isso depende do tipo de sistema que está sendo desenvolvido. A maneira de projetar um sistema sequencial de processamento de dados é diferente da maneira de projetar um sistema embutido de tempo real; assim você terá modelos de projeto diferentes. A UML suporta 13 tipos diferentes de modelos mas raramente todos são usados. Minimizar o número de modelos produzidos reduz os custos de projeto, você normalmente desenvolve dois tipos de modelos de projeto:

1. Modelos estruturais, os quais descrevem a estrutura estática do sistema, usando as classes de objetos e seus relacionamentos. Relacionamentos importantes que podem ser documentados nesse estágio são os de generalização (herança), usa/usado por e composição.

2. Modelos dinâmicos, os quais descrevem a estrutura dinâmica do sistema e mostram as interações entre os objetos do sistema. Interações que podem ser documentadas incluem a sequência de solicitações de serviço feitas pelos objetos e as mudanças de estado que são disparadas por essas interações de objetos.

Existem três modelos particularmente úteis para acrescentar detalhes aos modelos de caso de uso e de arquitetura, nos estágios iniciais do processo de projeto: 

1. Modelos de subsistema, que mostram agrupamentos lógicos de objetos em subsistemas coerentes. Estes são representados por uma forma de diagrama de classe com cada subsistema exibido como um pacote de objetos. Modelos de subsistemas são modelos estáticos (estruturais).

2. Modelos sequência, que mostram a sequência de interações de objetos. Estes são representados por um diagrama de sequência ou de colaboração da UML e normalmente se cria um modelo de sequência para cada caso de uso criado. Modelos de sequência são modelos dinâmicos.

3. Modelos de máquina de estado, que mostram como objetos individuais mudam de estado em resposta aos eventos. Estes são representados pela UML por diagramas de estado. Modelos de máquina de estados são modelos dinâmicos.












● Servidores 
O objeto é implementado como um processo paralelo (servidor) com pontos de entrada que correspondem às operações de objeto. Se nenhuma chamada é feita para ele, o objeto suspende a sua execução e aguarda outras solicitações de serviço.
 
● Objetos ativos
Os objetos são implementados como processos paralelos, e o estado interno do objeto pode ser modificado por ele próprio, e não simplesmente por chamadas externas.

Engenharia de Software / Ian Sommerville, 8 edição. Capítulo de Projeto orientado a objetos 



