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