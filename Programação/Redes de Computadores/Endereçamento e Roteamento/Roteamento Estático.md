
O **roteamento estático** é um método de roteamento no qual o administrador de rede configura manualmente as rotas que o tráfego deve seguir dentro de uma rede. Isso contrasta com o roteamento dinâmico, no qual os roteadores aprendem as rotas automaticamente através de protocolos de roteamento.

### Conceito de Roteamento Estático

No roteamento estático, o administrador de rede define explicitamente a rota pela qual um pacote deve viajar para alcançar um destino específico. Essas rotas são configuradas diretamente no roteador, e permanecem inalteradas até que o administrador as modifique manualmente.

Uma rota estática inclui:

- **Endereço de destino**: O endereço IP da rede de destino.
- **Máscara de rede**: Define o tamanho da rede de destino.
- **Gateway ou próximo salto**: O endereço IP do próximo roteador para o qual o pacote deve ser enviado.
- **Interface de saída**: A interface do roteador pela qual o pacote será enviado.

### Exemplo de Configuração de Rota Estática

Suponha que temos duas redes:

- **Rede 1**: 192.168.1.0/24 (com gateway 192.168.1.1)
- **Rede 2**: 192.168.2.0/24 (com gateway 192.168.2.1)

Para configurar uma rota estática que permite que os pacotes da Rede 1 alcancem a Rede 2, seria algo assim (em um roteador Cisco):

bash

Copiar código

`Router(config)# ip route 192.168.2.0 255.255.255.0 192.168.1.2`

Aqui, a rota estática instrui o roteador a enviar pacotes destinados à rede 192.168.2.0/24 através do próximo salto, que é o IP 192.168.1.2 (o gateway).

### Características do Roteamento Estático

1. **Manual**: O administrador é responsável por adicionar, remover ou modificar as rotas. Se houver mudanças na topologia da rede, como links caindo ou novos roteadores sendo adicionados, as rotas estáticas precisam ser ajustadas manualmente.
    
2. **Previsível e Simples**: Como as rotas são configuradas manualmente, o comportamento de roteamento é totalmente previsível, o que pode ser uma vantagem em redes pequenas ou com pouca variação.
    
3. **Baixo consumo de recursos**: Ao contrário do roteamento dinâmico, o roteamento estático não gera tráfego de controle adicional (como troca de informações de roteamento), e não consome recursos de CPU e memória do roteador para recalcular rotas.
    
4. **Sem adaptação automática**: Se um link falhar, o roteador não pode redirecionar automaticamente o tráfego para uma rota alternativa, a menos que uma rota de backup também tenha sido configurada manualmente.
    
5. **Escalabilidade limitada**: Em redes grandes ou dinâmicas, o roteamento estático pode se tornar difícil de gerenciar, pois a quantidade de rotas que precisam ser configuradas manualmente aumenta significativamente.
    

### Vantagens do Roteamento Estático

- **Simplicidade**: Em redes pequenas e estáveis, o roteamento estático é fácil de implementar e gerenciar.
- **Segurança**: O roteamento estático pode ser mais seguro porque os roteadores não divulgam ou compartilham informações de roteamento com outros dispositivos. Isso limita a exposição da topologia da rede.
- **Previsibilidade**: O comportamento do roteamento é exatamente como o administrador o configurou, sem surpresas causadas por algoritmos dinâmicos ou mudanças automáticas.

### Desvantagens do Roteamento Estático

- **Manutenção intensiva**: Qualquer alteração na rede (como links ou dispositivos novos) exige que o administrador atualize manualmente as rotas.
- **Falta de adaptação a falhas**: Se uma rota configurada falhar, o roteador não ajusta automaticamente a rota, levando à interrupção do tráfego até que uma nova rota seja configurada.
- **Escalabilidade limitada**: Em redes grandes ou dinâmicas, o roteamento estático pode se tornar impraticável, já que a quantidade de rotas e alterações necessárias pode ser esmagadora.

### Comparação com Roteamento Dinâmico

No **roteamento dinâmico**, roteadores utilizam protocolos de roteamento (como OSPF, RIP ou EIGRP) para trocar informações e aprender rotas automaticamente. Isso permite que a rede se adapte dinamicamente a falhas ou mudanças, recalculando novas rotas conforme necessário.

|**Roteamento Estático**|**Roteamento Dinâmico**|
|---|---|
|Rota configurada manualmente|Rota aprendida automaticamente por protocolos|
|Não se adapta automaticamente a falhas|Se adapta automaticamente a falhas e mudanças na topologia|
|Sem consumo adicional de CPU e memória|Exige recursos do roteador para calcular e manter rotas|
|Mais seguro (sem propagação de rotas)|Potencialmente menos seguro (divulgação de rotas)|
|Ideal para redes pequenas e estáveis|Ideal para redes grandes e dinâmicas|

### Quando Usar o Roteamento Estático?

1. **Redes Pequenas e Simples**: Em uma rede com poucas sub-redes ou roteadores, o roteamento estático é mais simples e eficiente.
2. **Cenários de Backup**: O roteamento estático pode ser usado como rota de backup em combinação com roteamento dinâmico. Em caso de falha de roteamento dinâmico, as rotas estáticas podem assumir.
3. **Controle Total**: Quando você deseja total controle sobre as rotas, especialmente para fins de segurança ou performance.

### Considerações Finais

O roteamento estático é uma ferramenta útil e eficaz em muitas situações, especialmente em redes pequenas ou onde a simplicidade e o controle são mais importantes do que a flexibilidade. No entanto, em redes maiores e mais dinâmicas, o roteamento dinâmico geralmente é preferível devido à sua capacidade de se adaptar automaticamente às mudanças.

4o