- **Função**: Mostra o caminho que um pacote percorre até o destino, revelando todos os roteadores intermediários.
- **Como funciona**: Envia pacotes ICMP com incrementos de TTL (time-to-live) e registra os roteadores pelos quais os pacotes passam.
- **Usos**:
    - Diagnosticar onde a conexão falha ao tentar alcançar um destino.
    - Identificar latência em cada salto na rede.
- **Comando básico**:

    `traceroute google.com`
    
    No Windows:
    
    `tracert google.com`