#ProtocolosDeRede 

**FTPS (File Transfer Protocol Secure)** é uma extensão segura do protocolo **[[FTP]]** (File Transfer Protocol), que adiciona criptografia através de **[[SSL]] (Secure Sockets Layer)** ou **[[TLS]] (Transport Layer Security)** para proteger a transferência de arquivos entre um cliente e um servidor. 

O FTPS visa fornecer a mesma funcionalidade do [[FTP]], mas com maior segurança, garantindo que os dados transmitidos sejam protegidos contra interceptações e alterações.

### Como o FTPS funciona:

1. **Criptografia [[SSL]]/[[TLS]]**:
    
    - O FTPS usa [[SSL]] ou [[TLS]] para criptografar a comunicação entre o cliente e o servidor. Isso garante que os dados, incluindo senhas e arquivos, sejam transmitidos de forma segura, sem que possam ser lidos ou modificados por terceiros.
2. **Modos de Conexão no FTPS**:
    
    - **FTPS Explícito**: O cliente se conecta ao servidor [[FTP]] na porta padrão (geralmente a porta 21) e, em seguida, solicita a ativação da criptografia [[SSL]]/[[TLS]], elevando a sessão para uma conexão segura. Esse modo é preferido porque o cliente pode optar por não usar criptografia, se desejado.
    - **FTPS Implícito**: A criptografia é obrigatória desde o início. O cliente deve se conectar diretamente a uma porta segura (geralmente a porta 990) e a sessão começa criptografada desde o primeiro momento.
3. **Autenticação no FTPS**:
    
    - O FTPS permite a autenticação usando **certificados [[SSL]]/[[TLS]]**. Além da autenticação por nome de usuário e senha, o servidor pode usar certificados digitais para autenticar a identidade do cliente e vice-versa.

### Diferença entre FTPS e [[FTP]]:

- **[[FTP]]**: Protocolo de transferência de arquivos padrão, sem qualquer mecanismo de segurança integrado, enviando dados (incluindo credenciais de login) em texto simples.
- **FTPS**: Adiciona uma camada de segurança criptografada, protegendo as comunicações e os arquivos transferidos.

### Portas usadas pelo FTPS:

- **Porta 21**: Para o modo FTPS explícito, onde a conexão segura é iniciada por comando após o estabelecimento da conexão.
- **Porta 990**: Para o modo FTPS implícito, onde a criptografia é obrigatória desde o início da conexão.

### Benefícios do FTPS:

1. **Segurança Criptografada**: A criptografia SSL/TLS protege tanto os dados quanto as credenciais de login.
2. **Compatibilidade**: O FTPS é uma extensão do FTP padrão, o que significa que muitos servidores e clientes de FTP podem ser configurados para usar FTPS com alterações mínimas.
3. **Autenticação por Certificado**: Pode usar certificados digitais para garantir a autenticação e a segurança, além de métodos tradicionais como nome de usuário e senha.
4. **Conformidade**: FTPS ajuda a atender regulamentos de segurança, como os padrões PCI-DSS para transferência de dados em setores como o financeiro e o de saúde.

### FTPS vs SFTP:

- **FTPS**: É uma extensão do FTP e usa [[SSL]]/[[TLS]] para criptografia, mantendo a estrutura de portas múltiplas (21, 990, etc.).
- **[[SFTP]] ([[SSH]] File Transfer Protocol)**: É um protocolo completamente diferente que funciona sobre [[SSH]] (Secure Shell), utilizando uma única porta (geralmente a porta 22), e oferece criptografia nativa e mais simplicidade na configuração de firewall.

### Casos de Uso:

- **Transferência segura de arquivos**: Em ambientes corporativos e servidores de hospedagem, o FTPS é amplamente utilizado para mover grandes volumes de dados com segurança.
- **Conformidade com padrões de segurança**: Em setores regulamentados (financeiro, saúde), o FTPS é usado para proteger transferências de dados sensíveis.

FTPS é uma escolha robusta para transferências seguras de arquivos, proporcionando uma camada de proteção em ambientes onde o [[FTP]] tradicional seria inseguro.

4o