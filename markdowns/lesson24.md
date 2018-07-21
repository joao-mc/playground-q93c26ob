----
Passagem de Parâmetros por valor
----
+ A passagem de parâmetros apresentada até aqui é chamada de passagem por valor. 
+ Os valores contidos nas variáveis do programa, no momento da chamada da função, são copiados para as variáveis parâmetros da função.
+ As alterações dos valores dos parâmetros dentro da função não afetarão os valores das variáveis do progrmama usadas na chamada da função. 
No exemplo a seguir a variável f, passada por parâmetro para a função cem não terá o valor alterado dentro da função.
```C runnable
#include <stdio.h>

void Cem(float a)
{
    a = 100.0;
}

void main()
{
   float f;

    f = 20.7;
    Cem(f);
    printf("%f", f); // o valor impresso será 20.7 pois o parâmetro da função foi passado por valor.
} 
```

Obs: <b>void</b> significa que a função não retorna valor para o programa que a chama, logo é denominada de <b>procedimento</b>.

----
Exercício
----
Faça um programa que leia duas notas de um aluno numa turma de 10 alunos. Para cada aluno, calcular a média ponderadas das notas, sabendo que a nota1 tem peso 4 e a nota2 tem peso 6. Imprimir a média do aluno e o conceito final, conforme tabela abaixo:

| Intervalo | Conceito |
| --------- | -------- |
| 0.0 a 4.9 |    D     |
| 5.0 a 6.9 |    C     |
| 7.0 a 8.9 |    B     |
| 9.0 a 10.0|    A     |

Fazer 2 funções:
A primeira função denominada <b>médiapond</b> irá receber as duas notas, calcular e retornar a média ponderada. A segunda função denominada <b>conceito</b> irá receber a média das notas e retornar o conceito conforme a tabela acima.
@[IDE]({"stubs": ["./www/exercicio"],"command": "sh /project/target/www/exercicio.sh"
})
::: Solução

``` C
#include <stdio.h>
#include <stdlib.h>
#include<math.h>
 
int main()
{
    int x, y, resultado; 
    int op;
    x=0;
    y=0;
    resultado=0;
    op=0;
 
    printf(" \n Digite o valor do primeiro operando: ");
    scanf("%d", &x);
    printf(" \n Digite o valor do segundo operando: ");
    scanf("%d", &y);
 
    printf(" \n Escolha uma das opções abaixo: ");
    printf(" \n 1. Soma ");
    printf(" \n 2. Subtração ");
    printf(" \n 3. Multiplicação ");
    printf(" \n 4. Divisão ");
    printf(" \n 5. Exponenciação ");
    
    printf(" \n Digite o número da opção desejada: ");
    scanf("%d", &op);
 
    switch (op)
    {
    case 1:
        printf(" \n Opção selecionada: 1. Soma ");
        resultado = x + y;
        printf(" \n A soma dos dois números é: %d ", resultado);
        break;
 
    case 2:
        printf(" \n Opção selecionada: 2. Subtração ");
        resultado = x - y;
        printf(" \n A subtração dos dois números é: %d", resultado);
        break;
 
    case 3:
        printf(" \n Opção selecionada: 3. Multiplicação ");
        resultado = x * y;
        printf(" \n A multiplicação dos dois números é: %d", resultado);
        break;
 
    case 4:
        printf(" \n Opção selecionada: 4. Divisão ");
        if(y=0)
        {
            printf(" \n Não existe divisão por zero ");
        }
        else
        {
            resultado = x / y;
            printf(" \n A divisão dos dois números é: %d", resultado);
        }
 
        break;
    case 5:
        printf(" \n Opção selecionada: 5. Exponenciação ");
        resultado = pow(x, y);
        printf(" \n A exponenciação dos dois números é: %d", resultado);
        break;    
    default:
        printf(" \n Você digitou uma opção inválida!");
    }
 
    return 0;
}


```
:::
----
