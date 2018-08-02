# Arquivos em C
---
+ Arquivo é um conjunto de dados nomeados, armazenados e organizados em um meio de armazenamento de dados. 
+ Por que usar arquivos?
    + Permitem armazenar grande quantidade de informação;
    + Dados não são perdidos (persistência dos dados);
    + Acesso aos dados poder ser não seqüencial;
    + Acesso concorrente aos dados (mais de um programa pode usar os dados ao mesmo tempo).
+ Basicamente, a linguagem C trabalha com dois tipos de arquivos: de texto e binários.
    + Arquivo texto : Armazenam caracteres que podem ser mostrados diretamente na tela ou modificados por um editor de textos simples como o Bloco de Notas.
 ``` c runnable
#include <stdio.h>
#include <conio.h>
#include <string.h>
void main()
{
  FILE *arq;
  int i;
  int result;
  struct
  {
       int matric;
       char nome[10];
       float salario;
  } func;


  arq = fopen("arqGrav.txt", "wt");  // Cria um arquivo texto para gravação
  if (arq == NULL) // Se nào conseguiu criar
  {
     printf("Problemas na CRIACAO do arquivo\n");
     return;
  }

  for (i = 0; i<5;i++)
  {
// A funcao 'fprintf' devolve o número de bytes gravados
// ou EOF se houve erro na gravação
        fflush(stdin);
        printf("\ndigite nome:");
       gets(func.nome);
        printf("\ndigite matric:");

       scanf("%d",&func.matric);
        printf("\ndigite sal:");

       scanf("%f",&func.salario);
         result = fprintf(arq, "%d %s %2f\n", func.matric, func.nome, func.salario);
      if (result == EOF)
	  printf("Erro na Gravacao\n");
  }
  fclose(arq);
}

 ```
    + Arquivo binário : Armazena uma sequência de bits que está sujeita as convenções dos programas que o gerou. Ex: arquivos executáveis, arquivos compactados, arquivos de registros, etc.


