----
Passagem de Parâmetros por valor
----
+ A passagem de parâmetros que será apresentada aqui é chamada de passagem por valor. 
+ Os valores contidos nas variáveis do programa, no momento da chamada da função, são <b>copiados</B> para as variáveis parâmetros da função.  
+ As alterações dos valores dos parâmetros dentro da função não afetarão os valores das variáveis do programa, usadas na chamada da função.
+ Quando uma função não for retornar valor (procedimento), utilize <b>void</b> como tipo da função. Quando se usa <b>void</b> não podemos usar <b>return</b> na função.
<p>No exemplo a seguir a variável <b>f</b>, declarada na <b>main()</b>, passada por parâmetro para a função <b>Cem</b> não terá o valor alterado dentro da função, pois o valor de <b>f(20.7)</b> será copiado para o parâmetro <b>a</b> da função.</p>

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
Exercício 1
----
Faça um programa que leia duas notas de um aluno numa turma de 10 alunos. Para cada aluno, calcular a média ponderadas das notas, sabendo que a <b>nota1</b> tem <b>peso = 4</b> e a <b>nota2</b> tem <b>peso = 6</b>. Imprimir a média do aluno e o conceito final, conforme tabela abaixo:

| Intervalo | Conceito |
| --------- | -------- |
| 0.0 a 4.9 |    D     |
| 5.0 a 6.9 |    C     |
| 7.0 a 8.9 |    B     |
| 9.0 a 10.0|    A     |

Fazer 2 funções:
A primeira função denominada <b>float mediapond</b> irá receber as duas notas, calcular e retornar a média ponderada. A segunda função denominada <b>char conceito</b> irá receber a média das notas e retornar o conceito conforme a tabela acima.
@[IDE]({"stubs": ["./www/exercicio"],"command": "sh /project/target/www/exercicio.sh"
})
::: Solução

``` C
#include<stdio.h>
float mediapond(float nota1, float nota2)
{
    float media;
    media = nota1 * 0.4 + nota2 * 0.6; // 0.4 e 0.6 corresponde aos pesos das notas dividido pela soma dos pesos.
    return media;
}

char conceito(float media)
{
    char conc;
    if (media <= 4.9){
      conc = 'D';
    }
    else {
      if (media <= 6.9) {
        conc = 'C';
      }
      else {
        if (media <= 8.9 ){
            conc ='B';
        }
        else {
            conc = 'A';
        }
      }
    }
  return conc;
}

int main() {
  int i;
  float nota1, nota2, med;
  char conce;

  for (i=0; i < 10; i++) {
    printf("\n\nDigite a nota 1:");
    scanf("%f", &nota1);
    printf("\nDigite a nota 2:");
    scanf("%f", &nota2);
    med = mediapond(nota1,nota2);
    conce = conceito(med);
    printf("\n\nmédia = %f \nConceito final = %c", med, conce);
  }
}


```
:::

----
Exercício 2
----
Faça um programa para calcular o valor das parcelas de um financiamento no regime de juros compostos com capitalização mensal. O programa deverá ler o valor do financiamento e o número de parcelas, calcular e exibir o valor da parcela. O programa termina quando o valor do financiamento for igual a zero. Abaixo apresentamos a tabela contendo os prazos de financiamentos e a taxa de juros anual:

| Prazo | taxa a.a. |
| ----- | --------- |
|   6   |     7%    |
|  12   |    10%    |
|  18   |    12%    |
|  24   |    15%    |
|  36   |    18%    |
Fazer uma função denominada <b>float financiamento</b> que deverá receber o valor do financiamento e o número de parcelas, calcular e retornar o valor da prestação. Utilizar a estrutura </>switch ... case</b> apar selecionar a taxa de juros representada em valor decimal. Como a capitalização é mensal, dividir a taxa por 12. 
A fórmula de cálcula da prestação é: 

$`prestacao=valor financiamento × \frac{(1+taxa)^p × taxa}{(1+taxa)^p  - 1}`$

<b>*obs: p = número de parcelas</b>


@[IDE]({"stubs": ["./www/exercicio"],"command": "sh /project/target/www/exercicio.sh"
})
::: Solução

``` C
#include<stdio.h>
#include<math.h>
float financiamento(float valor, int parcelas)
{
   float tx, prestacao;

   switch(parcelas)
   {
   case 6:
    tx = 0.07/12;
    break;
   case 12:
    tx = 0.1/12;
    break;
   case 18:
    tx = 0.12/12;
    break;
   case 24:
    tx = 0.15/12;
    break;
   case 36:
    tx = 0.18/12;
    break;
   default:
    tx = 0.0;
    break;
   }

 prestacao = valor * (pow((1+tx), parcelas)*tx)/(pow((1+tx),parcelas)-1);
 return prestacao;
}

int main(){
  int parc;
  float financia, presta;

  printf("\n\nDigite o valor a ser financiado:");
  scanf("%f",&financia);
  while(financia != 0){
    printf("\n\nDigite o numero de parcelas:");
    scanf("%d",&parc);
    presta = financiamento(financia, parc);
    printf("O valor da sua prestação e: %f", presta);
    printf("\n\nDigite o valor a ser financiado:");
    scanf("%f",&financia);

  }
}


```
:::
----
