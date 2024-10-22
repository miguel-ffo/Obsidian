Pilhas são uma estrutura de dados linear que segue o principio **LIFO (Last In, First Out)**.

Isso significa que o ultimo elemento inserido na pilha, será o primeira a ser removido.

### Características principais de uma pilha:

1. **Push:** Operação que insere um novo elemento no topo da pilha.
2. **Pop:** Operação que remove o elemento do topo da pilha.
3. **Peek:** Operação que permito visualizar o elemento do topo da pilha , sem removê-lo.

### Exemplo prático de uma pilha:

Imagine uma pilha de pratos, quando você coloca um novo prato ele vai para o topo, e quando você retira um prato, também é do podo que sai primeiro.

Esse comportamento é similar ao de uma pilha em ciência da computação.

### Aplicações de Pilhas:

- **Navegadores:** usam pilhas para armazenar o histórico de páginas visitadas. Quando você clica no botão "voltar", a página anterior é removida do topo da pilha.
- **Expressões matemáticas e compiladores:** Utilizam pilhas para avaliar as expressões ou verificar a correção de parênteses.
- **Funções recursivas:** Utilizam uma pilha de chamadas (call stack) para rastrear as funções que ainda precisam ser completadas.

### Implementação:

Pilhas podem ser implementadas usando arrays ou listas ligadas (linked lists).
A versão baseada em array tem tamanho fixo, enquanto a de lista ligada é mais flexível em termos de tamanho.

- **Pilhas baseadas em arrays**: Nesta implementação, o tamanho da pilha é limitado pela capacidade do array. Se o array estiver cheio, é necessário realocá-lo para um novo array maior, o que pode causar uma operação **O(n)** no pior caso (onde _n_ é o número de elementos na pilha). No entanto, fora essa realocação, as operações de push e pop continuam sendo **O(1)**.
- **Pilhas baseadas em listas ligadas**: Não há limitação de tamanho, já que a pilha pode crescer conforme a necessidade. Cada novo elemento é adicionado como um novo nó no topo da lista ligada. As operações de inserção (push) e remoção (pop) ainda têm complexidade **O(1)**, porque apenas o ponteiro para o topo precisa ser atualizado.
### Complexidade das operações em Pilhas:

1. **Push (inserir)**:
    
    - **Complexidade de tempo**: **O(1)** – A inserção de um elemento em uma pilha ocorre no topo, sendo uma operação direta que não requer movimentação de outros elementos, apenas a atualização de um ponteiro ou índice.
    - **Complexidade de espaço**: **O(n)** – O espaço total utilizado pela pilha é proporcional ao número de elementos armazenados, já que cada elemento ocupa espaço na memória.
2. **Pop (remover)**:
    
    - **Complexidade de tempo**: **O(1)** – A remoção de um elemento também acontece no topo da pilha, não havendo a necessidade de realocar ou mover outros elementos. Apenas o ponteiro ou índice do topo é ajustado.
    - **Complexidade de espaço**: A remoção em si não altera o uso de espaço na memória (o espaço já foi alocado para os elementos), mas conforme os elementos são removidos, o espaço utilizado pela pilha diminui.
3. **Peek (ou Top)**:
    
    - **Complexidade de tempo**: **O(1)** – O acesso ao elemento do topo da pilha é imediato, pois o topo está sempre sendo rastreado por um ponteiro ou índice.

### Pilhas com Arrays vs. Pilhas com Listas Ligadas:

- **Pilhas baseadas em arrays**:
    - **Push e Pop** são geralmente **O(1)**, mas se o array precisar ser realocado (quando ele enche e precisa ser expandido), o tempo de execução do `push` pode se tornar **O(n)** no pior caso, pois é necessário copiar todos os elementos para um novo array de tamanho maior.
- **Pilhas baseadas em listas ligadas**:
    - Como listas ligadas não têm uma limitação de tamanho fixa, as operações **push** e **pop** são sempre **O(1)**, e não há necessidade de realocação, tornando-a mais flexível em termos de tamanho, porém com um ligeiro aumento no uso de memória para armazenar ponteiros adicionais.

### Comparação:

- **Array**: Operações de inserção e remoção são rápidas, mas há o risco de estourar o tamanho do array, o que pode levar à necessidade de realocação, aumentando o tempo no pior caso.
- **Lista Ligada**: Garante **O(1)** para push e pop, sem a necessidade de realocação, mas consome mais memória para armazenar os ponteiros extras.
### Vantagens e desvantagens de pilhas:

- **Vantagens**:
    - Simplicidade: Pilhas são fáceis de implementar e têm um comportamento previsível.
    - Eficiência: Operações no topo da pilha são rápidas.
- **Desvantagens**:
    - Acesso restrito: Em uma pilha, você só pode acessar o elemento no topo, o que limita sua flexibilidade comparada a outras estruturas como listas ou filas, onde é possível acessar qualquer elemento.

### Exemplos de uso:

- **Recursão**: Pilhas são usadas para armazenar o estado de funções recursivas, permitindo que uma função volte ao ponto correto após uma chamada recursiva.
- **Conversão de expressões**: Pilhas são comumente usadas para converter entre diferentes tipos de notação matemática, como de **notação infixa** (onde o operador está entre os operandos) para **notação pós-fixa (postfix)** ou **notação polonesa reversa (RPN)**, onde o operador vem após os operandos.
- **Controle de fluxo**: Muitas linguagens de programação usam uma pilha de execução para rastrear funções e seus parâmetros durante a execução do programa.


