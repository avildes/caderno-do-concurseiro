
Resumo dos assuntos do MPPB:

1. Administração de Banco de Dados. 

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

2. Projeto lógico e físico de banco dados.
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

3. Modelagem de dados relacional e orientada a objetos. 

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

4. Análise e tratamento de vulnerabilidades. 
- 
5. Arquitetura de Banco de Dados. 
- objeto relacional
hierarquico
em redes
 relacional
etc.
6. Conceitos de Stored Procedure e Triggers. 
- 
7. Controle de acesso a Bancos de Dados. 
- 
8. Gerência de falhas no ambiente de produção. 
- 
9. Linguagem SQL ANSI (DDL, DML, DCL, DTL, DQL, Operadores e Funções). 

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

10. Modelagem semântica, conceitual, física e lógica. 
- Diferenças entre os tipos de modelagem, classificação?
11. Plano de contingência. 
- 
12. Segurança em Bancos de Dados. 
- 
13. Sistemas Gerenciadores de Bancos de Dados (SGBD): PostgreSQL, MySQL e Oracle. 
- Estudar peculiaridades do Oracle (Revisar COALESCE) e Postgres
13.1. Instalação, configuração e administração em ambiente Linux Kernel 4.0. 
- ? 
14. Data Warehouse e Data Mining. 
- O que é, objetivos, como se relacionam
	14.1 - Data Warehouse
		• "É uma coleção de dados orientados por assunto, integrados, variáveis com o tempo e não voláteis, para dar suporte ao processo de tomada de decisão." - Inmon
		• "É um conjunto de ferramentas e técnicas de projeto, que quando aplicadas às necessidades específicas dos usuários e aos banco de dados específicos permitirá que planejem e construam um data warehouse." - Kimball
		• Características:
			--> Orientados por assunto:
				Os dados são organizados para ressaltar temas específicos importantes para o negócio da empresa. Por exemplo: Produtos, Clientes, Atividades, Contas. Em contrapartida, o ambiente operacional é organizado por aplicações funcionais. Por exemplo, uma organização bancária incluiria, empréstimos, investimentos e seguros.
			--> Integrado:
				Os dados presentes no Data Warehouse passaram por um processo de transformação para uniformizar os nomes, unidades e formatação utilizados. Conforme os dados são inseridos no Data Warehouse, eles são convertidos para um mesmo padrão. Por exemplo, considerando sexo como um elemento de dado, uma aplicação pode codificar sexo como M/F, outra como 1/0 e uma terceira como H/M.
	 		--> Não-Volátil:
				O Data Warehouse permite apenas a carga inicial e consultas a estes dados. Após serem integrados e transformados, os dados são carregados em bloco para o Data Warehouse, para que estes estejam disponíveis aos usuários para acesso. No ambiente operacional, ao contrário, os dados são, em geral, atualizados registro a registro, em múltiplas transações. 
			--> Variante no tempo
				O dado presente em um DW refere-se a um momento específico, significando que ele não é atualizável. O dado de produção é atualizado de acordo com mudanças do objeto em questão, refletindo assim, o estado do objeto no momento do acesso.
		• Em um DW, a cada ocorrência de uma mudança, uma nova entrada é criada, para marcar essa mudança.
		• O tratamento de séries temporais apresenta características específicas que adicionam complexidade ao ambiente do DW.
		• Deve-se considerar que não apenas os dados tem uma característica temporal, mas também os metadados, que incluem definições dos itens de dados, rotinas de validação, algoritmos de derivação, etc.
		• Sem a manutenção do histórico dos metadados as mudanças das regras de negócio que afetam os dados no DW são perdidas, invalidando dados históricos.
		• Granularidade:

------------------------------

14.x - Star Schema
		• Esquema estrela: abordagem que recomenda a não normalizacão das tabelas dimensão.
		• Snow flake ou esquema de flocos de neve: abordagem que recomenda a normalizacão das tabelas dimensão. 


O esquema estrela é uma arquitetura física que permite definir estruturas multidimensionais de dados. Ela é composta por uma tabela central, denominada fato, e várias tabelas periféricas a ela relacionadas, denominadas dimensões. Fazem com que a expansão e a evolucão da base de dados necessite de pouca atividade de manutenca
	


15. Normalização 
- Objetivos, níveis de normalização
16. Replicação de banco de dados; performance e tuning: índices e otimização de acesso, otimização de código SQL ANSI, uso do join, union, exists e subconsultas, desempenho e detecção de problemas. 
- Otimização de código SQL
- Detecção de problemas
17. Modelagem de processos de negócio e BPMN. 
18. Visão do PMBOK 5a edição.
19. Fundamentos da ITIL v3.
20. Fundamentos de COBIT. 5.


