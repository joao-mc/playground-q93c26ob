# Gravando e lendo cadeias de caracteres em arquivos C
---
+ Existem funções na linguagem C que permitem escrever <b>fputs()</b> e ler <b>fgets()</b>  cadeias de caracteres.

   <em><b>int fputs(char* cadeia, FILE *arq)</b></em>

+ Esta função recebe como parâmetro uma cadeia de caracteres (string) e um ponteiro para o arquivo que queremos gravar.
+ Exemplo de um trecho de gravação de cadeia de caracteres  <br/>
```C
char tentrada[50] = {"Teste de gravacao e leitura de dados-arquivo texto"};
  
farq = fopen("arqtexto.txt", "w");

fputs(tentrada,farq);

fclose(farq);
```
 + Diferentemente da função de gravação, a função de leitura possui um parâmetro a mais para indicar o tamanho, isto é, o número máximo de caracteres que serão lidos.
 + Essa função pode retornar a cadeia de caracteres (ponteiro para o primeiro caractere da cadeia) ou NULL em caso de erro ou fim do arquivo.

 <em><b>int fgets(char* cadeia, int tamanho, FILE *arq)</b></em>
 
+ Exemplo de um trecho de leitura e gravação de cadeia de caracteres  <br/>
```C
char tsaida[50];
int tam = 50;  
farq = fopen("arqtexto.txt", "r");

fputs(tentrada, tam, farq);

fclose(farq);
```


