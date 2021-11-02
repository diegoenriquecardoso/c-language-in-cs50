# Loops

Temos várias formas de fazer Loops em C, para fazer um loop eterno:
```
while (true)
{
    printf("hello, world\n");
}
```
A palavra-chave while requer uma condição, ao colocar true dentro da expressão booleana, fazemos com que a condição seja sempre verdadeira e com que o loop nunca acabe.

Para fazer com que algo aconteça um determinado número de vezes, poderíamos utilizar:
```
int i = 1;
while (i <= 50)
{
    printf("hello, world\n");
    i++;
}
```
Onde enquanto a variável i for menor ou igual a 50, o loop continuará se repetindo e a frase "Hello, world" continuará sendo imprimida na tela do usuário. Porém, para garantir que o loop acontecerá 50 vezes, inserimos o comando "i++" que é o mesmo que "i = i + 1" e significa que cada vez que o código for executado, o valor da variável em questão aumentará em 1, eventualmente esse valor chegará em 50 e a condição não será mais verdadeira, terminando o loop. Caso quiséssemos começar com a variável valendo 50 e que ela diminuísse cada vez que o programa fosse executado, poderíamos simplesmente utilizar "i--" ao invés de "i++" e fazer com que o loop só funcionasse enquanto i > 0.
Entretando, a forma ideal de se realizar este tipo de loop é a seguinte:
```
for (int i = 0; i < 50; i++)
{
    printf("hello, world\n");
}
```
Este se trata do "comando for", onde é estabelecida uma variável e seu valor inicial; a condição para que o loop ocorra e o que acontecerá com a variável cada vez que esse loop ocorrer, tudo em apenas uma linha. Nota-se que assim como os comandos if, o comando for também não termina com ";".

# Abstração e Declaração de mais funções

Até agora utilizamos a apenas a função principal de nossos programas, como criamos outras funções? podemos começar fazendo um programa que imprime a palavra "meow" três vezes, como um gatinho.
```
#include <stdio.h>

int main(void)
{
    printf("meow\n");
    printf("meow\n");
    printf("meow\n");
}
```
Poderíamos aprimorá-lo utilizando o comando for:
```
#include <stdio.h>

int main(void)
{
    for (int i = 0; i < 3; i++)
    {
        printf("meow\n");
    }
}
```
E também podemos definir uma função para o nosso miado:
```
#include <stdio.h>

void meow(void) {
  printf("meow\n");
}

int main(void)
{
    for (int i = 0; i < 3; i++)
    {
        meow();
    }
}
```
Porém, nossa função principal deve sempre ser a primeira de nosso programa, portanto iremos mover algumas linhas:
```
#include <stdio.h>

void meow(void);

int main(void)
{
    for (int i = 0; i < 3; i++)
    {
        meow();
    }
}

void meow(void)
{
    printf("meow\n");
}
```
Dessa forma, primeiro declaramos nossa nova função no início do código, mas esta é apenas um protótipo, assim funcionam as funções em C: devem ser declaradas primeiro e definidas depois para que possam ser utilizadas na função principal. A função do gatinho começa em void pois não retorna nenhum tipo de valor, apenas mia. Outro exemplo de declaração de funções e que também apresenta uma nova forma de loop:
```
#include <cs50.h>
#include <stdio.h>

int get_positive_int(void);

int main(void)
{
    int i = get_positive_int();
    printf("%i\n", i);
}

// Prompt user for positive integer
int get_positive_int(void)
{
    int n;
    do
    {
        n = get_int("Positive Integer: ");
    }
    while (n < 1);
    return n;
}
```
Aqui vemos um programa que pede um input do usuário, mas só aceita números positivos, declaramos um protótipo da nossa função get_positive_int que recusará números negativos, dessa vez começando com int e não void, pois retornará um valor. A função em si foi definida após a principal, nela vemos um loop "do while", que fará algo enquanto uma condição for verdadeira, no caso, enquanto o input do usuário for um número negativo, continuará pedindo um valor, denovo e denovo, até que recebe um valor positivo e a condição se torne falsa. Esse tipo de loop garante que algo irá acontecer pelo menos uma vez.

# Mario

Por fim, podemos fazer um loop dentro de outro loop, da seguinte maneira:
```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    for (int i = 0; i < 3; i++)
    {
        for (int j = 0; j < 3; j++)
        {
            printf("#");
        }
        printf("\n");
    }
}
```
Note que sempre que o loop externo acontece, o de baixo acontece três vezes. O primeiro Sempre faz uma linha nova, enquanto o segundo imprime o símbolo "#". Ao fim do loop, o primeiro terá acontecido três vezes e o segundo nove vezes. e terão formado uma coluna hashes em ASCII da seguinte forma:

![image](https://user-images.githubusercontent.com/93105584/139908281-60cabd4e-ef25-4cbe-8334-65cdbf22946b.png)


Anterior: [4 - Condições](https://github.com/diegoenriquecardoso/c-language-in-cs50/blob/main/content/condicoes.md) / Próximo: [6 - Debugging]()

[Index]()
