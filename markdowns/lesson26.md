Utilizar funções de manipulação de cadeias fornecidas na biblioteca padrão (String.h)
---
A movimentação de valores de/para as cadeias de caracteres não pode ser efetuadas diretamente, mas apenas através de funções de manipulação de cadeias de caracteres. Estas funções estão no cabeçalho do arquivo <b><string.h></b>: 

<b>#include <string.h></b>

Nesse momento, apresentaremos apenas as funções mais importantes de manipulação de Strings.

1. mover caracteres para uma variável string. 
<p>A movimentação pode ser efetuada caracter a caracter (como em um vetor) ou através da função strcpy (string copy).</p>
<p><b>char *stpcpy (const char *dest,const char *src)</b> - Copia uma string de <b>src</b> para outra string <b>dest</b>.</p>
<p>Exemplo de movimentação manual e através da função strcpy.</p>


``` C runnable
#include<string.h>
#include<stdio.h>
int main() {
  char origem[16] = {'T', 'E', 'S','T','E',' ', 'D','E', ' ', 'S','T','R','I','N','G','\0'};
  char destino[16];
  int i;
  /* Movimentação Manual */
  for (i= 0; i < 16; i++) {
     destino[i] = origem[i];
  }
  printf("\nManual\nOrigem = %s\n\nDestino = %s", origem, destino);

  /*Movimentação com Strcpy*/
  strcpy(destino, origem);
   printf("\n\nCom Funcao\nOrigem = %s\n\nDestino = %s", origem, destino);
}

```
2. Comparação de Strings.
<p>A comparação pode ser efetuada caracter a caracter (como em um vetor) ou através da função strcmp (string compare).</p>

<p><b>int strcmp(const char *string1,const char *string2)</b> - Compara duas strings e determina a ordem (alfabetica) das duas.</p>

int strlen(const char *string) Retorna o tamanho de uma
string.
char *strncat(const char *string1, char *string2,
size_t n)
Concatena n caracteres da
string2 na string1.
int strncmp(const char *string1, char *string2, size_t
n)
Compara os n primeiros
caracteres de duas strings.
char *strncpy(const char *string1,const char *string2,
size_t n)
Copia os n primeiros caracteres
da string1 na string2
int strcasecmp(const char *s1, const char *s2) Versão case insensitive de
strcmp(). 
