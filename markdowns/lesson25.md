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

