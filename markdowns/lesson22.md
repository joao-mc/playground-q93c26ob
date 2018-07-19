Estrutura Condicional switch...case
----
A estrutura <b>switch...case</b> representa de uma maneira mais simples o encadeamento de ```IF´s```. É uma forma de reduzir a complexidade de vários <b>if … else</b> encadeados.
O conteúdo da <b>variável</b> da cláusula ,b>switch</b> é comparado com os valores constantes das cláusulas <b>case</b>, e caso uma das comparações seja verdadeira, o comando associado é executado (somente esse comando). Caso nenhuma comparação seja Verdadeira, a estrutura executará a cláusula <b> default</b>.

```C
switch (variável)
{
   case constante1:
     comandosA;
   break;

   case constante2:
     comandosB;
   break;

   default
     comandosC;
}
```
Obs: Cada estrutura case deve finalizar com o comando <b>break</b>, pois é a forma de sair da estrutura <b>switch</b>, caso a condição seja Verdadeira.  
