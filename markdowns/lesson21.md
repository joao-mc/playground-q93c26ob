Aninhamento de IFs
----
A estrutura de decisão (condicional) ```IF``` permite, no máximo, duas possibilidades de escução dos comandos: uma possibilidade é a execução de comandos associadas a condição <b>Verdadeira</b> e a outra possibilidade está associada a condição <b>Falsa</b>, como mostra o exemplo a seguir:
``` C
if(condição) {
     <b>comandosA   <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira.
} 
else {
     <b>comandosB   <----- Esses comandos só serão executados, se a condição for avaliada Falsa.
}
```
