# Manipulando arquivos em C

+ Os protótipos dos comandos de manipulação de arquivos em C encontram-se definidos na biblioteca padrão <b>sdtio.h</b>.
+ Para se trabalhar com arquivos é necessário declarar uma variável ponteiro do tipo <b>FILE</b>. </br>
    <b>FILE *farq;</b>
+ Para manipular um arquivo em C é necessário abrí-lo. Para tanto, a linguagem C possui o comando fopen. 

     <b>farq = fopen(char *Nome_do_arquivo, char *modo_de_abertura);</b> </br>

+ O primeiro parâmetro é o nome do arquivo. Pode-se trabalhar com caminhos absolutos ou relativos.<br/>
           + <b>Caminho absoluto</b>: descrição de um caminho desde o diretório raiz.<br/>
              <b>C:\\MinhaPasta\\arquivo.txt</b><br/>
           + <b>Caminho relativo</b>: descrição de um caminho desde o diretório corrente (onde o programa está salvo)<br/>
                <b>arquivo.txt</b> ou <b>..\\dados.txt</b><br/>

+ O segundo parâmetro define-se o modo de abertura:
             ![programa](/markdowns/abertura.png) 
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

