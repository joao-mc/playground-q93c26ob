# Manipulando arquivos em C
---
+ Os protótipos dos comandos de manipulação de arquivos em C encontram-se definidos na biblioteca padrão <b>sdtio.h</b>.
+ Para se trabalhar com arquivos é necessário declarar uma variável ponteiro do tipo <b>FILE</b>. </br>
    <b>FILE *farq;</b>
+ Para manipular um arquivo em C é necessário abrí-lo. Para tanto, a linguagem C possui o comando fopen. 

     <b>farq = fopen("Nomedoarquivo.extensão", "modo de abertura");</b>

      ---> O primeiro parâmetro é o nome do arquivo (pex. "arquivo.txt")
      ---> O segundo parâmetro define-se o modo de abertura:
           "wt": abertura para gravação, arquivo texto
           "rt": abertura para leitura, arquivo texto
+ Exemplo:            
``` C
FILE *farq;

arq = fopen("arquivo.txt", "rt");

if (arq == NULL)
{
    printf("Problemas na CRIACAO do arquivo\n");
    return;
} 
```

