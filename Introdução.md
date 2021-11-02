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
O Header em si no caso é o stdio.h, todos headers sempre devem ser colocados entre "<" e ">".

A função do stdio.h aqui é a de permitir o uso do comando printf, não originalmente parte da Linguagem C, o comando permite que os programas imprimam textos e/ou símbolos como output.

Após o Header, vemos "int main(void)": Esta linha está sempre inclusa nos programas que não precisam de um input para serem iniciados, o (void) representa que nada deve ser colocado adjacente ao comando de iniciar o programa.

