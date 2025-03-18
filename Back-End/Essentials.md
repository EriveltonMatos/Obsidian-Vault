
## **O que é IP?**

O **IP (Internet Protocol)** é um conjunto de regras que define como os dispositivos se comunicam na internet ou em redes locais. Ele é responsável pelo **endereçamento e roteamento** dos pacotes de dados, garantindo que as informações cheguem ao destino correto.

---

## **1. Endereço IP**

O **endereço IP** é um número único atribuído a cada dispositivo conectado a uma rede. Ele serve para identificar e permitir a comunicação entre computadores, servidores, roteadores e outros dispositivos na internet ou em redes locais.

### **Exemplos de endereços IP**

- IPv4: `192.168.1.1`
- IPv6: `2001:db8::ff00:42:8329`

Cada dispositivo conectado à internet possui pelo menos um endereço IP para poder enviar e receber informações.

---

## **2. Tipos de Endereço IP**

Os endereços IP podem ser classificados em diferentes categorias:

### **a) IPv4 e IPv6**

|Tipo|Características|
|---|---|
|**IPv4**|Endereços de 32 bits, representados por 4 números de 0 a 255 separados por pontos (exemplo: `192.168.0.1`). Possui um limite de **4,3 bilhões** de endereços, o que levou à criação do IPv6.|
|**IPv6**|Endereços de 128 bits, escritos em 8 grupos de números hexadecimais separados por dois pontos (exemplo: `2001:db8::ff00:42:8329`). Criado para resolver a escassez de endereços IPv4.|

### **b) Público e Privado**

| Tipo           | Descrição                                                                                                      |
| -------------- | -------------------------------------------------------------------------------------------------------------- |
| **IP Público** | É um endereço único na internet, fornecido pelo provedor de internet (ISP). Exemplo: `177.23.45.10`            |
| **IP Privado** | Usado dentro de redes locais (LANs). Não pode ser acessado diretamente pela internet. Exemplo: `192.168.1.100` |

Os endereços privados seguem essas faixas reservadas:

- **Classe A:** `10.0.0.0 – 10.255.255.255`
- **Classe B:** `172.16.0.0 – 172.31.255.255`
- **Classe C:** `192.168.0.0 – 192.168.255.255`

Dispositivos em redes locais usam **IPs privados** e se comunicam com a internet por meio de um **IP público compartilhado pelo roteador**.

### **c) Estático e Dinâmico**

| Tipo            | Descrição                                                                                                                              |
| --------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| **IP Estático** | Permanece fixo e não muda ao longo do tempo. Usado em servidores web e serviços que precisam de um IP constante.                       |
| **IP Dinâmico** | Atribuído automaticamente pelo provedor de internet e pode mudar periodicamente. Usado por usuários comuns para economia de endereços. |

---

## **3. Como Funciona o IP?**

Quando um dispositivo se conecta à internet, ele recebe um **endereço IP** atribuído pelo provedor de internet (ISP). Esse IP é usado para enviar e receber pacotes de dados.

### **Exemplo de comunicação usando IP**

1. Você digita `www.google.com` no navegador.
2. O computador consulta um **servidor DNS** para obter o **endereço IP do Google**.
3. Com o IP do Google, o navegador envia uma **requisição HTTP** para esse IP.
4. O servidor do Google responde com a página web, que é carregada no navegador.

O **IP garante que os pacotes de dados saibam para onde ir e como voltar**.

---

## **4. Roteamento de IP e Máscara de Sub-rede**

Os endereços IP são organizados em **redes** e **sub-redes** para facilitar o roteamento de dados.

- **Máscara de Sub-rede:** Define quais partes do IP representam a **rede** e quais representam o **dispositivo** dentro da rede.
    - Exemplo: `192.168.1.1/24`
    - Máscara: `255.255.255.0` → Indica que os primeiros 24 bits representam a rede.

**Exemplo de divisão de rede**

- `192.168.1.0/24` → Rede principal
- `192.168.1.1` → Roteador
- `192.168.1.10` → Computador
- `192.168.1.50` → Impressora

Dispositivos com o **mesmo prefixo de rede** podem se comunicar diretamente, enquanto dispositivos em redes diferentes precisam de um **roteador** para intermediar a comunicação.

---

## **5. NAT (Network Address Translation)**

O **NAT** permite que vários dispositivos em uma rede privada compartilhem um único IP público.

### **Como funciona?**

- Um **roteador** com IP público `177.23.45.10` recebe requisições de dispositivos internos (com IPs privados).
- O roteador modifica os pacotes, substituindo os IPs privados pelo **IP público**.
- Quando a resposta chega, o roteador encaminha os pacotes de volta para os dispositivos corretos.

O NAT é usado para **economizar endereços IPv4**, já que há um número limitado disponível.

---

## **6. Como Descobrir seu IP?**

### **IP Público**

- Você pode ver seu IP público acessando sites como [https://whatismyipaddress.com](https://whatismyipaddress.com)

### **IP Privado**

- No Windows, use o comando:
    
    nginx
    
    CopiarEditar
    
    `ipconfig`
    
- No Linux/macOS, use:
    
    nginx
    
    CopiarEditar
    
    `ifconfig`
    
    ou
    
    css
    
    CopiarEditar
    
    `ip a`
    

---

## **7. Diferença entre IP e DNS**

- O **IP** é o endereço numérico do dispositivo na rede.
- O **DNS (Domain Name System)** traduz **nomes de domínio** (`google.com`) para **endereços IP** (`142.250.184.238`), tornando a navegação mais fácil para os humanos.

---

## **Conclusão**

O **IP é essencial para a comunicação na internet**, pois identifica dispositivos e roteia pacotes de dados. Ele pode ser **IPv4 ou IPv6, público ou privado, dinâmico ou estático**. Além disso, tecnologias como **NAT, máscaras de sub-rede e DNS** ajudam a organizar e otimizar o uso dos endereços IP.
## **HTTP/HTTPS**

### **O que é HTTP?**

HTTP (Hypertext Transfer Protocol) é o protocolo de comunicação que permite a transferência de dados entre clientes (navegadores, aplicativos) e servidores na web. Ele define como as mensagens são formatadas e transmitidas, e como servidores e clientes devem responder a diferentes comandos.

### **O que é HTTPS?**

HTTPS (Hypertext Transfer Protocol Secure) é uma versão segura do HTTP que utiliza criptografia TLS (Transport Layer Security) ou SSL (Secure Sockets Layer) para proteger os dados transmitidos. Ele garante:

- **Confidencialidade** (dados criptografados, protegendo contra ataques de interceptação)
- **Integridade** (dados não são alterados durante a transmissão)
- **Autenticidade** (garantia de que o usuário está se comunicando com o servidor correto)

### **Métodos HTTP**

Os métodos HTTP, também chamados de verbos HTTP, definem a ação que será realizada em um recurso. Os principais são:

| Método     | Descrição                                                                                             |
| ---------- | ----------------------------------------------------------------------------------------------------- |
| **GET**    | Recupera dados de um servidor. Exemplo: Buscar uma lista de usuários.                                 |
| **POST**   | Envia dados para o servidor para criar um novo recurso. Exemplo: Criar um novo usuário.               |
| **PUT**    | Atualiza um recurso existente, substituindo seus dados. Exemplo: Atualizar os detalhes de um usuário. |
| **PATCH**  | Atualiza parcialmente um recurso existente. Exemplo: Alterar apenas o nome de um usuário.             |
| **DELETE** | Remove um recurso do servidor. Exemplo: Excluir um usuário.                                           |

### **Status Codes HTTP**

Os códigos de status HTTP indicam o resultado de uma requisição. Alguns exemplos:

- **200 OK** → Requisição bem-sucedida
- **201 Created** → Recurso criado com sucesso
- **204 No Content** → Requisição bem-sucedida, mas sem resposta (exemplo: DELETE)
- **400 Bad Request** → Erro no formato da requisição
- **401 Unauthorized** → Usuário não autenticado
- **403 Forbidden** → Usuário autenticado, mas sem permissão
- **404 Not Found** → Recurso não encontrado
- **500 Internal Server Error** → Erro no servidor

### **Headers HTTP**

Os headers (cabeçalhos) HTTP fornecem informações adicionais sobre a requisição ou resposta. Alguns exemplos:

- **Authorization**: Inclui credenciais de autenticação (exemplo: JWT)
- **Content-Type**: Indica o tipo de dado enviado/recebido (exemplo: `application/json`)
- **Accept**: Define quais formatos de resposta o cliente aceita (exemplo: `application/json`)
- **Cache-Control**: Controla o cache da resposta
- **User-Agent**: Indica o navegador ou aplicativo que fez a requisição

## **3. JSON e XML**

### **O que são?**

Tanto JSON quanto XML são formatos para troca de dados na web.

- **JSON (JavaScript Object Notation)**:
    - Leve, fácil de ler e escrever.
    - Utiliza pares **chave-valor**.
    - Muito usado em APIs REST.

Exemplo JSON:

json

CopiarEditar

`{   "id": 1,   "nome": "João",   "email": "joao@email.com" }`

- **XML (eXtensible Markup Language)**:
    - Mais verboso, baseado em tags.
    - Usado em algumas APIs antigas e serviços SOAP.

Exemplo XML:

xml

CopiarEditar

`<usuario>   <id>1</id>   <nome>João</nome>   <email>joao@email.com</email> </usuario>`

### **Diferença entre JSON e XML**

|Característica|JSON|XML|
|---|---|---|
|Sintaxe|Simples e compacta|Mais verbosa|
|Facilidade de leitura|Alta|Média|
|Suporte nativo|Sim (JavaScript)|Não (precisa de parser)|
|Uso|REST APIs, Web, Bancos NoSQL|SOAP, Configurações|

---

## **4. Autenticação e Autorização**

### **Autenticação vs Autorização**

- **Autenticação**: Verifica **quem** é o usuário (exemplo: login e senha).
- **Autorização**: Define **o que** o usuário pode acessar (exemplo: permissões de administrador).

### **Principais Métodos de Autenticação**

1. **Basic Auth**
    
    - Envia o `username:password` codificado em **Base64** no header `Authorization`.
    - Simples, mas inseguro sem HTTPS.
    
    Exemplo:
    
    makefile
    
    `Authorization: Basic dXNlcm5hbWU6cGFzc3dvcmQ=`
    
2. **JWT (JSON Web Token)**
    
    - Token compacto assinado digitalmente.
    - Contém informações do usuário e permissões.
    - Exemplo de um JWT decodificado:
        
        json
        
        CopiarEditar
        
        `{   "sub": "1234567890",   "name": "João",   "role": "admin",   "exp": 1719000000 }`
        
    - Usado em APIs RESTful para autenticação **stateless**.
    
    Exemplo de header:
    
    makefile
    
    CopiarEditar
    
    `Authorization: Bearer <token>`
    
3. **OAuth 2.0**
    
    - Protocolo de autenticação usado para permitir login via Google, Facebook, etc.
    - Usa **tokens de acesso** para autorização.
    - Fluxo comum:
        - O usuário faz login em um provedor (Google, Facebook).
        - A API recebe um **token de acesso** válido.
        - O token é enviado nas requisições para autenticação.
    
    Exemplo de requisição com token OAuth:
    
    makefile
    
    CopiarEditar
    
    `Authorization: Bearer <access_token>`