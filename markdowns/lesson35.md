# Praticando Ponteiros e Funções
---
?[Assinale a alternativa correta com relação ao estudo de Ponteiros?]
-[ ] Ponteiro é o valor de uma variável 
-[ ] Ponteiro é o indicador da próxima variável a ser passada
-[x] Ponteiro é uma variável que armazena endereço
-[ ] Ponteiro é o endereço que aponta para uma variável

?[Quais das seguintes instruções declaram um ponteiro para uma variável float?]
-[x] float *p; 
-[ ] float p;
-[ ] *float p;
-[ ] float p*;

```C
int x, y, *p;
y = 0;
p = &y;
x = *p;
x = 4;
(*p)++;
--x;
(*p) += x;
printf("x=%d  y=%d *p=%d", x, y, *p);
```
?[Seja o trecho de código acima, quais serão os valores de x, y e *p no comando printf?]
-[ ] x = 4  y = 0 *p = 4
-[ ] x = 3  y = 3 *p = 3
-[ ] x = -1 y = 0 *p = 0
-[x] x = 3  y = 4 *p = 4

---
Exercício 1
---
Faça um programa que modifique as vogais de uma frase. O programa deve ler uma frase (max. 100 caracteres) e armazeá-la num vetor. Imprimir a frase lida trocando as vogais, isto é, trocar 'a' pelo 'u',  'e' pelo 'o', 'i' pelo 'u', 'o' pelo 'a' e o 'u' pelo 'e'. Usar uma função void (procedimento) para realizar a troca e uma função para realizar a impressão da frase trocada. A função deve ter como parâmetro um ponteiro char referente ao vetor. Dica: Use a função <b>gets()</b> da biblioteca string.h para realizar a leitura da frase. use o switch para realizar as trocas.


@[IDE]({"stubs": ["./www/exercicio"],"command": "sh /project/target/www/exercicio1.sh"
})


::: Solução

``` C
#include<stdio.h>
int main(){
int estoque[5][5]= {{150,0,100,150,200}, {200,300,230,100,90}, {250,300,0,200,150}, {300,100,90,450,0},{350,300,400,250,200}};
int lin, col;
int quant;

 printf("\n\nDigite lin correspondente ao armazem:");
 scanf("%d", &lin);
 while(lin != -1) {
  printf("\n\nDigite col correspondente ao produto:");
  scanf("%d", &col);
  printf("\n\nDigite a quantidade pedida:");
  scanf("%d", &quant);
  if (quant <= estoque[lin][col]){
    estoque[lin][col] = estoque[lin][col] - quant;
  }
  else {
    printf("\n\nEstoque com quantidade insuficiente para atender ao pedido");
  }

  printf("\n\nDigite lin correspondente ao armazem:");
  scanf("%d", &lin);

 }
 for (lin=0; lin < 5; lin++){
  printf("\n");
  for (col=0; col < 5; col++){
     printf("%d ", estoque[lin][col]);
  }
 }
}

```
:::
----

