**3- HTTP Flood**

O ataque por HTTP (Hypertext Transfer Protocol) é feito através de requisições get para um determinado site que retorna um html, essas requisições levam algum tempo e ao fazer um flood pode haver uma sobrecarga do servidor.

Objetivo: esgotar os recursos do alvo (servidor - rede, cpu, ram, etc).

Não é necessário uma máquina mais “potente” do que a máquina do servidor para ser eficiente.

Fácil de ser detectado.

Para realizar o ataque a ferramenta “LOIC” foi utilizada para enviar várias requisições get para um determinado DNS ou IP.

Verificando o WireShark, uma ferramenta que mostra o tráfego de rede em tempo real, é possível ver a quantidade de requisições que estão sendo feitas.

Realizando o ataque em um IP de outra máquina virtual que gera um html, o Metasploitable,  é possível verificar o aumento de consumo da CPU.

Outra ferramenta utilizada é o apache benchmark, que por padrão já vem instalada no Kali Linux.

**Entrando em prática**

    ab --help mostra todos os comandos do apache benchmark.

- ab -c 100 -n 100000 -m get 192.168.200.8/mutillidae/

- -c 100 quantas conexões concorrentes diferentes (quantos requests serão feitos), ou seja, toda vez que eu fizer um request na verdade serão feitos 100 requests

- -n 100000 o número total de requisições que eu quero fazer

- -m get é o tipo de requisição que eu quero fazer, que no caso é o “get”

- 192\.168.200.8/mutillidae/ é o alvo do ataque

`Ao parar o comando ele mostra as estatísticas do teste.`

**3.1- HTTP Slowloris**

O HTTP Slowloris é um ataque de DoS que mantém conexões HTTP abertas com o servidor de destino sem completá-las, forçando o servidor a manter recursos ocupados por longos períodos. Ele é semelhante ao ataque SYN Flood no objetivo de esgotar os recursos do servidor, mas atua especificamente na camada de aplicação (HTTP).

**Como funciona**

O atacante inicia conexões HTTP enviando cabeçalhos de requisição incompletos e estende o máximo possível o tempo da conexão sem finalizá-la. O servidor fica aguardando indefinidamente o restante da requisição, o que o impede de liberar recursos para novas conexões.

O atacante estende ao máximo o tempo na conexão antes que ela seja fechada.

Nesse caso, o hardware do atacante necessita de ser maior que o hardware do atacado.

Ataque é mitigado na camada 7 (WAF).

A ferramenta NMAP é utilizada nesse caso.

**Entrando em prática**

`nmap –script http-slowloris --max-parallelism 400 192.168.200.8`

- --script http-slowloris é o script que vai ser utilizado

- --max-parallelism 400 quantidade de requisições simultâneas que serão feitas

- 192\.168.200.8 IP do servidor alvo

Nesse ataque usa-se menos requisições em relação a outros ataques de flood, mas, ao deixar as conexões abertas por longos períodos, ele tem um efeito similar de sobrecarga e lentidão para os usuários legítimos que tentam acessar o servidor.