Aninhamento de IFs
----
A estrutura de decisão (condicional) ```IF``` permite, no máximo, duas possibilidades de execução dos comandos: uma possibilidade é a execução de comandos associadas a condição <b>Verdadeira</b> e a outra possibilidade está associada a condição <b>Falsa</b>, como mostra o exemplo a seguir:
``` C
if(condição) {
  comandosA;     <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira.
} 
else {
  comandosB;     <----- Esses comandos só serão executados, se a condição for avaliada Falsa.
}
```
Mas, existem situação em que temos mais de duas possibilidades na condição associada ao <b>IF</b> (p.ex. menus com várias opções de escolha). Nesses casos nos vemos obrigados a arruma a estrutura para possibilitar a representação desses <b>"Caminhos"</b>. Estamos falando do "Aninhamento de if´s".
``` C
if(condição) {
  comandosA;       <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira.
} 
else {
  if (condição) { 
    comandosB;     <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira.
  }
  else {
    if (condição) {
      comandosC;    <----- Esses comandos só serão executados, se a condição for avaliada Verdadeira. 
    }  
    else{
      comandosD;    <----- Esses comandos só serão executados, se a condição do último if for avaliada Falsa.               
    }
  }      <-------- Fechamento do Segundo else   
} <-------- Fechamento do Terceiro else  
```

