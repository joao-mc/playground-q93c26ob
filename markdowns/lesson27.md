# Estruturas de dados Heterogêneas(struct)

+ As estruturas de dados (Homogêneas e Heterogêneas) possibilitam a construção de estruturas mais complexas que os tipos de dados primitivos (int, char,..).
+ Diferentemente dos tipos homogêneos, essas estrturas permitem a manipulação de um conjunto de informações de tipos de dados primitivos diferentes, mas que possuem um relacionamento lógico entre si;
+ Exemplo de um registro de Funcionário
![programa](/markdowns/registro.png)
+ O Resgistro acima possui um conjunto informações relacionadas a um funcionário, logo poderiam ser vistas agrupadas num único nome (como as Matrizes).
+ A linguagem C possui uma estrutura denominada <b>struct</b> que permite agrupar um conjunto de informações de tipos diferentes cob um mesmo nome.
 ```
 Declaração:
     struct {
       tipo_de_dado1 <Nome das Varáveis1>;
       tipo_de_dado2 <Nome das Variáveis2>;
       ....
       tipo_de_dadoN <Nome das VariáveisN>;
     } nome_Variavel_struct;
     
     Exemplo:
      struct{
       int    matricula;
       string nome[30];
       string dataNasc[9];
       string cargo[20];
       float  salario
     }func;
 ```
 + A variável <b>func</b> é do tipo registro (struct) e, para individualizar cada dado (nesse caso é denominado de campo), basta colocar o nome da variável seguido de um ponto seguido com o nome do campo.
    ex: <b>func.matricula</b>
+ O exemplo a seguir cria a estrutura funcionário, lê as informações de cada um dos campos e exibe o que foi lido.
``` C runnable
#include<stdio.h>

int main() {
 struct {
       int    matricula;
       char nome[30];
       char dataNasc[9];
       char cargo[20];
       float  salario;
     }func;
  printf("\n\nDigite a matricula: ");
  scanf("%d", &func.matricula);
  printf("\n\nDigite o nome: ");
  scanf("%s", &func.nome);
  printf("\n\nDigite a Data Nascimento: ");
  scanf("%s", &func.dataNasc);
  printf("\n\nDigite o cargo: ");
  scanf("%s", &func.cargo);
  printf("\n\nDigite o salario: ");
  scanf("%f", &func.salario);

  printf("\n\nFuncionario: %s \n\nMatricula:%d\n\nNascimento:%s\n\ncargo:%s\n\nSalario:%f",&func.nome ,func.matricula,&func.dataNasc,func.cargo,func.salario );
}

```
