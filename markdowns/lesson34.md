# Funções com passagem de parâmetros por referência
+ Outra maneira de realizar a passagem de parâmetros para um função qualquer é denominada de <b>passagem por referência</b>. Nesse tipo, utiliza-se o endereço da variável para passá-lo a função. 
+ As manipulações/alterações efetuadas nos parâmetros dentro das funções afetam diretamente as variáveis usadas nas chamadas.
+ 
 ![programa](/markdowns/referencia.png)

``` C runnable
#include<stdio.h>
void loop_count( int *i ) { // void não retorna valor
 printf( "Na função loop_count, i = " );
 while( *i < 10 )
 printf ( "%d ", (*i)++); //==> i = 2 3 4 5 6 7 8 9
}
int main( ) {
 int i = 2;
 loop_count( &i );
 printf( "\nEm main, i = %d.\n", i ); //==> a variável i foi modificada na funç~so i = 10.
}
```
