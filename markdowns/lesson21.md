Aninhamento de IFs
----
A estrutura de decisão (condicional) ```IF``` permite, no máximo, duas possibilidades de execução dos comandos: uma possibilidade é a execução de comandos associadas a condição <b>Verdadeira</b> e a outra possibilidade está associada a condição <b>Falsa</b>, como mostra o exemplo a seguir:
``` C
if(condição) {
  comandosA;     <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira.
} 
else {
  comandosB;     <----- Esses comandos só serão executados, se a condição for avaliada Falsa.
}
```
Mas, existem situação em que temos mais de duas possibilidades na condição associada ao <b>IF</b> (p.ex. menus com várias opções de escolha). Nesses casos nos vemos obrigados a arruma a estrutura para possibilitar a representação desses <b>"Caminhos"</b>. Estamos falando do "Aninhamento de if´s".
``` C
if(condição) {
  comandosA;       <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira.
} 
else {
  if (condição) { 
    comandosB;     <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira.
  }
  else {
    if (condição) {
      comandosC;    <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira. 
    }  
    else{
      comandosD;    <----- Esses comandos só serão executados, se a condição do último if for avaliada Falsa.               
    }
  }      <-------- Fechamento do Segundo else   
} <-------- Fechamento do Terceiro else  
```
Podemos ter quantos if´s forem necessários a solução do problema (no exemplo acima apresentamos apenas 3).
----
Exemplo
----
Faça um programa que calcule o desconto de uma compra efetuada obedecendo os seguintes percentuais: 
+ 10% de desconto se a compra for menor ou igual que R$2.000,00; 
+ 5% de desconto se a compra for maior que R$ 2.000,00 e menor ou igual a R$ 3.000,00;
+ 3% de desconto se for maior que R$ 3.000,00 e menor ou igual a R$ 5.000,00;
+ 2% de desconto para compras acima de R$ 5.000,00.
no exemplo abaixo modifique o valor da variável compr para avaliar as outras situações.
``` C runnable
#include<stdio.h>
int main() {
if(condição) {
  comandosA;       <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira.
} 
else {
  if (condição) { 
    comandosB;     <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira.
  }
  else {
    if (condição) {
      comandosC;    <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira. 
    }  
    else{
      comandosD;    <----- Esses comandos só serão executados, se a condição do último if for avaliada Falsa.               
    }
  }      <-------- Fechamento do Segundo else   
} 
pritnf("O seu desconto foi de %f e você ira pagar %f reais.", perc, desconto);
```
