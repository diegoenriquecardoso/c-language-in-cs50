# Introdução
Primeiramente, todos os códigos descritos a seguir e nos próximos arquivos deste repositório foram escritos utilizando o [CS50 IDE](https://ide.cs50.io).

Três aspectos devem ser levados em conta quando escrevendo em C: **quão correto** está o código, quão **bem escrito** está o código (Design) e se ele foi estéticamente **bem formatado** (Estilo).

# Exemplo Inicial
```
#include <stdio.h>

int main(void)
{
    printf("hello, world");
}
```
Aqui vemos um código que terá como output a frase "Hello, World", de início vemos "#include <stdio.h>": Trata-se de um header. Headers são adicionados antes de qualquer outra função no código e servem para adicionar novas funcionalidades a linguagem C. Muitas vezes quando programando um novo projeto, percebemos que falta algum comando ou função para que possamos realizar nosso objetivo, é ai que os Headers se tornam essenciais, são como uma livraria de novas capacidades para a programação em C.
> #include

Comando para introduzir o Header.

> <stdio.h>

O Header em si, todos sempre devem ser colocados entre "<" e ">".

A função do stdio.h nesse caso específico é a de permitir o uso do comando printf, não originalmente parte da Linguagem C, o comando permite que os programas imprimam textos e/ou símbolos como output, mas ele também permite o uso de uma série de outras funções que serão descritas mais tarde.

Após o Header, vemos: 

> int main(void)

Esta linha está sempre inclusa nos programas que não precisam de um input para serem iniciados, "int main" se trata da declaração da função principal "main" do programa, já " (void)" dita como nada deve ser escrito adjacente ao comando de iniciação quando for se executar o programa. 

> printf("hello, world");

O corpo do programa que dirá o que o deve ser feito e de que forma sempre deve ser colocado entre chaves "{" e "}". Aqui vemos o comando "printf", ele irá imprimir para o usuário o que tiver sido escrito dentro das parênteses e entre aspas após o mesmo. Como outros "corpos" ou "branches", sempre após um comando printf, deve-se utilizar ponto e vírgula ";".

# Compilação

Após um programa ser escrito, antes de podermos executá-lo, o mesmo deve ser compilado, isso é feito através de um comando no terminal.

> make <nome-do-programa.c>

Caso haja erros, a compilação não será feita e o usuário deve buscar encontrar os bugs em seu código. Caso a compilação seja um sucesso, para inicializar o programa utilizados outro comando no terminal.

> ./\<nome-do-programa\>
   
A Linguagem C é capaz das mais variadas possibilidades, algumas das quais veremos neste repositório. Antes disso devemos entender melhor sobre outros elementos muito presentes nos códigos em C.

# Data Types, Comandos Get e Variáveis
```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    string answer = get_string("What's your name? ");
    printf("hello, %s", answer);
}
```
Aqui vemos três novos elementos, "data types", "comandos get" e uma variável.

> string answer

String é um data type, uma tipo de formato de alocação de memória do hardware para que trabalhe com "palavras", ou seja, uniões de letras. Há muitos outros data types que ainda citaremos. Após a sua declaração vemos "answer", ao unir um "data type" com um nome escolhido para o mesmo, temos uma variável, nesse caso é uma variável do tipo "String" que se chama "answer"

> get_string

Os "comandos get" são utilizados para conseguir algum tipo de input especifico do usuário dependendo de qual "data type" é escrito em junção ao comando, nesse caso "get_string", ou seja, o computador só irá aceitar palavras, caso o usuário escreva um número, por exemplo, o programa irá pedir novamente por um input até que recebe o especificado. O "comando get" assim como o "printf" visto mais cedo, também imprime algo na tela. Ademais, como sua função é a de receber inputs, dentro das parênteses e entre as aspas deve sempre ser colocado um espaçamento no final para que a resposta do usuário possa ser alocada. Assim como outros comandos, ponto e vírgula ";" no fim de sua linha é necessário. Ademais, o header <cs50.h> incluso neste código é o que possibilita o uso de comandos "get".

> printf("hello, %s", answer);

Como vimos mais cedo, "printf" imprime um output para o usuário, este que sempre está dentro das parênteses e entre aspas. No caso vamos algo um pouco diferente do primeiro ("Hello, World"), aqui temos ("hello, %s", answer), "%" representa que alguma variável será imprimida no comando, o data type da variável deve ser especificado com uma letra no caso "%s" significa que uma variável do tipo string será imprimida, após isso, finalizando as aspas e separando-os por uma vírgula, a variável em si deve ser especificada, no caso a variável "answer". O Objetivo deste programa era que o output fosse Hello + o nome do usuário(pedido como input inicial), para isso criamos uma variável que utilizasse palavras como valores e pedimos um input do mesmo tipo. Foi utilizado um sinal de igual "=" para alocar qualquer fosse o input do usuário ao valor da variável.

# Tipos

**bool**: representa expressões booleanas, aceita apenas valores de "verdadeiro" ou "falso"

**char**: um único caractere ASCII, como "a" ou "2" 

**string**: uma "corrente" de caracteres

**int**: um número inteiro que pode ir até um certo número positivo ou negativo, ou até um número de bytes.

**long**: número inteiro assim como o int, só que com mais bits, portando consegue suportar numeros maiores, em detrimento da capacidade de se utilizar números negativos.

**float**: um valor que pode alocar tanto números reais como números com vírgula ou decimais.

**double**: um float capaz de utilizar mais digitos

### E os comandos get correspondentes:

> get_char, get_string, get_int, get_long, get_float, get_double

### Para o comando printf, também temos diferentes placeholders correspondentes para imprimir cada data type:

> %c para chars, %s para strings, %i para ints %li para longs, %f para floats e doubles

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

Por fim, como pode ser visto, há **comentários** no código do último exemplo, para fazê-los basta colocar "//" em junção do que se deseja comentar sobre qualquer um dos códigos. Esta é uma função muito importante que permite que outras pessoas possam entender melhor o que foi programado, assim como possibilita uma melhor colaboração coletiva e aprendizado sobre o código.

# Condições

O principal comando que estabelece condições para que algo aconteça se trata do comando "if".
```
if (x < y)
{
    printf("x is less than y\n");
}
```
Também podemos utilizar o comando "else" em sua junção para adicionar mais possibilidades
```
if (x < y)
{
    printf("x is less than y\n");
}
else
{
    printf("x is not less than y\n");
}
```
E mesmo "else if"
```
if (x < y)
{
    printf("x is less than y\n");
}
else if (x > y)
{
    printf("x is greater than y\n");
}
else if (x == y)
{
    printf("x is equal to y\n");
}
```
Percebe-se que na Linguagem C, o símbolo "=" é usado apenas para alocar um valor a outro, normalmente dar um valor para uma variável. Quando desejamos expressar uma igualdade, utilizamos "==". Podemos expressar isso através do seguinte programa:
```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    // Prompt user for x
    int x = get_int("x: ");

    // Prompt user for y
    int y = get_int("y: ");

    // Compare x and y
    if (x < y)
    {
        printf("x is less than y\n");
    }
    else if (x > y)
    {
        printf("x is greater than y\n");
    }
    else
    {
        printf("x is equal to y\n");
    }
}
```
Note que utilizamos aqui novamente Header para incluir funções não-nativas ao C, int main(void) para declarar a função principal do programa e que não exige input inicial, assim como comando get para conseguir input do usuário após a execução do código. 
Ademais, não precisamos dizer a condição "else if (x == y)" e sim apenas "else", pois é a única possibilidade que sobrou.


# Loops


