# Gravando e lendo Blocos de dados em Arquivos C
---
+ Podemos escrever e ler blocos de dados em arquivos C através das funções: <b>fwrite()<b/> e <b>fread()</b> 
+ A função <b>fwrite()</b> 

<em><b>unsigned fwrite(void *bloco, int numero_de_bytes, int total, FILE *arq)<b/></em> 
 
    + <b>bloco:</b> ponteiro para a região de memória na qual estão os dados;</br>
    + <b>numero_de_bytes:</b> tamanho de cada posição de memória a ser escrita;</br>
    + <b>total:</b> quantidade de blocos de memória de tamanho "numero_de_bytes" que devem ser escritos;</br>
    + <b>arq:</b> ponteiro associado ao arquivo onde os dados serão escritos.</br>
Exemplo:
``` C
Int main()
{
   FILE *farq;
   int i;
   char texto[50]={"Teste de gravacao e leitura de dados-arquivo texto"};
   int vet = {1,2,3,4};
 
   farq = fopen("arqtexto.txt", "w");
   fwrite(texto, sizeof(char), strlen(texto), farq); // grava a cadeia texto no arquivo
   fwrite(vet, sizeof(int), 4, farq);                       // grava o vetor vet no arquivo
   fclose(farq);
}
```

+ A função <b>fread()</b> é semelhante a <b>fwrite()</b> para realizar a leitura dos dados.

<em><b>unsigned fread(void *bloco, int numero_de_bytes, int total, FILE *arq)<b/></em> 

Exemplo:
``` C
Int main()
{
   FILE *farq;
   int i;
   char texto[51];
   int num, i;
   int vet[4];
 
    farq = fopen("arqtexto.txt", "r");
    num = 50;
    fwrite(texto, sizeof(char), num, farq);                   // lê a cadeia texto no arquivo
    texto[50] ='\0'; 
    printf("%s", texto);
    num = 4;
    fwrite(vet, sizeof(int),num, farq);                       // Lê o vetor vet no arquivo
    for (i=0; i < num; i++)
    {
      printf("%d ", vet[i]);
    }  
    fclose(farq);
}
```
+ Os acessos aos dados em um arquivo geralmente é sequencial, mas é possível fazer buscas e acessos randômicos através da função <b>fseek()<b>: 
+ Esta função posiciona a leitura ou escrita no arquivo em tantos bytes, a partir de um ponto especificado.
+ A função fseek recebe 3 parâmetros
    + <b>fptr:</b> o ponteiro para o arquivo;
    + <b>numbytes:</b> é o total de bytes a partir do <b>tipo</b> a ser pulado;
    + <b>tipo:</b> determina a partir de onde os numbytes de movimentação serão contados.
+ Os valores possíveis para tipo estão definidos em <b>stdio.h</b> e são:
 ![programa](/markdowns/seek.png) 
+ Portanto, para mover numbytes a partir
    + do início do arquivo, tipo deve ser SEEK_SET
    + da posição atual, tipo deve ser SEEK_CUR
    + do final do arquivo, tipo deve ser SEEK_END
 ``` C runnable
#include<stdio.h>
struct  alunos {
    int matric;
    char nome[10];
    int idade;
   };
int main()
{
    FILE *farq;
    struct alunos al, alun[4] = {1, "Maria", 20, 2, "Ana", 19, 3, "Carlos", 16, 4, "Celso",19};

    farq = fopen("arqtexto.txt", "wb");
    fwrite(alun, sizeof(struct alunos), 4, farq); // grava o array de registros alunos
    fclose(farq);
    farq = fopen("arqtexto.txt", "rb");
    fseek(farq, 3*sizeof(struct alunos), SEEK_SET); // posiciona a leitura no quarto registro
    fread(&al, sizeof(struct alunos), 1, farq); // lê o quarto registro de aluno
    printf("\n\n%d\n%s\n%d", al.matric, al.nome, al.idade);
    fclose(farq);
}

```
