
As **árvores** são estruturas de dados hierárquicas amplamente utilizadas em computação. 

Elas organizam dados de forma que cada elemento (chamado **nó**) tem uma relação com outros elementos, criando uma estrutura de "parentesco" em que um nó pode ter nós filhos.

A árvores são uma das estruturas mais importantes devido à sua eficiência em operações como busca, inserção e remoção, especialmente quando comparadas com listas e arrays.

### Estrutura básica de uma árvore:

- **Raiz**: O nó no topo da árvore, sem um nó pai.
- **Nós**: Cada ponto de dados na árvore.
- **Filhos**: Nós que descendem de outro nó.
- **Pai**: O nó que precede os nós filhos.
- **Folha**: Um nó sem filhos.
- **Altura**: O comprimento do maior caminho da raiz até uma folha.
- **Profundidade**: O número de arestas do nó até a raiz.

### Tipos de árvores:

1. **Árvore binária**: Cada nó tem no máximo dois filhos, chamados de filho esquerdo e filho direito.
2. **[[Árvore binária de busca]] (BST - Binary Search Tree)**: Uma árvore binária onde, para cada nó, os valores no subárvore à esquerda são menores que o valor do nó, e os valores no subárvore à direita são maiores.
3. **Árvore balanceada**: Uma árvore onde a altura dos sub-árvores esquerda e direita de qualquer nó difere no máximo por uma constante, para evitar o pior caso de desempenho.
4. **Árvore AVL**: Uma árvore binária de busca balanceada automaticamente.
5. **Árvore B**: Usada principalmente em bancos de dados e sistemas de arquivos, é uma árvore que pode ter mais de dois filhos por nó, sendo balanceada para operações eficientes de leitura/escrita em grandes quantidades de dados.

### Operações em uma árvore binária de busca (BST):

1. **Inserção**:
    
    - Começa na raiz e, para cada nó, se o valor a ser inserido for menor que o valor do nó atual, move-se para o filho esquerdo; se for maior, move-se para o filho direito. A inserção ocorre quando se encontra um nó vazio (sem filho).
    - **Complexidade de tempo**: No caso médio, **O(log n)**, onde `n` é o número de nós. No pior caso (árvore degenerada, semelhante a uma lista), a complexidade é **O(n)**.
2. **Busca**:
    
    - Segue a mesma lógica da inserção, movendo-se para a esquerda ou direita dependendo se o valor procurado é menor ou maior que o nó atual.
    - **Complexidade de tempo**: No caso médio, **O(log n)**; no pior caso, **O(n)**.
3. **Remoção**:
    
    - Existem três casos para a remoção:
        - Nó sem filhos (folha): Apenas remova o nó.
        - Nó com um único filho: Substitua o nó pelo filho.
        - Nó com dois filhos: Substitua o nó pelo menor valor do subárvore à direita (ou o maior valor do subárvore à esquerda) e remova esse nó.
    - **Complexidade de tempo**: No caso médio, **O(log n)**; no pior caso, **O(n)**.
4. **Travessias de árvore**:
    
    - **Pré-ordem (Pre-order)**: Visita o nó atual antes de seus filhos.
    - **Em-ordem (In-order)**: Visita o nó esquerdo, depois o nó atual e depois o nó direito (em árvores binárias de busca, a travessia em-ordem resulta em uma lista ordenada dos elementos).
    - **Pós-ordem (Post-order)**: Visita os filhos antes do nó atual.

### Árvores balanceadas:

Em uma **árvore binária de busca não balanceada**, as operações podem se degenerar para **O(n)** no pior caso, semelhante a uma lista encadeada. Para evitar isso, existem árvores balanceadas que mantêm a altura baixa, garantindo eficiência nas operações.

- **Árvores AVL**: Após cada inserção ou remoção, a árvore verifica se está balanceada e realiza rotações para corrigir desequilíbrios, garantindo que a altura da árvore permaneça **O(log n)**.
- **Árvores rubro-negras (Red-Black Trees)**: Uma árvore binária de busca balanceada onde cada nó tem uma "cor" (vermelho ou preto), e um conjunto de regras garante que a altura seja balanceada, mantendo as operações em **O(log n)**.

### Aplicações de árvores:

- **Árvores binárias de busca**: Usadas para implementar conjuntos ordenados, mapas e dicionários.
- **Árvores de decisão**: Usadas em aprendizado de máquina para modelar decisões e suas possíveis consequências.
- **Árvores de prefixo (tries)**: Usadas em algoritmos de busca de strings, como autocompletar e dicionários de compressão de dados.
- **Árvores B**: Usadas em bancos de dados para indexação eficiente, permitindo operações rápidas em grandes volumes de dados.

### Comparação entre árvores e outras estruturas de dados:

- **Vs. Listas**: As árvores geralmente permitem operações de busca e inserção mais eficientes do que listas, que precisam ser percorridas sequencialmente.
- **Vs. Tabelas Hash**: As tabelas hash oferecem tempo constante para inserções e buscas, mas as árvores mantêm os elementos em ordem, o que é útil em aplicações onde se precisa de ordenação ou travessias em ordem.

### Complexidade geral em árvores binárias de busca (BST):

|Operação|Complexidade (caso médio)|Complexidade (pior caso)|
|---|---|---|
|Inserção|O(log n)|O(n)|
|Busca|O(log n)|O(n)|
|Remoção|O(log n)|O(n)|
|Travessia|O(n)|O(n)|

### Conclusão:

As árvores, especialmente as árvores binárias de busca e suas variantes balanceadas, são estruturas de dados poderosas e eficientes para armazenar, buscar e organizar dados.

Seu uso é comum em muitos algoritmos e sistemas, desde bancos de dados até inteligência artificial. 

A eficiência das árvores depende de como são mantidas balanceadas, sendo as árvores AVL e as árvores rubro-negras algumas das soluções para garantir operações eficientes.