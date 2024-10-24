- **Função**: Combina as funcionalidades de `ping` e `traceroute`, mostrando tanto a rota quanto as estatísticas de perda de pacotes e latência em tempo real.
- **Como funciona**: Envia pacotes ICMP e mede o tempo e a perda de pacotes em cada salto até o destino.
- **Usos**:
    - Diagnosticar onde está ocorrendo perda de pacotes ou aumento de latência em uma rede.
    - Monitorar rotas de rede de forma contínua.
- **Comando básico**:

    `mtr google.com`