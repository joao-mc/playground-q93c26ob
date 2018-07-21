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

  for (i=0; i < 3; i++) {
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
