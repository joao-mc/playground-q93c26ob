----
Passagem de Parâmetros por valor
----
A passagem de parâmetros apresentada a até aqui é chamada de passagem por valor. 
Nesta tipo, os valores contidos nas variáveis do programa, no momento da chamada da função são copiados para as variáveis parâmetros da função.
As alterações dos valores dos parâmetros dentro da função não afetarão os valores das variáveis do progrmama usadas na chamada da função. 
No exemplo a seguir a variável f, passada por parâmetro para a função cem não terá o valor alterado dentro da função.

#include <stdio.h>

void Cem(float a)
{
    a = 100.0;
}

void main()
{
   float f;

    f = 20.7;
    Zera(f);
    printf("%d", f); // o valor impresso será 20.7 pois o parâmetro da função foi passado por valor.
} 


Obs: <b>void</b> significa que a função não retorna valor para o programa que a chama, logo é denominada de <b>procedimento</b>.
