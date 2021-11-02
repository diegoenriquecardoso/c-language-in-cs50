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

# Abstração


