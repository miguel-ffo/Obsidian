
## Estrutura do nó:

```
typedef struct No {
    int dado;
    struct No *no_esquerdo;
    struct No *no_direito;
} t_no;

```
Cria uma nova variável contendo o dado, um ponteiro para o filho esquerdo, e ou ponteiro para o filho direito.

## Funções

### Criar um novo nó:

```
#include <stdlib.h>  // Necessário para malloc
```

Biblioteca para usar alocação de memória

```
t_no *novoNo(int valor) {
    t_no *No = (t_no *)malloc(sizeof(t_no));
    if (No == NULL) {
        printf("Erro ao alocar memória!\n");
        exit(1);
    }
    No->dado = valor;
    No->no_esquerdo = NULL;
    No->no_direito = NULL;
    return No;
}
```

Cria uma função chamada 'novoNo' com um ponteiro para a variável criada lá no struct, com o parâmetro 'valor'.

Dentro alocamos memória para a variável 'No' com ponteiro para 't_no'.
Depois uma verificação se a memória foi alocada.

Inicializamos as variáveis 'dado', 'no_esquerdo' e 'no_direito', que estão dentro da struct 'No', e atribuímos 'NULL' ao no_esquerdo e no_direito.

Retorna o Nó
### Inserir:

```
t_no *Inserir(t_no *raiz, int valor) {
    if (raiz == NULL) {
        return novoNo(valor);
    }

    if (valor < raiz->dado) {
        raiz->no_esquerdo = Inserir(raiz->no_esquerdo, valor);
    } else if (valor > raiz->dado) {
        raiz->no_direito = Inserir(raiz->no_direito, valor);
    }

    return raiz;
}
```

Cria uma função chamada 'Inserir' com ponteiro para a struct 't_no', e com parâmetros de 'raiz' que e um ponteiro para a struct 't_no', e um valor.

Verifica se 'raiz' é 'NULL', se sim, retorna a função 'novoNo' passando o 'valor' como parâmetro.

Caso o valor inserido seja menor que o contido na raiz, a função chama recursivamente ela mesma, passando o 'no_esquerdo' da raiz e o valor como parâmetro.

Caso seja maior, chama recursivamente a função inserir passando o 'no_direito' e o valor como parâmetro.

Retorna a raiz

### Buscar:

```
t_no *Buscar(t_no *raiz, int valor) {
    if (raiz == NULL) {
        return NULL;
    }

    if (valor == raiz->dado) {
        return raiz;
    }

    if (valor < raiz->dado) {
        return Buscar(raiz->no_esquerdo, valor);
    } else {
        return Buscar(raiz->no_direito, valor);
    }
}
```

Cria a função chamada 'Buscar' que é um ponteiro para a struct 't_no' , passando a raiz com ponteiro para 't_no', e o valor buscado.

Faz uma verificação se a raiz é 'NULL'.

Verifica se o valor já existe na árvore.

Verifica se o valor é menor do que a raiz, se sim, chama a função recursivamente passando a raiz contida no 'no_esquerdo' e o valor a ser buscado.

Se for maior, chama recursivamente passando , agora, a raiz do 'no_direito' e o valor a ser buscado.


### Remover:

```
t_no *Remover(t_no *raiz, int valor) {
    if (raiz == NULL) {
        return raiz; // O valor não foi encontrado
    }

    if (valor < raiz->dado) {
        raiz->no_esquerdo = Remover(raiz->no_esquerdo, valor);
    } else if (valor > raiz->dado) {
        raiz->no_direito = Remover(raiz->no_direito, valor);
    } else {
        // Caso 1: O nó é uma folha
        if (raiz->no_esquerdo == NULL && raiz->no_direito == NULL) {
            free(raiz);
            return NULL;
        }
        // Caso 2: O nó tem apenas um filho
        else if (raiz->no_esquerdo == NULL) {
            t_no *temp = raiz->no_direito;
            free(raiz);
            return temp;
        } else if (raiz->no_direito == NULL) {
            t_no *temp = raiz->no_esquerdo;
            free(raiz);
            return temp;
        }
        // Caso 3: O nó tem dois filhos
        else {
            t_no *sucessor = raiz->no_direito;
            while (sucessor->no_esquerdo != NULL) {
                sucessor = sucessor->no_esquerdo;
            }
            raiz->dado = sucessor->dado;
            raiz->no_direito = Remover(raiz->no_direito, sucessor->dado);
        }
    }
    return raiz;
}
```

Cria a função 'Remover' que é um ponteiro para a struct 't_no' , passando os parâmetros raiz com ponteiro para 't_no', e o valor a ser removido.

Verifica se a raiz é 'NULL' , se sim , retorna a raiz.

Verifica se o valor a ser removido é menor que o dado contido na raiz, se sim , chama a função recursivamente passando o 'no_esquerdo' contido na raiz, e o valor a ser removido.

Se for maior, chama recursivamente passando o 'no_direito', e o valor a ser removido.

Caso não se encaixe em nenhuma dessas verificações, chama outra verificação se o 'no_esquerdo' da raiz for 'NULL' E o 'no_direito' também for 'NULL'.
Libera a raiz e retorna 'NULL'.

Outra verificação se o 'no_esquerdo' for 'NULL', cria uma variável 'temp' que é um ponteiro para a struct 't_no' passando o 'no_direito' da raiz.
Libera a raiz e retorna o 'temp'.

Verifica mais uma vez , porem se o 'no_direito' for 'NULL', cria a variável 'temp' como ponteiro para 't_no' passando o 'no_esquerdo'.
Libera a raiz e retorna o 'temp' .

Caso não seja nenhuma das anteriores, cria a variável 'sucessor' como ponteiro para 't_no' passando o 'no_direito' da raiz.

Cria um loop , enquanto o 'no_esquerdo' do sucessor não for 'NULL', o 'sucessor' recebe o no_esquerdo contido do 'sucessor'.

Depois passa o 'dado' contido na raiz recebendo o 'dado' do 'sucessor'.
E o 'no_direito' passando a função recursivamente , com o 'no_direito' contido na raiz e o 'dado' contido no 'sucessor'.

Após isso tudo, retorna a raiz.


### Liberar Arvore

```
void LiberarArvore(t_no *raiz) {
    if (raiz != NULL) {
        LiberarArvore(raiz->no_esquerdo);
        LiberarArvore(raiz->no_direito);
        free(raiz);
    }
}
```

Cria uma função 'void' nomeada 'LiberarArvore' , passando a raiz com ponteiro para a struct 't_no'.

Verifica se a raiz não é 'NULL',  se não for, chama recursivamente a função passando o 'no_esquerdo', e depois chama novamente passando o 'no_direito'.

Libera a raiz.

### Main

```
int main() {
    t_no *resultado;
    t_no *raiz = NULL;
    int op;

    do {
        printf("====================================\n");
        printf("|     ARVORE BINARIA DE BUSCA      |\n");
        printf("====================================\n");
        printf("|             OPÇÕES               |\n");
        printf("====================================\n");
        printf("|           1 - INSERIR            |\n");
        printf("|           2 - BUSCAR             |\n");
        printf("|           3 - REMOVER            |\n");
        printf("|           4 - SAIR               |\n");
        printf("====================================\n\n");

        scanf("%d", &op);

        switch (op) {
        case 1:
            do {
                int valor;
                printf("====================================\n");
                printf("|   DIGITE O VALOR A SER INSERIDO: |\n");
                printf("====================================\n\n");

                scanf("%d", &valor);
                raiz = Inserir(raiz, valor);

                printf("====================================\n");
                printf("|   DESEJA CONTINUAR INSERINDO?    |\n");
                printf("====================================\n");
                printf("|              1 - SIM             |\n");
                printf("|              2 - NAO             |\n");
                printf("====================================\n\n");

                scanf("%d", &op);
            } while (op == 1);
            break;

        case 2:
            do {
                int valor;
                printf("====================================\n");
                printf("|   DIGITE O VALOR A SER BUSCADO:  |\n");
                printf("====================================\n\n");

                scanf("%d", &valor);
                resultado = Buscar(raiz, valor);

                if (resultado != NULL) {
                    printf("====================================\n");
                    printf("|   VALOR %d ENCONTRADO NA ÁRVORE  |\n", resultado->dado);
                    printf("====================================\n\n");
                } else {
                    printf("====================================\n");
                    printf("|       VALOR NÃO ENCONTRADO       |\n");
                    printf("====================================\n\n");
                }

                printf("====================================\n");
                printf("|   DESEJA CONTINUAR BUSCANDO?    |\n");
                printf("====================================\n");
                printf("|              1 - SIM             |\n");
                printf("|              2 - NAO             |\n");
                printf("====================================\n\n");

                scanf("%d", &op);
            } while (op == 1);
            break;

        case 3:
            do {
                int valor;
                printf("====================================\n");
                printf("|   DIGITE O VALOR A SER REMOVIDO: |\n");
                printf("====================================\n\n");

                scanf("%d", &valor);
                t_no *temp = Remover(raiz, valor);

                if (temp != NULL) {
                    printf("====================================\n");
                    printf("|   VALOR %d REMOVIDO DA ÁRVORE    |\n", valor);
                    raiz = temp;  // Atualiza a raiz com a nova árvore
                } else {
                    printf("====================================\n");
                    printf("|       VALOR NÃO ENCONTRADO       |\n");
                    printf("====================================\n\n");
                }

                printf("====================================\n");
                printf("|   DESEJA CONTINUAR REMOVENDO?    |\n");
                printf("====================================\n");
                printf("|              1 - SIM             |\n");
                printf("|              2 - NAO             |\n");
                printf("====================================\n\n");

                scanf("%d", &op);
            } while (op == 1);
            break;

        case 4:
            printf("Saindo do programa...\n");
            break;

        default:
            printf("Opção inválida! Por favor, escolha novamente.\n");
            break;
        }

    } while (op != 4);

    LiberarArvore(raiz);
    printf("Memória da árvore liberada. Programa encerrado.\n");

    return 0;
}
```


Um painel básico de opções com loop para voltar ao menu ate escolher sair.

