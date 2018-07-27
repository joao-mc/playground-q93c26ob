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
+ O formato da declaração da <b>union</b> é o seguinte -
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
+ As enumerations definem um novo tipo de variável e limita desde logo os valores.
+ O formato da declaração da <b>enum</b>  é o seguinte -
```
enum [Nome_do_Tipo_enum] {
   identificador1,
   identificador2;
   ...
   identificadorN;
} [uma ou mais variaveis enum];  
```
+ Exemplo:
 <b> enum {black, blue, green, cyan, red, purple, yellow, white} cores;</b>
+ A maneira mais simples de interpretar uma enumeration é imagina-la como uma matriz de apenas uma linha. Temos o nome da linha de temos as várias células na linha. Cada constante enumerada (muitas vezes chamado de enumerator) tem um valor inteiro (caso não seja especificado ele começa em zero)

Exemplo:

![programa](/markdowns/enum.png)
``` C runnable
#include <stdio.h>
 int main(void)
 {
    enum { black, blue, green, cyan, red, purple, yellow, white} cores;

    cores = green;

     switch(cores) {
         case 0:
           printf("Cor preto \n");
           break;
         case 1:
           printf("Cor azul \n");
           break;
         case 2:
           printf("Cor verde \n");
           break;
         case 3:
           printf("Cor ciano \n");
           break;
         case 4:
           printf("Cor vermelho \n");
           break;
         case 5:
           printf("Cor roxo \n");
           break;
         case 6:
           printf("Cor amarelo \n");
           break;
         default:
           printf("Cor branco \n");
     }
  return  0 ;

 }

```

