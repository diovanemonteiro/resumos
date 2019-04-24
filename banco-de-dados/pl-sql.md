# PL/SQL

## INSTRUÇÃO **CASE WHEN** SIMPLES

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

## FUNÇÃO **NULLIF**

A função **NULLIF** compara duas expressões. Se elas forem iguais, então retorna NULL, caso contrário retorna o valor da primeira expressão.

A função tem a seguinte estrutura:

```sql
NULLIF(EXPRESSION 1, EXPRESSION 2);
```

## FUNÇÃO **COALESCE**

A função **COALESCE** compara cada expressão com NULL a partir da lista de expressões e retorna o valor da primeira expressão com valor não nulo.

A função **COALESCE** tem a estrutura abaixo:

```sql
COALESCE(EXPRESSION 1, EXPRESSION 2, EXPRESSION 3, ..., EXPRESSION N);
```

### Exercício de fixação

Em PL/SQL, COALESCE (expr1, expr2) é equivalente a:

a) CASE WHEN expr1 = expr2 AND expr1 IS NOT NULL END

b) SUBSTR (expr1, expr2)

c) MAX ( expr1, expr2)

d) CASE WHEN expr1 IS NOT NULL THEN expr1 ELSE expr2 END

e) WHERE expr1 IN expr2