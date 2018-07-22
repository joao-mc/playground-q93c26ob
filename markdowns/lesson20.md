# Estruturas de Dados Homogêneas
---
+ Estrutura de dados Homogênea ou Matriz é uma coleção de variáveis de mesmo tipo, acessíveis com um único nome e armazenados contiguamente (um após o outro) na memória.

+ A individualização de cada variável é feita através do uso de índices.

+ Os Vetores são matrizes de uma só dimensão, isto é, necessita apenas 1 índice para acesso as variáveis. 

+ As Matrizes possuem mais de uma dimensão, isto é,  necessitam de um índice para cada dimensão para acesso as variáveis. 
 
![programa](/markdowns/vetor.gif)

---
# Declaração de Matrizes
---
        int Vetor[6];   /* declara um vetor do tipo int (números inteiros) de 6 posições */

        float Matriz[5][3]; /*declara uma matriz do tipo float(números com casas decimais) de 5 linhas e 3 colunas(15 elementos) */
        
        char Vetor[10] /* declara um vetor do tipo char com 10 posições  */

---
# Mover valores para os elementos do vetor
---
+ Na linguagem C, os vetores tem o primeiro elemento na posição 0(zero). Assim, se tomarmos "K" como sendo o tamanho do vetor a última posição é a de índice "K-1". Por exemplo, um vetor de tamanho 10 (k=10) tem o seu último elemento na posição 9.
+ Exemplos de mover valor para uma matriz/vetor 
```
               Vetor[0] = 4; /*  Move o valor 4 para a primeira posição do "Vetor" */
               Vetor[4] = 8; /*  Move o valor 8 a quinta posição do "Vetor" (Não se esqueçam que a primeira é zero). */
               Matriz[0][1] = 15; /*  coloca 15 na célula que está na primeira linha e na segunda coluna da matriz */
```
