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

+ Semelhantemente aos vetores, podemos também mover valores para as matrizes através do comando de leitura(scanf).
```
 for(i = 0; i < 2; i++)
   {
     for(j = 0; j < 5; j++)
     {
       scanf("%d", &vet[i][j]);
     }
    }
```    
---
Exercicio 1
---
Dada a Matriz A = {{10, 30, 50}, {5, 15, 25}, {2, 5, 9}} e a Matriz B= {{5, 35, 70}, {1, 25, 30}, {1, 4, 7}}, faça um programa que gere a Matriz C contendo os maiores valores de cada posição. Mostre a Matriz C.
@[IDE]({"stubs": ["./www/exercicio"],"command": "sh /project/target/www/exercicio.sh"
})
::: Solução

``` C
#include<stdio.h>
int main(){
  int A[3][3] = {{10, 30, 50}, {5, 15, 25}, {2, 5, 9}};
  int B[3][3] ={{5, 35, 70}, {1, 25, 30}, {1, 4, 7}};
  int C[3][3], i, j;

  for(i = 0; i < 3; i++){      /* percorre as linhas da Matriz */
    for(j = 0; j < 3; j++){      /* percorre as colunas da Matriz */
      if (A[i][j] > B[i][j]) {
         C[i][j] = A[i][j];
      }
      else {
        C[i][j] = B[i][j];
      }
    }
   }
  printf("\n");   /* Pula Linha*/
  for(i = 0; i < 3; i++){      /* percorre as linhas da Matriz */
    for(j = 0; j < 3; j++){      /* percorre as colunas da Matriz */
      printf("%d ",C[i][j]);
    }
   printf("\n"); /* Pula Linha*/
  }
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
