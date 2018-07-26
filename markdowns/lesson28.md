# Estruturas de dados Heterogêneas(Union e Enum)

Union
---
+ As estruturas de dados do tipo <b>Union</b> permite armazenar diferentes tipos de dados no mesmo local de memória. 
+ A grande vantagem dessa estrutura esta na organização da memória, e no seu reaproveitamento, isto é, as unions fornecem uma maneira eficiente de usar o mesmo local de memória para vários propósitos.
---
Definindo uma Union
---
+ Para definir uma union, você deve usar a instrução union da mesma forma que definiu uma estrutura. 
+ A instrução union define um novo tipo de dados com mais de um membro para o seu programa. 
+ O formato da declaração da união é o seguinte -
``` 
union [Nome_do_Tipo_Union] {
   Tipo_de_dado1 variavel1;
   Tipo_de_dado2 variavel2;
   ...
   Tipo_de_dadoN variavelN;
} [uma ou mais variaveis Union];  

*Nome_do_Tipo_Union é opcional. Não é necessário definir.
```
+ No exemplo a seguir, a variável <b>dado<b> é uma union e poderá ser do tipo int, float ou cadeia de caracteres. Depende do valor que será movido.
```C runnable
#include <stdio.h>
#include <string.h>
int main( ) { 
  union {
   int i;
   float f;
   char str[20];
  } dado;
 
  dado.i = 10; /* union sera do tipo inteiro */
  printf( "Sou inteiro : %d\n", dado.i);
  dado.f = 34.5; /* union sera do tipo float */
  printf( "Sou real : %f\n", dado.f);
  strcpy(dado.str,"Sou String"); /* union sera do tipo String */
  printf( "Sou string : %s\n", dado.str);

   return 0;
}
```
---
Enum
---
+ As Enumerações, são um tipo definido pelo usuario, utilizando se de uma lista de identificadores. Os indentificadores desta lista, se assemelham a constantes.
