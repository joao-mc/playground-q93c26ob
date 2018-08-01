# Funções Recursivas
---
+ A recursão é uma técnica que define um problema em termos de uma ou mais versões menores deste mesmo problema.
+ A recursão pode ser utilizada sempre que for possível expressar a solução de um problema em função do próprio problema.
+ Uma função é dita recursiva quando dentro do seu código existe uma chamada para si mesma.
Por Exemplo:
Calcular o Fatorial de um número N inteiro qualquer. Se formos analisar a forma de cálculo temos:

![programa](/markdowns/recursividade.png)

Logo, temos que:
```
fat(5) = 5 x fat(4)
fat(4) = 4 x fat(3)
fat(3) = 3 x fat(2) 
fat(2) = 2 x fat(1)
fat(1) = 1 x fat(0)
fat(0) = 1
```
A seguir, um exemplo da função fatorial com e sem recursão (modifique o valor de num e execute novamente):
``` C runnable
#include<stdio.h>
int fatorialrec(int num)
{
  if (num == 0) {
    return 1;
  }
  else {
    return num * fatorial(num-1);
  }
}
int fatorialsemrec(int num)
{
  int f, i;
  if (num == 0) {
    return 1;
  }
  else {
   f = 1;
   for(i= num; i > 1; i--){
     f = f + f * i;
   }     
    return f; 
  }
}
int main() {
  int num;
  num = 5;
  printf("\nfatR(%d) = %d", num, fatorialrec(num));
  printf("\n\nfatS(%d) = %d", num, fatorialsemrec(num));

}
```
