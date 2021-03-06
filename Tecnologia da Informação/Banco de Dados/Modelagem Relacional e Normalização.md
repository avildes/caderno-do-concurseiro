#Projeto lógico e físico de banco dados.
##Estrutura de um Projeto de Banco de Dados:
 
**1 - Análise de Requisitos:**

* Esta é a primeira etapa de um projeto de banco de dados. Nela, os requisitos devem ser coletados junto ao cliente para criar uma descrição textual (mini-mundo) do processo de forma que todos possam entender. É uma das partes mais importantes do projeto de banco de dados pois, caso seja mal feita, irá prejudicar todo o sistema.

**2 - Projeto Conceitual:**

* Nesta etapa o esquema conceitual do banco de dados é construído com base no mini-mundo gerado na etapa anterior. É muito comum utilizar o modelo entidade-relacionamento (E-R) nesta etapa. O esquema conceitual descreve o banco de dados em uma visão macro e tem o foco no conteúdo de informação: entidades, atributos, relacionamentos, etc. 

> Este nível de abstração do projeto de banco de dados representa o domínio observado independente de SGBD ou do paradigma utilizado por ele, como por exemplo, hierárquico, em rede, relacional ou orientado a objetos, entre outros. O modelo utilizado neste nível de abstração é o Modelo Entidade Relacionamento (ER).  - do livro: Questões comentadas CESPE (DominandoTI).

**3 - Projeto Lógico:**

* O objetivo do projeto lógico é definir a estrutura do banco de dados com base no projeto conceitual. Aqui serão definidas as tabelas, colunas, metadados (os tipos de dados, obrigatoriedade, chaves), relacionamentos, regras e etc. O resultado é um esquema do banco de dados parecido com o modelo conceitual, porém com mais detalhes de banco de dados e não apenas conceitos.

> O nível lógico também não depende de um SGBD específico, mas depende do paradigma utilizado pelo SGBD. Ao desenharmos um modelo lógico para o paradigma relacional, esse modelo é válido para qualquer SGBD Relacional, como por exemplo, Oracle, DB2 MS SQL SERVER, MySQL. Por outro lado, o modelo utilizado neste nível de abstração é dependente de paradigma. Por exemplo, para um SGBD Relacional será utilizado um modelo baseado em tabelas, para um SGBD Orientado a Objetos (OO), será utilizado o diagrama de classes da UML. - do livro: Questões comentadas CESPE (DominandoTI).

**4 - Projeto Físico:**

* Esta é a etapa final do projeto de banco de dados e é fortemente ligada ao Sistema de Gerenciamento de Banco de Dados (SGBD) que será utilizado. Nela definem-se os scripts de criação dos objetos no banco de dados (tabelas, visões, colunas, funções, ...), permissões de acesso de usuários e outros detalhes técnicos relacionados a implementação do banco.
* A otimização de desempenho do banco de dados é trabalhada nesta fase do projeto.

> Por último, o modelo físico depende do SGBD específico e do paradigma implementado por ele. O modelo utilizado neste nível de abstração deve ser capaz de descrever as estruturas físicas do SGBD específico. - do livro: Questões comentadas CESPE (DominandoTI).

#Modelagem de dados relacional e orientada a objetos. 

##**Modelagem Relacional:**

* Se baseia na teoria dos conjuntos (Álgebra Relacional) e representa o banco de dados como uma coleção de relações. Cada linha da tabela representa uma coleção de valores de dados relacionados. Uma linha representa um fato que normalmente corresponde a uma entidade ou relacionamento do mundo real.
	  Na terminlogia formal do modelo relacional, uma linha é chamada de tupla, um cabeçalho da coluna é chamado de atributo e a tabela é chamada relação. O tipo de dado que descreve os tipos de valores que podem aparecer em cada coluna é representado por um domínio de valores possíveis.
* **Características das relações:**

  1. **Ordenação das tuplas em uma relação:**

    Uma relação é definida como um conjunto de tuplas. Matemáticamente, os elementos de um conjunto não possuem ordem entre eles; logo, as tuplas em uma relação não possuem nenhuma ordem em particular.

  2. **Valores e NULLs nas tuplas:**

    Cada valor em uma tupla é um valor atômico; ou seja, ele não é divisível em componentes dentro da estrutura básica do modelo relacional. Logo, atributos compostos ou multivalorados não são permitidos. Grande parte da teoria por trás do modelo relacional foi desenvolvida com essa suposição em mente, que é chamada pressuposto da primeira forma normal. Assim, atributos multivalorados precisam ser representados por relações separadas e os atributos compostos são representados apenas por seus atributos de componentes simples no modelo relacional básico.
    
    Um valor especial, chamado NULL, é usado para representar os valores de atributos que podem ser desconhecidos ou não se aplicam.
	
* **Restrições:**

  1. **Restrição de domínio:**

    É possível determinar um tipo de atributo restringindo seus valores. Ao tentar inserir ou modificar um valor colocando um outro valor de um tipo diferente do primeiro, ou um valor fora do domínio especificado, esta restrição é violada e , por consequência, a operação é cancelada.
    
  2. **Restrição de integridade de chave:**
    
    Garante que tuplas de uma relação sejam únicas.

  3. **Restrição de integridade de vazio:**
    
    Especifica se os atributos podem ou não ser vazios a depender da relação a que se referem.

  4. **Restrição de integridade de entidade:**
    
    Afirma que nenhum valor de chave primária pode ser nulo.

  5. **Restrição de integridade referencial:**
    
    O valor da chave estrangeira corresponde a uma chave existente e não nula em uma tupla de outra relação.

  6. **Restrição de integridade semântica:**
    
    São normalmente especificada por regras de negócio e implementadas na aplicação. Podem ser implementadas pelos SGBD's através de TRIGGERS e ASSERTIONS.

> Questão retirada do livro: Questões comentadas CESPE (DominandoTI).
(TRT21-RN/Analista Judiciário/Tecnologia da Informação/2010) Uma chave estrangeira é um atributo ou uma combinação de atributos em uma relação, cujos valores são necessários para equivaler somente à chave primária de outra relação.

> Comentário:
  Os valores referenciados por uma chave estrangeira não precisam, necessariamente, referenciar valores de chaves candidatas. Outro erro da questão é afirmar que uma chave estrangeira sempre referencia valores de outra relação, pois a chave estrangeira pode referenciar a própria tabela no caso de um auto-relacionamento. GABARITO: Errada.
  
###Superchave, Chave Candidata, Chave Primária e Chave Alternada:

####Superchave:
Uma superchave é um conjunto de um ou mais atributos que, tomados coletivamente, nos permite identificar unicamente uma tupla (linha) da relação. Por exemplo, considerando uma tabela Empregado com as colunas CPF, Nome e Sexo, seriam exemplos de superchaves os conjuntos compostos pelas colunas (CPF, Nome, Sexo), (CPF, Sexo), (CPF, Nome) e (CPF), pois na tabela Empregado não haverá duas tuplas repetidas considerando esses subconjuntos de colunas.

####Chaves Candidatas:
As chaves candidatas são superchaves mínimas ou irredutíveis, ou seja, considerando-se uma superchave, caso qualquer atributo integrante da superchave seja suprimido ela deixa de ser uma superchave. Por exemplo, considerando-se a superchave (CPF, Nome, Sexo), ao retirarmos a coluna Sexo, o subconjunto (CPF, Nome) continua sendo uma superchave. Então (CPF, Nome, Sexo) é uma superchave, mas não é uma chave candidata. Por outro lado, a superchave (CPF) é um exemplo de chave candidata, pois é mínima e garante a unicidade das tuplas da tabela empregado.

####Chave Primária:
Chave Primária é o termo utilizado para denotar a chave candidata que é escolhida pelo projetista de banco de dados como principal meio de identificar tuplas dentro de uma relação.

####Chaves Alternadas ou Alternativas:
Chaves Primárias e Alternativas (ou Alternadas) são exemplos de chaves candidatas. Em certas situações mais de uma coluna ou combinação (irredutível) de colunas servem para distinguir uma linha das demais dentro de uma tabela. Se uma destas for escolhida como chave primária, as demais serão chamadas de chaves alternativas. Por exemplo, caso a tabela empregado também possuísse a coluna Matrícula, cujo valor fosse único para cada tupla da tabela, sua composição seria (CPF, Matrícula, Nome, Sexo). Neste caso, não há qualquer diferença entre usar CPF ou Matrícula como chave primária. Ao escolher CPF para chave primária, a coluna Matrícula passa a ser denominada chave alternativa ou alternadam também denominada chave secundária.

##**2 - Modelagem Orientada a Objetos:**

* O modelo de dados Objeto-Relacional combina os befícios do Modelo Relacional com a capacidade de modelagem do Modelo Orientado a Objetos. Este modelo utiliza referências para representar conexões entre objetos tornando as consultas baseadas em caminhos de referência mais compactas dos que as consultas feitas com junção. Com essas referências conseguimos suporte para realizar consultas complexas sobre dados complexos. 
* Utiliza os construtores set, list, multiset ou array para organizar coleções de objetos.
* Traz vantagens como o uso de herança e assim aumenta o reuso de código por parte da aplicação.
* Faz uso de uma extensão da linguagem de consulta SQL. 
	
#Normalização

##Objetivos da Normalização

Normalização é um processo aplicado às tabelas de um **modelo lógico** que visa:

* Diminuir o espaço de armazenamento dos dados

* Aumentar a eficiência de consultas e atualizações

* Remover possíveis anomalias de atualização

* Remover a redundância de dados nos arquivos.


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


## Formas Normais

Forma Normal | Teste | Solução (normalização)
------------ | ------------- | ------------- 
Primeira (1FN) | Relação não deve ter atributos multivalorados ou relações aninhadas | Formar novas relações para cada atributo multivalorado ou relação aninhada
Segunda (2FN) | Para relações em que a chave primária contém múltiplos atributos, nenhum atributo não chave deverá ser funcionalmente dependente de uma parte da chave primária | Decompor e montar uma nova relação para cada chave parcial com seu(s) atributo(s) dependente(s). Certificar-se de manter uma relação com a chave primária original e quaisquer atributos que sejam total e funcionalmente dependentes dela.
Terceira (3FN) | A relação não deve ter um atributo não chave determinado funcionalmente por outro atributo não chave (ou por um conjunto de atributos não chave). Ou seja, não deve haver dependência transitiva de um atributo não chave sobre a chave primária | Decompor e montar uma relação que inclua o(s) atributo(s) não chave quem determina(m) funcionalmente outro(s) atributo(s) não chave

###Primeira Forma Normal (1FN)
Afirma que o domínio de um atributo deve incluir apenas valores atômicos (simples, indivisíveis) e que o valor de qualquer atributo em uma tupla deve ser um único valor do domínio desse atributo. 

Em resumo: remover atributos multivalorados, atributos compostos e suas combinações.

###Segunda Forma Normal (2FN)
Um esquema de relação R está na Segunda Forma Normal se, e somente se, está na Primeira Forma Normal e se cada atributo não principal A em R for total e funcionalmente dependente da chave primária em R.

Em resumo: remover dependencias parciais.

###Terceira Forma Normal (3FN)
Uma relação está na Terceira Forma Normal se ela está na Segunda Forma Normal e nenhum atributo não chave (não-primário) é transitivamente dependente da chave primária.

Em resumo: não deve existir dependência transitiva.

###Forma Normal de Boyce-Codd (FBNC)
A **Forma Normal Boyce-Codd (FBNC)** foi proposta como uma forma mais simples da 3FN mas descobriu-se que ela era mais rigorosa. Ou seja, cada relação em FBNC também está na 3FN. Porém, uma relação na 3FN não necessariamente está na FBNC.

Uma relação está na Forma Normal de Boyce-Codd se todo determinante é uma chave candidata.

###Quarta Forma Normal (4FN) 
* Dependência Funcional: Significa que o valor de um atributo pode ser determinado a partir de outros.
* Multi-dependência Funcional: Embora um conjunto de atributos não possa determinar o valor de outro atributo, ainda assim esse conjunto consegue restringir os valores possíveis para aquele atributo.

Um esquema de relação R está na 4FN com relação a um conjunto de dependências funcionais ou multivaloradas F se, para toda dependência multivalorada não-trivial X ->-> Y em F+, X for uma superchave de R.

###Quinta Forma Normal (5FN)
Ocorre quando há uma multi-dependência cíclica entre pelo menos 3 conjuntos de atributos da chave da relação. É importante pois a decomposição de uma relação em um conjunto de relações (devido principalmente as necessidades de normalização), quando envolve multi-dependências cíclicas implicam na perda de informações devido à dependência de junção.
Só ocorre em relações que possuem pelo menos três atributos como parte da chave primária. Encontra a dependência de junção que permite decompor a relação sem perdas.
