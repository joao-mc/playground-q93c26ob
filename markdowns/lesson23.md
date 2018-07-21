# Funções em C

+ Uma função pode ser vista como um conjunto de comandos que realiza uma tarefa específica. Em outras palavras, pode-se dizer que é um pequeno "programa" utilizado por outros programas.

+ A função é referenciada (chamada) pelo programa principal através de um nome atribuído a ela.

+ A utilização de funções, muito comum na programação estruturada, visa subdividir um programa em partes (módulos) menores que realizam uma tarefa bem definida.
+ Benefícios da utilização de funções:
   + Permite o reaproveitamento de código já construído(por você ou por outros programadores);
   + Evita que um mesmo trecho de código seja repetido várias vezes dentro de um mesmo programa e, com isso, qualquer alteração é feita apenas nesse trecho e de forma simples.
   + Para que os blocos do programa não fiquem grandes demais e, por conseqüência, mais difíceis de entender;
   + Facilita a leitura do programa de maneira que os blocos de código possam ser logicamente compreendidos de forma isolada.
----
Esqueleto de uma função
----
```
tipo_de_retorno nome_da_função (lista de parâmetros)
{
   instruções;
   retorno_da_função;
}
 
```
----
Parâmetros
----
+ A Lista de Parametros, também é chamada de Lista de Argumentos, é opcional. Funcionam como a interface de comunicação (passagem de valores/dados) entre o programa e a função. 
+ Os parâmetros de uma função são definidos como se estivesse declarando uma variável, entre os parênteses do cabeçalho da função. Caso precise declarar mais de um parâmetro, basta separá-los por vírgulas. 
+ No exemplo a seguir temos a função SOMA que possui dois parâmetros, sendo o primeiro um float (a) e o segundo um int (b).

```
void SOMA(float a, int b)  // basta separar por vírgulas
{
   float result;     // a declaração de variáveis é igual ao que 
                     // se faz na função main 
   result = a + b;
   return result;     // retorna para o programa o resultado da soma de a + b  
}
```
Os parâmetros são passados para uma função de acordo com a sua posição. Ou seja, o primeiro parâmetro da chamada (programa) define o valor o primeiro parâmetro na definição da função, o segundo parâmetro do programa define o valor do segundo parâmetro da função e assim por diante. Os nomes dos parâmetros na chamada não tem relação com os nomes dos parâmetros na definição da função.
No código a seguir, por exemplo, a função SOMA é chamada recebendo como parâmetros as variáveis "a" e "b", nesta ordem.

``` C runnable
#include <stdio.h>

float SOMA(float a, int b)  
{
   float result;     
   result = a + b;
   return result;
}

int main()
{
    float a;
    int b;
    float s;
    a = 10;
    b = 12.3;
    s = SOMA(a,b);  // Chamada da função SOMA(12.3,10);
    printf("A soma de %f com %d é %f\n", a,b,s); 
    return 0;
}
```
