---
Mover valores para um vetor
---
+ Uma segunda maneira de mover valores para os elementos do vetor é na declaração do vetor. Por exemplo, podemos declarar um vetor do tipo int com tamanho igual a 5 e inicializarmos com o valor 100.
```
int vet[5] = {100,100,100,100,100};
```
+ Uma outra forma de mover valores é utilizar o comando de leitura(scanf) para mover valores digitado pelos usuários. Utilizando os exempos anteriores:
```
for(i = 0; i < 5; i++)
{
   scanf("%d", &vet[i]);
}
```
---
Exercicio 1
---
Faça um programa que leia 5 números inteiros e armazene-os em um vetor. A seguir, percorra o vetor e conte quantos números são maiores que 100. Ao final exiba essa quantiddade.
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
