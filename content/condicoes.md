# Condições

O principal comando que estabelece condições para que algo aconteça se trata do comando "if".
```
if (x < y)
{
    printf("x is less than y\n");
}
```
Dentro das parênteses após o If, temos uma expressão booleana, que pode ser apenas verdadeira ou falsa, caso seja verdeira, o programa irá imprimir algo.
Também podemos utilizar o comando "else" em sua junção para que o programa faça algo caso a condição seja falsa.
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
E mesmo "else if" para adicionar ainda mais possibilidades conforme as expressões vão sendo verdadeiras ou falsas.
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
Note que utilizamos novamente "**headers**" para incluir funções não-nativas ao C, "**int main(void)**" para declarar a função principal do programa e que não exige input inicial, assim como o comando "**get**" para conseguir input do usuário após a execução do código. 
Ademais, não precisamos da condição "else if (x == y)" e sim apenas "else", pois é a única possibilidade que sobrará.

Mais um exemplo:
```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    char c = get_char("Do you agree? ");

    // Check whether agreed
    if (c == 'Y' || c == 'y')
    {
        printf("Agreed.\n");
    }
    else if (c == 'N' || c == 'n')
    {
        printf("Not agreed.\n");
    }
}
```
Nota aqui que dentro das expressões booleanas(que podem apenas ser verdadeiras ou falsas) temos o uso do símbolo "||", ele representa que a expressão inteira será tida como verdadeira desde que no mínimo uma das condições presentes sejam verdadeiras, o mesmo que um "ou" e foi utilizada no código para que independentemente de o usuário fazer seu input em caixa alta ou baixa, o programa rode normalmente. Também dentro das expressões booleanas podemos ver entre uma ou mais condições o símbolo "&&" e ele significa que a condição será verdadeira apenas se todos argumentos dentro dela sejam verdadeiros, o oposto de "||". Também imporante denotar que os comandos if não terminam em ";".

Anterior: [3 - Operações](https://github.com/diegoenriquecardoso/c-language-in-cs50/blob/main/content/operacoes.md) / Próximo: [5 - Loops](https://github.com/diegoenriquecardoso/c-language-in-cs50/blob/main/content/loops.md)

[Index]() / [Todos desta]() / [Todos comandos]()
