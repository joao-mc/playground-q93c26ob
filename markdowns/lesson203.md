# Estrutura de Dados Homogênea (Matriz)
---
Inicializar uma Matriz
---
+ Semelhantemente aos vetores podemos inicializar as matrizes no momento da declaração, para isso devemos colocar cada linha entre chaves {}, e separar elas por vírgulas, veja:
<p><b> int Mat[2][5] = { {100, 90, 80, 70, 60 }, {200, 190, 180, 170, 160 } };</b></p>

Exemplo
---
Percorrer a matriz Mat (3 x 3) contendo números inteiros e transformar, caso existam, os números negativos em positivos.
``` C runnable
#include<stdio.h>
int main() {
  int i, j;
  int mat[3][3] = {{2, -4, 5},{-8, -1, 7},{-3, -6, 9}};
  for(i=0; i < 3; i++)
   {    
    for(j=0; j < 3; j++)
     {
       if (mat[i][j]< 0)
        {
           mat[i][j] = mat[i][j] * -1;
        }
     }    
    } 
   for(i=0; i < 3; i++)
   {    
    for(j=0; j < 3; j++)
     {
       printf("%d ", mat[i][j]);
     }
     printf("\n");
    } 
       
}
```
---
Exercicio 1
---
Faça um programa que leia 5 números inteiros e armazene-os em um vetor. A seguir, percorra o vetor e conte quantos números são maiores que 100. Ao final, exiba essa quantidade.
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
---
Exercicio 2
---
Faça um programa que leia 6 números inteiros e armazene-os no vetor A. A seguir, percorra o vetor A e crie o vetor B, onde cada elemento de B é formado pelo quadrado do elemento de A correspondente. Ao final, exiba os dois vetores. Utilize a função pow(base, expoente). <b>#include<math.h></b>.
@[IDE]({"stubs": ["./www/exercicio"],"command": "sh /project/target/www/exercicio.sh"
})
::: Solução

``` C
#include<stdio.h>
#include<math.h>
int main(){
  int A[5], B[5], i;

  for(i= 0; i < 5; i++){      /* inicialização do vetor */
    printf("\n\nDigite um numero qualquer:");
    scanf("%d",&A[i]);
  }

  for(i= 0; i < 5; i++){      /* percorrendo do vetor */
      B[i] = pow(A[i],2);
  }
  for(i= 0; i < 5; i++){      /* percorrendo do vetor */
     printf("\n A[%d] = %d  B[%d] = %d", i,A[i],i,B[i]);
  }

}


```
:::
