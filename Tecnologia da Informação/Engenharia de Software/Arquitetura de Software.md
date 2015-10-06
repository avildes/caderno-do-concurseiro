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

	
###SOAP - Simple Object Access Protocol


![Relacionamento entre padroes](https://raw.githubusercontent.com/avildes/caderno-do-concurseiro/master/Tecnologia%20da%20Informação/Engenharia%20de%20Software/image001.gif)

Transcrevendo a figura:
O UDDI (Universal Description, Discovery and Integration) é acessado usando SOAP e permite a descoberta de WSDL (Web Service Definition Language). O WSDL, por sua vez, se liga ao SOAP e descreve um Web Service. O SOAP permite a comunicação entre Web Services.


# Referencias:

http://www.devmedia.com.br/introducao-as-tecnologias-web-services-soa-soap-wsdl-e-uddi-parte1/2873
