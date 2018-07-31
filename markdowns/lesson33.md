# Ponteiros e Vetores
---
+ Vetores são conjuntos de dados do mesmo tipo dispostos contiguamente (um depois do outro) na memória.
+ No momento da declaração de um vetor, informamos ao computador para reservar uma certa quantidade de memória a fim de armazenar os elementos do array de forma sequencial. 
+ A variavel vetor é um ponteiro que aponta para o começo da sequência elementos do vetor na memória. Portanto, podemos inicializar uma variável ponteiro com o endereço de início do vetor.

![figura](/markdowns/vetpoint.png) 

``` C runnable
#include<stdio.h>
int main() {
 char *ptr;
 int i;
 char vet[5] = {'a', 'b', 'c', 'd', 'e'};
 
 ptr = vet;  // A variavel ponteiro ptr aponta para o primeiro elemento do vetor
 for (i=0; i < 5; i++){
  printf("\nVet[%d] = %c    ptr = %c", i, vet[i], *ptr); // o conteudo do vetor acessado pela variavel e pelo ponteiro
  ptr++; 
 } 
}
````
+ Em Resumo:
  <p><b>*p</b> é equivalente a <b>vet[0];</b></p>
  <p><b>vet[índice]</b> é equivalente a <b>*(p+índice);</b></p>
  <p><b>vet</b> é equivalente a <b>&vet[0];</b></p>
  <p><b>&vet[índice]</b> é equivalente a <b>(vet + índice);</b></p>

+ As matrizes, apesar de terem mais de uma dimensão, são dispostas linearmente na memória e, por isso, podem ser manipuladas com ponteiros semelhante aos vetores. 
<p>Ex.: 
int mat[5][5];</p>

![figura1](/markdowns/mat.png) 
