
#Resumo dos assuntos do MPPB:

##1. Administração de Banco de Dados. 

1.1 - Administrador de Banco de Dados (DBA)
	• A administração dos recursos primário (banco de dados) e secundário (SGBD) é de responsabilidade do Administrador de Banco de Dados. Ele também é responsável por autorizar o acesso ao banco de dados, coordenar e monitorar seu uso e adquirir recursos de software e de hardware conforme a necessidade. Também é responsável por problemas como falhas na segurança e demora no tempo de resposta ao sistema.
	• Funções:
		--> Mapear o modelo conceitual no modelo lógico
		--> Realizar o projeto físico do banco de dados
		--> Criar usuários, definir visões e permissões, além de regras de integridade
		--> Controlar os processos de backup e recuperação
		--> Garantir o bom desempenho no acesso e manuseio do banco pelos usuários.
1.2 - Projetista de Banco de Dados ou Administradores de Dados (AD's)
	• Os projetistas de banco de dados são responsáveis por identificar os dados a serem armazenados e escolher estruturas apropriadas para representar e armazenar esses dados. É responsabilidade dos projetistas de banco de dados (AD's) se comunicar com todos os potenciais usuários a fim de entender suas necessidades e criar um projeto que as atenda. A partir dessa comunicação eles definem visões do banco de dados que cumprem os requisitos de cada grupo de usuários. O projeto final de banco de dados contém uma integração de todas essas visões para ser capaz de atender às necessidades de todos os grupos de usuários.
	• Funções:
		--> Levantar os requisitos funcionais para o banco de dados;
		--> Modelar conceitualmente o banco de dados;
		--> Especificar as regras de negócio das aplicações
		--> Definir padrões de nomes para conceitos e variáveis
		--> Determinar normas de incorporação e manuseio dos dados


Obs.: A banca gosta de confundir esses dois cargos, fique atento!

##2. Projeto lógico e físico de banco dados.
Estrutura de um Projeto de Banco de Dados:
 
2.1 - Análise de Requisitos:
	• Esta é a primeira etapa de um projeto de banco de dados. Nela, os requisitos devem ser coletados junto ao cliente para criar uma descrição textual (mini-mundo) do processo de forma que todos possam entender. É uma das partes mais importantes do projeto de banco de dados pois, caso seja mal feita, irá prejudicar todo o sistema.

2.2 - Projeto Conceitual:
	• Nesta etapa o esquema conceitual do banco de dados é construído com base no mini-mundo gerado na etapa anterior. É muito comum utilizar o modelo entidade-relacionamento (E-R) nesta etapa. O esquema conceitual descreve o banco de dados em uma visão macro e tem o foco no conteúdo de informação: entidades, atributos, relacionamentos, etc.

2.3 - Projeto Lógico:
	• O objetivo do projeto lógico é definir a estrutura do banco de dados com base no projeto conceitual. Aqui serão definidas as tabelas, colunas, metadados (os tipos de dados, obrigatoriedade, chaves), relacionamentose, regras etc. O resultado é um esquema do banco de dados parecido com o modelo conceitual, proém com mais detalhes de banco de dados e não apenas conceitos.

2.4 - Projeto Físico:
	• Esta é a etapa final do projeto de banco de dados e é fortemente ligada ao Sistema de Gerenciamento de Banco de Dados (SGBD) que será utilizado. Nela definem-se os scripts de criação dos objetos no banco de dados (tabelas, visões, colunas, funções, ...), permissões de acesso de usuários e outros detalhes técnicos relacionados a implementação do banco.
	• A otimização de desempenho do banco de dados é trabalhada nesta fase do projeto. 

##3. Modelagem de dados relacional e orientada a objetos. 

3.1 - Modelagem Relacional:
	• Se baseia na teoria dos conjuntos (Álgebra Relacional) e representa o banco de dados como uma coleção de relações. Cada linha da tabela representa uma coleção de valores de dados relacionados. Uma linha representa um fato que normalmente corresponde a uma entidade ou relacionamento do mundo real.
	  Na terminlogia formal do modelo relacional, uma linha é chamada de tupla, um cabeçalho da coluna é chamado de atributo e a tabela é chamada relação. O tipo de dado que descreve os tipos de valores que podem aparecer em cada coluna é representado por um domínio de valores possíveis.
	• Características das relações:
		--> Ordenação das tuplas em uma relação:
			Uma relação é definida como um conjunto de tuplas. Matemáticamente, os elementos de um conjunto não possuem ordem entre eles; logo, as tuplas em uma relação não possuem nenhuma ordem em particular.
		--> Valores e NULLs nas tuplas:
			Cada valor em uma tupla é um valor atômico; ou seja, ele não é divisível em componentes dentro da estrutura do modelo relacional básica. Logo, atributos compostos ou multivalorados não são permitidos. Grande parte da teoria por trás do modelo relacional foi desenvolvida com essa suposição em mente, que é chamada pressuposto da primeira forma normal. Assim, atributos multivalorados precisam ser representados por relações separadas e os atributos compostos são representados apenas por seus atributos de componentes simples no modelo relacional básico.
			Um valor especial, chamado NULL, é usado para representar os valores de atributos que podem ser desconhecidos ou não se aplicam.
	
• Restrições:
		--> Restrição de domínio:
			É possível determinar um tipo de atributo restringindo seus valores. Ao tentar inserir ou modificar um valor colocando um outro valor de um tipo diferente do primeiro, ou um valor fora do domínio especificado, esta restrição é violada e , por consequência, a operação é cancelada.
		--> Restrição de integridade de chave:
			Garante que tuplas de uma relação sejam únicas.
		--> Restrução de integridade de vazio:
			Especifica se os atributos podem ou não ser vazios a depender da relação a que se referem.
		--> Restrição de integridade de entidade:
			Afirma que nenhum valor de chave primária pode ser nulo.
		--> Restrição de integridade referencial:
O valor da chave estrangeira corresponde a uma chave existente e não nula em uma tupla de outra relação.
		--> Restrição de integridade semântica:
			São normalmente especificada por regras de negócio e implementadas na aplicação. Podem ser implementadas pelos SGBD's através de TRIGGERS e ASSERTIONS.

3.2 - Modelagem Orientada a Objetos.
	• O modelo de dados Objeto-Relacional combina os befícios do Modelo Relacional com a capacidade de modelagem do Modelo Orientado a Objetos. Este modelo utiliza referências para representar conexões entre objetos tornando as consultas baseadas em caminhos de referência mais compactas dos que as consultas feitas com junção. Com essas referências conseguimos suporte para realizar consultas complexas sobre dados complexos. 
	• Utiliza os construtores set, list, multiset ou array para organizar coleções de objetos.
	• Traz vantagens como o uso de herança e assim aumenta o reuso de código por parte da aplicação.
	• Faz uso de uma extensão da linguagem de consulta SQL. 


##4. Análise e tratamento de vulnerabilidades. 

- 

##5. Arquitetura de Banco de Dados. 

- objeto relacional
hierarquico
em redes
 relacional
etc.

##6. Conceitos de Stored Procedure e Triggers. 

###Stored Procedure

Os procedimentos armazenados (ou Stored Procedures) são procedimentos ou funções que são armazenados e executados pelo SGBD no servidor de bancos. O termo usado no padrão SQL para os procedimentos armazenados é **módulos armazenados persistentes** por que esses programas são armazenados persistentemente pelo SGBD, de modo semelhante aos dados persistentes armazenados pelo SGBD.

Os procedimentos armazenados são úteis nas seguintes circunstâncias:
* Se um programa de banco de dados é necessário por várias aplicações, ele pode ser armazenado no servidor e invocado por qualquer um dos programas de aplicação. Isso reduz a duplicação de esforço e melhora a modularidade do software.
* A execução de um programa no servidor pode reduzir a transferência de dados e o custo de comunicação entre o cliente e o servidor em certas situações.
* Esses procedimentos podem melhorar o poder de modelagem fornecido pelas visões ao permitir que tipos mais complexos de dados derivados estejam disponíveis aos usuários do banco de dados. Além disso, eles podem ser usados para verificar restrições complexas que estão além do poder de especificação de asserções e triggers.

O formato geral da declaração de procedimentos armazenados é a seguinte: 
```
CREATE PROCEDURE <nome do procedimento>
(<parametros>)
<declaracoes de local>
<corpo do procedimento>;
```
Os parâmetros e declarações locais são opcionais e especificados apenas se necessário. Para declarar uma função, um tipo de retorno é necessário, de modo que o formato da declaração é:
```
CREATE FUNCTION <nome da funcao>
(<parametros>)
RETURNS <tipo de retorno>
<declaracoes de local>
<corpo da funcao>;
```
Em geral, cada parâmetro deve ter um **tipo de parâmetro**, o qual é um dos tipos de dados da SQL. Cada parâmetro também deve ter um **modo de parâmetro**, que é um dentre IN, OUT, ou INOUT. Estes correspondem a parâmetros cujos valores são apenas de entrada, apenas de saída (retornados) ou de entrada e saída, respectivamente.

> CESPE: Em PL/SQL, parâmetros cujo tipo não esteja explicitamente declarado são considerados como do tipo IN. **(CORRETO)**
 Obs: apesar de a CESPE marcar como correto pois o comportamento existe, o que deixou de ser especificado foi o modo e não o tipo (tipo seria VARCHAR(2), INTEGER, BOOLEAN, etc.).



### Triggers

Outro comando importante em SQL é o CREATE TRIGGER. Em muitos casos, é conveniente especificar um tipo de ação a ser tomada quando certos eventos ocorrem e quando certas condições são satisfeitas. Por exemplo, pode ser útil especifircar uma condição que, se violada, faz que algum usuário seja informado dela. Um gerente pode querer ser informado se despesas de viagem de um funcionário execederem certo limite, recebendo uma mensagem sempre que isso acontecer. A ação que o SGBD deve tomar nesse caso é enviar uma mensagem apropriada a esse usuário. A condição, portanto, é usada para monitorar o banco de dados. Outras ações podem ser especificadas, como executar um procedimento armazenado (Stored Procedure) específico ou disparar outras atualizações.

* Trigger em nível de linha: trigger que contém o comando FOR EACH ROW e que será executado para cada linha. As palavras-chave NEW e OLD só podem ser utilizadas com triggers em nível de linha.

* Trigger em nível de comando: É executado apenas uma vez.

##7. Controle de acesso a Bancos de Dados. 

- 

##8. Gerência de falhas no ambiente de produção. 

- 

##9. Linguagem SQL ANSI (DDL, DML, DCL, DTL, DQL, Operadores e Funções). 

Diferença entre comandos DDL, DML, DCL, DTL, DQL:
• DDL - Data Definition Language é usada para definir a estrutura do banco de dados ou esquema. Exemplos:
CREATE, ALTER, TRUNCATE, COMMENT, RENAME
• DML - Data Manipulation Language é utilizada para o gerenciamento de dados dentro de objetos do banco. Exemplos:
	SELECT, INSERT, UPDATE, DELETE, CALL, EXPLAIN PLAN, LOCK TABLE
• DCL - Data Control Language é usada para declarações. Exemplos:
	GRANT, REVOKE
• TCL (DTL) - Transaction Control Language é usada para gerenciar as mudanças feitas por instruções DML. Exemplos:
	COMMIT, SAVEPOINT, ROLLBACK
• DQL - Data Query Language contém comandos que fazem consultas ao banco de dados.

Obs.: Existe uma confusão sobre onde o comando SELECT se encaixa nessas categorias, alguns autores colocam como sendo parte da DML e outros como parte da DQL

```
Funções NULL relacionadas:

NVL

A função NVL permite substituir valores nulos com um valor padrão. Se o valor do primeiro parâmetro for nulo, a função retorna o valor no segundo parâmetro. Se o primeiro parâmetro é qualquer valor diferente de nulo, ele é retornado inalterado.

  SELECT id, NVL(col1, 'ZERO') AS output FROM null_test_tab ORDER BY id;

DECODE

A função DECODE não é especificamente para o tratamento de valores nulos, mas ele pode ser usado de uma forma semelhante à função NVL. Sintaxe:

  DECODE( expression , search , result [, search , result]... [, default] )

Exemplo:

  SELECT id, DECODE(col1, NULL, 'ZERO', col1) AS output FROM null_test_tab ORDER BY id;

NVL2

A função NVL2 aceita três parâmetros. Se o primeiro valor do parâmetro não é nulo que devolve o valor do segundo parâmetro. Se o primeiro valor do parâmetro é null, ele retorna o terceiro parâmetro.

  SELECT id, NVL2(col1, col2, col3) AS output FROM null_test_tab ORDER BY id;

COALESCE

Ele aceita dois ou mais parâmetros e retorna o primeiro valor não nulo em uma lista. Se todos os parâmetros conter valores nulos, retorna nulo.

  SELECT id, COALESCE(col1, col2, col3) AS output FROM null_test_tab ORDER BY id;

NULLIF

Ele aceita dois parâmetros e retorna nulo se ambos os parâmetros são iguais. Se eles não são iguais, o primeiro valor do parâmetro é devolvido.

  SELECT id, NULLIF(col3, col4) AS output FROM null_test_tab ORDER BY id;

LNNVL

A função LNNVL está disponível desde, pelo menos, Oracle 9i, mas foi indocumentados até Oracle 11g. Ele é utilizado em uma cláusula WHERE para avaliar uma condição. Se essa condição for avaliada como falsa ou desconhecida, ele retorna true. Se a condição for avaliada como verdadeira, ele retorna falso.

  SELECT id, col3 FROM null_test_tab WHERE LNNVL(col1 IS NULL) ORDER BY id;

NANVL

A função NANVL foi introduzido no Oracle 10g para uso com o BINARY_FLOAT e tipos de dados BINARY_DOUBLE, que pode conter um especial "não é um número" ou valor "NaN". A função é semelhante à NVL, mas em vez de testar NULL ele testa valores "NaN".

SYS_OP_MAP_NONNULL

Vimos que uma comparação de "NULL = NULL" sempre retornará falso, mas às vezes você quer que ele retorne true. É possível fazer isso acontecer usando as funções NVL e DECODE, mas dependendo de como você usá-los esta depende de você converter o valor nulo para outro valor que você espera nunca vai estar presente na coluna ou variável.

  SELECT id, 'col1=col2'

FROM null_test_tab
WHERE SYS_OP_MAP_NONNULL(col1) = SYS_OP_MAP_NONNULL(col2);
```

##10. Modelagem semântica, conceitual, física e lógica. 

- Diferenças entre os tipos de modelagem, classificação?

##11. Plano de contingência. 

- 

##12. Segurança em Bancos de Dados. 

Um SGBD normalmente inclui um **subsistema de segurança e autorização do banco de dados** que  é responsável por garantir a segurança de partes de um banco de dados contra acesso não autorizado. Agora, é comum referir-se a dois tipos de mecanismos de segurança de banco de dados:

* **Mecanismos de segurança discricionários**: estes são usados para conceder privilégios aos usuários, incluindo a capacidade de acessar arquivos de dados, registros ou campos específicos em um modo especificado (como leitura, inserção, exclusão ou atualização).

* **Mecanismos de segurança obrigatórios (Mandatários ou ainda Compulsórios)**: Estes são usados para impor a segurança multinível pela classificação de dados e usuários em várias classes (ou níveis) de segurança e, depois, pela implementação da política de seguranca apropriada da organização. Por exemplo, uma política de segurança típica é permitir que os usuários em certo nível de classificação (ou liberação) vejam apenas os itens de dados classificados no próprio nível de classificação (ou inferior) do usuário. Uma extensão disso é a segurança baseaada em papéis, que impõe políticas e privilégios com base no conceito de papéis organizacionais.

> CESPE: A principal desvantagem dos modelos de políticas de controle discricionário em relação às políticas de acesso obrigatório é a sua vulnerabilidade a ataques maliciosos. **(CORRETO)**

**Funções do DBA na segurança de dados**

Os comandos privilegiados do DBA incluem aqueles para conceder e revogar privilégios a contas, usuários ou grupos de usuários individuais e para realizar os seguintes tipos de ações:
* **Criação de conta**: Essa ação cria uma conta e senha para um usuário ou grupo de usuários para permitir acesso ao SGBD.
* **Concessão de privilégio**: Essa ação permite que o DBA conceda certos privilégios a determinadas contas.
* **Revogação de privilégio**: Essa ação permite que o DBA revogue (cancele alguns privilégios que foram dados anteriormente a certas contas.
* **Atribuição de nível de segurança**: Essa ação consiste em atribuir contas do usuário ao nível de liberação de segurança apropriado.

---

Informalmente existem dois níveis de privilégios para o uso do sistema de banco de dados. 
* Nível de conta: nesse nível, o DBA estabelece os privilégios específicos que cada conta tem, independente das relações no banco de dados.

* Nível de relação: Nesse nível, o DBA pode controlar o privilégio para acessar cada relação ou visão individual no banco de dados.

---

**Medidas de Controle**

Quatro medidas de controle principais são usadas para fornecer a segurança nos bancos de dados:
* Controle de acesso
* Controle de inferência
* Controle de fluxo
* Criptografia de dados

---
**Três tipos de SQL Injection:**
* Manipulação de SQL:
 Um ataque de manipulação, que é do tipo mais comum de ataque de injeção, muda um comando SQL na aplicação - por exemplo, ao acrescentar condições a cláusula WHERE de uma consulta, ou ao expandir uma consulta com componentes de consultas adicionais, usando operações de união como UNION, INTERSECT, ou MINUS.
* Injeção de código:
 Esse tipo de ataque tenta acrescentar instruções SQL ou comandos adicionais à instrução SQL existente, explorando um bug do computador, que é causado pelo processamento de dados inválidos. O atacante pode injetar ou introduzir código em um programa de computador para alterar o curso da execução. A injeção de código é uma técnica popular para a invasão ou penetração no sistema para obter informações.
* Injeção de chamada de função:
 Nesse tipo de ataque, uma função do banco de dados ou uma chamada de função do sistema operacional é inserida em uma instrução SQL vulnerável para manipular os dados ou fazer uma chamada privilegiada. Por exemplo, é possível explorar uma função que realiza algum aspecto relacionado à comunicação na rede.

---

##13. Sistemas Gerenciadores de Bancos de Dados (SGBD): PostgreSQL, MySQL e Oracle. 

- Estudar peculiaridades do Oracle (Revisar COALESCE) e Postgres

###13.1. Instalação, configuração e administração em ambiente Linux Kernel 4.0. 

- ? 

##14. Data Warehouse e Data Mining. 

- O que é, objetivos, como se relacionam

	###14.1 - Data Warehouse

>"É uma coleção de dados orientados por assunto, integrados, variáveis com o tempo e não voláteis, para dar suporte ao processo de tomada de decisão." - Inmon

>"É um conjunto de ferramentas e técnicas de projeto, que quando aplicadas às necessidades específicas dos usuários e aos banco de dados específicos permitirá que planejem e construam um data warehouse." - Kimball

Características:
* Orientados por assunto:
Os dados são organizados para ressaltar temas específicos importantes para o negócio da empresa. Por exemplo: Produtos, Clientes, Atividades, Contas. Em contrapartida, o ambiente operacional é organizado por aplicações funcionais. Por exemplo, uma organização bancária incluiria, empréstimos, investimentos e seguros.
* Integrado:
Os dados presentes no Data Warehouse passaram por um processo de transformação para uniformizar os nomes, unidades e formatação utilizados. Conforme os dados são inseridos no Data Warehouse, eles são convertidos para um mesmo padrão. Por exemplo, considerando sexo como um elemento de dado, uma aplicação pode codificar sexo como M/F, outra como 1/0 e uma terceira como H/M.
* Não-Volátil:
O Data Warehouse permite apenas a carga inicial e consultas a estes dados. Após serem integrados e transformados, os dados são carregados em bloco para o Data Warehouse, para que estes estejam disponíveis aos usuários para acesso. No ambiente operacional, ao contrário, os dados são, em geral, atualizados registro a registro, em múltiplas transações. 
* Variante no tempo
O dado presente em um DW refere-se a um momento específico, significando que ele não é atualizável. O dado de produção é atualizado de acordo com mudanças do objeto em questão, refletindo assim, o estado do objeto no momento do acesso.

Em um DW, a cada ocorrência de uma mudança, uma nova entrada é criada, para marcar essa mudança.

O tratamento de séries temporais apresenta características específicas que adicionam complexidade ao ambiente do DW.

Deve-se considerar que não apenas os dados tem uma característica temporal, mas também os metadados, que incluem definições dos itens de dados, rotinas de validação, algoritmos de derivação, etc.

Sem a manutenção do histórico dos metadados as mudanças das regras de negócio que afetam os dados no DW são perdidas, invalidando dados históricos.

Granularidade:

------------------------------

###14.x - Star Schema

		• Esquema estrela: abordagem que recomenda a não normalização das tabelas dimensão.
		• Snow flake ou esquema de flocos de neve: abordagem que recomenda a normalização das tabelas dimensão. 


O esquema estrela é uma arquitetura física que permite definir estruturas multidimensionais de dados. Ela é composta por uma tabela central, denominada fato, e várias tabelas periféricas a ela relacionadas, denominadas dimensões. Fazem com que a expansão e a evolução da base de dados necessite de pouca atividade de manutenção. É um esquema onde o número de junções realizadas é relativamente menor que o realizado em bases de dados relacionais convencionais.

####Star Schemas e Cubos OLAP (Online Analytical Processing)

Esquemas estrela são estruturas multidimensionais implantados em um SGBD relacional (RDBMS - Relational Database Management System).
Consistem em uma tabela fato ligada a um conjunto de tabelas dimensão associadas através de relações chave primária/estrangeira.

O cubo de processamento analítico online é uma estrutura multidimensional implementada em um banco de dados multidimensional, que pode ser equivalente em conteúdo, ou mais frequentemente derivado de um esquema em estrela relacional. Um cubo OLAP contém atributos dimensionais e fatos, mas é acessado através de linguagens com mais capacidade analítica do que SQL, como [XMLA (XML for Analysis)] (https://en.wikipedia.org/wiki/XML_for_Analysis) e [MDX (Multidimensional Expressions)] (https://en.wikipedia.org/wiki/MultiDimensional_eXpressions).

Cubos OLAP são incluídos nesta lista de técnicas básicas (vide aula) porque um cubo OLAP é muitas vezes o último passo na implantação de um sistema de DW/BI dimensional, ou pode existir como uma estrutura agregada com base em um esquema estrela relacional mais atômico.

Considerações sobre OLAP:

* Um esquema em estrela hospedado em um BD relacional é uma boa base física para a construção de um cubo OLAP, e é geralmente considerado como uma base mais estável para backup e recuperação.
* Cubos OLAP eram tradicionalmente conhecidos por vantagens extremas de desempenho comparados com RDBMSs, mas essa distinção tornou-se menos importante com avanços técnologicos.
* Estruturas de dados de cubo OLAP são as mais variadas entre os diferentes fornecedores de SGBDs relacionais, assim, os detalhes da implantação final muitas vezes dependem do fornecedor que foi escolhido.
* Normalmente, é mais difícil de portar aplicações de BI entre as diferentes ferramentas OLAP do que portar aplicações de BI entre diferentes bancos de dados relacionais.

** Tabelas de fatos agregados vs cubos OLAP **

####OLAP (Online Analytical Processing) vs OLTP (Online Transactional Processing)

**OLTP** - Sistemas transacionais, também conhecidos como sintéticos ou OLTP, são aqueles que, como o nome sugere, baseiam-se em transações. São caracterizados pela alta taxa de atualização, grande volume de dados e acessos pontuais, ou seja, pesquisas cujo resultado seja de pequeno volume ( até milhares de linhas, mas preferencialmente menos).

**OLAP** - Sistemas analíticos se caracterizam por fornecer subsídio para tomadas de decisão, a partir de análises realizadas sobre bases de dados históricas, por vezes com milhões de registros a serem totalizados.

Característica | Sistemas Transacionais (OLTP) | Sistemas Analíticos (OLAP)
------------ | ------------- | -------------
Atualizações | Mais Frequentes | Menos Frequentes
Tipo de Informação | Detalhes | Agrupamento
Quantidade de Dados | Poucos | Muitos
Precisão | Dados atuais | Dados históricos
Complexidade | Baixa | Alta
Consistência | Microscópica | Global
Exemplos | CRM, ERP, Supply Chain | MIS, DSS, EIS
Terminologia | Linhas e Colunas | Dimensões, Medidas e Fatos

[Fonte] (https://vivianeribeiro1.wordpress.com/2011/07/12/o-que-e-olap/)

O fato dos sistemas transacionais (OLTP) refletirem a situação atual de um determinado tipo de dado conduz todas as demais características, como:
* A realização de atualizações frequentemente, matendo os dados atuais;
* Informação detalhada com a maior granularidade possível (consistência microscópica);
* Pesquisas pontuais, portanto de baixa complexidade no tocante ao negócio (do ponto de vista técnico, a pesquisa pode ser bem elaborada).

Do mesmo modo, o fato das análises serem realizadas sobre dados históricos leva às seguintes características:
* Umas vez que os dados são históricos as atualizações não precisam ser tão frequentes. Por exemplo, numa comparação entre a produtividade de três filiais de uma empresa para um determinado produto nos últimos quatro anos, por mês, o dia de hoje ou mesmo o de ontem não é, em geral, de grande representatividade.
* As análises geralmente agrupam informações, sendo tais agrupamentos mais importantes neste contexto do que os dados detalhados. No exemplo do item anterior, o importante é a produção conjunta mensal, e não a produção de uma unidade particular do produto analisado.

As arquiteturas OLAP podem ter:
* **Alicerce Relacional:** Diversas ferramentas analíticas, também chamadas ferramentas de OLAP, operam sobre bases de dados multidimensionais armazenadas em SGBDRs. Além disso, as agregações são também mantidas em banco de dados relacional. Esta forma de armazenamento é conhecida como ROLAP. Uma vez que os dados já se encontram em um modelo apropriado, chamado multidimensional, basta processar as agregações. Com isso obtém-se ganho de espaço de armazenamento, uma vez que os dados permanecem apenas na base de origem.

* **Alicerce em Cubos:** Outra forma de armazenamento, cujo modelo matemático denomina-se hipercubos, apresenta a característica de possuir armazenamento e indexação em estruturas de dados que otimizam consultas ao invés de atualizações. Quando o modelo multidimensional é processado, nova base é gerada, desta vez contendo tanto os dados quanto as agregações em formato próprio, utilizando-se de estruturas apropriadas para pesquisas.

```
    Operações do OLAP:
    
        -Slice: Seleção de dados em 1 dimensão
        
        -Dice: Seleção de dados em 2 ou mais dimensões
        
        -Roll-Up: Agregação de dados - maior generalização, menor detalhe
        
        -Drill-Down: Desagregação de dados - menor generalização, maior detalhe
        
        -Rotation: Permite visualizar os dados sob uma nova perspectiva, sem reduzir/aumentar o escopo dos dados
        
    Na figura 1, os dados permanecem os mesmos, mas são vistos de uma maneira diferente, sob uma nova perspectiva. Trata-se da ROTAÇÃO.
    
    Na figura 2, estamos entrando mais a fundo nos dados de um Continente, detalhando-os por países. Trata-se da desagregação, ou DRILL-DOWN.
    
    
    Slice - operação que corta o cubo mas mantem as perpectivas de visualização dos dados
    
Dice - mudança de perpectiva de visão como se girasse o cubo em nossas mãos buscando descobrir comportamentos conforme a perspectiva de analise dos dados

    
    Galera segue um bizu:
Operações OLAP
Drill Through: Ocorre quando o usuário passa de uma informação contida em uma dimensão para uma outra.
Slice: Corta o cubo(extrai uma fatia), mas mantém a mesma perspectiva de visualização dos dados. Funciona como um filtro que restringe uma dimensão à apenas um ou alguns de seus valores.
Dice: extrai um subcubo do cubo original executando uma operação de seleção em duas ou mais dimensões. Mudança de perspectiva da visão multidimensional, como se o cubo fosse girado. Permite descobrir comportamentos e tendências entre os valores das medidas analisadas em diversas perspectivas.
Drill Across: O nível de análise dentro de uma mesma dimensão é alterado, ou seja, o usuário avança um nível intermediário dentro de uma mesma dimensão.
Pivot: Adicionar ou rearranjar as dimensões das tabelas.
Drill Down: proporciona uma visão mais detalhada de um conjunto de dados, descendo na hierarquia de uma dimensão.
Roll Up: apresenta os dados cada vez mais agrupados ou sumarizados, subindo na hierarquia de uma dimensão.
Rotation: permite visualizar dados de uma nova perspectiva.
Fonte:Teleco,UFSC

    
    
```

###14.x - Data Mining

##15. Normalização

###Objetivos da Normalização

Por que normalizar as tabelas de um banco de dados?
* Diminuir o espaço de armazenamento dos dados
* Aumentar a eficiência de consultas e atualizações
* Remover possíveis anomalias de atualização


```
 Um processo de normalização aplicado com rigor nas tabelas relacionais de um modelo de dados poderá implicar em
a)
menor segurança nos acessos aos sistemas.
**b)**
menor desempenho em transações de consultas.
c)
maior redundância de dados nos arquivos.
d)
maior performance nas atualizações dos bancos.
e)
maior simplificação na administração das tabelas.

Explicação: ?

```


### Formas Normais

Forma Normal | Teste | Solução (normalização)
------------ | ------------- | ------------- 
Primeira (1FN) | Relação não deve ter atributos multivalorados ou relações aninhadas | Formar novas relações para cada atributo multivalorado ou relação aninhada
Segunda (2FN) | Para relações em que a chave primária contém múltiplos atributos, nenhum atributo não chave deverá ser funcionalmente dependente de uma parte da chave primária | Decompor e montar uma nova relação para cada chave parcial com seu(s) atributo(s) dependente(s). Certificar-se de manter uma relação com a chave primária original e quaisquer atributos que sejam total e funcionalmente dependentes dela.
Terceira (3FN) | A relação não deve ter um atributo não chave determinado funcionalmente por outro atributo não chave (ou por um conjunto de atributos não chave). Ou seja, não deve haver dependência transitiva de um atributo não chave sobre a chave primária | Decompor e montar uma relação que inclua o(s) atributo(s) não chave quem determina(m) funcionalmente outro(s) atributo(s) não chave

####Primeira Forma Normal (1FN)
Afirma que o domínio de um atributo deve incluir apenas valores atômicos (simples, indivisíveis) e que o valor de qualquer atributo em uma tupla deve ser um único valor do domínio desse atributo. 

Em resumo: remover atributos multivalorados, atributos compostos e suas combinações.

####Segunda Forma Normal (2FN)
Um esquema de relação R está na Segunda Forma Normal se, e somente se, está na Primeira Forma Normal e se cada atributo não principal A em R for total e funcionalmente dependente da chave primária em R.

Em resumo: remover dependencias parciais.

####Terceira Forma Normal (3FN)
Uma relação está na Terceira Forma Normal se ela está na Segunda Forma Normal e nenhum atributo não chave (não-primário) é transitivamente dependente da chave primária.

Em resumo: não deve existir dependência transitiva.

####Forma Normal de Boyce-Codd (FBNC)
A **Forma Normal Boyce-Codd (FBNC)** foi proposta como uma forma mais simples da 3FN mas descobriu-se que ela era mais rigorosa. Ou seja, cada relação em FBNC também está na 3FN. Porém, uma relação na 3FN não necessariamente está na FBNC.

Uma relação está na Forma Normal de Boyce-Codd se todo determinante é uma chave candidata.

####Quarta Forma Normal (4FN) 
* Dependência Funcional: Significa que o valor de um atributo pode ser determinado a partir de outros.
* Multi-dependência Funcional: Embora um conjunto de atributos não possa determinar o valor de outro atributo, ainda assim esse conjunto consegue restringir os valores possíveis para aquele atributo.

Um esquema de relação R está na 4FN com relação a um conjunto de dependências funcionais ou multivaloradas F se, para toda dependência multivalorada não-trivial X ->-> Y em F+, X for uma superchave de R.

####Quinta Forma Normal (5FN)
Ocorre quando há uma multi-dependência cíclica entre pelo menos 3 conjuntos de atributos da chave da relação. É importante pois a decomposição de uma relação em um conjunto de relações (devido principalmente as necessidades de normalização), quando envolve multi-dependências cíclicas implicam na perda de informações devido à dependência de junção.
Só ocorre em relações que possuem pelo menos três atributos como parte da chave primária. Encontra a dependência de junção que permite decompor a relação sem perdas.

##16. Replicação de banco de dados; performance e tuning: índices e otimização de acesso, otimização de código SQL ANSI, uso do join, union, exists e subconsultas, desempenho e detecção de problemas. 

- Otimização de código SQL
- Detecção de problemas

##17. Modelagem de processos de negócio e BPMN. 

##18. Visão do PMBOK 5a edição.

##19. Fundamentos da ITIL v3.

###Links 
http://fagury.com.br/sys/wp-content/uploads/2010/09/apostila-itil-v3-3.pdf

###Ciclo de vida
O Ciclo de Vida do ITIL v3 é composto de cinco livros. São eles, a Estratégia do Serviço, que fica no núcleo do ciclo, o Desenho do Serviço, a Transição do Serviço e a Operação do Serviço em volta do núcleo e o quinto e último livro, a Melhoria Contínua do Serviço que permeia todo o ciclo de vida.

Principais mudanças em relação à v2:
* Abordagem baseada no ciclo de vida dos serviços;
* Visão integrada de TI, negócios e fornecedores.

Para melhor entendimento, pode-se dividir o cicle de vida em três grupos de conceitos:

Análise de requisitos e definição inicial | Estratégia do Serviço e Desenho de Serviço
Migração para o ambiente produtivo/operacional | Transição de Serviço
Operação e melhoria em produção | Operação de Serviço e Melhoria Contínua do Serviço

###Estratégia

Identifica requisitos e necessidades de negócio, que são acordados e documentados em um SLP (Service Level Package).

###Desenho
A partir do requisito concebe a solução, em todos os seus aspectos, que são documentados em um SDP (Service Design Package).

###Transição
Implementação em produção. Tal implementação é testada e acompanhada, bem como validada. O SKMS(Service Knowledge Management System) é atualizado com as informações do ambiente de produção.

###Operação
O serviço é mantido em operação/funcionamento de acordo com os níveis de serviço (SLAs) estabelecidos para gerar os resultados esperados.

###Melhoria Contínua do Serviço
Identifica oportunidades de melhoria no serviço. É produto desse trabalho o plano de melhoria de serviços (SIP - Service Improvement Plan)

###Conceitos Básicos ou Definições aleatórias cobradas pela FCC

**Incidente:**
Uma interrupção não planejada de um serviço de TI ou uma redução da qualidade de um serviço de TI. Falha de um item de configuração que ainda não tenha impactado um serviço de TI é também um incidente.

**Erro:**
Uma falha de desenho ou uma disfunção que causa uma falha em um ou mais itens de configuração ou serviços de TI. Um erro cometido por uma pessoa ou um processo falho que impacta um item de configuração ou serviço de TI é também um erro.

>Diferença entre erro e incidente:
>
>Um operador de um Centro de Processamento de Dados executou um programa de computador antes do momento previsto, criando defeitos nos relatórios impressos gerados por tal programa de aplicação. Segundo os princípios da ITIL V.3, o operador cometeu ou criou

> **a)** um erro.

> b) um incidente.

> c) um problema.

> d) uma configuração.

> e) uma mudança.

**Requisição de serviço:**
É um pedido de informação para uma mudança ou para acessar um serviço de TI. É geralmente atendida pela Central de Serviço e não requer a abertura de uma requisição de mudança.

**Evento:**
É um status report criado por um serviço, IC ou ferramenta de monitoramento causado pela alteração no desempenho da infraestrutura ou de entrega de serviço. Geralmente requer que incidentes sejam registrados e uma ação seja tomada pelo pessoal de operações de TI. É uma mudança de estado significativa para um Item de Configuração ou serviço.

**Alerta:**
É um aviso ou advertência sobre uma meta (threshold), mudança ou falha que
ocorreu. É produzido e tratado por ferramentas de gerenciamento de sistemas e pelo processo de gerenciamento de eventos.

**Incidente:**
Interrupção inesperada ou redução na qualidade de um serviço de TI. Pode
ser uma falha de um IC que ainda não tenha impactado o serviço.

**Problema:**
É a causa de um ou mais incidentes. O processo de Gerenciamento de
Problema é responsável pela investigação da causa raiz.

**Solução de contorno (workaround):**
Resolve uma dificuldade ou questão de forma temporária, paliativa.

**Erro conhecido (known error):**
É um problema que tem a causa raiz documentada e uma solução de contorno identificada. Erros conhecidos são criados no ciclo de vida do processo de Gerenciamento de Problema.

**Base de Erros Conhecidos:**
Registro centralizado de erros conhecidos. Tais registros são utilizados pelo processo de Gerenciamento de Incidente para resolver incidentes. Esta base, por sua vez, faz parte do SKMS / SGCS – Sistema de Gerenciamento do
Conhecimento de Serviço. Esta base pode ser disponibilizada para que os usuários façam o próprio atendimento.

**Impacto, urgência e prioridade:** 
A avaliação de impacto e da urgência de incidentes, problemas e mudanças é importante para determinar suas prioridades. A prioridade determina a ordem de execução. Determiná-la baseado na combinação entre impacto x urgência é uma boa prática. O impacto considera quantas pessoas, clientes ou quanto do negócio será afetado, enquanto a urgência determina a velocidade em que
o incidente precisa ser resolvido.

**Matriz RACI (Responsible/Accountable/Consulted/Informed):**
O ITIL v3 recomenda o uso da matriz RACI para mapear os papéis definidos neste processo e atividades endereçadas à equipe. Em outras palavras define papéis e responsabilidades de um perfil (que pode ser uma pessoa, mas também um grupo com responsabilidades semelhantes).

--

O **dono do processo** é responsável pelos resultados do processo e por garantir que todas as atividades definidas para o processo tenham responsáveis.

O **gerente do processo** é o responsável pela operacionalização do processo, garantindo o cumprimento de seus objetivos. É responsável pela estrutura e realização do processo e reporta-se ao dono do processo.

Os **praticantes do processo** são responsáveis por atividades definidas, que são reportadas ao gerente do processo.

###Processos do ITIL v3 em resumo:

**Estratégia do Serviço**
* Gerenciamento de Estratégia para Serviços de TI
* Gerenciamento de Demanda
* Gerenciamento do Portfólio de Serviços
* Gerenciamento Financeiro para Serviços de TI
* Gestão do Relacionamento com o Negócio

**Desenho do Serviço**
* Coordenação do Desenho
* Gerenciamento do catálogo de Serviços
* Gerenciamento de nível de Serviço
* Gerenciamento de Fornecedores
* Gerenciamento de Disponibilidade
* Gerenciamento de Capacidade
* Gerenciamento de Continuidade de Serviços de TI
* Gerenciamento de Segurança da Informação

**Transição do Serviço**
* Planejamento e Suporte à Transição
* Gerenciamento de Configuração e Ativos de Serviço
* Gerenciamento de Mudanças
* Gerenciamento de Liberação e Implantação
* Gerenciamento do Conhecimento
* Avaliação de Mudanças
* Validação e Teste de Serviço
* Gerenciamento de Conhecimento

**Operação de Serviço**
* Gerenciamento de Eventos
* Gerenciamento de Incidentes
* Gerenciamento de Problemas
* Gerenciamento de Requisição
* Gerenciamento de Acesso

**Melhoria Contínua**
* Processo de Melhoria em Sete Etapas

```
**Sete Etapas**
1 - Definir o que **deve** ser medido

2 - Definir o que **pode** ser medido

3 - Reunir os dados

4 - Formatar os dados

5 - Analisar os dados

6 - Mostrar e usar a informação

7 - Executar ações corretivas

```

##20. Fundamentos de COBIT. 5.
