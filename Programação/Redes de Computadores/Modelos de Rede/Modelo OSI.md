#ModelosDeRede

O **modelo OSI** (Open Systems Interconnection) é um modelo de referência que descreve como diferentes sistemas de comunicação de rede devem interagir. 

Ele foi criado pela **ISO** (International Organization for Standardization) para padronizar a forma como dados são transmitidos entre dispositivos em uma rede. 

O modelo divide o processo de comunicação em **7 camadas**, cada uma com funções específicas e interdependentes.

### As 7 camadas do modelo OSI:

1. **Camada Física** (Layer 1):
    
    - Responsável pela transmissão física dos dados entre dispositivos.
    - Lida com a representação dos bits e a interface física (Cabos, ondas de rádio, conectores).
    - Exemplo: cabos de Fibra Óptica, sinais elétricos, repetidores.
2. **Camada de Enlace de Dados** (Layer 2):
    
    - Garante que os dados sejam transmitidos corretamente na camada física.
    - Organiza os dados em **frames** e corrige erros que podem ocorrer na camada física.
    - Exemplo: Switches, MAC (Media Access Control) addresses, Ethernet.
3. **Camada de Rede** (Layer 3):
    
    - Responsável pelo roteamento e endereçamento lógico (endereços IP).
    - Determina o caminho que os dados seguirão para chegar ao destino.
    - Exemplo: Roteadores, IP (Internet Protocol).
4. **Camada de Transporte** (Layer 4):
    
    - Garante a entrega confiável dos dados entre o remetente e o destinatário.
    - Controla a segmentação, reagrupamento, e verificação de erros dos dados.
    - Protocolo de controle de fluxo e controle de congestionamento.
    - Exemplo: TCP (Transmission Control Protocol), UDP (User Datagram Protocol).
5. **Camada de Sessão** (Layer 5):
    
    - Estabelece, gerencia e encerra as conexões (sessões) entre as aplicações.
    - Coordena o diálogo entre as máquinas e controla o intercâmbio de dados.
    - Exemplo: controle de sessões em chamadas VoIP.
6. **Camada de Apresentação** (Layer 6):
    
    - Traduz os dados entre os formatos da aplicação e o formato utilizado na rede.
    - Faz criptografia, compressão e conversão de dados (como transformar dados binários em caracteres legíveis).
    - Exemplo: SSL/TLS (Segurança de criptografia), conversão de formatos de arquivos (como JPEG, ASCII).
7. **Camada de Aplicação** (Layer 7):
    
    - Interface entre o usuário final e os serviços de rede.
    - Oferece serviços de rede diretamente às aplicações, como navegação na web, e-mail, transferência de arquivos, etc.
    - Exemplo: HTTP, FTP, SMTP, DNS.

### Funcionamento geral:

Os dados são transmitidos da camada superior (aplicação) até a inferior (física) no dispositivo de envio. 

Cada camada adiciona suas próprias informações (chamadas cabeçalhos) aos dados, até que a camada física transmita os bits pela rede. 

No dispositivo receptor, o processo é invertido: a camada física recebe os bits e, camada por camada, as informações são retiradas e os dados são entregues à aplicação final.

### Importância do modelo OSI:

- **Padronização**: O OSI padroniza a comunicação em rede, permitindo que dispositivos de diferentes fabricantes funcionem juntos.
- **Modularidade**: Ao dividir a comunicação em camadas, facilita o desenvolvimento, depuração e atualização de redes.
- **Isolamento de funções**: Cada camada tem uma função específica, o que torna a manutenção mais eficiente, já que alterações em uma camada não afetam as outras diretamente.

Embora o **modelo OSI** seja uma referência teórica, muitos protocolos de redes atuais, como a **pilha TCP IP**, seguem uma estrutura semelhante, mas com menos camadas.