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
  int mat[3][3] = {{100, -4, 50},{-10, -1, 70}};
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
