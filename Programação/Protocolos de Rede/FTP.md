#ProtocolosDeRede 

**FTP (File Transfer Protocol)** é um protocolo usado para transferir arquivos entre um cliente e um servidor através de uma rede, como a [[Internet]]. 

Ele permite que usuários enviem e recebam arquivos de forma eficiente e é um dos protocolos mais antigos de transferência de arquivos, ainda amplamente utilizado em diversos cenários.

### Como funciona o FTP:

1. **Cliente-Servidor**:
    
    - O FTP funciona em uma arquitetura cliente-servidor. O cliente é o dispositivo ou software que solicita os arquivos, enquanto o servidor é o dispositivo que armazena os arquivos e os fornece mediante solicitação.
2. **Conexões**:
    
    - O FTP usa duas conexões separadas para funcionar:
        - **Conexão de controle**: Estabelece a comunicação entre o cliente e o servidor para comandos e respostas.
        - **Conexão de dados**: Transfere os arquivos propriamente ditos entre o cliente e o servidor.
3. **Modos de Transferência**:
    
    - **Modo ativo**: O servidor inicia a conexão de dados com o cliente.
    - **Modo passivo**: O cliente inicia a conexão de dados com o servidor, sendo mais comum em redes protegidas por firewalls.

### Tipos de FTP:

1. **FTP anônimo**:
    - Permite que os usuários se conectem ao servidor sem a necessidade de uma conta ou senha específica. Comumente usado para disponibilizar arquivos publicamente.
2. **FTP autenticado**:
    - Exige um nome de usuário e senha para acessar os arquivos no servidor. É utilizado quando há controle sobre quem pode baixar ou enviar arquivos.

### Segurança:

O protocolo **FTP tradicional** não é seguro, pois transfere dados, incluindo senhas, em texto simples, tornando-os vulneráveis a interceptações. Por isso, existem variações mais seguras:

- **FTPS (FTP Secure)**: Adiciona uma camada de criptografia usando [[SSL]]/[[TLS]].
- **SFTP (SSH File Transfer Protocol)**: Um protocolo de transferência de arquivos seguro que funciona sobre o protocolo [[SSH]], garantindo a criptografia dos dados.

O FTP é utilizado principalmente em servidores de hospedagem de sites, ambientes corporativos e na transferência de arquivos em grandes volumes.
