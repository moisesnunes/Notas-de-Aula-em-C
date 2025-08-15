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

### 1.2
