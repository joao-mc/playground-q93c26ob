# Cadeia de caracteres (ou string)

+ Uma cadeia de caracteres (string em inglês) é uma sequência de caracteres ou símbolos definido pelo código ASCII. 

+ Em linguagem C, uma cadeia de caracteres pode ser tratado como um "Vetor" do tipo char, cujo último elemento é o caractere nulo '\0', ou seja, o primeiro caractere do código ASCII (cujo valor é 0). 

+ Este caractere é um caractere de controle (ou seja, não exibível) que indica o fim de uma cadeia de caracteres. Assim, uma cadeia composta de n elementos será, na realidade, um vetor de n +1 elementos do tipo char. 

+ Podemos, por exemplo, representar a string "Ola Mundo!" da seguinte maneira: 
![programa](/markdowns/olamundo.gif)

---
Declaração de Cadeias de caracteres
---
A declaração de uma string em C é semelhante a declaração de um  vetor do tipo char. O número máximo de caracteres que comportará a cadeia será igual ao número de elementos do vetor menos um (reservado para o caractere do final da cadeia), por exemplo, se definirmos uma cadeia de caracteres de tamanho 30, ela conterá 29 caracteres + '\0'. 

```
char Nome_da_tabela[Número_de_elementos]
```
---
Inicialização de cadeia de caracteres
---
+ A inicialização de uma string, ou seja, mover caracteres, pode ser feita de duas maneiras:

  + Mover manualmente os dados, célula por célula; ou
  + Utilizar funções de manipulação de cadeias de fornecidas nas bibliotecas padrão

Exemplo de inicialização manual de cadeia de caracteres (para impressão de cadeia de caracteres com o comando <b>printf</b> devemos utilizar o caracter formatção <b>"%s"</b> : 
``` C runnable
#include <stdio.h> 
int main(){ 
 char Cadeia[11]; 
 Cadeia[0]= 'L'; 
 Cadeia[1]= 'i'; 
 Cadeia[2]= 'n'; 
 Cadeia[3]= 'g'; 
 Cadeia[4]= 'u'; 
 Cadeia[5]= 'a'; 
 Cadeia[6]= 'g'; 
 Cadeia[7]= 'e';
 Cadeia[8]= 'm';
 Cadeia[9]= ' ';
 Cadeia[10]= 'C';
 Cadeia[11]= '\0'; 
 
 printf("%s",Cadeia);
 }
```

Outra maneira (mais simples) de inicializarmos uma cadeia de caracteres é na sua declaração, como no exmplo abaixo: 
``` C 
#include <stdio.h> 
int main(){ 
 char Cadeia[11] = {'L', 'i', 'n', 'g', 'u', 'a', 'g', 'e', 'm', ' ', 'C',  '\0'}; 
 
 printf("%s",Cadeia);
 }
```

#include <stdio.h> void main(){ char Cadeia[20+1]={ 'B', 'o', 'n', 'j', 'o', 'u', 'r', '\0' }; }
