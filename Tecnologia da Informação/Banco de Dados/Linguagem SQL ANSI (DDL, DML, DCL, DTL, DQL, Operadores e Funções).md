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
