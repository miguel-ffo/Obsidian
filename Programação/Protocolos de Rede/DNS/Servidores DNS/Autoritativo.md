Um **servidor DNS autoritativo** é um tipo de servidor que possui as informações definitivas e confiáveis sobre um domínio específico.

Ele é responsável por fornecer as respostas finais para as consultas [[DNS]] sobre esse domínio, como o endereço [[IP]] associado a um nome de domínio (por exemplo, `example.com`), entre outros registros, como registros MX (servidores de e-mail), CNAME (alias), e assim por diante.

### Funções do Servidor Autoritativo:

1. **Armazenamento de Registros DNS**: O servidor autoritativo contém os registros DNS de um domínio, como:
    
    - **A Record**: Associando o nome de domínio a um endereço [[IP]] (IPv4).
    - **AAAA Record**: Associando a um endereço [[IP]] (IPv6).
    - **MX Record**: Definindo os servidores de e-mail para o domínio.
    - **NS Record**: Definindo quais servidores são autoritativos para o domínio.
    - **CNAME**: Um alias para outro [[Nomes de Domínio]].
    - **TXT Record**: Usado para verificações e informações adicionais, como validação de e-mails (SPF, DKIM).
2. **Fornecer Respostas Autoritativas**: Quando uma consulta [[DNS]] chega a um servidor autoritativo, ele fornece uma resposta definitiva. Isso significa que ele tem as informações "originais" sobre o domínio, ao contrário de servidores recursivos que apenas buscam as informações em outros servidores.
    
3. **Gerenciamento do Domínio**: Um servidor autoritativo é mantido pelo responsável pelo domínio ou por um provedor de hospedagem [[DNS]], que gerencia as alterações e atualizações dos registros [[DNS]].
    

### Diferença entre Servidor Autoritativo e Servidor [[Recursivos]]:

- **Servidor DNS [[Recursivos]]**:
    
    - Atua como intermediário. Ele recebe a solicitação de resolução de um nome de domínio e faz consultas a outros servidores [[DNS]] (como os autoritativos) até encontrar a resposta.
    - **Não possui** as informações definitivas, ele apenas consulta os servidores corretos e retorna as respostas.
- **Servidor DNS Autoritativo**:
    
    - **Possui** as informações definitivas de um domínio e pode fornecer as respostas finais para consultas [[DNS]].
    - Não faz consultas a outros servidores; ele responde diretamente à consulta com base nas informações que possui.

### Exemplos de Operação:

1. **Quando um servidor recursivo consulta um servidor autoritativo**:
    
    - Imagine que você quer acessar `www.example.com`.
    - Seu provedor de internet envia a consulta a um **servidor DNS [[Recursivos]]**.
    - Se o servidor recursivo não tiver a resposta em cache, ele faz uma série de consultas, eventualmente chegando ao **servidor autoritativo** para `example.com`.
    - O servidor autoritativo responde com o endereço [[IP]] correspondente a `www.example.com`, e o servidor recursivo então passa essa resposta de volta para o seu navegador.
2. **Servidores DNS Primários e Secundários**:
    
    - Normalmente, cada domínio tem pelo menos dois servidores DNS autoritativos: um **primário** (ou master) e um **secundário** (ou slave), para garantir redundância e confiabilidade. O servidor primário é onde as alterações nos registros DNS são feitas, e o servidor secundário é uma cópia de backup.

### Exemplo de uso na prática:

- Se você registrar um domínio como `meusite.com`, o provedor onde você registrou o domínio ou onde o site está hospedado manterá servidores autoritativos que armazenarão os registros [[DNS]] de `meusite.com`.

- Esses servidores são os responsáveis por responder consultas como "Qual o endereço [[IP]] de `www.meusite.com`?".

### Importância:

- **Precisão**: Um servidor autoritativo tem as informações mais atualizadas e precisas sobre um domínio.
- **Respostas Finais**: Ele fornece respostas finais e definitivas, enquanto servidores recursivos ou intermediários só retransmitem a resposta.

Os servidores autoritativos são fundamentais para garantir a resolução correta e confiável dos domínios na internet.
