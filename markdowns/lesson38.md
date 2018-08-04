# Manipulando arquivos em C

+ Os protótipos dos comandos de manipulação de arquivos em C encontram-se definidos na biblioteca padrão <b>sdtio.h</b>.
+ Para se trabalhar com arquivos é necessário declarar uma variável ponteiro do tipo <b>FILE</b>. </br>

    <em><b>FILE *farq;</b></em>
    
+ Para manipular um arquivo em C é necessário abrí-lo. Para tanto, a linguagem C possui o comando fopen. 

     <em><b>farq = fopen(char *Nome_do_arquivo, char *modo_de_abertura);</b></em> </br>

+ O primeiro parâmetro é o nome do arquivo. Pode-se trabalhar com caminhos absolutos ou relativos.<br/>
           > Caminho absoluto: descrição de um caminho desde o diretório raiz.<br/>
                 <em><b>C:\\MinhaPasta\\arquivo.txt</b></em><br/>
           > Caminho relativo: descrição de um caminho desde o diretório corrente (onde o programa está salvo)<br/>
                <em><b>arquivo.txt</b> ou <b>..\\dados.txt</em></b><br/>

+ O segundo parâmetro define-se o modo de abertura:
             ![programa](/markdowns/abertura.png) 
+ Exemplo:            
``` C
FILE *farq;

farq = fopen("arquivo.txt", "rb");

if (farq == NULL)   // <---- Testa se o arquivo foi aberto corretamente.
{
    printf("Problemas na CRIACAO do arquivo\n");
    return;
} 
```
+ Ao terminar de usar o arquivo é necessário fechá-lo. Para isso usamos a função <em><b>fclose(FILE *farq)</b></em>. 
+ O ponteiro <b>*farq</b> indica que arquivo deve ser fechado. Após o seu fechamento o arquivo não pode ser manipulado.


