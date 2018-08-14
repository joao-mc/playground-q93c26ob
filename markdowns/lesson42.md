# Vamos Praticar?

Exercício 1
---
Dado o seguinte exemplo:
``` C
FILE *farq 
farq = fopen (“arqdata.dat", “wb");
```
?[Em linguagem C, a função fopen () abre um arquivo, retornando o ponteiro associado ao arquivo, como no exemplo acima, pode-se afirmar que:]
-[ ] a criação de um arquivo binário chamado arqdata.dat, em que poderão ser realizadas operações de leitura e de escrita. 
-[ ] a criação de um arquivo chamado farq, em que poderão ser realizadas somente as operações de leitura.
-[x] a criação de um arquivo binário chamado arqdata.dat em que poderão ser realizadas somente as operações de escrita.
-[ ] a criação de um arquivo chamado farq.dat, em que poderão ser realizadas operações de leitura. 

Exercício 2
---

<p>Crie um programa C que:</p>
<p>(a) crie/abra um arquivo texto de nome "arq.txt",</p>
<p>(b) permita que o usuario entre com diversos caracteres nesse arquivo, até que o usuario entre com o caractere ’0’ (fim da entrada de dados),</p>
<p>(c) Feche o arquivo e abra novamente o arq.txt, e</p>
<p>(d) lendo-o caractere por caractere, e escrevendo na tela (printf) todos os caracteres armazenados.</p>

![programa](/markdowns/projetos.png)

@[IDE]({"stubs": ["./www/exercicio"],"command": "sh /project/target/www/exercicio.sh"
})

::: Solução

``` C
#include<stdio.h>
int main(){
 float projetos[10];
 int i;
 struct {
  int numero;
  float valor;
  char tipo;
  } boleto;
  /* Inicializar o vetor*/
  for (i=0; i < 10; i++){
    projetos[i] = 0.0;
  }

  printf("\n\nDigite o código do projeto: ");
  scanf("%d", &boleto.numero);
  while (boleto.numero != -1) {
   printf("\n\nDigite o Valor : ");
   scanf("%f", &boleto.valor);
   printf("\n\nDigite o tipo de transação (R ou D): ");
   getchar();//limpar o teclado do Enter anterior
   scanf("%c", &boleto.tipo);

   if (boleto.tipo == 'R' || boleto.tipo == 'r') {
      projetos[boleto.numero] = projetos[boleto.numero] + boleto.valor;
   }
   else {
    if (boleto.tipo == 'D' || boleto.tipo == 'd') {
      projetos[boleto.numero] = projetos[boleto.numero] - boleto.valor;
    }
    else {
      printf("Tipo Inválido !!");
    }
   }
   printf("\n\nDigite o código do projeto: ");
   scanf("%d", &boleto.numero);
  }
  for (i=0; i < 10; i++){
    printf("\nSaldo do projeto %d = %f",i, projetos[i]);
  }
}
```
:::
