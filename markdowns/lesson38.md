# Operações com ficheiros em C

+ Os protótipos dos comandos de manipulação de ficheiros em C encontram-se definidos na biblioteca padrão <b>sdtio.h</b>.
+ Para se trabalhar com ficheiros é necessário declarar uma variável ponteiro do tipo <b>FILE</b>. </br>

    <em><b>FILE *farq;</b></em>
    
+ Para manipular um ficheiro em C é necessário abrí-lo. Para tanto, a linguagem C possui o comando fopen. 

     <em><b>farq = fopen(char *Nome_do_arquivo, char *modo_de_abertura);</b></em> </br>

+ O primeiro parâmetro é o nome do ficheiro. Pode-se trabalhar com caminhos absolutos ou relativos.<br/>
           > Caminho absoluto: descrição de um caminho desde o diretório raiz.<br/>
                 <em><b>C:\\MinhaPasta\\ficheiro.txt</b></em><br/>
           > Caminho relativo: descrição de um caminho desde o diretório corrente (onde o programa está salvo)<br/>
                <em><b>ficehiro.txt</b> ou <b>..\\dados.txt</em></b><br/>

+ O segundo parâmetro define-se o modo de abertura:
             ![programa](/markdowns/abertura.png) 
+ Exemplo:            
``` C
FILE *farq;

farq = fopen("ficheiro.txt", "rb");

if (farq == NULL)   // <---- Testa se o ficheiro foi aberto corretamente.
{
    printf("Problemas na criacao do ficheiro\n");
    return;
} 
```
+ Ao terminar de usar o ficheiro é necessário fechá-lo. Para isso usamos a função <em><b>fclose(FILE *farq)</b></em>. 
+ O ponteiro <b>*farq</b> indica que ficheiro deve ser fechado. Após o seu fecho, o ficheiro não pode ser manipulado.


