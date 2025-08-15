## Sintaxe de um programa básico em C

Um programa C consiste de uma ou mais partes chamadas funções. Pelo menos uma função chamada <b>main<b> deve existir. Esta função marca o ponto de início de execução do programa.

```c
#include <stdio.h>

int main()
{
    ...
}
```

### 1.1 Senteças: simples e compastas

Em c uma intrução pode ser classificada de duas formas: simples e composta.

- Sentenças simples são terminadas com ponto e vírgula

```c
x = 3;
```

- Sentenças compostas podem ser defindas pelo uso de chaves, que são conhecidas como blocos

```c
{
    x = 1;
    printf("%d\n", x);
    x = x + 1;
}
```

### 1.2 Variáveis em C

Uma variável é nada mais que um nome que damos a uma determinada posição na memória para conter um valor de um determinado tipo.
Como seu próprio nome indica, o valor contido em uma variável pode variar ao longo da execução de um programa.
O nome da variável e o endereço da memória onde a informação está armazenada estão associados.
O nome e o endereço não mudam. Mas, o valor da informação pode mudar. Cada variável tem um tipo associado. Alguns tipos de variáveis que discutiremos incluem:

```c
int
char
float
double
```

Cada variável usa uma determinada quantidade de armazenamento em memória. A maneira como sabemos quantos bytes são utilizados é pelo tipo da variável. Variáveis do mesmo tipo utilizam o mesmo número de bytes, não interessando qual o valor que a variável armazena.

Um dos tipos utilizados para armazanar números é o int. Ele é usado para armazenar números inteiros e ocupa geralmente 4 bytes.

```c
int i;
```

Outro tipo é o char, usado para armazenar caracteres e ocupa apenas um byte

```c
char ch1, novo_char;
```

Outro tipo existente é o float, usado para armazenar números reais (números com o ponto decimal) e ocupa geralmente 4 bytes

```c
float pi, raio, perimetro;
```

Outro tipo básico é o double, usado para armazenar números reais com maior precisão e ocupa geralmenete 8 bytes

```c
double total, k1234;
```

### 1.3 Definição de Variável em C

Se você usa variáveis no programa, você deve defini-las. Isto envolve especificar o tipo da variável e o seu nome.

```c
tipo var
```

A declaração de variáveis tem que ser sempre realizadas antes de sua untilização e antes de qualquer instrução

As regras para formar nomes de variáveis em C são:

- qualquer sequência de letras, digitos, e ’_’, MAS DEVE COMEÇAR com uma letra ou com ’_’. Por exemplo, hora_inicio, tempo, var1 são nomes de variáveis válidos, enquanto 3horas, total$ e azul-claro não são nomes válidos;

- Maiúsculas 6= Minúsculas;

- Não são permitidos nomes ou palavras reservadas da linguagem.

Estas são as palavras reservadas em C e que não podem ser usadas como nome de variáveis:

<!--
| auto    | break    | case   | char    | const  | continue |
| default | do       | double | else    | enum   | extern   |
| float   | for      | goto   | if      | int    | long     |
| main    | register | retur  | short   | signed | sizeof   |
| static  | struct   | switch | typedef | union  | unsigned |
| void    | volatile | while  |  -->

|         |          |        |         |        |          |
| ------- | -------- | ------ | ------- | ------ | -------- |
| auto    | break    | case   | char    | const  | continue |
| default | do       | double | else    | enum   | extern   |
| float   | for      | goto   | if      | int    | long     |
| main    | register | return | short   | signed | sizeof   |
| static  | struct   | switch | typedef | union  | unsigned |
| void    | volatile | while  |         |        |          |

Uma tabela mais atualizada com o padrão iso c23:

|                 |               |                     |
| --------------- | ------------- | ------------------- |
| alignas (c23)   | extern        | sizeof              |
| alignof (c23)   | false (c23)   | static              |
| auto            | float         | static_assert (c23) |
| bool (c23)      | for           | struct              |
| break           | goto          | switch              |
| case            | if            | thread_local (c23)  |
| char            | inline        | true (c23)          |
| const           | int           | typedef             |
| constexpr (c23) | long          | typeof (c23)        |
| continue        | nullptr (c23) | typeof_unqual (c23) |
| default         | register      | union               |
| do              | restrict      | unsigned            |
| double          | return        | void                |
| else            | short         | volatile            |
| enum            | signed        | while               |

Para uma definição mais completa veja o link: [KeyWords](https://en.cppreference.com/w/c/keyword.html)

Quando variáveis são definidas, elas não possuem valores ainda. Nós damos valores às variáveis usando o operador de atribuição (=). Variáveis também podem ser inicializadas para conter valores quando são definidas.

Para resumir: quando um programa é executado, uma variável é associada com:

- um tipo: diz quantos bytes a variável ocupa, e como ela deve ser interpretada.

- um nome: um identificador.

- um endereço: o endereço do byte menos significativo do local da memória associado a variável.

- um valor: o conteúdo real dos bytes associados com a variável; o valor da variável depende do tipo da variável; a definição da variável não dá valor a variável; o valor é dado pelo operador de atribuição, ou usando a função scanf().

- Em C , nomes de variáveis devem ser declarados antes de serem usados. Se não for declarado, ocorrerá um erro de compilação.

- Devem ser dados valores às variáveis antes que sejam utilizadas. Se você tentar utilizar a variável antes de especificar o seu valor, você obterá “lixo” (o que quer que esteja armazenado no endereço da variável na memória quando o programa começa sua execução), culminando com falha na execução do programa.
