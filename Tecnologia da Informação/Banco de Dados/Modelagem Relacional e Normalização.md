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


###Funções NULL relacionadas:

>As bancas costumam colocar alguma destas funções em questões perguntando o que elas fazem.

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
