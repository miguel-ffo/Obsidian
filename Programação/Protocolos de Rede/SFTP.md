#ProtocolosDeRede 

**SFTP ([[SSH]] File Transfer Protocol)** é um protocolo de transferência de arquivos que funciona sobre o protocolo **[[SSH]] (Secure Shell)**, proporcionando uma maneira segura de enviar, receber e gerenciar arquivos entre sistemas remotos. 

Diferente do **[[FTP]]** e do **[[FTPS]]**, o SFTP não usa várias portas nem precisa de um canal separado para criptografia, pois é nativamente seguro devido ao uso do [[SSH]].

### Como o SFTP funciona:

1. **Baseado em [[SSH]]**:
    
    - O SFTP opera sobre o protocolo [[SSH]] (geralmente na **porta 22**), o que significa que ele já possui criptografia integrada e oferece uma camada de proteção tanto para os dados transferidos quanto para as credenciais (nome de usuário e senha).
2. **Autenticação**:
    
    - O SFTP utiliza métodos de autenticação do [[SSH]], que incluem nome de usuário/senha e autenticação baseada em **chaves públicas**. Com chaves públicas, o cliente e o servidor trocam chaves criptográficas para autenticação, dispensando a necessidade de senha.
3. **Criptografia**:
    
    - Todo o tráfego entre o cliente e o servidor é criptografado usando criptografia simétrica (geralmente AES) e assimétrica (RSA, DSA, etc.). Isso protege os dados de interceptação e alteração enquanto são transmitidos pela rede.

### Benefícios do SFTP:

1. **Segurança Nativa**:
    
    - Como o SFTP funciona sobre [[SSH]], a criptografia é ativada por padrão para proteger a confidencialidade e a integridade dos dados. Isso é uma vantagem significativa em comparação ao **[[FTP]]**, que transmite dados em texto simples.
2. **Simplicidade de Configuração**:
    
    - Diferente do [[FTPS]], que requer a abertura de várias portas para comunicação, o SFTP usa apenas a **porta 22** para todas as operações, facilitando a configuração de firewalls e aumentando a segurança.
3. **Transferência de Arquivos e Gerenciamento**:
    
    - Além de transferir arquivos, o SFTP permite gerenciar arquivos remotamente (listar diretórios, remover arquivos, alterar permissões, etc.), fornecendo uma solução completa para administração remota de arquivos.
4. **Firewall Amigável**:
    
    - Com o SFTP, como toda a comunicação ocorre pela porta 22 (a mesma usada pelo [[SSH]]), ele é muito mais fácil de configurar em ambientes onde a segurança de rede é uma preocupação, pois não requer múltiplas portas.

### Diferença entre SFTP, [[FTP]] e [[FTPS]]:

- **[[FTP]]**: Envia dados e credenciais em texto simples, sem criptografia, e usa portas diferentes para controle e dados.
- **[[FTPS]]**: Adiciona criptografia via [[SSL]]/[[TLS]] ao [[FTP]], mas ainda depende de múltiplas portas (portas 21, 990, etc.).
- **SFTP**: É um protocolo diferente que opera sobre [[SSH]], oferecendo segurança nativa e simplicidade ao usar uma única porta (porta 22).

### Vantagens do SFTP:

- **Segurança robusta**: Todo o tráfego é criptografado, protegendo tanto os arquivos quanto as credenciais.
- **Autenticação flexível**: Oferece suporte tanto para autenticação por senha quanto por chaves públicas, tornando-o mais seguro.
- **Simplicidade operacional**: A transferência de dados e o gerenciamento de arquivos ocorrem na mesma conexão, facilitando a administração e o uso.

### SFTP vs [[SCP]]:

- **SFTP**: Fornece transferência segura de arquivos, além de comandos adicionais para manipulação e gerenciamento de arquivos remotamente.
- **[[SCP]] (Secure Copy Protocol)**: Também usa [[SSH]] para transferir arquivos de forma segura, mas é mais limitado em funcionalidade, pois apenas transfere arquivos sem oferecer os recursos de gerenciamento de arquivos do SFTP.

### Casos de Uso:

- **Hospedagem de Arquivos**: O SFTP é amplamente usado em servidores de hospedagem de arquivos para mover e gerenciar dados com segurança.
- **Administração de Sistemas**: Admins de sistemas usam SFTP para transferir e gerenciar arquivos de forma segura entre servidores e clientes.
- **Compliance**: Organizações que precisam cumprir regulamentações de privacidade e segurança de dados (como PCI-DSS e HIPAA) usam SFTP para proteger transferências de arquivos sensíveis.

Em resumo, o SFTP é a escolha ideal quando é necessária uma solução de transferência de arquivos segura e fácil de configurar, graças ao seu suporte nativo ao [[SSH]] e criptografia forte.

4o