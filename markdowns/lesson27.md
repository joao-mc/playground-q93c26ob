# Estruturas de dados Heterogêneas(struct)

+ As estruturas de dados (Homogêneas e Heterogêneas) possibilitam a construção de estruturas mais complexas que os tipos de dados primitivos (int, char,..).
+ Diferentemente dos tipos homogêneos, essas estrturas permitem a manipulação de um conjunto de informações de tipos de dados primitivos diferentes, mas que possuem um relacionamento lógico entre si;
+ Exemplo de um registro de Funcionário
![programa](/markdowns/registro.png)
+ O Resgistro acima possui um conjunto informações relacionadas a um funcionário, logo poderiam ser vistas agrupadas num único nome (como as Matrizes).
+ A linguagem C possui uma estrutura denominada <b>struct</b> que permite agrupar um conjunto de informações de tipos diferentes cob um mesmo nome.
 ```
 Declaração:
     struct <nome da Estrutura> {
       tipo_de_dado1 <Nome das Varáveis1>;
       tipo_de_dado2 <Nome das Variáveis2>;
       ....
       tipo_de_dadoN <Nome das VariáveisN>;
     };
     
     Exemplo:
      struct Funcionario {
       <b>int</b>    matricula;
       string nome;
       string dataNasc;
       string cargo;
       float  salario
     };
     ```
