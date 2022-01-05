# Ambiente de Trabalho para IOS

## Dependências

-   Para configurar o ambiente iOS no macOS, iremos realizar 6 instalações principais:

    -   Homebrew;
    -   Node.js 14 (LTS);
    -   Watchman;
    -   CocoaPods;
    -   Xcode.
    -   VScode

    > Nota: Não será realizada a instalação global do react-native-cli pois ela tem causado erros. Para criar e executar nossos projetos React Native, utilizaremos os comandos via npx

-   Instalando Homebrew

    -   O Homebrew é um gerenciador de pacotes para OS X muito famoso e útil. Vamos instalá-lo em nosso sistema como seguinte comando:

    ```
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```

-   Instalando Node 14 (LTS) e Watchman

    -   Com o Homebrew instalado, vamos instalar o Node 14 (LTS) e o Watchman:

    > Nota: Se você já tiver o Node.js instalado em sua máquina, certifique-se que sua versão é a 12 ou mais recente.

    ```
    brew install node@14 watchman
    ```

-   Após a instalação do Node, precisamos adicionar o seu caminha a nossa variável ambiente PATH. Procure pelo primeiro dos seguintes arquivos existentes no seu sistema: ~/.zshrc ou ~/.bashrc, e adicione essas linhas no arquivo (de preferência no final):

    > Nota: Se nenhum desses arquivos existir, crie o ~/.bashrc caso utilize o Shell padrão ou ~/.zshrc caso utilize o ZSH.

    ```
    export PATH=$PATH:/usr/local/opt/node@14/bin
    ```

-   Após a instalação, verifique se ela foi realizada com sucesso com os comandos (execute um de cada vez):

    ```
    node -v
    ```

    ```
    npm -v
    ```

-   CocoaPods

    -   CocoaPods é um gerenciador de dependências que precisaremos instalar para que nossos projetos React Native funcionem corretamente. Execute o seguinte comando no seu terminal:

    ```
    sudo gem install cocoapods
    ```

-   Xcode

    -   A equipe do React Native recomenda que a versão mínima do XCode utilizada seja a 12 para garantir que não ocorram erros. Caso não consiga atualizar sua versão por ter um SO antigo e tenha muitos problemas com os projetos iOS, recomendamos que utilize o Android

    > Xcode é uma ferramenta gratuita desenvolvida pela Apple e essencial nos projetos React Native para iOS, visto que é a partir dela que temos acesso a SDKs e Simuladores de diversos dispositivos Apple.

    -   Para baixar, basta acessar a Mac App Store, buscar por Xcode e clicar no botão de Download.

    -   Após Download, entre no Xcode, faça login com seu ID.

    -   Entre em Preferencias, Components e faça download do iOS simulator.

-   VScode

    -   Faça Download do aplicativo clicando [aqui](https://code.visualstudio.com/sha/download?build=stable&os=darwin-universal)

    -   Abra o arquivo baixado.

    -   Siga os passos da instalação normalmente e finalize

    -   Arraste o arquivo baixado para a barra de aplicativos

-   Executando app no Simulador

    -   Para esse passo é preciso que você já tenha criado o seu projeto react native. Caso não tenha criado ainda, você pode criar com o comando npx react-native init nomedoprojeto

    -   Com o projeto criado, abra um terminal, vá até a pasta do projeto e digite:

        ```
        npm install
        ```

    -   Apos instalar as dependencias, entre dentro da pasta iOS (Dentro do Projeto) e digite:

        ```
        pod install
        ```

    -   Com o projeto criado, abra o terminal, navegue até a pasta e digite:

        ```
        react-native run-ios
        ```
