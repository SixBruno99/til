**Técnicas de ataque**

Nota de esclarecimento: Este documento foi feito para documentar meus aprendizados durante a realização do curso “Uma abordagem prática do ZERO sobre técnicas e ferramentas utilizadas em ataques Hackers de DoS e DDoS com o Kali Linux” na Udemy do professor Clécius Wilton e tem fins única e exclusivamente educacionais.

    3-way handshake [SYN] -> [SYN, ACK] -> [ACK]

Para entender melhor, imagine que o cliente é você tentando acessar uma página na web, como o Facebook, e o servidor seria o provedor do Facebook.

O 3-way handshake consiste na forma que uma conexão é formada, primeiramente o cliente inicia a conexão com uma flag SYN para o servidor indicando que deseja estabelecer uma conexão. Segundamente o servidor, ao receber o pacote SYN, responde com um pacote contendo as flags SYN e ACK para confirmar que recebeu o SYN do cliente. Por último, o cliente recebe o pacote SYN, ACK e responde com um pacote ACK, confirmando que recebeu a resposta do servidor. Assim é feito a conexão do cliente e servidor.

**1- TCP SYN Flood**
**2- ICMP e UDP Flood**
**3- HTTP Flood**
**3.1- HTTP Slowloris**