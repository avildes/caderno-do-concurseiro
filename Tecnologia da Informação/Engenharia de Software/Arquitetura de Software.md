#Arquitetura de Software

##Arquitetura Orientada a Serviços

**Princípios Básicos da SOA**

* Fraco Acoplamento:

  Busca-se um fraco acoplamento, menor dependência entre os componentes da aplicação.
  
* Contrato de Serviço:

  Representa descrições de serviço e outros documentos que descrevem como um serviço pode ser acessado.
 
* Autonomia:

  Serviços tem controle sobre a lógica que encapsulam.
  
* Abstração:

  Além do que é descrito no contrato de serviço, serviços escondem sua parte lógica do mundo exterior.
  
* Reusabilidade:

  A lógica é dividida no serviço com a intenção de reuso.

* Composição:

  Vários serviços pequenos criam um serviço maior.
  
* Sem estado (Stateless):

  Serviços minimizam a retenção da informação em determinada atividade.
  
* Descoberta:

  Serviços são projetados para ser exteriormente descritos, para que possam ser encontrados e avaliados através de mecanismos de descobertas disponíveis.
  
* Heterogeneidade:

  Para promover a interoperabilidade, SOA promove na implementação de serviços a independência de plataforma de desenvolvimento, tecnologias de implementação e linguagens de programação.

###VANTAGENS DA ARQUITETURA ORIENTADA A SERVIÇOS
O reuso de serviços é grande vantagem dessa arquitetura, aumentando produtividade, alinhamento com negócio, melhorias para corporação e facilidade na gerencia da tecnologia da informação, focando em melhorias continuas e automatizando os processos, disponibilizando qualidade nas informações trafegadas na empresa (SOBRINHO, 2011).

Mudar o negócio e os sistemas das empresas não é uma tarefa fácil, particularmente em um contexto de mudanças constantes, a implantação de SOA não é diferente, sendo assim, porque deve ser utilizada essa arquitetura? Abaixo são listadas algumas vantagens que ela pode trazer para o negócio.

* **Reutilização**: O serviço pode ser reutilizado para outras aplicações.

* **Produtividade**: Com o reuso, a equipe de desenvolvimento pode reutilizar serviços em outros projetos, diminuindo o tempo de desenvolvimento.

* **Flexibilidade**: Isolando a estrutura de um serviço as mudanças são feitas com maior facilidade.

* **Manutenibilidade**: Com baixo acoplamento, facilita a manutenção dos serviços.

* **Alinhamento com o negócio**: A área de negócio visualiza os processos alinhados com a tecnologia.

* **Interoperabilidade**: Disponibilizar serviços independentemente da plataforma e tecnologia.

* **Integração**: A integração com outros serviços, aplicativos e sistemas legados.

* **Governança**: Gerenciamento nos processamentos de negócio.

* **Padronizado**: É baseado no uso de padrões.

* **Abstração**: Serviço totalmente abstraído da sua implementação.

###DESVANTAGENS DA ARQUITETURA ORIENTADA A SERVIÇOS
A principal preocupação em implementações dessa arquitetura é a questão da segurança. Em uma pesquisa global patrocinada pela CA, 43% dos executivos classifica a segurança como o ponto mais crítico nas iniciativas SOA. (TI INSIDE ONLINE, 2012).

Todos os tipos de desenvolvimento de software tem suas desvantagens, na arquitetura orientada a serviço não é diferente, ela depende da implementação de normas, não é utilizada em aplicações com grande transferência de dados, alto acoplamento e aplicações que precisam manter estado. A seguir são listadas algumas desvantagens.

* **Complexidade**: Uma grande quantidade de serviços precisa ser gerenciada.

* **Performance**: A performance depende do servidor onde o serviço está publicado, como também da rede.

* **Robustez**: Caso uma exceção acontecer não tem como reverter o processo.

* **Disponibilidade**: Uma queda na rede ou no servidor deixa todos os serviços indisponíveis.

* **Testabilidade**: O debug no serviço é um problema para os desenvolvedores.

* **Segurança**: Os serviços estão disponíveis na rede, qualquer aplicativo pode consumir esse serviço, os dados são trafegados pela rede podendo ser interceptados.


###Web Services

Serviços são como componentes, blocos de construção independentes entre si mas o conjunto deles representa o ambiente de aplicação. Porém, os serviços possuem algumas características específicas como a autonomia em relação a outros serviços. Um serviço é responsável pelo seu próprio domínio, o que significa limitar seu alcance para uma função de negócio específica (ou um grupo de funções relacionadas).

**Web Services não se encaixam no modelo clássico cliente-servidor. Na verdade eles tendem a estabelecer um sistema ponto-a-ponto, onde cada serviço pode atuar como cliente ou servidor.**
 
 
![Relacionamento entre web services](https://raw.githubusercontent.com/avildes/caderno-do-concurseiro/master/Tecnologia%20da%20Informação/Engenharia%20de%20Software/image002.gif)

Cada bloco de construção (serviço) da SOA pode assumir uma ou mais de três funções:

* Provedor de Serviços
* Registro de Serviços (Service Broker)
* Cliente de Serviços
    
	
![Relacionamento entre web services](https://raw.githubusercontent.com/avildes/caderno-do-concurseiro/master/Tecnologia%20da%20Informação/Engenharia%20de%20Software/relacaoWS.png)

####Provedor de Serviços

O provedor de serviços é quem fornece o serviço. Neste momento, funciona como um servidor, um cliente vai lá e faz uma requisição a qual ele responde. Um provedor pode vir a publicar no registro de serviços sua interface e suas informações de acesso. Cada provedor deve decidir quais serviços vai expor e como vai fazer o intercâmbio entre a segurança e a fácil disponibilidade. Deve definir também quanto custa o uso de cada serviço, caso necessário, e como ele irá explorar serviços gratuitos. É importante também que ele defina em qual **categoria** o serviço será listado em um determinado broker.

####Registro de Serviços

O registro de serviços é o intermediário em um processo de requisição de serviços. Um web service assume este papel quando recebe uma requisição de um cliente (neste caso o intermediário também faz o papel de provedor) e encaminha a requisição para um provedor (agora fazendo o papel de cliente). O mais comum é que um registro de serviços apenas encaminhe a requisição sem fazer alterações na mensagem. É possível que um intermediário processe ativamente uma mensagem antes de repassá-la, mas é mais comum que altere apenas o cabeçalho da mensagem. 

O registro é responsável por disponibilizar a interface do web service, as informações de acesso aos serviços.

####Cliente de Serviços

O cliente é quem faz a requisição de um serviço. Tem a função de localizar as entradas no registro de web services para encontrar o serviço que procura, e liga-se ao fornecedor/provedor de serviços para invocar um de seus web services.
	

###Camadas de Abstração

São 5 as camadas de abstração de um projeto na Arquitetura Orientada a Serviços:

* **Camada Corporativa:**
  Descreve as operações empresariais relaizadas por uma determinada organização ou empresa.
  
* **Camada de Processos:**
  Identifica como alguns processos podem ser modelados e posteriormente implementados como serviços.
  
* **Camada de Serviços:**
  Nesta camada, os serviços são mapeados por suas funcionalidades básicas e de negócios, identificando as ações críticas para satisfazer as regras de negócio.

* **Camada de Componentes:**
  Os componentes utilizados nesta camada são blocos de construção de serviços que podem englobar uma ou mais rotinas escritas em determinada linguagem de programação.

* **Camada de Objetos:**
  Comtempla a larga quantidade de classes e objetos, seus atributos e relacionamentos utilizados em componentes para compor os serviços de um projeto baseado em SOA.

###Ciclo de vida SOA


![Relacionamento entre padroes](https://raw.githubusercontent.com/avildes/caderno-do-concurseiro/master/Tecnologia%20da%20Informação/Engenharia%20de%20Software/ciclodevidasoa.png)

####Estratégia

Neste estágio são definidas algumas diretrizes para o uso de SOA:

* As atividades que estarão no escopo da arquitetura
* O foco dos processos e medidas estratégicas com a adoção da SOA

####Modelagem

Engloba um conjunto de práticas ou tarefas realizadas pelas instituições para descrever visualmente todos os aspectos de um processo de negócio. Incluindo seus principais pontos de decisão para a execução das atividades.

####Implementação

Neste estágio o foco é o desenvolvimento dos serviços, ou seja, sua codificação em alguma plataforma e linguagem de programação, levando em consideração as tecnologias de implementação disponíveis e as decisões tomadas nos estágios anteriores quanto a adoção da SOA, tanto nas decisões estratégicas quanto nas modelagens definidas pelos gestores e analistas.

####Monitoramento (Bussiness Activity Monitoring - BAM)

Análise em tempo real dos dados que trafegam em uma rede através do uso de um software que analisa os dados e exibe informações gerenciais como resultado.

###ESB
Enterprise Service Bus (ESB) é um barramento de serviços corporativos que fornece uma abstração de camadas na implementação de um sistema empresarial de mensagens. Combina uma abordagem orientada a eventos e orientada a serviços, simplificando integrações de negócios e unindo plataformas heterogêneas e ambientes (MARÉCHAUX, 2006)

ESB é um dos mais importantes componentes de SOA, é um software de infraestrutura que torna os serviços de negócios reutilizáveis e amplamente disponíveis para usuários, aplicações, processo e outros serviços.

Para desenvolver as integrações é cada vez mais complicado e não é rápido como o mercado exige, os barramentos de serviços corporativos aceleram e simplificam as integrações nas aplicações. Empresas como Totvs, IBM e Microsoft vendem essa ferramenta. Principais características dessas ferramentas são:

* Roteamento de mensagens.
 
* Conversão de protocolo de transporte.

* Requisição de serviços.
 
* Transformação de mensagens.
 
* Distribuição de eventos de negócio.


###SOAP - Simple Object Access Protocol


![Relacionamento entre padroes](https://raw.githubusercontent.com/avildes/caderno-do-concurseiro/master/Tecnologia%20da%20Informação/Engenharia%20de%20Software/image001.gif)

Transcrevendo a figura:
O UDDI (Universal Description, Discovery and Integration) é acessado usando SOAP e permite a descoberta de WSDL (Web Service Definition Language). O WSDL, por sua vez, se liga ao SOAP e descreve um Web Service. O SOAP permite a comunicação entre Web Services.


# Referencias:

http://www.devmedia.com.br/introducao-as-tecnologias-web-services-soa-soap-wsdl-e-uddi-parte1/2873

http://www.devmedia.com.br/vantagens-e-desvantagens-de-soa/27437#ixzz3RGviPdi5
