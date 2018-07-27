# Vamos Praticar?

Exercício 1
---
<p>Uma empresa comercial possui um programa para controle de estoques as receitas e despesas de 10 projetos que ela controla. Os projetos são numerados de 0 até 9. Faça um programa C que controle a entrada e saída de recursos dos projetos.
O programa deverá ler um conjunto de informações contendo: Número do projeto, valor, tipo despesa ("R" - Receita e "D" - Despesa). O programa termina quando o valor do código do projeto for igual a -1.
Sabe-se que Receita deve ser somada ao saldo do projeto e despesa subtraída do saldo do projeto. Ao final do programa, imprirmir o saldo final de cada projeto.</p> 
<p>Dica: Usar uma estrutura do tipo vetor para controlar os saldos dos projetos. Usar o conceito de <b>struct</b> para agrupar as informações lidas.</p>
![programa](/markdowns/projetos.png)

Exercício 2
---
Faça um programa C para calular o número de lâmpadas 60 watts necessárias para um determinado cômodo. O programa deverá ler um conjunto de informações, tais como: tipo de cômodo, largura e comprimento do cômodo. O programa termina quando o tipo de cômodo for igual -1. A tabela abaixo mostra, para cada tipo de cômodo, a quantidade de watts por metro quadrado.
<p>Dica: Usar uma função (CalulaArea) para calcular a área do cômodo. Os atributos de entrada serão a largura e comprimento do cômodo. Usar uma função (Lampada) para calcular a quantidade de lâmpadas necesárias para o cômodo. O atributo de entrada será o tipo de cômodo</p>
![programa](/markdowns/projetos.png)


que usa, para guardar informações, um vetor e uma matriz:
a) uma matriz bidimensional ESTOQUE na qual a primeira dimensão (linhas) corresponde aos 50 produtos vendidos na empresa e a segunda dimensão (colunas), às 4 lojas da
empresa;
b) um vetor ESTOQUE_TOTAL onde são armazenados os totais em estoque de cada produto no conjunto das 4 lojas (soma do produto em todas as lojas).
Faça:
a) um procedimento que preencha a matriz ESTOQUE;
b) um procedimento que atualize o vetor ESTOQUE_TOTAL a partir dos dados da
matriz;
c) um procedimento que emita um relatório com os códigos (iguais aos índices) dos
produtos que apresentam estoque inferior a 10 unidades em qualquer uma das lojas,
indicando também em qual a loja;
d) um programa que use os procedimentos anteriores.
