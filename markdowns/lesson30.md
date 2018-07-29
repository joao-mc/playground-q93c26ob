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

+ Agora podemos definir <b>Ponteiros</b> como variáveis que armazenam endereços (de outras variáveis) em vez de valor. 
