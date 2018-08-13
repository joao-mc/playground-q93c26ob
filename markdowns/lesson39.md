# Gravando e lendo caracteres em Arquivos C
---
+ Após a abertura do arquivo é possível Ler e/ou gravar dados nele.
+ A função <b>fputc()</b> possibilita a gravação de dados caracter a caracter. 

<em><b>int fputc(int ch, FILE *arq);</b></em>

+ A função <b>fgetc()</b> possibilita a leitura de dados do arquivo caracter a caracter. 

<em><b>int fgetc(FILE *arq);</b></em>     
              
+ Quando não houver mais dados a serem lidos no arquivo, a <b>fgetc</b> devolve a constante <em><b>EOF (end of file)</b></em>, que está definida na biblioteca stdio.h, indica o fim de um arquivo. Isso indica chegamos ao fim do arquivo e não se pode realizar a leitura dos dados. Em geral, o valor de EOF é igual −1. 
+ Após a abertura do arquivo é necessário realizar o teste de fim de arquivo (o arquivo pode estar vazio):
``` C
if((fp = fopen("arquivo.txt","r")) == NULL){

printf( "Erro na abertura do arquivo");
exit(1);
}
```
+ O Exemplo a seguir exibe a gravação e leitura de dados caracter a caracter.
    + No comando fopen será criado o arquivo <b>arqtexto.txt</b> na pasta corrente 
    + A string tentrada será gravada no arquivo caracter a caracter. 
    + O arquivo será fecado e posteriormente aberto para leitura.
    + Utilizamos a função <b>fgetc()</b> para ler esses dados do arquivo caracter a caracter:
    +
``` C runnable
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int main()
{
    FILE *farq;
    int i;
    char tentrada[50] = {"Teste de gravacao e leitura de dados-arquivo texto"};
    char tsaida[50], car;


if((farq = fopen("arqtexto.txt","w")) == NULL){
  printf( "Erro na abertura do arquivo");
  exit(1);
}

for (i=0; i < strlen(tentrada); i++)
{
   fputc(tentrada[i],farq);
}
fclose(farq);
farq = fopen("arqtexto.txt", "r");

if (farq == NULL) // Pode-se fazer o teste dessa forma
{
     printf("Erro na abertura do arquivo");
     exit(1);
}
printf("\n\nVou ler e mostrar o texto gravado....\n\n");
i=0;
car=fgetc(farq);
while (car!=EOF)
{
   tsaida[i]=car;
   printf("%c",tsaida[i]);
   i++;
   car =fgetc(farq);
}

fclose(farq);

}
```
 + A constante <b>EOF</b> pode ser substituida pela função <b><em>feof()</em></b> que realiza o teste de fim de arquivo.<br/>
 <b><em>int feof(FILE *arq)</em></b>
 + O teste do while do exemplo acima poderia ficar assim: <b><em>while ( !feof (farq) )</em></b>
 
