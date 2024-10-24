#TecnologiasDeConexão 

Ethernet é a tecnologia de rede mais comum usada em redes locais (LAN - Local Area Networks). Ela define os protocolos de comunicação e as regras para dispositivos que desejam se comunicar dentro de uma rede. A Ethernet conecta dispositivos como computadores, switches, roteadores e servidores através de cabos, embora também possa ser aplicada em redes sem fio (Wi-Fi).

### Principais características do Ethernet:

1. **Velocidade**:
    
    - As redes Ethernet evoluíram ao longo do tempo e suportam diferentes velocidades de transmissão de dados. As velocidades mais comuns são:
        - **Ethernet tradicional**: 10 Mbps (Megabits por segundo).
        - **Fast Ethernet**: 100 Mbps.
        - **Gigabit Ethernet**: 1 Gbps (Gigabit por segundo).
        - **10 Gigabit Ethernet**: 10 Gbps.
    - Hoje, o Gigabit Ethernet é o mais amplamente usado em redes modernas.
2. **Topologia e Meio Físico**:
    
    - Ethernet geralmente utiliza uma topologia de estrela, onde os dispositivos estão conectados a um switch central. Isso permite comunicação eficiente entre os dispositivos conectados.
    - Ethernet usa cabos de cobre (como **cabo de par trançado** Cat5e, Cat6, etc.) ou cabos de fibra óptica para conectar dispositivos.
3. **Frame Ethernet**:
    
    - Os dados na Ethernet são transmitidos em "frames". Um frame Ethernet contém várias informações, como:
        - **Endereço de destino**: o endereço MAC (Media Access Control) do dispositivo de destino.
        - **Endereço de origem**: o endereço MAC do dispositivo de origem.
        - **Dados**: a carga útil, que são os dados reais sendo transmitidos.
        - **CRC**: um código para verificação de erros.
4. **Endereço MAC**:
    
    - Todo dispositivo conectado a uma rede Ethernet tem um identificador único chamado **endereço MAC** (Media Access Control). Esse endereço é atribuído à interface de rede de cada dispositivo e é usado para encaminhar pacotes de dados na rede.
5. **Switches e Roteadores**:
    
    - Em uma rede Ethernet, switches e roteadores são dispositivos cruciais:
        - **Switch**: Atua na camada de enlace de dados (camada 2), encaminhando pacotes de dados entre dispositivos dentro da mesma rede local com base nos endereços MAC.
        - **Roteador**: Atua na camada de rede (camada 3), encaminhando pacotes entre diferentes redes.
6. **Half-duplex e Full-duplex**:
    
    - Ethernet pode operar em modos **half-duplex** (envio e recebimento de dados não ocorrem ao mesmo tempo) ou **full-duplex** (envio e recebimento de dados simultâneos). Hoje, a maioria das redes opera em full-duplex.
7. **Detecção de Colisões**:
    
    - Nas primeiras versões da Ethernet, utilizava-se o método **CSMA/CD (Carrier Sense Multiple Access with Collision Detection)** para lidar com colisões quando dois dispositivos tentavam transmitir dados ao mesmo tempo. No entanto, isso é menos relevante em redes modernas com switches, que evitam colisões ao permitir transmissões dedicadas entre dispositivos.

### Evolução da Ethernet:

A Ethernet evoluiu para atender às demandas de redes mais rápidas e mais confiáveis. As principais tecnologias Ethernet incluem:

- **Fast Ethernet (100 Mbps)**: Introduzida para aumentar a velocidade de 10 Mbps para 100 Mbps.
- **Gigabit Ethernet (1 Gbps)**: Suporta 1 Gbps e é amplamente usada em redes corporativas e domésticas.
- **10 Gigabit Ethernet (10 Gbps)**: Suporta velocidades de 10 Gbps, utilizada principalmente em redes backbone e data centers.

### Vantagens da Ethernet:

- **Confiável e eficiente**: Ethernet é extremamente confiável e mantém a integridade dos dados durante a transmissão.
- **Altas velocidades**: Ethernet continua a evoluir para oferecer velocidades de transmissão mais altas.
- **Custo-benefício**: Componentes Ethernet são amplamente disponíveis e relativamente baratos.

### Desvantagens da Ethernet:

- **Distância limitada**: Os cabos de cobre Ethernet têm limitações de distância (100 metros em muitos casos). Em redes que exigem distâncias maiores, a fibra óptica é usada.
- **Mobilidade limitada**: Diferente de redes Wi-Fi, a Ethernet com fio limita a mobilidade, pois os dispositivos precisam estar fisicamente conectados à rede.