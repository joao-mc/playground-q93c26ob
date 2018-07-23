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

int main(){
  int vet[5], cont, i;

  for(i= 0; i < 5; i++){      /* inicialização do vetor */
    printf("\n\nDigite um numero qualquer:");
    scanf("%d",&vet[i]);
  }
  cont = 0;
  for(i= 0; i < 5; i++){      /* percorrendo do vetor */
     if (vet[i] > 100)
         cont = cont + 1;
  }

  printf("\n\nExistem %d valores acima de 100", cont);
}

```
:::
