#ProtocolosDeRede 

**TLS (Transport Layer Security)** é o sucessor mais seguro e atualizado do **SSL (Secure Sockets Layer)**. 

Ele é um protocolo criptográfico que fornece comunicação segura entre dispositivos conectados à Internet, protegendo a privacidade e a integridade dos dados durante a transmissão.

### Diferenças entre TLS e SSL:

- **TLS é mais seguro**: O TLS corrige várias vulnerabilidades que existiam nas versões anteriores do SSL (como SSL 2.0 e SSL 3.0).
- **Protocolos mais eficientes**: TLS implementa algoritmos criptográficos mais modernos e robustos.
- **Continuidade de nomenclatura**: Embora TLS seja tecnicamente diferente, muitas pessoas ainda chamam de "SSL" as conexões seguras na web.

### Como o TLS funciona:

1. **Handshake TLS**:
    
    - O processo de **handshake** é onde cliente e servidor estabelecem uma conexão segura. Durante o handshake:
        - O servidor apresenta seu certificado digital ao cliente, autenticando-se.
        - As chaves de criptografia são negociadas entre o cliente e o servidor para criar uma sessão segura.
2. **Certificados TLS**:
    
    - O servidor precisa de um **certificado digital** para iniciar a comunicação. Esse certificado é emitido por uma **Autoridade Certificadora (CA)** confiável e contém a chave pública que o cliente usará para criptografar os dados.
3. **Criptografia**:
    
    - O TLS utiliza **criptografia assimétrica** durante o handshake (com uma chave pública e uma chave privada) para estabelecer uma conexão.
    - Depois, usa **criptografia simétrica** para transmitir dados durante a sessão, já que é mais rápida.
1. **Autenticação**:
    
    - O TLS garante que o cliente esteja se comunicando com o servidor legítimo através do uso de certificados e da verificação de sua autenticidade.
5. **Integridade dos dados**:
    
    - O protocolo verifica que os dados enviados não foram alterados durante a transmissão. 
    - Isso é feito por meio de um "código de autenticação de mensagem" (MAC), que detecta qualquer modificação.

### Versões do TLS:

- As versões mais recentes do TLS (como **TLS 1.2** e **TLS 1.3**) oferecem melhorias significativas em relação à segurança e eficiência. A versão **TLS 1.3** é a mais atual e recomendada, sendo muito mais rápida e mais segura.

### Vantagens do TLS:

- **Segurança forte**: Protege as comunicações de espionagem, falsificação e alterações maliciosas.
- **Autenticação**: O cliente sabe que está se comunicando com o servidor correto.
- **Confidencialidade**: A comunicação é criptografada, impedindo que terceiros leiam os dados trocados.
- **Integridade**: Garantia de que os dados transmitidos não foram modificados.

### Uso do TLS:

- **HTTPs**: O protocolo TLS é o que torna o **HTTPs** (HTTP sobre TLS) seguro, sendo amplamente usado em sites para proteger transações financeiras, login de usuários e qualquer troca de informações sensíveis.
- **Outros protocolos**: Além do HTTP, o TLS pode ser usado com outros protocolos como **SMTP** (e-mails), **FTPS** (transferência de arquivos segura), **IMAP** e **POP3** (para e-mails).

TLS é essencial para garantir a segurança na Internet moderna, protegendo os usuários de uma ampla gama de ameaças cibernéticas.

