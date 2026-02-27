# Como configurar/instalar/usar o `boot-repair` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `boot-repair` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings for configuring/installing/using the `boot-repair` on `Linux Ubuntu`._


## Descrição [2]

### `boot-repair`

`Boot-Repair` é uma ferramenta de diagnóstico e reparo de inicialização para sistemas operacionais baseados em `Linux`, como `Ubuntu`. Ele ajuda a resolver uma variedade de problemas de inicialização, incluindo a recuperação do gerenciador de inicialização `GRUB`, reparo de partições corrompidas e configuração de opções de inicialização avançadas. Com uma _interface_ intuitiva e procedimentos automatizados, o `Boot-Repair` torna mais fácil para os usuários resolverem problemas de inicialização e restaurarem seus sistemas operacionais em caso de falhas.


## 1. Como configurar/instalar/usar o `boot-repair` no `Linux Ubuntu` [1][3]

Para configurar/instalar/usar o `boot-repair` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
    ```bash
    sudo apt clean
    ```

    2.2 Remover pacotes `.deb` antigos ou duplicados do `cache` local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:
    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:
    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt update
    ```

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes:
    ```bash
    sudo apt --fix-broken install
    ```

    2.6 Limpar o `cache` do gerenciador de pacotes `apt` novamente:
    ```bash
    sudo apt clean
    ```

    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt list --upgradable
    ```

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt full-upgrade -y
    ```

Para instalar o `boot-repair` no `Linux Ubuntu` através do `Terminal Emulator`, você pode seguir os seguintes passos. O `boot-repair` é uma ferramenta útil para corrigir problemas de inicialização do sistema, especialmente útil quando você está lidando com problemas relacionados ao `GRUB`.

1. **Adicione o repositório do `Boot Repair`**: Antes de instalar o `boot-repair`, você precisa adicionar o repositório PPA (Personal Package Archive) que contém o pacote. No `Terminal Emulator`, digite o seguinte comando:

    ```bash
    sudo add-apt-repository ppa:yannubuntu/boot-repair
    ```

2. **Atualize a lista de pacotes**: Após adicionar o repositório, atualize a lista de pacotes para incluir os novos pacotes disponíveis no repositório que você acabou de adicionar. Execute:

    ```bash
    sudo apt update -y
    ```

3. **Instale o `Boot Repair`**: Agora, instale o `boot-repair` usando o comando:

    ```bash
    sudo apt install boot-repair -y
    ```

4. **Inicie o `Boot Repair`**: Uma vez instalado, você pode iniciar o `boot-repair` diretamente do `Terminal Emulator` com o comando:

    ```bash
    boot-repair
    ```

    4.1 Depois de iniciar, o `boot-repair` vai oferecer algumas opções através de uma interface gráfica para corrigir problemas comuns de boot. Geralmente, selecionar a opção `"Recommended repair"` resolve a maioria dos problemas de inicialização.

Se você precisar usar a ferramenta novamente no futuro, ela estará instalada no seu sistema e poderá ser acessada através do terminal ou do menu de aplicações.

### 2. Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `boot-repair` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Digite o seguinte comando e pressione `Enter`:

    ```bash
    sudo apt clean
    sudo apt autoclean -y
    sudo apt autoremove -y
    sudo apt update -y
    sudo apt uptoremove -y
    sudo apt autoclean -y
    sudo add-apt-repository ppa:yannubuntu/boot-repair
    sudo apt update -y
    sudo apt install boot-repair -y 
    boot-repair
    ```


## Referências

[1] OPENAI. ***Instalar o `boot repair` no `linux ubuntu` pelo `terminal emulator`.*** Disponível em: <https://chat.openai.com/c/83c3d966-b8d6-47a6-851a-0b6cac3018e8> (texto adaptado). Acessado em: 18/04/2023 17:11.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 18/04/2024 17:10.

