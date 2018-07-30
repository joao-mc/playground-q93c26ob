# Ponteiros
+ <p>Para se declarar uma variável em C, devemos declarar o seu tipo e dar um nome (identificador):</p>
<b>tipo_da_variável variavel1,...,variavelN;</b>

+ <p>Para se declarar uma variável ponteiro em C, é necessário também declarar o seu tipo e o nome, mas na frente do nome colocar um asterisco(*):</p>
<b>tipo_da_variável *variavel1,...,*variavelN;</b>

+ <p>É o asterisco (*) que informa ao compilador que aquela variável não vai guardar um valor mas sim um endereço para o tipo especificado.
</p>

![figura](/markdowns/declaracao.png) 

+ Para serem usados, os ponteiros precisam ser inicializados. Para inicializarmos uma variável ponteiro com o endereço de outra variável, usamos o operador &. 

![figura1](/markdowns/ponteiro.png) 

+ Para imprimir o conteúdo da variável <b>numero</b> a partir do ponteiro <b>p</b> basta colocar o asterisco na frente da variável:
  
![figura2](/markdowns/printf.png) 

---
Exemplo
``` C runnable
#include<stdio.h>
int main(){
  int numero;
  int *p;

  numero = 100;

  p = &numero; //Move o endereço da variável numero para p

  printf("\nConteúdo de numero = %d", *p); //imprime o conteúdo da variável numero

  *p = *p  * 10; //multiplica o conteúdo da variável numero por 10

   printf("\nConteúdo de numero = %d", numero);
}
```
---
Em resumo:
       <p><b>  p     : conteúdo é o endereço de memoria apontada por p (número);<b></p>
       <p><b> *p     : é o conteúdo da variável apontada por p (número);<b></p>
       <p><b> &numero: é o endereço na memória da variável numero.</b></p>
