**Modelo OSI**

***Physical***

- Padrões de cabos, cabo coaxial, fibras óticas, conector RJ45

- Codificação de dados (transforma a informação em bits)

- Informações tratados como bits

Data-Link (Enlace):

- Transmitir os dados

- Garante que os dados vão ser entregues sem erro

- Endereços físicos ou MAC address

- switches (encaminhamento)

- Informações tratados como frames

- Ethernet

***Network***

- Comunicação fim-a-fim

- Endereço lógico (IP)

- Roteadores que encaminham pacotes entre redes

- Conceito de melhor esforço

- Informações tratados como pacotes

- ICMP, IPv4, IPv6

***Transport***

- Controle de fluxo e confiabilidade de entrega dos dados

- Informações tratados como segmentos

- TCP e UDP

- TCP garante qualidade

- UDP garante velocidade

***Session***

- Iniciar e encerrar conexão entre hosts

- Sincroniza comunicação

- Registro de logs

- Informações tratados como dados

Presentation:

- Tradução dos dados para camada de aplicação

- Conversão de caracteres

- Informações tratados como dados

***Application***

- Mais próxima do usuário

- Prover serviços para as aplicações

- DNS, HTTP, FTP, SSH, SMTP, etc

- Protocolos associados às portas TCP e UDP (HTTP/80, DNS/53)

- Informações tratados como dados
