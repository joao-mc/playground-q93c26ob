Estrutura Condicional switch...case
----
A estrutura <b>switch...case</b> representa de uma maneira mais simples o encadeamento de ```IF´s```. É uma forma de reduzir a complexidade de vários <b>if … else</b> encadeados.
O conteúdo da <b>variável</b> da cláusula <b>switch</b> é comparado com os valores constantes das cláusulas <b>case</b>, e caso uma das comparações seja verdadeira, o comando associado é executado (somente esse comando). Caso nenhuma comparação seja Verdadeira, a estrutura executará a cláusula <b> default</b>.

```C
switch (variável)
{
   case constante1:
     comandosA;
   break;

   case constante2:
     comandosB;
   break;

   default:
     comandosC;
}
```
Obs: Cada cláusula <b>case</b> na estrutura deverá finalizar com o comando <b>break</b>, pois é a forma de sair da estrutura <b>switch</b>, caso a condição seja Verdadeira.  

Exemplo
----
Faça um programa que exiba o número contido na variável associada ao comando switch: 
No exemplo abaixo modifique o valor da variável <b>resp</b> para avaliar as outras situações.
``` C runnable
#include<stdio.h>
int main() {
 int resp;

 resp = 3; /* Modifique o valor da variavel resp e teste outras condições*/
 switch (resp)
{
   case 1:
     printf("Voce selecionou a opcao %d", resp);
   break;

   case 2:
     printf("Voce selecionou a opcao %d", resp);
   break;
   case 3:
     printf("Voce selecionou a opcao %d", resp);
   break;
   
   default:
      printf("Voce selecionou uma opcao deiferent de 1, 2 ou 3 --> %d", resp);
}

}
```
---
###### Exercício  
----
Faça um programa em c que solicite dois operandos e o tipo de operação aritmética que desejar, conforme opções abaixo:
1 - Soma
2 - Subtração
3 - Multiplicação
4 - Divisão
5 - Exponenciação

Caso o usuário selecione a opção 4 (divisão), verificar se o denominador é diferente de zero. Caso o usuário digitar uma opção inválida emitir mensagem.
 
@[IDE]({"stubs": ["./www/exercicio"],"command": "sh /project/target/www/exercicio.sh"
})
::: Solução

``` C
#include <stdio.h>
#include <stdlib.h>
#include<math.h>
 
int main()
{
    int x, y, resultado, 
    int op;
    x=0;
    y=0;
    resultado=0;
    op=0;
 
    printf(" \n Digite o valor do primeiro operando: ");
    scanf("%d", &x);
    printf(" \n Digite o valor do segundo operando: ");
    scanf("%d", &y);
 
    printf(" \n Escolha uma das opções abaixo: ");
    printf(" \n 1. Soma ");
    printf(" \n 2. Subtração ");
    printf(" \n 3. Multiplicação ");
    printf(" \n 4. Divisão ");
    printf(" \n 5. Exponenciação ");
    
    printf(" \n Digite o número da opção desejada: ");
    scanf("%d", &op);
 
    switch (op)
    {
    case 1:
        printf(" \n Opção selecionada: 1. Soma ");
        resultado = x + y;
        printf(" \n A soma dos dois números é: %d ", resultado);
        break;
 
    case 2:
        printf(" \n Opção selecionada: 2. Subtração ");
        resultado = x - y;
        printf(" \n A subtração dos dois números é: %d", resultado);
        break;
 
    case 3:
        printf(" \n Opção selecionada: 3. Multiplicação ");
        resultado = x * y;
        printf(" \n A multiplicação dos dois números é: %d", resultado);
        break;
 
    case 4:
        printf(" \n Opção selecionada: 4. Divisão ");
        if(y=0)
        {
            printf(" \n Não existe divisão por zero ");
        }
        else
        {
            resultado = x / y;
            printf(" \n A divisão dos dois números é: %d", resultado);
        }
 
        break;
    default:
        printf(" \n Você digitou uma opção inválida!");
    }
 
    return 0;
}


```
:::
----
