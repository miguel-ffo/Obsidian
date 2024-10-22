#ProtocolosDeRede 

**SSL (Secure Sockets Layer)** é um protocolo de segurança que cria uma conexão criptografada entre um servidor e um cliente (normalmente um site e um navegador) para garantir a privacidade e a integridade dos dados transmitidos. 

Ele protege a comunicação online, tornando-a segura contra interceptações ou modificações durante a transmissão.

### Como funciona o SSL:

1. **Criptografia**:
    - SSL usa criptografia para codificar os dados que são transmitidos entre o servidor e o cliente, impedindo que terceiros possam interceptar e ler essas informações.
2. **Certificado SSL**:
    - Para implementar SSL, um servidor precisa de um certificado SSL. Esse certificado é emitido por uma autoridade de certificação (CA), que verifica a autenticidade da identidade do servidor. Um certificado SSL contém a chave pública necessária para iniciar a conexão criptografada.
3. **Handshake SSL**:
    - Quando um cliente tenta se conectar a um servidor seguro, um processo chamado "handshake" SSL ocorre. 
    - Nele, o servidor e o cliente trocam informações de criptografia e autenticam-se antes que os dados sejam trocados.
1. **Chaves Pública e Privada**:
    - SSL usa uma combinação de criptografia simétrica e assimétrica:
        - **Criptografia assimétrica** (com chaves pública e privada): Para estabelecer a conexão inicial.
        - **Criptografia simétrica**: Para criptografar os dados reais durante a sessão, pois é mais rápida.

### Evolução para TLS:

O SSL foi amplamente substituído pelo **[[TLS]] (Transport Layer Security)**, uma versão mais segura e atualizada. As versões mais antigas do SSL (como SSL 2.0 e SSL 3.0) têm vulnerabilidades de segurança e não são mais recomendadas. 
No entanto, o termo "SSL" ainda é amplamente usado para se referir a criptografia em sites, mesmo quando o protocolo [[TLS]] está sendo usado.

### Como identificar SSL/TLS em sites:

- Quando você visita um site com SSL/[[TLS]] ativo, a [[Url.canvas|Url]] começa com **"https://"** (o "s" significa seguro).
- Navegadores também mostram um ícone de cadeado na barra de endereços ao visitar sites seguros.

### Benefícios:

- **Segurança de dados**: Impede que informações como senhas, dados bancários e dados pessoais sejam interceptadas.
- **Autenticação**: Garante que o usuário está se comunicando com o servidor legítimo.
- **Integridade dos dados**: Garante que as informações não sejam alteradas durante a transmissão.

SSL/[[TLS]] é fundamental para proteger transações online, como compras, acesso a contas e outras interações sensíveis na web.

