#ProtocolosDeRede 

**DNS (Domain Name System)** é um sistema que traduz [[nomes de domínio]] legíveis por humanos (como `www.example.com`) em endereços IP (como `192.168.1.1`), que são usados pelos computadores para localizar e se comunicar com servidores na internet. 

O DNS atua como uma espécie de "catálogo telefônico" da internet, facilitando a navegação, já que é mais fácil lembrar um nome de domínio do que um endereço IP numérico.

### Como o DNS funciona:

Quando você digita um nome de domínio em seu navegador (por exemplo, `www.google.com`), o processo de resolução DNS acontece para converter esse nome em um endereço IP. Este é o fluxo básico:

1. **Requisição DNS**: O navegador envia uma consulta DNS para o **Resolver local**, que geralmente é mantido pelo seu provedor de internet (ISP).
2. **Cache Local**: O **Resolver DNS** verifica se o endereço já foi consultado recentemente e está armazenado em cache. Se estiver, ele retorna o endereço IP diretamente.
3. **Servidor DNS Recursivo**: Se o endereço não estiver em cache, o resolver local consulta o **servidor DNS recursivo**.
4. **Servidores Raiz (Root Servers)**: Se o servidor recursivo também não tiver a informação, ele envia a solicitação para um dos **servidores Raiz**, que direcionam a consulta para o servidor de domínio de nível superior (TLD), como `.com`, `.net`, etc.
5. **Servidor Autoritativo**: O servidor TLD encaminha a consulta ao **servidor autoritativo** do domínio, que conhece o endereço IP exato do servidor que hospeda o site em questão.
6. **Resposta DNS**: O servidor autoritativo retorna o endereço IP ao resolver local, que o envia ao navegador. O navegador então usa esse IP para se conectar ao servidor e carregar o site.

### Componentes principais do DNS:

1. **Domínios**:
    
    - **Domínio de nível superior (TLD)**: Os domínios de nível superior são as terminações dos endereços de site, como `.com`, `.org`, `.net`, e domínios específicos de países como `.br` (Brasil).
    - **Domínio de segundo nível (SLD)*: É o nome registrado pelo proprietário, como `google` em `google.com`.
    - **Subdomínios**: São divisões do nome de domínio principal, como `mail.google.com`, onde `mail` é o subdomínio de `google.com`.
2. **Servidores DNS**:
    
    - **Servidores Recursivos**: Recebem a solicitação do usuário e fazem o trabalho de buscar o endereço IP correspondente, consultando outros servidores DNS até encontrar a resposta.
    - **Servidores Raiz**: Existem 13 conjuntos de servidores raiz no mundo, que formam a base do sistema DNS e direcionam as consultas para os servidores de domínio de nível superior (TLDs).
    - **Servidores Autoritativo**: São os servidores finais que têm a resposta exata sobre qual é o endereço IP de um domínio.
3. **Resolver DNS**:
    
    - É o serviço responsável por iniciar e coordenar todo o processo de resolução de nomes. 
    
    - Geralmente, é o servidor DNS do seu provedor de internet que cumpre essa função, mas você pode usar servidores DNS públicos, como os do Google (`8.8.8.8`) ou Cloudflare (`1.1.1.1`).

### Registros DNS:

Os servidores DNS mantêm diferentes tipos de registros para fornecer as informações corretas sobre o domínio. Alguns tipos de registros comuns incluem:

- **A Record (Address Record)**: Associa um nome de domínio a um endereço IP (IPv4).
- **AAAA Record**: Associa um nome de domínio a um endereço IPv6.
- **CNAME (Canonical Name Record)**: Um alias para outro domínio. Por exemplo, `www.example.com` pode ser um CNAME para `example.com`.
- **MX Record (Mail Exchange Record)**: Especifica os servidores de e-mail para o domínio.
- **NS Record ([[Name Server]] Record)**: Indica quais servidores são autoritativos para aquele domínio.
- **TXT Record**: Contém texto arbitrário, usado para propósitos diversos como verificação de domínio e configurações de segurança.

### Cache DNS:

O cache é uma parte fundamental do sistema DNS. Quando um endereço IP é resolvido, ele pode ser armazenado em cache pelo servidor DNS recursivo ou até pelo navegador local por um período de tempo (definido pelo **TTL - Time to Live**). Isso ajuda a acelerar o acesso a sites já visitados, evitando a necessidade de resolver o nome de domínio a cada vez que um site é acessado.

### DNS e Segurança:

1. **DNSSEC (Domain Name System Security Extensions)**: DNSSEC adiciona verificações de segurança às consultas DNS, garantindo que as respostas não sejam alteradas ou interceptadas por atacantes. Ele usa assinaturas digitais para validar a autenticidade das respostas DNS.
2. **Ataques de DNS Spoofing/Poisoning**: Nesse tipo de ataque, os invasores manipulam a resolução DNS, fornecendo endereços IP falsos para redirecionar os usuários para sites maliciosos.

### DNS Público:

Alguns servidores DNS públicos são oferecidos por grandes empresas para fornecer resolução de nomes de domínio mais rápida e segura. Exemplos:

- **Google Public DNS**: `8.8.8.8` e `8.8.4.4`
- **Cloudflare DNS**: `1.1.1.1`
- **OpenDNS**: `208.67.222.222`

### Funções do DNS:

- **Facilitar o uso da internet**: O DNS permite que os usuários acessem sites usando nomes de domínio fáceis de lembrar, em vez de endereços IP numéricos.
- **Gerenciar serviços de rede**: Além de resolver nomes de domínio, o DNS também gerencia serviços como e-mails, através de registros MX, e redirecionamento de tráfego por meio de CNAMEs.

Em resumo, o DNS é um componente essencial da infraestrutura da internet, garantindo que os nomes de domínio legíveis sejam convertidos em endereços IP, permitindo a navegação fácil e eficiente na web.



Domain Name System (DNS)


---
### Para que serve?

Serve para a tradução de um nome (url) em um IP(Server).

Ex:  www.google.com.br  -> para 64.233.163.103

---
## Onde ele fica?

pode ficar no arquivo interno Hosts;
ou externamente; usando um sistema de nomes distribuídos:  [[DNS Externo.canvas|DNS Externo]]

Não é preciso um servidor DNS saber o nome de todos os outros servidores, apenas de um que sabe mais do que ele.

---
## Servidores DNS

[[Autoritativo]]

[[Raiz]]

[[TLD]]

[[SLD]]

[[Resolver]]

[[Requisitante]]

[[Recursivos]]

---
##  [[Url.canvas|Url]]

---
## Consulta ao DNS:

### [[Interativa.canvas|Interativa]]
### [[Recursiva.canvas|Recursiva]]

---

