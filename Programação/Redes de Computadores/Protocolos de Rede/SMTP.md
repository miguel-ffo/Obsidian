#ProtocolosDeRede 

**SMTP (Simple Mail Transfer Protocol)** é um protocolo usado para enviar e-mails pela Internet. 

Ele é o padrão para o envio de mensagens de e-mail de um cliente (como um programa de e-mail) para um servidor de e-mail, e entre servidores de e-mail. 

O SMTP é um protocolo baseado em texto que facilita a transmissão de e-mails, especificando como os dados da mensagem devem ser formatados e enviados.

### Como o SMTP funciona:

1. **Cliente de E-mail para Servidor SMTP**:
    - Quando um usuário envia um e-mail através de um cliente (como Outlook, Gmail ou Thunderbird), o cliente se conecta ao servidor SMTP para entregar a mensagem.
2. **Servidor SMTP para Servidor de Destino**:
    - O servidor SMTP então roteia a mensagem para o servidor de e-mail do destinatário. 
    - Esse processo pode envolver vários servidores intermediários antes que o e-mail chegue ao destino correto.
1. **Entrega Final**:
    - O servidor SMTP de destino entrega o e-mail à caixa de correio do destinatário, onde ele pode ser acessado através de protocolos como **IMAP** ou **POP3**.

### Componentes principais:

- **Agente de Transferência de Mensagens (MTA)**: Um servidor que executa o protocolo SMTP para enviar ou retransmitir e-mails.
- **Agente de Envio de E-mails**: O software cliente, como o Outlook ou o Gmail, que se comunica com o servidor SMTP para enviar a mensagem.
- **Portas SMTP**:
    - **Porta 25**: Usada tradicionalmente para a comunicação entre servidores SMTP.
    - **Porta 587**: Usada para o envio de e-mails por clientes de e-mail.
    - **Porta 465**: Usada para SMTP com criptografia SSL/TLS.

### Funções do SMTP:

- **Envio de mensagens**: O SMTP é responsável por garantir que os e-mails sejam enviados do remetente para o servidor de e-mail e do servidor de e-mail para o destinatário correto.
- **Roteamento de e-mails**: Quando um e-mail precisa ser encaminhado entre vários servidores, o SMTP cuida do roteamento, garantindo que ele chegue ao servidor de destino.
- **Erro e Notificação**: Se houver problemas no envio (como um endereço de e-mail incorreto), o SMTP gera mensagens de erro ou "bounce" que retornam ao remetente.

### SMTP e Segurança:

O protocolo SMTP por si só não é criptografado, o que significa que as mensagens podem ser interceptadas se forem transmitidas em texto simples. Para melhorar a segurança, o SMTP geralmente é combinado com SSL ou **TLS**, usando o **SMTPS** (SMTP Secure) para criptografar a comunicação entre cliente e servidor.

### Limitações do SMTP:

- O SMTP foi projetado apenas para **enviar** e-mails, não para recebê-los. Para ler e-mails recebidos, é necessário usar outros protocolos, como **IMAP** ou **POP3**.
- **Autenticação fraca**: O SMTP original não tinha suporte nativo para autenticação, embora versões modernas, como **SMTP-AUTH**, exijam autenticação para envio de e-mails.

### Fluxo de um E-mail via SMTP:

1. O cliente de e-mail cria e formata a mensagem.
2. O cliente envia a mensagem para o servidor SMTP do remetente.
3. O servidor SMTP encaminha a mensagem para o servidor SMTP do destinatário.
4. O servidor de destino armazena a mensagem na caixa de correio do destinatário.
5. O destinatário usa um cliente de e-mail para baixar a mensagem via IMAP ou POP3.

SMTP é o backbone do envio de e-mails na Internet, garantindo que as mensagens sejam entregues de forma eficiente e confiável.