**1- TCP SYN Flood**

    sudo hping3 -S 192.168.200.4 -p 80 --faster

- 192\.168.200.4 -> IP configurado na rede das máquinas virtuais do seu laboratório (servidor alvo)

- 80 -> Porta de destino (geralmente usada para HTTP)

- --faster -> Envia pacotes de forma mais rápida

- sudo hping3 -S 192.168.200.4 – a 192.168.200.6 -p 80 –faster

- -a Troca o IP de origem que está sendo utilizado no ataque para o 192.168.200.6, que é o IP de outra máquina virtual no laboratório. Isso simula o ataque vindo de um IP diferente.

O objetivo desse ataque é sobrecarregar o servidor enviando múltiplas requisições SYN (primeira etapa do 3-way handshake) sem concluir o handshake. O servidor, ao receber muitas requisições, mantém as conexões abertas esperando pela última parte do processo, que é o pacote ACK, que nunca chega.

Com isso, o servidor esgota seus recursos (memória, portas, etc.) tentando gerenciar essas conexões incompletas, o que impede que novos clientes legítimos consigam completar o 3-way handshake e acessar o servidor, já que não recebem a flag ACK de volta.

