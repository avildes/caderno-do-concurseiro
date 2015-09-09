##1. Administra��o de Banco de Dados. 

1.1 - Administrador de Banco de Dados (DBA)
	� A administra��o dos recursos prim�rio (banco de dados) e secund�rio (SGBD) � de responsabilidade do Administrador de Banco de Dados. Ele tamb�m � respons�vel por autorizar o acesso ao banco de dados, coordenar e monitorar seu uso e adquirir recursos de software e de hardware conforme a necessidade. Tamb�m � respons�vel por problemas como falhas na seguran�a e demora no tempo de resposta ao sistema.
	� Fun��es:
		--> Mapear o modelo conceitual no modelo l�gico
		--> Realizar o projeto f�sico do banco de dados
		--> Criar usu�rios, definir vis�es e permiss�es, al�m de regras de integridade
		--> Controlar os processos de backup e recupera��o
		--> Garantir o bom desempenho no acesso e manuseio do banco pelos usu�rios.
1.2 - Projetista de Banco de Dados ou Administradores de Dados (AD's)
	� Os projetistas de banco de dados s�o respons�veis por identificar os dados a serem armazenados e escolher estruturas apropriadas para representar e armazenar esses dados. � responsabilidade dos projetistas de banco de dados (AD's) se comunicar com todos os potenciais usu�rios a fim de entender suas necessidades e criar um projeto que as atenda. A partir dessa comunica��o eles definem vis�es do banco de dados que cumprem os requisitos de cada grupo de usu�rios. O projeto final de banco de dados cont�m uma integra��o de todas essas vis�es para ser capaz de atender �s necessidades de todos os grupos de usu�rios.
	� Fun��es:
		--> Levantar os requisitos funcionais para o banco de dados;
		--> Modelar conceitualmente o banco de dados;
		--> Especificar as regras de neg�cio das aplica��es
		--> Definir padr�es de nomes para conceitos e vari�veis
		--> Determinar normas de incorpora��o e manuseio dos dados


Obs.: A banca gosta de confundir esses dois cargos, fique atento!

##2. Projeto l�gico e f�sico de banco dados.
Estrutura de um Projeto de Banco de Dados:
 
2.1 - An�lise de Requisitos:
	� Esta � a primeira etapa de um projeto de banco de dados. Nela, os requisitos devem ser coletados junto ao cliente para criar uma descri��o textual (mini-mundo) do processo de forma que todos possam entender. � uma das partes mais importantes do projeto de banco de dados pois, caso seja mal feita, ir� prejudicar todo o sistema.

2.2 - Projeto Conceitual:
	� Nesta etapa o esquema conceitual do banco de dados � constru�do com base no mini-mundo gerado na etapa anterior. � muito comum utilizar o modelo entidade-relacionamento (E-R) nesta etapa. O esquema conceitual descreve o banco de dados em uma vis�o macro e tem o foco no conte�do de informa��o: entidades, atributos, relacionamentos, etc.

2.3 - Projeto L�gico:
	� O objetivo do projeto l�gico � definir a estrutura do banco de dados com base no projeto conceitual. Aqui ser�o definidas as tabelas, colunas, metadados (os tipos de dados, obrigatoriedade, chaves), relacionamentose, regras etc. O resultado � um esquema do banco de dados parecido com o modelo conceitual, pro�m com mais detalhes de banco de dados e n�o apenas conceitos.

2.4 - Projeto F�sico:
	� Esta � a etapa final do projeto de banco de dados e � fortemente ligada ao Sistema de Gerenciamento de Banco de Dados (SGBD) que ser� utilizado. Nela definem-se os scripts de cria��o dos objetos no banco de dados (tabelas, vis�es, colunas, fun��es, ...), permiss�es de acesso de usu�rios e outros detalhes t�cnicos relacionados a implementa��o do banco.
	� A otimiza��o de desempenho do banco de dados � trabalhada nesta fase do projeto. 

##3. Modelagem de dados relacional e orientada a objetos. 

3.1 - Modelagem Relacional:
	� Se baseia na teoria dos conjuntos (�lgebra Relacional) e representa o banco de dados como uma cole��o de rela��es. Cada linha da tabela representa uma cole��o de valores de dados relacionados. Uma linha representa um fato que normalmente corresponde a uma entidade ou relacionamento do mundo real.
	  Na terminlogia formal do modelo relacional, uma linha � chamada de tupla, um cabe�alho da coluna � chamado de atributo e a tabela � chamada rela��o. O tipo de dado que descreve os tipos de valores que podem aparecer em cada coluna � representado por um dom�nio de valores poss�veis.
	� Caracter�sticas das rela��es:
		--> Ordena��o das tuplas em uma rela��o:
			Uma rela��o � definida como um conjunto de tuplas. Matem�ticamente, os elementos de um conjunto n�o possuem ordem entre eles; logo, as tuplas em uma rela��o n�o possuem nenhuma ordem em particular.
		--> Valores e NULLs nas tuplas:
			Cada valor em uma tupla � um valor at�mico; ou seja, ele n�o � divis�vel em componentes dentro da estrutura do modelo relacional b�sica. Logo, atributos compostos ou multivalorados n�o s�o permitidos. Grande parte da teoria por tr�s do modelo relacional foi desenvolvida com essa suposi��o em mente, que � chamada pressuposto da primeira forma normal. Assim, atributos multivalorados precisam ser representados por rela��es separadas e os atributos compostos s�o representados apenas por seus atributos de componentes simples no modelo relacional b�sico.
			Um valor especial, chamado NULL, � usado para representar os valores de atributos que podem ser desconhecidos ou n�o se aplicam.
	
� Restri��es:
		--> Restri��o de dom�nio:
			� poss�vel determinar um tipo de atributo restringindo seus valores. Ao tentar inserir ou modificar um valor colocando um outro valor de um tipo diferente do primeiro, ou um valor fora do dom�nio especificado, esta restri��o � violada e , por consequ�ncia, a opera��o � cancelada.
		--> Restri��o de integridade de chave:
			Garante que tuplas de uma rela��o sejam �nicas.
		--> Restru��o de integridade de vazio:
			Especifica se os atributos podem ou n�o ser vazios a depender da rela��o a que se referem.
		--> Restri��o de integridade de entidade:
			Afirma que nenhum valor de chave prim�ria pode ser nulo.
		--> Restri��o de integridade referencial:
O valor da chave estrangeira corresponde a uma chave existente e n�o nula em uma tupla de outra rela��o.
		--> Restri��o de integridade sem�ntica:
			S�o normalmente especificada por regras de neg�cio e implementadas na aplica��o. Podem ser implementadas pelos SGBD's atrav�s de TRIGGERS e ASSERTIONS.

3.2 - Modelagem Orientada a Objetos.
	� O modelo de dados Objeto-Relacional combina os bef�cios do Modelo Relacional com a capacidade de modelagem do Modelo Orientado a Objetos. Este modelo utiliza refer�ncias para representar conex�es entre objetos tornando as consultas baseadas em caminhos de refer�ncia mais compactas dos que as consultas feitas com jun��o. Com essas refer�ncias conseguimos suporte para realizar consultas complexas sobre dados complexos. 
	� Utiliza os construtores set, list, multiset ou array para organizar cole��es de objetos.
	� Traz vantagens como o uso de heran�a e assim aumenta o reuso de c�digo por parte da aplica��o.
	� Faz uso de uma extens�o da linguagem de consulta SQL. 
	
	##9. Linguagem SQL ANSI (DDL, DML, DCL, DTL, DQL, Operadores e Fun��es). 

Diferen�a entre comandos DDL, DML, DCL, DTL, DQL:
� DDL - Data Definition Language � usada para definir a estrutura do banco de dados ou esquema. Exemplos:
CREATE, ALTER, TRUNCATE, COMMENT, RENAME
� DML - Data Manipulation Language � utilizada para o gerenciamento de dados dentro de objetos do banco. Exemplos:
	SELECT, INSERT, UPDATE, DELETE, CALL, EXPLAIN PLAN, LOCK TABLE
� DCL - Data Control Language � usada para declara��es. Exemplos:
	GRANT, REVOKE
� TCL (DTL) - Transaction Control Language � usada para gerenciar as mudan�as feitas por instru��es DML. Exemplos:
	COMMIT, SAVEPOINT, ROLLBACK
� DQL - Data Query Language cont�m comandos que fazem consultas ao banco de dados.

Obs.: Existe uma confus�o sobre onde o comando SELECT se encaixa nessas categorias, alguns autores colocam como sendo parte da DML e outros como parte da DQL

```
Fun��es NULL relacionadas:

NVL

A fun��o NVL permite substituir valores nulos com um valor padr�o. Se o valor do primeiro par�metro for nulo, a fun��o retorna o valor no segundo par�metro. Se o primeiro par�metro � qualquer valor diferente de nulo, ele � retornado inalterado.

  SELECT id, NVL(col1, 'ZERO') AS output FROM null_test_tab ORDER BY id;

DECODE

A fun��o DECODE n�o � especificamente para o tratamento de valores nulos, mas ele pode ser usado de uma forma semelhante � fun��o NVL. Sintaxe:

  DECODE( expression , search , result [, search , result]... [, default] )

Exemplo:

  SELECT id, DECODE(col1, NULL, 'ZERO', col1) AS output FROM null_test_tab ORDER BY id;

NVL2

A fun��o NVL2 aceita tr�s par�metros. Se o primeiro valor do par�metro n�o � nulo que devolve o valor do segundo par�metro. Se o primeiro valor do par�metro � null, ele retorna o terceiro par�metro.

  SELECT id, NVL2(col1, col2, col3) AS output FROM null_test_tab ORDER BY id;

COALESCE

Ele aceita dois ou mais par�metros e retorna o primeiro valor n�o nulo em uma lista. Se todos os par�metros conter valores nulos, retorna nulo.

  SELECT id, COALESCE(col1, col2, col3) AS output FROM null_test_tab ORDER BY id;

NULLIF

Ele aceita dois par�metros e retorna nulo se ambos os par�metros s�o iguais. Se eles n�o s�o iguais, o primeiro valor do par�metro � devolvido.

  SELECT id, NULLIF(col3, col4) AS output FROM null_test_tab ORDER BY id;

LNNVL

A fun��o LNNVL est� dispon�vel desde, pelo menos, Oracle 9i, mas foi indocumentados at� Oracle 11g. Ele � utilizado em uma cl�usula WHERE para avaliar uma condi��o. Se essa condi��o for avaliada como falsa ou desconhecida, ele retorna true. Se a condi��o for avaliada como verdadeira, ele retorna falso.

  SELECT id, col3 FROM null_test_tab WHERE LNNVL(col1 IS NULL) ORDER BY id;

NANVL

A fun��o NANVL foi introduzido no Oracle 10g para uso com o BINARY_FLOAT e tipos de dados BINARY_DOUBLE, que pode conter um especial "n�o � um n�mero" ou valor "NaN". A fun��o � semelhante � NVL, mas em vez de testar NULL ele testa valores "NaN".

SYS_OP_MAP_NONNULL

Vimos que uma compara��o de "NULL = NULL" sempre retornar� falso, mas �s vezes voc� quer que ele retorne true. � poss�vel fazer isso acontecer usando as fun��es NVL e DECODE, mas dependendo de como voc� us�-los esta depende de voc� converter o valor nulo para outro valor que voc� espera nunca vai estar presente na coluna ou vari�vel.

  SELECT id, 'col1=col2'

FROM null_test_tab
WHERE SYS_OP_MAP_NONNULL(col1) = SYS_OP_MAP_NONNULL(col2);
```

##15. Normaliza��o

###Objetivos da Normaliza��o

Por que normalizar as tabelas de um banco de dados?
* Diminuir o espa�o de armazenamento dos dados
* Aumentar a efici�ncia de consultas e atualiza��es
* Remover poss�veis anomalias de atualiza��o


```
 Um processo de normaliza��o aplicado com rigor nas tabelas relacionais de um modelo de dados poder� implicar em
a)
menor seguran�a nos acessos aos sistemas.
**b)**
menor desempenho em transa��es de consultas.
c)
maior redund�ncia de dados nos arquivos.
d)
maior performance nas atualiza��es dos bancos.
e)
maior simplifica��o na administra��o das tabelas.

Explica��o: ?

```


### Formas Normais

Forma Normal | Teste | Solu��o (normaliza��o)
------------ | ------------- | ------------- 
Primeira (1FN) | Rela��o n�o deve ter atributos multivalorados ou rela��es aninhadas | Formar novas rela��es para cada atributo multivalorado ou rela��o aninhada
Segunda (2FN) | Para rela��es em que a chave prim�ria cont�m m�ltiplos atributos, nenhum atributo n�o chave dever� ser funcionalmente dependente de uma parte da chave prim�ria | Decompor e montar uma nova rela��o para cada chave parcial com seu(s) atributo(s) dependente(s). Certificar-se de manter uma rela��o com a chave prim�ria original e quaisquer atributos que sejam total e funcionalmente dependentes dela.
Terceira (3FN) | A rela��o n�o deve ter um atributo n�o chave determinado funcionalmente por outro atributo n�o chave (ou por um conjunto de atributos n�o chave). Ou seja, n�o deve haver depend�ncia transitiva de um atributo n�o chave sobre a chave prim�ria | Decompor e montar uma rela��o que inclua o(s) atributo(s) n�o chave quem determina(m) funcionalmente outro(s) atributo(s) n�o chave

####Primeira Forma Normal (1FN)
Afirma que o dom�nio de um atributo deve incluir apenas valores at�micos (simples, indivis�veis) e que o valor de qualquer atributo em uma tupla deve ser um �nico valor do dom�nio desse atributo. 

Em resumo: remover atributos multivalorados, atributos compostos e suas combina��es.

####Segunda Forma Normal (2FN)
Um esquema de rela��o R est� na Segunda Forma Normal se, e somente se, est� na Primeira Forma Normal e se cada atributo n�o principal A em R for total e funcionalmente dependente da chave prim�ria em R.

Em resumo: remover dependencias parciais.

####Terceira Forma Normal (3FN)
Uma rela��o est� na Terceira Forma Normal se ela est� na Segunda Forma Normal e nenhum atributo n�o chave (n�o-prim�rio) � transitivamente dependente da chave prim�ria.

Em resumo: n�o deve existir depend�ncia transitiva.

####Forma Normal de Boyce-Codd (FBNC)
A **Forma Normal Boyce-Codd (FBNC)** foi proposta como uma forma mais simples da 3FN mas descobriu-se que ela era mais rigorosa. Ou seja, cada rela��o em FBNC tamb�m est� na 3FN. Por�m, uma rela��o na 3FN n�o necessariamente est� na FBNC.

Uma rela��o est� na Forma Normal de Boyce-Codd se todo determinante � uma chave candidata.

####Quarta Forma Normal (4FN) 
* Depend�ncia Funcional: Significa que o valor de um atributo pode ser determinado a partir de outros.
* Multi-depend�ncia Funcional: Embora um conjunto de atributos n�o possa determinar o valor de outro atributo, ainda assim esse conjunto consegue restringir os valores poss�veis para aquele atributo.

Um esquema de rela��o R est� na 4FN com rela��o a um conjunto de depend�ncias funcionais ou multivaloradas F se, para toda depend�ncia multivalorada n�o-trivial X ->-> Y em F+, X for uma superchave de R.

####Quinta Forma Normal (5FN)
Ocorre quando h� uma multi-depend�ncia c�clica entre pelo menos 3 conjuntos de atributos da chave da rela��o. � importante pois a decomposi��o de uma rela��o em um conjunto de rela��es (devido principalmente as necessidades de normaliza��o), quando envolve multi-depend�ncias c�clicas implicam na perda de informa��es devido � depend�ncia de jun��o.
S� ocorre em rela��es que possuem pelo menos tr�s atributos como parte da chave prim�ria. Encontra a depend�ncia de jun��o que permite decompor a rela��o sem perdas.