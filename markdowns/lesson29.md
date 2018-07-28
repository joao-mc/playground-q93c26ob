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
<p>Dica: Usar uma função (float CalulaArea) para calcular a área do cômodo. Os atributos de entrada serão a largura e comprimento do cômodo. Usar uma função (float Lampada) para calcular a quantidade de lâmpadas necesárias para o cômodo. O atributo de entrada será o tipo de cômodo</p>

![programa](/markdowns/potencia.png)

Exercício 3
---
Faça um programa que receba uma frase (máximo 100 caracteres) e uma letra qualquer, calcule e mostre a quantidade que essa letra aparece na frase digitada. Para descobrir o tamanho da frase digitada utilize a função <b>strlen</b>.


Exercício 4
---
Faça um programa que controle os estoque de 5 produtos em 5 armazéns de um supermercado, conforme figura abaixo: 

![programa](/markdowns/estoque.png)

O programa deverá ler o número da linha e da coluna, correspondete ao produto no armazem, e a quantidade a ser retirada do estoque. Caso a quantidade solicitada for menor ou igual a quantidade em estoque, o programa deverá emitir uma mensagem de atendiemtneo e dar baixa no estoque. Do contrário, emitir mensagem, "Estoque com quantidade insuficiente para atender ao pedido. O programa termina quando o numero da linha for igual a -1.
Utilize a declaração anbaixo para resolver o exercício:
int estoque[5][5]= {{150,0,100,150,200}, {200,300,230,100,90}, {250,300,0,200,150}, {300,100,90,450,0},{350,300,400,250,200}}

