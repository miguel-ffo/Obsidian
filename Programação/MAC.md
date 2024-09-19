

**MAC (Media Access Control)** é um termo que se refere a dois conceitos principais em redes de computadores:

### 1. **Endereço MAC**:

O **endereço MAC** é um identificador único atribuído a interfaces de rede de hardware, como placas de rede, [[Roteadores]] e [[Switches]]. 

É um endereço de 48 [[bits]] (6 [[bytes]]) geralmente representado em formato hexadecimal, por exemplo: `00:1A:2B:3C:4D:5E`. 

Esse endereço é atribuído pela fabricante do hardware e é utilizado para identificar de forma única cada dispositivo em uma rede local.

#### Funções e características do endereço MAC:

- **Identificação Única**: Cada dispositivo de rede tem um endereço MAC único, o que facilita a identificação e a comunicação entre dispositivos na mesma rede local.
- **Camada de Enlace**: O endereço MAC opera na **Camada 2 do [[Modelo OSI]]**, sendo responsável pela comunicação de dados dentro de uma rede local, como uma [[LAN]] (Local Area Network).
- **Estático**: Normalmente, o endereço MAC é fixo e não muda, sendo embutido no hardware da interface de rede. No entanto, em alguns casos, é possível alterar temporariamente o endereço MAC via software.
- **Tabela de Endereços MAC**: [[Switches]] de rede usam tabelas de endereços MAC para encaminhar pacotes de dados de forma eficiente, enviando-os apenas para a porta onde o dispositivo de destino está conectado.

### 2. **Protocolo de Controle de Acesso ao Meio (MAC)**:

O **protocolo de controle de acesso ao meio (MAC)** é um conjunto de regras e procedimentos que gerencia como os dados são transmitidos e acessados em um meio de comunicação compartilhado, como uma rede [[Ethernet]] ou[[ Wi-Fi]]. 

O protocolo MAC garante que múltiplos dispositivos possam compartilhar o mesmo meio de transmissão sem causar colisões ou interferências.

#### Funções e características do protocolo MAC:

- **Controle de Acesso**: Define como os dispositivos no mesmo segmento de rede podem acessar o meio físico para transmitir dados, evitando colisões e garantindo a eficiência da comunicação.
- **Métodos de Acesso**:
    - **CSMA/CD (Carrier Sense Multiple Access with Collision Detection)**: Usado em redes Ethernet, permite que os dispositivos verifiquem o meio para detectar se está ocupado antes de transmitir. Se duas transmissões colidirem, o protocolo lida com a retransmissão dos dados.
    - **CSMA/CA (Carrier Sense Multiple Access with Collision Avoidance)**: Usado em redes [[Wi-Fi]], tenta evitar colisões antecipadamente, aguardando períodos de espera e usando sinais de aviso antes de transmitir dados.
- **Detecção e Correção de Erros**: Alguns protocolos MAC incluem mecanismos para detectar e corrigir erros de transmissão, melhorando a integridade dos dados.

### Endereço MAC vs. [[IP]] Address:

- **Endereço MAC**:
    - **Nível de Operação**: Camada 2 (Enlace de Dados)
    - **Objetivo**: Identificar de forma única o hardware da interface de rede em uma rede local.
    - **Formato**: 48 [[bits]] (6 [[bytes]]), hexadecimal.
    - **Exemplo**: `00:1A:2B:3C:4D:5E`
- **Endereço IP**:
    - **Nível de Operação**: Camada 3 (Rede)
    - **Objetivo**: Identificar e localizar dispositivos em uma rede global, como a Internet.
    - **Formato**: IPv4 (32 bits, 4 octetos, como `192.168.1.1`) ou IPv6 (128 bits, 8 blocos de 16 [[bits]], como `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).

### Importância e Uso:

- **Endereço MAC**: Essencial para a comunicação em redes locais e é usado pelos switches para encaminhar pacotes. Ajuda a identificar dispositivos de forma única em uma [[LAN]].
- **Protocolo MAC**: Crucial para garantir uma comunicação eficiente e sem colisões em redes compartilhadas, seja [[Ethernet]] ou [[Wi-Fi]].

O conceito de MAC é fundamental tanto para a identificação de dispositivos em redes locais quanto para a gestão eficiente do acesso ao meio de transmissão em redes.