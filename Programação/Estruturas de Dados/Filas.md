Filas são uma estrutura de dados linear que segue o princípio **FIFO (First In, First Out)**. Isso significa que o primeiro elemento a ser inserido na fila será o primeiro a ser removido.

### Características principais de uma fila:

1. **Enqueue (inserir)**: Operação que adiciona um novo elemento no final (ou "traseira") da fila.
2. **Dequeue (remover)**: Operação que remove o elemento que está no início (ou "frente") da fila.
3. **Peek (ou Front)**: Operação que permite visualizar o elemento na frente da fila sem removê-lo.

### Exemplo prático de uma fila:

Imagine uma fila em um banco. A primeira pessoa que chega é a primeira a ser atendida. Outras pessoas que chegam vão para o fim da fila, aguardando sua vez.

### Implementações de fila:

- **Fila baseada em array**: A fila é implementada usando um array com dois ponteiros, um para o início (frente) e outro para o final (traseira). Porém, à medida que elementos são removidos da frente, o array pode ficar fragmentado, o que pode ser resolvido com a utilização de uma **fila circular**.
- **Fila baseada em lista ligada**: A fila é implementada com nós ligados onde há um ponteiro para o início e um para o final da fila. Quando um elemento é adicionado, ele é anexado ao final da lista, e quando removido, é retirado da frente.

### Fila Circular:

Uma fila circular é uma otimização da fila baseada em array. Em vez de mover todos os elementos após uma remoção, o índice do início da fila "circular" volta para o início do array quando atinge o final, reutilizando o espaço livre. Isso evita a necessidade de deslocar todos os elementos e melhora a eficiência.

### Complexidade de tempo:

- **Enqueue (inserir)**: **O(1)**, pois o novo elemento é sempre adicionado no final da fila.
- **Dequeue (remover)**: **O(1)**, pois o elemento é removido da frente da fila.
- **Peek (visualizar o primeiro)**: **O(1)**, já que acessa diretamente o primeiro elemento sem removê-lo.

Assim como em pilhas, essas operações têm um desempenho eficiente, porque envolvem apenas a atualização de ponteiros para o início ou final da fila, sem a necessidade de percorrer todos os elementos.

### Vantagens e desvantagens das filas:

- **Vantagens**:
    - Simples de implementar.
    - Operações rápidas de inserção e remoção com complexidade constante.
- **Desvantagens**:
    - Acesso restrito: Não é possível acessar diretamente qualquer elemento da fila, apenas o primeiro (frente) e o último (traseira).

### Aplicações de filas:

1. **Gerenciamento de tarefas (Job Scheduling)**: Fila é usada para armazenar processos ou tarefas que aguardam execução, como em sistemas operacionais onde tarefas são executadas em ordem de chegada.
2. **Fila de impressão**: Em uma fila de impressão, os documentos são processados na ordem em que foram enviados.
3. **Largura em primeiro (BFS - Breadth-First Search)**: Em algoritmos de busca em grafos, uma fila é usada para explorar os nós em camadas, processando-os em ordem de descoberta.
4. **Sistemas de atendimento**: Como em filas de espera em call centers, onde as chamadas são atendidas na ordem em que chegam.

### Fila de prioridade:

Embora uma fila padrão siga a ordem de chegada dos elementos, existem **filas de prioridade** que organizam os elementos de acordo com uma prioridade atribuída a cada um. 

O elemento com a maior prioridade é removido primeiro, mesmo que tenha sido adicionado após outros elementos.