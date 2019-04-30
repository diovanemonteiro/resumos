# MySQL 5.5 ou superior

## Histórico de Versões

 - **1999:** Iniciou na Suécia
 - **2000:** Lançamento da versão 5.0

## ENGINES

**InnoDB** é um mecanismo de armazenamento (ENGINE) para o MySQL. O MySQL 5.5, e versões posteriores, o utilizam por padrão. Ele fornece as funcionalidades padrões de transação complacentes com ACID, juntamente com o suporte a chave estrangeira (Integridade Referencial Declarativa).

vejamos algumas características sobre a engine InnoDB:

- As operações da linguagem DML seguem o model ACID (Atomicidade, Consistência, Isolamento, Durabilidade), com transações commit, rollback, e crash-recovery para proteger os dados do usuário;
- Transações com bloqueio a nível de linha (row);
- Organização dos dados de forma a otimizar consultas baseadas em chaves primárias;
- Suporte a FOREIGN KEY constraints.

## ÍNDICES

Vamos passar rapidamente sobre o conceito e suas implicações:
 
A melhor maneira de melhorar o desempenho das operações SELECT é criar índices em uma ou mais colunas testadas na consulta.
 
As entradas de índice agem como ponteiros para as linhas da tabela, permitindo que a consulta determine rapidamente quais linhas correspondem a uma condição na cláusula WHERE e recupera os outros valores de coluna para essas linhas. Todos os tipos de dados do MySQL podem ser indexados.
 
Embora possa ser tentador criar um índice para cada coluna possível usada em uma consulta, índices desnecessários desperdiçam espaço e desperdiçam tempo para o MySQL determinar quais índices usar.
 
Os índices também aumentam o custo de inserções, atualizações e exclusões, pois cada índice deve ser atualizado. Você deve encontrar o equilíbrio certo para obter consultas rápidas usando o conjunto ideal de índices.
 
Assim, como a questão apresenta, é adequado afirmar que no MySQL os índices são usados para desconsiderar linhas a serem pesquisadas e/ou encontrar linhas abrangidas pelo WHERE mais rapidamente.

## MySQL Utilities

O **MySQL Utilities** é um pacote de utilitários voltados à manutenção e à administração de servidores MySQL. 

Cada um desses utilitários encapsula comandos primitivos e os agrupa para que possam ser utilizados no cumprimento de operações compostas a partir da execução de um único comando.

## TRIGGERS

OLD e NEW são pseudo registros na hora de execução de uma trigger. Servem para diferenciar o valor da coluna que está na tabela (OLD), e o valor do registro que será inserido(NEW). São usados para realizar operações durante a execução da trigger.
 
Para as DMLs (data manipulation language) tem-se:
 
 - Para uma trigger de INSERT: o OLD não contém valores e NEW contém os novos valores.
 - Para uma trigger de UPDATE: o OLD contém os valores antigos e NEW contém os novos valores.
 - Para uma trigger de DELETE: o OLD contém os valores antigos e NEW não contém valores.
 
Então a presença do termo NEW refere-se ao valor da coluna quant de um registro sendo inserido na tabela T.
Gabarito LETRA D.
