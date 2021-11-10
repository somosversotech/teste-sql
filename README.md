# TESTE SQL

###### Dado a seguinte estrutura de banco de dados, considerando:
* Colunas de Nomes como VARCHAR(255)
* Colunas de Ids como INTEGER
* Colunas de datas como DATE

##### TABLE: AUTOR
```
+-------+---------------+
|   ID  |   NOME        |
+-------+---------------+
|   1   | JOAO          |
+-------+---------------+
|   2   | PEDRO         |
+-------+---------------+
|   3   | PAULO         |
+-------+---------------+
```

##### TABLE: LIVRO
```
+-------+---------------+----------+------------+
|   ID  |   NOME        | AUTOR_ID | LANCAMENTO |
+-------+---------------+----------+------------+
|   1   | CÓDIGO LIMPO  |    1     | 2021-01-01 |
+-------+---------------+----------+------------+
|   2   | TDD           |    1     | 2019-10-01 |
+-------+---------------+----------+------------+
|   3   | ADS           |    2     | 2021-12-08 |
+-------+---------------+----------+------------+
|   4   | SQL           |    2     | 2020-10-10 |
+-------+---------------+----------+------------+
```

###### RESPONDA AS PERGUNTAS ABAIXO:

1) Monte o comando SQL responsável pela criação da tabela de LIVRO:

2) Monte o comando SQL para selecionar todos os livros do autor JOAO.
Retorno esperado:
```
+-------+---------------+----------+------------+
|  ID   |   NOME        | AUTOR_ID | LANCAMENTO |
+-------+---------------+----------+------------+
|   1   | CÓDIGO LIMPO  |    1     | 2021-01-01 |
+-------+---------------+----------+------------+
|   2   | TDD           |    1     | 2019-10-01 |
+-------+---------------+----------+------------+
```

3) Monte o comando SQL que traga a quantidade de livros por AUTOR, que foram lançados no ano de 2019.
Retorno esperado:
```
+---------------+---------+
|   NOME        | LIVROS  |
+---------------+---------+
| JOAO          |   1     |
+---------------+---------+
| PEDRO         |   0     |
+---------------+---------+
| PAULO         |   0     |
+---------------+---------+
```

4) Monte o comando SQL que traga todos os autores que não possuem livros.
Retorno esperado:
```
+-------+---------------+
|   ID  |   NOME        |
+-------+---------------+
|   3   | PAULO         |
+-------+---------------+
```

5) Monte o comando SQL que traga todos os livros com os nomes e IDs de seus respectivos autores.
Retorno esperado:
```
+-------+---------------+----------+------------+----------+
|   ID  |   NOME        | AUTOR_ID | LANCAMENTO | AUTOR    |
+-------+---------------+----------+------------+----------+
|   1   | CÓDIGO LIMPO  |    1     | 2021-01-01 | JOAO     |
+-------+---------------+----------+------------+----------+
|   2   | TDD           |    1     | 2019-10-01 | JOAO     |
+-------+---------------+----------+------------+----------+
|   3   | ADS           |    2     | 2021-12-08 | PEDRO    |
+-------+---------------+----------+------------+----------+
|   4   | SQL           |    2     | 2020-10-10 | PEDRO    |
+-------+---------------+----------+------------+----------+
```
