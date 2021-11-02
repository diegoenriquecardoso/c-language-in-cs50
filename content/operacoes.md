# Operações

A linguagem C aceita diversos tipos de operadores para realização de cálculos e funções, como:

> \+ para adição, - para subtração, * para multiplicação, / para divisão e % para dizer o resto de uma divisão(módulo). 

```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    int x = get_int("x: ");

    int y = get_int("y: ");

    printf("%i\n", x + y);
}
```

> int x = get_int("x: ");

> int y = get_int("y: ");

Aqui vemos um programa com a função de somar valores, novamente percebe-se o uso do comando get para conseguir input do usúário assim como declaração de váriaveis e alocação de seus valores a o que o usuário digitou para que possamos utiliza-los em outra parte do código. Dessa vez, o data type utilizado é int, que representa números inteiros e que podemos utilizar para fazer as mais variadas operações matemáticas.

> printf("%i\n", x + y);

Para dar o resultado da soma como output, dessa vez imprimiremos apenas valores relacionados as variáveis, portanto o uso do "%i". Nota-se que ele esta em junção de "\n", este serve para que o valor exibido pelo programa fique separado da próxima linha do terminal.

Sem \n:

![image](https://user-images.githubusercontent.com/93105584/139869175-f7336735-4565-42f1-ab1e-8ce925a36e38.png)

Com \n:

![image](https://user-images.githubusercontent.com/93105584/139869389-515a8d70-57c3-4546-834c-6f9178d0ff4c.png)

Como desta vez não imprimiremos o valor de apenas uma variável, mas de duas somadas, colocamos um sinal de "+" entre elas ao colocá-las dentro do comando printf.

Caso quiséssemos trabalhar com valores possívelmente maiores (no caso maiores que 4 bilhões), poderíamos trocar o data type do código de "int" para "long". Assim como se quiséssemos dividir em vez de somar trocaríamos o símbolo de "+" por um de "/". 

Porém, por sua vez caso quisséssemos que nossas divisões pudessem resultar em números com vírgula, teríamos que fazer algumas mudanças além de simplesmente utilizar os data types "float" ou "double":
```
#include <stdio.h>
#include <cs50.h>

int main(void)
{   
    // Get numbers from user
    int x = get_int("x: ");
    int y = get_int("y: ");

    // Divide x by y
    float z = (float) x / (float) y;
    printf("%f/n", z);
}
```
Aqui, simplesmente criamos uma nova variável para representar o valor da divisão, ao invés de simplesmente deixar a operação dentro do printf como na soma. Além disso, utilizamos uma outra função muito importante da Linguagem C:

> float z = (float) x / (float) y;

Tanto a variável x como a variável y se tratam de "ints", porém, ao colocarmos um novo data type entre parênteses quando as apresentamos em outra linha, como na operação de divisão, elas são convertidas para o o tipo escolhido, no caso floats, mas apenas na linha em que isso foi feito, isso é denominado **Typecasting**. Mesmo a variável z a qual foi alocado o valor da divisão sendo um "float", caso X e Y permaneçam ints, quaisquer divisões que resultem em valores com vírgula seriam equívocados. 

> // Get numbers from user

> // Divide x by y

Por fim, como pode ser visto, há **comentários** no código do último exemplo, para fazê-los basta colocar "//" em junção do que se deseja comentar sobre qualquer um dos códigos. Esta é uma função muito importante que permite que outras pessoas possam entender melhor o que foi programado, assim como possibilita uma melhor colaboração coletiva e aprendizado sobre o código.

Extra: [Lista de Operadores](https://github.com/diegoenriquecardoso/c-language-in-cs50/blob/main/content/operadores.md)

Anterior: [2 - Data Types](https://github.com/diegoenriquecardoso/c-language-in-cs50/blob/main/content/datatypes.md) / Próximo: [4 - Condições](https://github.com/diegoenriquecardoso/c-language-in-cs50/blob/main/content/condicoes.md)

[index]() / [Todos desta]() / [Todos comandos]()
