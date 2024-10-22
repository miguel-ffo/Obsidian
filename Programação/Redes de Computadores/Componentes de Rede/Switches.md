#CompotentesDeRede 

**Switches** são dispositivos de rede que conectam múltiplos dispositivos dentro de uma mesma rede local (LAN), permitindo que eles se comuniquem entre si. 

Um switch opera na **camada 2 do Modelo OSI (Camada de Enlace)**, com base nos endereços MAC (Media Access Control), para encaminhar dados entre dispositivos conectados. Alguns switches mais avançados também operam na **camada 3 (Camada de Rede)**, utilizando endereços IP, oferecendo funções de roteamento.

### Funções e características principais dos switches:

1. **Comutação (Switching)**:
    
    - A principal função de um switch é **encaminhar dados** de forma inteligente, recebendo os pacotes de um dispositivo e enviando-os apenas para o destino correto. 
    - Isso é feito ao aprender os endereços MAC de cada dispositivo conectado às suas portas e criar uma tabela de endereços MAC.
1. **Tabela de Endereços MAC**:
    
    - O switch mantém uma tabela de endereços MAC, que associa cada dispositivo conectado (através do seu endereço MAC) a uma porta específica do switch. Quando um pacote chega, o switch consulta essa tabela para determinar para qual porta enviar o pacote, evitando o envio desnecessário para todas as portas.
3. **Full-Duplex e Half-Duplex**:
    
    - **Full-duplex**: A comunicação entre o switch e os dispositivos pode acontecer simultaneamente nos dois sentidos, o que aumenta a eficiência e a velocidade da rede.
    - **Half-duplex**: A comunicação ocorre em um único sentido de cada vez, o que pode resultar em colisões de pacotes em redes antigas.
4. **Redução de Colisões**:
    
    - Diferente de hubs, que enviam dados para todas as portas, os switches enviam os dados apenas para a porta de destino. Isso reduz significativamente as colisões de pacotes e melhora o desempenho da rede.
5. **VLANs (Virtual LANs)**:
    
    - Switches gerenciáveis permitem a configuração de **VLANs**, que segmentam fisicamente a rede em Sub-redes virtuais, permitindo maior controle e segurança. Dispositivos em diferentes VLANs não podem se comunicar diretamente, a menos que haja um roteador para encaminhar o tráfego entre elas.
6. **QoS (Qualidade de Serviço)**:
    
    - Switches avançados oferecem suporte a **QoS**, que prioriza certos tipos de tráfego (como voz ou vídeo) para garantir que dados sensíveis a atrasos tenham prioridade sobre tráfego menos crítico.

### Tipos de switches:

1. **Switches Não Gerenciáveis**:
    
    - São simples de usar, plug-and-play, e não requerem configuração. Eles são ideais para redes pequenas, onde não há necessidade de controlar ou monitorar o tráfego da rede.
2. **Switches Gerenciáveis**:
    
    - Permitem uma série de configurações e monitoramentos, como a criação de VLANs, ajustes de QoS, controle de portas, e visualização do tráfego da rede. São ideais para redes empresariais ou ambientes onde há a necessidade de otimização e segurança avançada.
3. **Switches de Camada 2 vs. Camada 3**:
    
    - **Switch de Camada 2**: Opera apenas com endereços MAC e faz comutação de pacotes com base nos endereços de hardware dos dispositivos.
    - **Switch de Camada 3 (Switch Roteador)**: Além de comutação, também oferece roteamento baseado em IP, permitindo que o tráfego seja encaminhado entre diferentes sub-redes dentro da LAN.

### Vantagens dos switches:

- **Melhora o desempenho da rede**: Ao encaminhar pacotes apenas para o dispositivo de destino correto, os switches minimizam o tráfego desnecessário na rede.
- **Maior segurança**: Com VLANs e outros recursos de controle, switches gerenciáveis oferecem mais segurança em comparação com Hubs ou switches não gerenciáveis.
- **Expansão da rede**: Permitem conectar vários dispositivos, ampliando a capacidade da rede local sem degradação significativa do desempenho.

### Casos de uso:

- **Redes Domésticas e Pequenos Escritórios**: Switches não gerenciáveis são frequentemente usados em redes pequenas para conectar PCs, impressoras e outros dispositivos de rede.
- **Redes Corporativas**: Switches gerenciáveis são usados para segmentar redes, configurar VLANs, e monitorar o tráfego em grandes redes empresariais, garantindo maior controle e desempenho.
- **Centros de Dados**: Em ambientes de grande escala, switches de alta capacidade são usados para gerenciar o tráfego entre servidores e dispositivos de armazenamento em alta velocidade.

Os switches desempenham um papel central nas redes locais, garantindo eficiência, escalabilidade e segurança ao interconectar dispositivos de rede.