# PL/SQL

## Cláusula SELECT

Na sintaxe tradicional do Oracle, o símbolo (+), denota um **outer join** na consulta e é inserido na coluna da tabela onde pode não haver linhas correspondentes.

No caso da questão, trata-se de left outer join, pois a consulta deve recuperar todas as linhas da tabela funcionários (tabela que está a esquerda na cláusula WHERE) mesmo que não haja correspondência na tabela departamento (tabela que está a direita na cláusula WHERE).

Logo, como a tabela departamento pode não haver linhas correspondentes, o termo (+) deve ser colocado junto a ele, conforme indicado na alternativa.
Outras maneiras de realizar essa consulta com o mesmo resultado seriam:

```sql
SELECT f.nome_funcionario, f.id_departamento, d.nome_departamento FROM funcionarios f LEFT OUTER JOIN departamentos d ON f.id_departamento = d.id_departamento;
```

```sql
SELECT f.nome_funcionario, f.id_departamento, d.nome_departamento FROM funcionarios f LEFT OUTER JOIN departamentos d USING (id_departamento);
```

## Instrução **CASE WHEN**

 - **Palavra reservada CASE:** marca o início da instrução
 - **Seletor:** valor que determina quando cláusula deve ser executada
 - **Cláusula WHEN:** contém uma expressão e uma ou mais instruções executáveis
associadas
 - **Cláusula ELSE:** opcional, funciona de forma semelhante à cláusula ELSE usado na instrução IF-THEN-ELSE
 - **END CASE:** frase reservada que indica o fim da instrução CASE

Exemplo:

```sql
CASE SELECTOR
    WHEN EXPRESSION 1 THEN STATEMENT := 1;
    WHEN EXPRESSION 2 THEN STATEMENT := 2;
    ...
    WHEN EXPRESSION N THEN STATEMENT := N;
    ELSE STATEMENT N + 1;
END CASE;
```

## Funções **NULLIF** e **COALESCE**

As funções **NULLIF** e **COALESCE** são definidas pela norma ANSI 1999 para serem abreviaturas do comando CASE. Ambas as funções podem ser usadas como variações da instrução CASE.

### Função **NULLIF**

A função **NULLIF** compara duas expressões. Se elas forem iguais, então retorna NULL, caso contrário retorna o valor da primeira expressão.

A função tem a seguinte estrutura:

```sql
NULLIF(EXPRESSION 1, EXPRESSION 2);
```

### Função **COALESCE**

A função **COALESCE** compara cada expressão com NULL a partir da lista de expressões e retorna o valor da primeira expressão com valor não nulo.

A função **COALESCE** tem a estrutura abaixo:

```sql
COALESCE(EXPRESSION 1, EXPRESSION 2, EXPRESSION 3, ..., EXPRESSION N);
```

### Função **NVL**

**Sintaxe:** NVL(expr1, expr2)

A função `NVL` permite substituir **null** por uma string no resultado de uma consulta. Se `expr1` é **null**, então `NVL` retorna `expr2`. Se `expr1` não é null, então `NVL` retorna `expr1`. Ou seja, caso `expr1` igual a **null**, o valor é substituído pela `expr2`.

### Função **TRUNC**

**Sintaxe:** TRUNC(n1 [, n2 ])

A função **TRUNC** retorna _n1_ truncado para _n2_ casas decimais. Se _n2_ é omitido , então _n1_ é truncado para 0 casas. _n2_ pode ser negativo para truncar(tornar zero) n2 dígitos à esquerda do ponto decimal.

Exemplo:

```sql
TRUNC(65.923,2)  -->  65.92
TRUNC(65.923,2)  -->  65
TRUNC(65.923,-1) --> 60
```

### Exercício de fixação

Em PL/SQL, COALESCE (expr1, expr2) é equivalente a:

a) CASE WHEN expr1 = expr2 AND expr1 IS NOT NULL END

b) SUBSTR (expr1, expr2)

c) MAX ( expr1, expr2)

d) CASE WHEN expr1 IS NOT NULL THEN expr1 ELSE expr2 END

e) WHERE expr1 IN expr2

## Procedures e Functions

## Triggers

A sintaxe básica para a criação de uma trigger é mostrada no trecho de código abaixo:

```sql
CREATE [OR REPLACE ] TRIGGER trigger_name 
    {BEFORE | AFTER | INSTEAD OF }
    {INSERT [OR] | UPDATE [OR] | DELETE} 
    [OF col_name]
    ON table_name
    [REFERENCING OLD AS o NEW AS n]
    [FOR EACH ROW] 
    WHEN (condition) 
    DECLARE
    Declaration-statements 
    BEGIN 
    Executable-statements
    EXCEPTION Exception-handling-statements 
END;
```

