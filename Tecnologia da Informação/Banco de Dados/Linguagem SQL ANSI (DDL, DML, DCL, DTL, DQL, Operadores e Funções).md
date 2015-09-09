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


###Fun��es NULL relacionadas:

>As bancas costumam colocar alguma destas fun��es em quest�es perguntando o que elas fazem.

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
