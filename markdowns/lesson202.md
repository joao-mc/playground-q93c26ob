# Estrutura de Dados Homogênea (Matriz)
---
+ As matrizes são estruturas de dados que possuem mais de uma dimensão (vetor). Diferentemente dos vetores que precisam de apenas um índice para acesso aos elementos, as matrizes necessitam utilizar um índice para cada dimensão.

+ Aqui, apenas apresentaremos as Matrizes bidimensionais, isto é, são matrizes onde seus elementos estão dispostos por linhas e colunas.

![programa](/markdowns/matriz.gif)

Como no exemplo acima, para  declarar a matriz 2x5, fazemos:
<b>int Mat[2][5];</b>

+ Note que temos duas linhas:<b> Mat[0][]</b> e <b>Mat[1][]</b>, e em cada linha dessa temos 5 elementos.
Ou seja, é uma matriz de duas linhas e cinco colunas. Sempre o primeiro número é a linha e o segundo é a coluna.
---
# Inicializar uma Matriz
---
+ Para inicializar uma Matriz, isto é, mover valores para todos os elementos precisamos de duas estrutura de repetição encadeadas. Uma estrutura de repetição <b>FOR</b> para percorrer as linhas da Matriz e outra para percorrer as colunas.
+ Por exemplo, mover o valor 100 para todas as posições de uma matriz do tipo int com 2 linhas e 5 colunas.
```
   for(i = 0; i < 2; i++)
   {
     for(j = 0; j < 5; j++)
     {
       vet[i][j] = 100;
     }
    }
```
![programa](/markdowns/movematriz.gif)


