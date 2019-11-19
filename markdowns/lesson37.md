# Ficheiros em C
---
+ Arquivo é um conjunto de dados nomeados, armazenados e organizados em um meio de armazenamento de dados. 
+ Por que usar arquivos?
    + Permitem armazenar grande quantidade de informação;
    + Dados não são perdidos (persistência dos dados);
    + Acesso aos dados poder ser não seqüencial;
    + Acesso concorrente aos dados (mais de um programa pode usar os dados ao mesmo tempo).
+ Basicamente, a linguagem C trabalha com dois tipos de arquivos: de texto e binários.
    + <b>Arquivo texto</b> : Armazenam caracteres que podem ser mostrados diretamente na tela ou modificados por um editor de textos simples como o Bloco de Notas. 
    + <b>Arquivo binário</b> : Armazena uma sequência de bits que está sujeita as convenções dos programas que o gerou. Ex: arquivos executáveis, arquivos compactados, arquivos de registros, etc.</br>
 

 A figura abaixo exibe o conteúdo dos arquivos (texto e binário) armazenando os seguintes dados: <br>

 struct <br/>
  {<br/>
       int matric; <br/>
       char nome[10]; <br/>
       float salario; <br/>
  } func; <br/>
  
                  Texto                                                                     Binário
 ![programa](/markdowns/arquivo.png)                                       
 
   
