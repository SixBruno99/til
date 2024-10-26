**Linux**

Variações do Linux:

**Distribuições do Linux**: Elas são sistemas operacionais baseados no kernel Linux e projetados para diferentes finalidades e públicos. Por exemplo, o **Debian** é uma distribuição mãe, que serve de base para outras como **Ubuntu**, que por sua vez serve de base para **Linux Mint** e **Kali Linux**.

- A família **Debian** inclui o Ubuntu, Linux Mint, Kali, entre outros.

- A família **Red Hat** inclui o CentOS e Fedora.

- A família **Slackware** inclui o OpenSUSE.

`Debian -> Ubunto -> Linux Mint e Kali Linux`

`Red Hat -> CentOS e Fedora`

`Slackware -> Open Suse`

**Utilizando o Terminal**

**Navegação**

pwd - print working directory (mostra o caminho do diretório atual)

    ls - lista tudo no diretório atual

        -a - inclui entradas que o nome começa com ponto (arquivos ou diretórios ocultos)

        -l - lista em formato longo

        -h - com -l, é um sufixo de tamanho para facilitar a leitura

<br>

    cd - change directory

        . - diretório atual

        .. - diretório acima

        / - o diretório root ou a separação de diretórios

        ~ - home (cd sem nada vai para a home)

        - menos - volta para o diretório que anterior

<br>

    tree - mostra a árvore do diretório atual

        -d - diretórios

        -a - mostra arquivos ocultos

<br>

    cat - concatena e/ou mostra o conteúdo de um arquivo

        -n - enumera as linhas

<br>

    tail - lista as últimas linhas do arquivo

        -n - mostra a quantidade de linhas que for adicionado em NÚMERO.

        -f - continua assistindo o arquivo em busca de novos dados.

<br>

    wc - conta linhas, palavras e caracteres

        -l - linhas

        -m - caracteres

        -w - palavras

**Manipulando arquivos e diretórios**

    cp - copia arquivos ou diretórios

        -R - copia o diretório em modo recursivo

        mv - move arquivos ou diretórios (com mv você pode renomear arquivos ou diretórios)

<br>

    mkdir - cria um diretório (use aspas ou barra invertida para separar caracteres inválidos)

        -p - cria uma estrutura inteira sem gerar erros

        Obs.: você pode usar chaves para criar múltiplos sub-diretórios.

        Ex: mkdir pasta1/pasta2/{pasta2-1, pasta2-2, pasta2-3}/pasta3/{pasta3-1, pasta3-2,}

<br>

    rm - apaga arquivos e diretórios

        -R - modo recursivo para diretórios

        -f - modo forçado e silencioso

<br>

    touch - muda os tempos de acesso e modificação de um arquivo.
    Grande parte dos casos, usamos este comando para criar um arquivo vazio.
