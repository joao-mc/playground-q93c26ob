# Ponteiros
---
+ Antes de apresentarmos ponteiros, vaos relembrar o conceito de variável.
+ A memória é formada por um conjunto de espaços, denominados variáveis, onde guardamos os dados.
+ Esses "espaços" são identificados por nomes (interno nos programas), e por números  ou "endereços" (externos aos programas), utilizados pelos programas para acessar os dados. 
+ A figura abaixo exibe um trecho da memória:

![figura](/markdowns/memoria.png)  

+ Suponha que você declare uma variável denominada "Total" em seu programa. Essa variável será associada a um (ou mais) endereço(s) na memória (endereço 3001), conforme a figura abaixo:

![figura1](/markdowns/memoria1.png)  

+ Agora você move o valor 100 para a variável Total (total = 100;), o programa procura o endereço da variável e move o valor.

![figura2](/markdowns/memoria2.png)  

+ Agora podemos começar a definir <b>Ponteiros</b>.
+ Ponteiros são variáveis que armazenam endereços (de outras variáveis) ao invés de amazenar valor. O conteúdo de uma variável ponteiro é o endereço de outra variável. 
+ Suponha que você defina a variável <b>Ptr</b> como sendo ponteiro e armazene o endereço 3001. Essa variável estará armazenando o endereço da variável <b>Total</b>, conforme figura abaixo:

![figura3](/markdowns/memoria3.png) 

+ Assim dizemos que a variável <b>Ptr</b> está "apontando" para variável <b>Total</b>, isto é, qualquer alteração em <b>Ptr</b> irá alterar o conteúdo de <b>Total</b>.
+ Os ponteiros são usados em muitas linguagens de programação para manipular cadeias de caracteres, passar parâmetros para funções , manipulação matrizes de dados e criação de listas ligadas e outras estruturas de dados complexas. 
+ Ponteiros proporcionam uma grande flexibilidade para o gerenciamento de memória e otimização de programas.


