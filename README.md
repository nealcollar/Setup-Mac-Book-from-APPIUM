# Configuração Mac
 
#### 1- Conhecimentos gerais

- Como acessar pasta root 
	- Pressione "Shift + Command + C" ou "Shift + Command + G" e digite "/" na caixa de busca e pressione "Return(enter)". 
	
- Acessar itens ocultos
	- Pressione "Shift + Command + . (ponto)"

- Criar .bash_profile
	- Digite no terminal o comando "touch .bash_profile" para criar o arquivo no diretorio "/Users/(UserName)"
	
- Edição de arquivos via terminal
	- Para editar o documento pode ser feito pelo comando "nano .bash_profile" ou por qualquer editor de codigo que prefira
	- Agora salve as alterações pressionando "Ctrl + o" e aperte "Return(enter)" para salvar. Então para sair do comando "nano" pressione "Ctrl + x"

#### 2- Baixar java JRE e JDK
* [Java Link](https://www.oracle.com/technetwork/pt/java/javase/downloads/index.html) - Versão recomendada java 1.8.0_221
 
#### 3- Configurar PATH (Java) .bash_profile 
* Abra o arquivo (.bash_profile) e digite os códigos a seguir: 

    ```
    export JAVA_HOME="/Library/Java/JavaVirtualMachines/jdk(version java).jdk/Contents/Home"
    export PATH="$PATH:$JAVA_HOME/bin"
    ```
    - Para adicionar esses PATHs siga os passos em [Conhecimentos gerais](#1--conhecimentos-gerais).

#### 4- Instalar Homebrew
* Copiar e colar no terminal: 
    ````
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    ````

#### 5- Instalar node
* Copiar e colar no terminal: 
    ````
    brew install node
    ````

#### 6- Instalar appium-doctor -g (global)
* Copiar e colar no terminal: 
    ````
    npm install -g appium-doctor
    ````

#### 7- Instalar Appium Desktop e command line
* [Appium Desktop](https://github.com/appium/appium-desktop/releases/download/v1.10.0/Appium-1.10.0.dmg) 
* Appium command line: 
    ````
    npm install –g appium@1.10.0
    ````

#### 8- Rodar appium-doctor  
* Resposta esperada:

    ````
    info AppiumDoctor ### Diagnostic for necessary dependencies starting ###
    info AppiumDoctor  ✔ The Node.js binary was found at: /usr/local/bin/node
    info AppiumDoctor  ✔ Node version is 12.8.0
    info AppiumDoctor  ✔ Xcode is installed at: /Applications/Xcode.app/Contents/Developer
    info AppiumDoctor  ✖ Xcode Command Line Tools are NOT installed
    info AppiumDoctor  ✔ DevToolsSecurity is enabled.
    info AppiumDoctor  ✔ The Authorization DB is set up properly.
    info AppiumDoctor  ✖ Carthage was NOT  found!
    info AppiumDoctor  ✔ HOME is set to: /Users/automacaoinmetrics
    WARN AppiumDoctor  ✖ ANDROID_HOME is NOT set!
    info AppiumDoctor  ✔ JAVA_HOME is set to: /Library/Java/JavaVirtualMachines/jdk1.8.0_221.jdk/Contents/Home
    WARN AppiumDoctor  ✖ adb could not be found because ANDROID_HOME is NOT set!
    WARN AppiumDoctor  ✖ android could not be found because ANDROID_HOME is NOT set!
    WARN AppiumDoctor  ✖ emulator could not be found because ANDROID_HOME is NOT set!
    info AppiumDoctor  ✔ Bin directory of $JAVA_HOME is set
    info AppiumDoctor ### Diagnostic for necessary dependencies completed, 6 fixes needed. ###
    ````

## Configuração para Android
 
#### 1- Baixar [Android Studio](https://developer.android.com/studio) 
 
#### 2- Inicializar e configurar Android Studio (SDK Manager)
* SDK platforms: Android 6 até mais atual. 
* SDK tools: Google webdriver, android emulator, android SDK platform-tools, android SDK tools, intel x86 emulator (HAXM).	
	
#### 3- Configurar PATH (Android Studio) .bash_profile
* Copiar e colar no arquivo (.bash_profile): 
    ````
    export ANDROID_HOME="/Users/(username)/Library/Android/sdk"
    export PATH="$PATH:$ANDROID_HOME/emulator"
    export PATH="$PATH:$ANDROID_HOME/platform-tools"
    export PATH="$PATH:$ANDROID_HOME/tools/bin"
    ````
    - Para adicionar esses PATHs siga os passos em [Conhecimentos gerais](#1--conhecimentos-gerais).

#### 4- Testar command line (adb, emulator)
* Copiar e colar no terminal: 
    ````
    adb
    emulator
    ````

#### 5- Testar Appium desktop
* Selecione alguns capability para o device da sua escolha (virtual ou real)
* Testar conexão appium e device
 
#### 6- Testar Appium command line (POC)
* Criar script de automação e teste no device da sua escolha (virtual ou real)
 
## Configuração para iPhone

#### 1- Instalar/Atualizar XCode via AppleStore

#### 2- Configurar usuário (Apple ID - Conta developer) no XCode
* Abrir XCode
* Pressione "Command + ,(virgula)" para abrir preferências do XCode
* Selecione a aba "Accounts" e pressione o "+" no canto inferior esquerdo da tela e adicione um Apple ID

#### 3- Habilitando configuração desenvolvedor command line
* Abrir XCode
* Pressione "Command + ,(virgula)" para abrir preferências do XCode
* Selecione a aba "Locations"
* No campo "Comand Line Tools" selecione a opção XCode

#### 4- Instalar Carthage
* Copiar e colar no terminal: 
    ````
    brew install carthage
    ````

#### 5- Instalar authorize-ios 
* Copiar e colar no terminal: 
    ````
    npm install -g authorize-ios
    ````

#### 6- Instalar iOS deploy 
* Copiar e colar no terminal: 
    ````
    brew install ios-deploy
    ````

#### 7- Instalar ideviceinstaller
* Copiar e colar no terminal: 
    ````
    brew install ideviceinstaller
    ````

#### 8- Instalar ios-webkit-debug-proxy
* Copiar e colar no terminal: 
    ````
    brew install ios-webkit-debug-proxy
    ````

#### 9- Rodar appium-doctor
* Resposta esperada

    ````
    info AppiumDoctor Appium Doctor v.1.11.1
    info AppiumDoctor ### Diagnostic for necessary dependencies starting ###
    info AppiumDoctor  ✔ The Node.js binary was found at: /usr/local/bin/node
    info AppiumDoctor  ✔ Node version is 12.8.0
    info AppiumDoctor  ✔ Xcode is installed at: /Applications/Xcode.app/Contents/Developer
    info AppiumDoctor  ✔ Xcode Command Line Tools are installed in: /Applications/Xcode.app/Contents/Developer
    info AppiumDoctor  ✔ DevToolsSecurity is enabled.
    info AppiumDoctor  ✔ The Authorization DB is set up properly.
    info AppiumDoctor  ✔ Carthage was found at: /usr/local/bin/carthage. Installed version is: 0.33.0
    info AppiumDoctor  ✔ HOME is set to: /Users/automacaoinmetrics
    info AppiumDoctor  ✔ ANDROID_HOME is set to: /Users/automacaoinmetrics/Library/Android/sdk
    info AppiumDoctor  ✔ JAVA_HOME is set to: /Library/Java/JavaVirtualMachines/jdk1.8.0_221.jdk/Contents/Home
    info AppiumDoctor  ✔ adb exists at: /Users/automacaoinmetrics/Library/Android/sdk/platform-tools/adb
    info AppiumDoctor  ✔ android exists at: /Users/automacaoinmetrics/Library/Android/sdk/tools/android
    info AppiumDoctor  ✔ emulator exists at: /Users/automacaoinmetrics/Library/Android/sdk/tools/emulator
    info AppiumDoctor  ✔ Bin directory of $JAVA_HOME is set
    info AppiumDoctor ### Diagnostic for necessary dependencies completed, no fix needed. ###
    info AppiumDoctor
    info AppiumDoctor ### Diagnostic for optional dependencies starting ###
    WARN AppiumDoctor  ✖ opencv4nodejs cannot be found.
    WARN AppiumDoctor  ✖ ffmpeg cannot be found
    WARN AppiumDoctor  ✖ mjpeg-consumer cannot be found.
    WARN AppiumDoctor  ✖ idb and idb_companion are not installed
    WARN AppiumDoctor  ✖ applesimutils cannot be found
    WARN AppiumDoctor  ✖ idevicelocation cannot be found
    info AppiumDoctor  ✔ ios-deploy is installed at: /usr/local/bin/ios-deploy. Installed version is: 1.9.4
    info AppiumDoctor  ✔ ios_webkit_debug_proxy is installed at: /usr/local/bin/ios_webkit_debug_proxy. Installed version is: 1.8.5, Built with libimobiledevice v1.2.0, libplist v2.0.0
    ````

#### 10- Habilitar modo desenvolvedor para o iPhone
* Conectar iPhone no Mac
* Abrir XCode
* Pressione "Command + ,(virgula)" para abrir preferências do XCode
* Selecione a aba "Server & Bots"
* Clicar no cadeado para habilitar mudanças (usuário:senha - administrador)
* Trocar botão Off para On
* Selecionar usuário da maquina logado

#### 11- Criar build do Webdriver
*  Verifique a existencia do arquivo "WebDriverAgent.xcodeproj",nos seguintes PATHs:
	
	- Appium Desktop: 
	````       
        /Applications/Appium.app/Contents/Resources/app/node_modules/appium/node_modules/appium-xcuitest-driver/WebDriverAgent
	ou 
	/Applications/Appium.app/Contents/Resources/app/node_modules/appium-xcuitest-driver/WebDriverAgent
	````
	
	- Appium command line:
	
	````       
	/usr/local/lib/node_modules/appium/node_modules/appium-xcuitest-driver/WebDriverAgent
	ou
        /usr/local/lib/node_modules/appium/node_modules/appium-webdriveragent
	````
	
	- Na falta do arquivo procure pelas pastas **`appium-webdriveragent` , `appium-xcuitest-driver`**:

* Após encontrar o arquivo siga os proximos passos:
    - Abra o terminal e digite essa lista de comandos:
        - Passo para Appium Desktop:
            
            ````       
            cd "PATH onde o arquivo foi encontrado"
            mkdir -p Resources/WebDriverAgent.bundle
            ./Scripts/bootstrap.sh -d
            ````

        - Passo para Appium (npm) command line:
        
            ````
            cd "PATH onde o arquivo foi encontrado"
            mkdir -p Resources/WebDriverAgent.bundle
            ./Scripts/bootstrap.sh -d
            ````
            
    - Abra o projeto no Xcode (WebDriverAgent.xcodeproj), após o projeto aberto clique no **WebDriverAgent**, ao clicar nele isso fará a janela dos **TARGETS** abrir, assim poderemos vizualizar alguns deles como `WebDriverAgentLib`, `WebDriverAgentRunner`, `IntegrationApp` repita os passos a seguir para todos os **TARGETS**:
        - No **TARGET** `WebDriverAgentLib` selecione a aba "General".
        - Dentro da aba "General" selecione o check-box para a função "**Automatically manage singin**".
        - Selecione o "**Team**" no qual você cadastrou no passo [Configuração do Apple ID](#2--configurar-usu%C3%A1rio-apple-id---conta-developer-no-xcode)
        
        ![Singin Webdriver](/images_for_readme/setup_webdriver_with_developer_acc.png)

    - No caso de conflito com o bundle ID existente, como na imagem a seguir:

        **Erro no bundle ID**![error_bundleid](/images_for_readme/falha_no_bundleid.png)

    - Mude para a aba "Build Settings" e procure o pela opção "Packaging" dentro dela procure o campo com o nome "Pruductor Bundle Identifier" e altere o nome do bundle.
        - Exemplo de bundle opcional: **com.inmetrics123.WebDriverAgentRunner**.

        **Mudando nome do bundle ID**![change_bundle_name](/images_for_readme/mundando_nome_do_bundleid.png)

    - Na repetição do mesmo erro repita os passos a cima para solucionar o problema.

* Agora vamos limpar o projeto e realizar o build:
    - Primeiro com o projeto aberto no xcode selecione o **Scheme** que deva realizar o build e o tipo do device que será montado.
    - Após a seleção pressione "Command + Shift + K" ou vá no menu "PRODUCT" e escolha a opção "CLEAN BUILD FOLDER" para limpar o projeto.
    - Agora pressione "Command + B" ou vá no menu "PRODUCT" e escolha a opção "BUILD" para realizar o build, as imagens a seguir mostram a resolução destes passos:

        **Campo para alterar Scheme**![campo de Scheme ](/image_for_readme/field_scheme_set.png)

        **Selecionando Scheme e device para BUILD**![seleção do scheme](/images_for_readme/set_scheme_and_device.png)

        **Clean BUILD folder**![clean build folder](/images_for_readme/clean_build_folder.png)

        **Realizando BUILD do projeto**![build project](/image_for_readme/build_project.png)
    
    - No caso do erro **"MESSAGING UNQUALIFIED ID"**, como na imagem a seguir:
        
        **Erro dado no XCode após BUILD**![error build xcode](/images_for_readme/error_missing_id.png)

    - Siga esses passos para resolver esse problema:
        - Click na aba "Show the Project Navigator".
        - Abra a pasta "Configuratios" e abra o arquivo "ProjectSettings.xcconfing".
        - Dentro do arquivo procure o item "GCC_TREAT_WARNINGS_AS_ERRORS" substitua o valor "YES" pelo valor "0".
        - Realize a "CLEAN BUILD FOLDER" e o "BUILD", como foi descrito nos itens a cima, segue as imagens com este fluxo.

            **Localizando e configurando arquivo .xcconfig**![find file in xcode](/images_for_readme/find_and_edit_xcconfing.png)

            **Erro resolvido**![error solved](/images_for_readme/error_soulved.png)



* Vamos verificar se as configurações foram relizadas com sucesso, para isso precisamos executar alguns comandos no terminal:
    - Primeiro conecte o celular (Iphone) no MAC-Book
    - Segundo abra o terminal e vá para o diretorio que deseja testar o WebDriverAgente.
        - Testando o Appium Desktop.
            
            ````
            cd "PATH onde o arquivo foi encontrado"
            xcodebuild -project WebDriverAgent.xcodeproj -scheme WebDriverAgentRunner -destination 'id=<udid>' test
            ````

        - Testando o Appium (npm) command line
        
            ````
            cd "PATH onde o arquivo foi encontrado"
            xcodebuild -project WebDriverAgent.xcodeproj -scheme WebDriverAgentRunner -destination 'id=<udid>' test
            ````
            
        - Lembrando o campo **'id=udid'**, você deve pegar o id do celular após conectado no MAC-Book.
            - Para pegar os dados do celular conectado abra o XCode e pressione "Command+SHIFT+2", isso fará abrir a janela de devices/simuladores
            - Se dirija a aba **"Devices"** e localize o seu device, caso haja mais de um device conectado.
            - Procure o campo com nome **"Identifier"** este id é o número que você precisa colocar no campo do comando.
            
            ![window_from_specs_device](/images_for_readme/janela_specs_device.png)

        - Resposta esperada após a execução do comando:
        
            ````
            Test Suite 'All tests' started at 2017-01-23 15:49:12.585
            Test Suite 'WebDriverAgentRunner.xctest' started at 2017-01-23 15:49:12.586
            Test Suite 'UITestingUITests' started at 2017-01-23 15:49:12.587
            Test Case '-[UITestingUITests testRunner]' started.
                t =     0.00s     Start Test at 2017-01-23 15:49:12.588
                t =     0.00s     Set Up
            ````
 
            - Para verificar se tudo ocorreu bem (lembrando o comando na aba anterior precisa estar em execução), abra outra aba no terminal e siga esses passos:
            
                ````
                export DEVICE_URL='http://<device IP>:8100'
                export JSON_HEADER='-H "Content-Type: application/json;charset=UTF-8, accept: application/json"'
                curl -X GET $JSON_HEADER $DEVICE_URL/status
                ````
            
                - Para pegar o **device IP** abra o celular e siga o caminho Ajustes=>Wi-Fi=>Rede atual conectada.
                - Quando executar o ultimo comando a seguinte resposta deve aparecer (lembrando que somente a estrutura deve parecer a mesma, não os resultados em cada campo) .
                    
                    ````
                    {
                      "value" : {
                        "state" : "success",
                        "os" : {
                          "name" : "iOS",
                          "version" : "12.4",
                          "sdkVersion" : "12.2"
                        },
                        "ios" : {
                          "simulatorVersion" : "12.4",
                          "ip" : "192.168.15.31"
                        },
                        "build" : {
                          "time" : "Aug 18 2019 11:25:25",
                          "productBundleIdentifier" : "com.facebook.WebDriverAgentRunner"
                        }
                      },
                      "sessionId" : "CBD5B219-90D6-45CD-A672-66E707916F85",
                      "status" : 0
                    }
                    ````
                    
    - **Lembrete, para cada usuário que for realizar automação deve ser feito este mesmo passo a passo da [inicialização do WebDriverAgent](#11--criar-build-do-webdriver)**
                
                
                
                
