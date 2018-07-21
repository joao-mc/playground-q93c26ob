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
A Lista de Parametros, também é chamada de Lista de Argumentos, é opcional. Funcionam como a interface de comunicação (passagem de valores/dados) entre o programa e a função.  
```
