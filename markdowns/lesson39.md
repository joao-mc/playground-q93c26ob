# Gravar e Ler em Arquivos
---
+ Após a abertura do arquivo é possível Ler e/ou gravar dados nele.
+ A função <b>fputc()</b> possibilita a gravação de dados caracter a caracter. </br>
              <em><b>int fputc(int ch, FILE *arq);</b></em>
+ A função <b>fgetc()</b> possibilita a leitura de dados do arquivo caracter a caracter. </br>
              <em><b>int fgetc(FILE *arq);</b></em>     
+ Quando não houver mais dados a serem lidos no arquivo, a <b>fgetc</b> devolve a constante <em><b>EOF (end of file)</b></em>, que está definida na biblioteca stdio.h. Em muitos computadores o valor de EOF é −1. Isso indica a parada do processo de leitura.
+ O Exemplo a seguir exibe a gravação e leitura de dados caracter a caracter.É criado o arquivo <b>arqtexto.txt</b> na pasta corrente e gravada a string caracter a caracter. Uma vez gravado os dados no arquivo, utilizamos a função <b>fgetc()</b> para ler esses dados caracter a caracter:
``` C runnable
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int main()
{
    FILE *farq;
    int i;
    char tentrada[61]={"Isso e um teste de gravar dados caracter a caracter"};
    char tsaida[61];
farq = fopen("arqtexto.txt", "w");
for (i=0; i < strlen(tentrada); i++)
{
   fputc(tentrada[i],farq);
}
fclose(farq);                        //<--- É Necessário fechar e abrir o arquivo novamente.
farq = fopen("arqtexto.txt", "r");
if (farq == NULL)
{
     printf("Deu Merda!!!");
     exit(1);
}
printf("\n\nVou ler e mostrar o texto gravado....\n\n");
i=0;
while (tsaida[i]!=EOF)
{
   tsaida[i]=fgetc(farq);
   printf("%c",tsaida[i]);
   i++;
}

fclose(farq);

}
```
 
