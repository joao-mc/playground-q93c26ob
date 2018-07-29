# Vamos Praticar?

Exercício 1
---
<p>Uma empresa comercial possui um programa para controle das receitas e despesas em seus 10 projetos. Os projetos são numerados de 0 até 9. Faça um programa C que controle a entrada e saída de recursos dos projetos. O programa deverá ler um conjunto de informações contendo: Número do projeto, valor, tipo despesa ("R" - Receita e "D" - Despesa). O programa termina quando o valor do código do projeto for igual a -1. Sabe-se que Receita deve ser somada ao saldo do projeto e despesa subtraída do saldo do projeto. Ao final do programa, imprirmir o saldo final de cada projeto.</p> 
<p>Dica: Usar uma estrutura do tipo vetor para controlar os saldos dos projetos. Usar o conceito de <b>struct</b> para agrupar as informações lidas.</p>

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
----

Exercício 2
---
Faça um programa C para calular o número de lâmpadas 60 watts necessárias para um determinado cômodo. O programa deverá ler um conjunto de informações, tais como: tipo, largura e comprimento do cômodo. O programa termina quando o tipo de cômodo for igual -1. A tabela abaixo mostra, para cada tipo de cômodo, a quantidade de watts por metro quadrado.
<p>Dica: Use uma estrutura <b>struct</b> para agrupar logicamente as informações de um comodo (int tipo de comodo, float largura e float altura). Usar uma função (float CalulaArea) para calcular a área do cômodo. Os atributos de entrada serão a largura e comprimento do cômodo. Usar uma função (float Lampada) para calcular a quantidade de lâmpadas necesárias para o cômodo. Os atributos de entrada serão o tipo de cômodo e a metragem (em m<sup>2</sup>) do cômodo.</p>
<p>Obs: Utilize a função <b>ceil(numero)</b> em <b>#include math.h </b> para realizar o arrendondamento para cima.</p>

![programa](/markdowns/potencia.png)

@[IDE]({"stubs": ["./www/exercicio"],"command": "sh /project/target/www/exercicio.sh"
})

::: Solução

``` C
#include<stdio.h>
#include<math.h>

float CalculaArea(float largura, float comprimento){
  return largura * comprimento;
}

float Lampada(int tipo, float metragem){
     float quantidade;
     int potencia;
    switch(tipo){
      case 0:
        potencia = 12;
        break;
      case 1:
        potencia = 15;
        break;
      case 2:
        potencia = 18;
        break;
      case 3:
        potencia = 20;
        break;
      case 4:
        potencia = 22;
        break;
      default:
        potencia = 0;  // Tipo inválido
    }
  quantidade = (metragem * potencia) / 60;
  return quantidade;
}
int main(){

 struct {
 int tipo;
 float larg, comp;
 } comodo;
 float nlampadas;
 float tamanho;
 printf("\n\nDigite o tipo de comodo (0 ate 4):");
 scanf("%d", &comodo.tipo);
 while(comodo.tipo != -1) {
  printf("\n\nDigite a largura do comodo:");
  scanf("%f", &comodo.larg);
  printf("\n\nDigite o comprimento do comodo:");
  scanf("%f", &comodo.comp);
  tamanho = CalculaArea(comodo.larg, comodo.comp);
  nlampadas = Lampada(comodo.tipo, tamanho);
  printf("\n\n Pela metragem de seu comodo voce ira precisar de %f lampadas",ceil(nlampadas));
  printf("\n\nDigite o tipo de comodo (0 ate 4):");
  scanf("%d", &comodo.tipo);

 }
}
```
:::
----

Exercício 3
---
Faça um programa que receba uma frase (máximo 100 caracteres) e uma letra qualquer, calcule e mostre a quantidade que essa letra aparece na frase digitada. Para descobrir o tamanho da frase digitada utilize a função <b>strlen(cadeia de caracteres)</b>.
<p>Dica: Usar a função <b>gets(cadeia de caracteres)</b> - biblioteca <b>sring.h</b> para realizar a leitura da frase. A função <b>scanf</b> só realiza leitura até o primeiro espaço em branco. </p>

@[IDE]({"stubs": ["./www/exercicio"],"command": "sh /project/target/www/exercicio.sh"
})
::: Solução

``` C
#include<stdio.h>
#include<string.h>
int main(){
 char frase[101];
 char letra;
 int i, cont, tam ;

 printf("\n\nDigite uma frase (Max. 100 caracteres): ");
 gets(frase);
 tam = strlen(frase);
 printf("\n\nDigite a letra que você deseja procurar: ");
 scanf("%c",&letra);

 cont =0;
 i=0;
 while (i <= tam) {

   if (frase[i] == letra) {
     cont = cont + 1;
   }
   i++;
 }
 printf("\n\nA letra \'%c\' apareceu %d vezes", letra, cont);

}
```
:::
----
Exercício 4
---
Faça um programa que controle os estoque de 5 produtos em 5 armazéns de um supermercado, conforme figura abaixo: 

![programa](/markdowns/estoque.png)

O programa deverá ler o número da linha e da coluna, correspondete ao produto no armazem, e a quantidade a ser retirada do estoque. Caso a quantidade solicitada for menor ou igual a quantidade em estoque, o programa deverá emitir uma mensagem de atendiemtneo e dar baixa no estoque. Do contrário, emitir mensagem, "Estoque com quantidade insuficiente para atender ao pedido. O programa termina quando o numero da linha for igual a -1.
Utilize a declaração abaixo para resolver o exercício:
<p>int estoque[5][5]= {{150,0,100,150,200}, {200,300,230,100,90}, {250,300,0,200,150}, {300,100,90,450,0},{350,300,400,250,200}}</p>

