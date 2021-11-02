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

> ./<nome-do-programa> (sem espaço)
   
A Linguagem C é capaz das mais variadas possibilidades, algumas das quais veremos neste repositório. Antes disso devemos entender melhor sobre outros elementos muito presentes nos códigos em C.

# Segundo Exemplo
```
#include <cs50.h>
#include <stdio.h>

int main(void)
{
    string answer = get_string("What's your name? ");
    printf("hello, %s", answer);
}
```










