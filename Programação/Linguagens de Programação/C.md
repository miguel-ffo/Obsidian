
A linguagem **C** é uma das mais antigas e amplamente usadas linguagens de programação, criada por **Dennis Ritchie** em 1972. 
Ela é conhecida por ser eficiente, de baixo nível (próxima do hardware) e por fornecer controle direto sobre a memória do computador, o que a torna ideal para o desenvolvimento de sistemas operacionais, softwares de sistemas e aplicativos de alto desempenho.

### Conceito

C é uma linguagem **imperativa** e **procedural**, o que significa que o programa é composto de funções e comandos sequenciais. 
Ela segue um paradigma de programação estruturada, promovendo o uso de funções, blocos de código e controle de fluxo para organizar o programa.

### Características principais

- **Eficiência:** Oferece controle direto sobre alocação e manipulação de memória através de ponteiros.
- **Portabilidade:** Código escrito em C pode ser facilmente compilado e executado em diferentes plataformas com poucas modificações.
- **Bibliotecas robustas:** Tem um vasto conjunto de bibliotecas padrão para operações de entrada/saída, manipulação de strings, alocação de memória, entre outras.
- **Modularidade:** Incentiva a divisão de código em funções menores, facilitando a manutenção.

### Sintaxe básica

1. **Estrutura de um programa** Um programa em C normalmente segue uma estrutura básica composta por funções, sendo a principal delas a `main()`, que é o ponto de entrada do programa:

```
#include <stdio.h>  // Diretiva de pré-processador para incluir bibliotecas

int main() {        // Função principal
    printf("Hello, World!");  // Função de saída
    return 0;       // Retorna 0 para indicar sucesso
}


```

2. **Declaração de variáveis** Em C, as variáveis precisam ser declaradas com seu tipo antes de serem usadas:

```
int idade = 25;
float altura = 1.75;
char letra = 'A';

```

3. **Estruturas de controle** C oferece as estruturas de controle básicas como condicionais e loops:

```
// Condicional if-else
if (idade > 18) {
    printf("Maior de idade.\n");
} else {
    printf("Menor de idade.\n");
}

// Loop for
for (int i = 0; i < 5; i++) {
    printf("%d\n", i);
}

```

4. **Funções** Funções em C são blocos de código reutilizáveis que podem ser chamados a partir de outras partes do programa:

```
int soma(int a, int b) {
    return a + b;
}

int main() {
    int resultado = soma(10, 5);
    printf("Resultado: %d", resultado);
    return 0;
}

```


5. **Ponteiros** Ponteiros são uma característica poderosa de C, que permitem a manipulação direta da memória:

```
int x = 10;
int *ptr = &x;  // Ponteiro aponta para o endereço de 'x'
printf("Valor de x: %d\n", *ptr);  // Desreferencia o ponteiro para acessar o valor

```

6. **Alocação dinâmica** C permite a alocação dinâmica de memória usando funções como `malloc()` e `free()`:

```
int *array = (int*) malloc(5 * sizeof(int));  // Aloca memória para um array de 5 inteiros
if (array != NULL) {
    // Usa o array
    free(array);  // Libera a memória alocada
}

```
### Aplicações

A linguagem C é amplamente usada no desenvolvimento de:

- Sistemas operacionais (como o Unix e o Linux)
- Compiladores
- Sistemas embarcados
- Jogos e motores gráficos
- Aplicativos que exigem alto desempenho