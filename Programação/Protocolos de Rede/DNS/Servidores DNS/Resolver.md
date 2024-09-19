O **resolver** (ou "resolutor [[DNS]]") é um componente fundamental no processo de resolução de nomes de domínio. É responsável por iniciar o processo de consulta [[DNS]] em nome de um cliente, como um navegador da web ou qualquer outro aplicativo que precise converter um nome de domínio (como `www.example.com`) em um endereço [[IP]].

### O que é o Resolver [[DNS]]?

O **resolver** é uma parte do software no sistema do cliente (ou dispositivo) que realiza as seguintes funções:

1. **Recebe a solicitação do cliente**: Quando um usuário tenta acessar um site ou recurso online, o aplicativo (como um navegador) envia uma solicitação ao resolver para descobrir o endereço [[IP]] correspondente ao nome de domínio.
    
2. **Inicia a consulta DNS**: O resolver envia a consulta ao servidor [[DNS]] configurado, que é normalmente um **servidor [[Recursivos]]**. O resolver pode estar configurado para se conectar a um servidor DNS [[Recursivos]] local, público (como o Google DNS ou Cloudflare DNS), ou o servidor [[Recursivos]] da rede do provedor de internet.
    
3. **Aguarda a resposta**: O resolver espera até que o servidor DNS [[Recursivos]] termine o processo de encontrar o endereço [[IP]] associado ao domínio solicitado. Quando o servidor recursivo retorna a resposta, o resolver a encaminha de volta para o aplicativo cliente (navegador ou outro).
    
4. **Entrega o IP ao cliente**: O resolver então devolve o endereço [[IP]] ao cliente, que pode usá-lo para se conectar ao servidor que hospeda o site ou serviço solicitado.
    

### Tipos de Resolvers:

Existem diferentes tipos de **resolvers** dependendo do papel que desempenham no processo de resolução DNS:

1. **Stub Resolver** (Resolver Básico):
    
    - Este é o tipo mais comum e é implementado na maioria dos dispositivos (como computadores e smartphones). Ele tem uma função simples: receber a solicitação de resolução de um nome de domínio e encaminhá-la a um servidor [[DNS]] recursivo configurado no sistema (geralmente através de configurações de rede).
    - Um **stub resolver** não faz consultas DNS diretamente aos servidores DNS [[Raiz]] ou autoritativos. Ele depende de um servidor DNS [[Recursivos]] para completar todo o processo de resolução.
2. **Full-Service Resolver** (Resolver Completo):
    
    - Um **resolver completo** é um servidor que realiza consultas recursivas em nome do cliente. Ele faz o trabalho de consultar os servidores DNS [[Raiz]], [[TLD]] e [[Autoritativo]] para obter a resposta final.
    - Um **resolver completo** é o que normalmente encontramos em servidores DNS [[Recursivos]], como os oferecidos por ISPs (provedores de serviços de [[Internet]]), ou serviços públicos de [[DNS]] como Google DNS (`8.8.8.8`) ou Cloudflare (`1.1.1.1`).

### Como Funciona o Resolver no Processo DNS:

Aqui está um exemplo simplificado do fluxo de trabalho com o **resolver**:

1. **Usuário solicita um site**: O navegador ou outro aplicativo tenta acessar `www.example.com`.
    
2. **Stub Resolver entra em ação**: O stub resolver no dispositivo do usuário recebe a solicitação e consulta o servidor DNS recursivo configurado (por exemplo, o servidor DNS do provedor de internet ou um DNS público como o Google DNS).
    
3. **Servidor DNS recursivo lida com o processo**: O servidor recursivo consulta, se necessário, os servidores raiz, TLD, e autoritativos até encontrar o endereço [[IP]] correto para `www.example.com`.
    
4. **Servidor DNS recursivo responde**: O servidor DNS [[Recursivos]] retorna o endereço IP encontrado para o stub resolver no dispositivo do usuário.
    
5. **Stub Resolver entrega o resultado**: O stub resolver então devolve o endereço IP ao navegador ou outro aplicativo, que pode agora usar o [[IP]] para acessar o site.
    

### Diferença entre Resolver e Servidor DNS Recursivo:

- **Resolver**: Refere-se ao componente no cliente (dispositivo ou aplicação) que inicia o processo de resolução [[DNS]]. Ele não faz as consultas diretamente aos servidores DNS raiz ou autoritativos, mas delega esse trabalho ao servidor DNS [[Recursivos]] configurado.
    
- **Servidor DNS Recursivo**: Este é o servidor que o resolver contata para buscar a resposta completa. O servidor [[Recursivos]] faz as consultas necessárias (possivelmente incluindo servidores [[Raiz]], [[TLD]] e [[Autoritativo]]) e retorna a resposta ao resolver.
    

### Resumo:

- O **resolver DNS** é o componente responsável por iniciar o processo de resolução DNS.
- O **stub resolver** (o tipo mais comum em dispositivos) envia consultas para servidores DNS recursivos.
- O **servidor [[Recursivos]]** realiza o trabalho completo de encontrar a resposta, consultando outros servidores DNS quando necessário.
  Em essência, o **resolver** é o ponto de partida no processo de tradução de nomes de domínio em endereços [[IP]], garantindo que os dispositivos possam se conectar corretamente aos recursos da internet.
---

