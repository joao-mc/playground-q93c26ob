# Gravar e Ler em Arquivos
---
+ Após a abertura do arquivo é possível Ler e/ou gravar dados nele.
+ A função <b>fputc()</b> possibilita a gravação de dados caracter a caracter. </br>
              <em><b>int fputc(int ch, FILE *arq);</b></em>
+ A função <b>fgetc()</b> possibilita a leitura de dados do arquivo caracter a caracter. </br>
              <em><b>int fgetc(FILE *arq);</b></em>              
+ O Exemplo a seguir solicita ao usuário um texto com até 50 caracteres de comprimento, cria o arquivo <b>arqtexto.txt</b> na pasta corrente e grava esse texto caracter a caracter. Uma vez gravado os dados no arquivo, utilizamos a função <b>fgetc()</b> para ler os dados caracter a caracter:
``` C runnable
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int main()
{
    FILE *farq;
    int i;
    char tentrada[50];
    char tsaida[50];
farq = fopen("arqtexto.txt", "w");
printf("Entre com um texto ate 50 cartacteres:");
gets(tentrada);
for (i=0; i < strlen(tentrada); i++)
{
   fputc(tentrada[i],farq);
}
fclose(farq);
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
 
