O **servidor DNS recursivo** é um servidor que atua como intermediário no processo de resolução de nomes de domínio. 

Sua principal função é receber consultas de clientes (como navegadores ou outros dispositivos) e fazer o trabalho de encontrar o endereço [[IP]] correspondente a um domínio, consultando outros servidores [[DNS]] até encontrar a resposta correta.

### Como funciona o servidor recursivo:

Quando você digita um endereço, como `www.example.com`, o processo de resolução DNS começa, e o servidor [[DNS]] recursivo realiza as seguintes etapas:

1. **Receber a Solicitação**: O seu dispositivo (cliente) envia uma solicitação DNS ao servidor recursivo para obter o endereço [[IP]] associado ao domínio (por exemplo, `www.example.com`).
    
2. **Verificar o Cache**: O servidor recursivo primeiro verifica se já tem a resposta armazenada em cache, resultado de uma consulta anterior. Se a resposta estiver em cache, ele retorna diretamente ao cliente sem precisar consultar outros servidores.
    
3. **Consultar o Servidor [[Raiz]]**: Se o servidor recursivo não tiver a resposta em cache, ele faz uma consulta a um **servidor [[Raiz]]**. Os servidores raiz não conhecem os endereços [[IP]] dos domínios, mas indicam qual servidor [[DNS]] de domínio de nível superior ([[TLD]]) deve ser consultado a seguir (por exemplo, o servidor responsável pelo `.com`).
    
4. **Consultar o Servidor [[TLD]]**: O servidor recursivo, em seguida, consulta o **servidor DNS do [[TLD]]** (como o servidor do `.com`, `.net`, `.org`, etc.), que informa qual servidor [[DNS]] é autoritativo para o domínio (por exemplo, o servidor autoritativo para `example.com`).
    
5. **Consultar o Servidor [[Autoritativo]]**: O servidor recursivo então consulta o **servidor [[Autoritativo]]** para o domínio, que é o servidor que possui a resposta final e pode fornecer o endereço [[IP]] do domínio solicitado (`www.example.com`).
    
6. **Responder ao Cliente**: Após receber a resposta do servidor autoritativo, o servidor recursivo retorna a resposta ao cliente (navegador, por exemplo) com o endereço [[IP]]. Agora, o cliente pode usar esse endereço para se conectar ao servidor de destino.
    
7. **Armazenamento em Cache**: O servidor recursivo normalmente armazena a resposta em seu cache por um determinado período (definido pelo **TTL - Time to Live**), de modo que, se uma solicitação semelhante for feita mais tarde, ele possa responder diretamente do cache, sem precisar refazer todo o processo de consulta.
    

### Exemplo de Resolução [[Recursiva.canvas|Recursiva]]:

Vamos dizer que você está acessando `www.example.com` pela primeira vez:

1. O navegador solicita o endereço [[IP]] de `www.example.com` ao servidor recursivo.
2. O servidor recursivo pergunta a um dos **servidores [[Raiz]]**: "Qual servidor [[TLD]] gerencia domínios `.com`?".
3. O servidor [[Raiz]] responde com a localização do **servidor [[TLD]]** para `.com`.
4. O servidor recursivo pergunta ao servidor [[TLD]] do `.com`: "Onde está o servidor autoritativo para `example.com`?".
5. O servidor [[TLD]] responde com o endereço do **servidor [[Autoritativo]]** para `example.com`.
6. O servidor recursivo consulta o servidor autoritativo: "Qual é o endereço [[IP]] de `www.example.com`?".
7. O servidor autoritativo responde com o endereço [[IP]] (por exemplo, `192.0.2.1`).
8. O servidor recursivo envia essa resposta de volta ao navegador, que agora pode se conectar ao site.

### Diferença entre Servidor Recursivo e Autoritativo:

- **Servidor Recursivo**: Não possui as informações por conta própria; ele atua como intermediário e faz consultas a outros servidores [[DNS]] (incluindo os autoritativos) até encontrar a resposta.
- **Servidor [[Autoritativo]]**: É o servidor que possui as informações definitivas sobre um domínio específico. Ele não faz consultas a outros servidores; apenas responde com base nos registros que mantém.

### Importância do Servidor Recursivo:

- **Eficiência**: O servidor recursivo simplifica o processo para o cliente (navegador ou dispositivo), fazendo todo o trabalho de buscar a resposta correta em diferentes servidores DNS.
- **Cache**: Ele armazena as respostas em cache por um tempo (definido pelo TTL), o que pode melhorar a velocidade das consultas subsequentes para domínios já consultados.
- **Intermediário**: O cliente só precisa fazer uma única consulta ao servidor recursivo, que cuida do restante do processo, mesmo que envolva várias consultas a diferentes servidores ([[Raiz]], [[TLD]], [[Autoritativo]]).

### Exemplo de Servidores Recursivos Públicos:

Alguns serviços de [[DNS]] público oferecem servidores [[DNS]] recursivos rápidos e confiáveis:

- **Google Public DNS**: `8.8.8.8` e `8.8.4.4`
- **Cloudflare DNS**: `1.1.1.1`
- **OpenDNS**: `208.67.222.222`

Esses servidores recursivos públicos são amplamente usados, pois oferecem baixa latência e boa segurança, além de resolver rapidamente nomes de domínio para usuários em todo o mundo.