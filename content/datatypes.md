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

Anterior: [1 - Introdução](https://github.com/diegoenriquecardoso/c-language-in-cs50/blob/main/content/introducao.md) / Próximo: [3 - Operações](https://github.com/diegoenriquecardoso/c-language-in-cs50/blob/main/content/operacoes.md)

[index]() / [Todos desta]() / [Todos comandos]() / Extra: 
[Lista Detalhada sobre os Data Types](https://github.com/diegoenriquecardoso/c-language-in-cs50/blob/main/content/dataspecify.md)
