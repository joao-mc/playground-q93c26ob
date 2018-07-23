# Estrutura de Dados Homogênea (Matriz)
---
+ As matrizes são estruturas de dados que possuem mais de uma dimensão (vetor). Diferentemente dos vetores que precisam de apenas um índice para acesso aos elementos, as matrizes necessitam utilizar um índice para cada dimensão.

+ Aqui, apenas apresentaremos as Matrizes bidimensionais, isto é, são matrizes onde seus elementos estão dispostos por linhas e colunas.

![programa](/markdowns/matriz.gif)

Como no exemplo acima, para  declarar a matriz 2x5, fazemos:
<b>int Mat[2][5];</b>

+ Note que temos duas linhas:<b> Mat[0][]</b> e <b>Mat[1][]</b>, e em cada linha dessa temos 5 elementos.
Ou seja, é uma matriz de duas linhas e cinco colunas. Sempre o primeiro número é a linha e o segundo é a coluna.

Para declarar matrizes e inicializar, devemos colocar cada linha entre chaves {}, e separar elas por vírgulas, veja:
float notas[2][5] = { {8.0, 7.5, 8.5, 9.0, 8.0 }, {8.9, 9.0, 8.6, 8.4, 8.0 } };

Uma maneira mais simples de ver essas linhas e colunas, como tabela, é da seguinte maneira:
float notas[2][5] = { {8.0, 7.5, 8.5, 9.0, 8.0 },
                              {8.9, 9.0, 8.6, 8.4, 8.0 } };
