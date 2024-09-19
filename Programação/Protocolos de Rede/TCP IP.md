#ProtocolosDeRede 

O **TCP/IP** (Transmission Control Protocol/Internet Protocol) é um conjunto de protocolos de comunicação que permite a interconexão de sistemas em rede, como a [[Internet]]. 

Ele define como os dados são transmitidos entre dispositivos diferentes, garantindo que a comunicação seja confiável e eficiente.

### Estrutura do TCP/IP:


1. **Camada de Aplicação**:
    
    - Interage com o software e os usuários para fornecer serviços de rede, como navegação na web ([[HTTP]]), transferência de arquivos (FTP), e-mails (SMTP), entre outros.
2. **Camada de Transporte**:
    
    - **TCP (Transmission Control Protocol)**: Garante que os dados sejam entregues de forma confiável e na ordem correta. Ele estabelece conexões entre os dispositivos, gerencia o controle de fluxo e verifica se os dados chegaram sem erros.
    - **UDP (User Datagram Protocol)**: É um protocolo mais simples que envia dados sem garantir a confiabilidade ou ordem, mas é mais rápido, sendo usado em transmissões ao vivo e jogos online.
3. **Camada de Rede**:
    
    - [[IP]] (Internet Protocol)**: É responsável por endereçar e encaminhar os pacotes de dados entre dispositivos na rede. Existem duas versões principais do IP: **IPv4** e **IPv6**.
4. **Camada de Enlace**:
    
    - Gerencia a transmissão de dados em uma rede local, lidando com o acesso ao meio físico, como cabos ou redes sem fio, e controlando a entrega de pacotes dentro de uma rede.

### Funcionamento:

Quando você envia dados pela rede (como uma mensagem ou arquivo), esses dados são divididos em pacotes. O TCP/IP define como esses pacotes devem ser formatados, endereçados, transmitidos, roteados e recebidos, garantindo que eles cheguem ao destino correto e possam ser reagrupados para reconstruir os dados originais.

O modelo TCP/IP é a base da Internet e de muitas redes modernas, permitindo a interoperabilidade entre diferentes dispositivos e sistemas.

