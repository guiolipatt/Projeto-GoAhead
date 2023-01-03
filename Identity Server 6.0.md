# Identity Server 6.0
# Configuração rápida
Siga as etapas abaixo para configurar e instalar o WSO2 Identity Server (WSO2 IS) em seu computador em tempo hábil.

- Informação:
    Para obter instruções detalhadas sobre outras opções de instalação e implantações, consulte o [guia de instalação](https://is.docs.wso2.com/en/latest/deploy/get-started/install/).

# Instalar o WSO2 IS
Siga os passos abaixo.

1. Faça o download e instale o Oracle Java SE Development Kit (JDK) versão 11 ou 17.
2. Vá para o site oficial do [WSO2 Identity Server](https://wso2.com/br/identity-server/) e clique em Começar.
3. Instale o WSO2 Identity Server baixando a VERSÃO BINÁRIA MAIS RECENTE.

- Informação: O local de instalação do WSO2 Identity Server é conhecido como .<IS_HOME>

# Configurar o servidor
Abra o arquivo (armazenado na pasta) e adicione a seguinte configuração para habilitar o CORS: **deployment.toml<IS_HOME>/repository/conf**

    [cors]
    allow_generic_http_requests = true
    allow_any_origin = true
    supported_methods = [
    "POST",
    "HEAD",
    "OPTIONS"
    ]
    supports_credentials = false
    max_age = 3600
    tag_requests = false

# Iniciar WSO2 IS
Para iniciar o WSO2 IS, abra um terminal, navegue até a pasta e execute um dos seguintes comandos no **<IS_HOME>/bin**

- No Linux/MacOS

        sh wso2server.sh
- No Windows

        wso2server.bat

Observe que o seguinte log aparece no prompt de comando quando o servidor é iniciado:

![1](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-start-server.png)

- Desligando o servidor: Para desligar o servidor, pressione . Observe que o log a seguir aparece no prompt de comando no desligamento do servidor com Ctrl + C.

    ![2](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-stop-server.png)

# Cenário de exemplo
Você pode experimentar facilmente os recursos de gerenciamento de identidade e acesso (IAM) no WSO2 Identity Server (WSO2 IS) usando o cenário explicado abaixo.

# Sobre o cenário de exemplo
Pickup é uma empresa de táxi que tem muitos funcionários que usam diferentes credenciais para entrar em diferentes aplicativos corporativos internos. A Pickup registrará seus usuários e aplicativos no WSO2 Identity Server para atender aos requisitos do IAM.

![3](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-overall-scenario.png)

A seguir estão duas dessas aplicações:

|Despacho de Recolha|Este aplicativo ajuda a gerenciar as operações gerais na Pickup.|
|:-:|:-:|
|Gerente de Coleta|	Esta aplicação ajuda a alocar veículos para os motoristas.|

A seguir estão três usuários na empresa:

|Rowan|	O gerente de RH da empresa que definirá os requisitos de acesso da empresa.|
|:-:|:-:|
Cameron	|Um gerente sênior que precisa entrar e usar os dois aplicativos acima.|
Alex|	Um gerente júnior que também precisa entrar e usar os dois aplicativos acima.|

# Requisitos
Listados abaixo estão os requisitos organizacionais que são abordados pelo WSO2 Identity Server.

- Os funcionários precisam se lembrar de várias credenciais ao fazer login nos muitos aplicativos do Pickup. É necessário unificar logins para funcionários com logon único para que os funcionários só tenham que se lembrar de uma única senha.

    **Experimente o logon único.**

- Os logins de funcionários devem ser protegidos, dificultando o acesso de fontes não autorizadas aos aplicativos. Portanto, é necessário aplicar uma camada adicional de segurança usando a autenticação multifator.

    **Experimente a autenticação multifator.**

- Os consultores externos precisam trabalhar em aplicativos de coleta temporariamente. É um incômodo criar e excluir contas para eles no banco de dados. Portanto, é necessário efetuar login com suas contas em um provedor de identidade externo usando autenticação federada.

    **Experimente a autenticação federada.**

- Com a expansão da Pickup, Rowan está tendo dificuldade em criar contas para cada funcionário que ingressa na organização. Permita que novos funcionários criem suas próprias contas para acelerar o processo usando o recurso de auto-inscrição.
  
    **Experimente a auto-inscrição.**

# Configurar os aplicativos de exemplo
Para experimentar os cenários de gerenciamento de identidade e acesso em sua instância de WSO2 IS, você precisa configurar os aplicativos para teste necessários ao seu WSO2 IS.

- Antes de começar

    Abra o arquivo e adicione a seguinte entrada:/etc/hosts

        127.0.0.1        localhost.com

- Se você estiver planejando usar o logon único (SSO), não use o **localhost**, pois isso causará o problema de host naked no Tomcat. Em vez disso, use **localhost.com**. Se você estiver usando o Windows, **localhost.com** é considerado como 127.0.0.1 .

- Certifique-se de que esta é a única entrada disponível para este endereço IP no arquivo **/etc/hosts** para evitar conflitos.

- [Baixe](https://curl.haxx.se/download.html) e instale o curl. Certifique-se de instalar o arquivo de tipo binário para sua versão.

# Siga os passos abaixo.

1. Baixe os exemplos do [GitHub](https://github.com/wso2/samples-is/releases/download/v4.5.2/is-samples-distribution.zip) e descompacte.

    unzip is-samples-distribution.zip

   - Informação: A pasta raiz da distribuição de amostras é chamada de **<IS_SAMPLE_DISTR>** .

2. Abra o arquivo **server.properties** na pasta **<IS_SAMPLE_DISTR>/IS-QSG/** e configure **wso2is.host.domain** e **wso2is.host.port** da seguinte maneira:

        #localhost.com is used to resolve naked hostname validation issue
        wso2is.host.domain=localhost.com
        wso2is.host.port=9443
        server.host.domain=localhost.com
        server.host.port=8080

3. Para configurar e executar os aplicativos de exemplo, abra um terminal, navegue até a pasta **<IS_SAMPLE_DISTR>/IS-QSG/bin** e siga as etapas abaixo: 

    - Execute um dos seguintes comandos para iniciar o aplicativo de exemplo:

        No Linux/MacOS

            sh app-server.sh

        No Windows

            app-server.bat

   - Execute o comando a seguir para iniciar os exemplos de início rápido de acordo.

        No Linux/MacOS

            sh qsg.sh

        No Windows

            qsg.bat

4. Quando solicitado, confirme as configurações.

# O que vem a seguir?
Depois de concluir a configuração dos exemplos, você verá a seguinte lista de cenários:
![4](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-sso.png)

# Logon único
Siga as instruções dadas para experimentar o logon único.

# Cenário de problema
Quando o número de aplicativos que são usados no Pickup aumenta, o os funcionários têm que manter mais credenciais. Isso não é escalável.

Portanto, o Pickup decide usar o logon único (SSO) para superar essa situação. Com o SSO, quando um usuário entra em um aplicativo, o usuário é conectado automaticamente a outros aplicativos, eliminando a necessidade de manter várias credenciais.

# Pré-requisitos
Siga as [instruções de configuração rápida](https://is.docs.wso2.com/en/latest/get-started/sample-use-cases/set-up/) para instalar e iniciar o WSO2 Identity Server.

# Experimente o SSO com SAML 2.0
Se os dois aplicativos estiverem usando SAML 2.0 como protocolo de autenticação, siga os passos abaixo.

# Executar o cenário de exemplo
Primeiro, vamos configurar e executar os aplicativos de exemplo.

1. Siga as instruções sobre como [configurar](https://is.docs.wso2.com/en/latest/get-started/sample-use-cases/sample-scenario/#set-up-the-sample-apps) os exemplos.

- Informação: Uma mensagem é exibida para escolher um cenário.
![5](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-sso.png)

2. Insira **1** como o número do cenário no prompt de comando.

- A execução do cenário 1 faz o seguinte:
  1. Cria os dois usuários: Cameron e Alex.
  2. Cria e atribui a função de usuário de Gerente a Cameron.
  3. Cria provedores de serviços para **Pickup Dispatch** e **Pickup Manager**.
  4. Configura o SSO da Web SAML2 para aplicativos Pickup-Dispatch e Pickup-Manager.

Observe que uma mensagem com os detalhes do usuário e do aplicativo Web é exibida.
![6](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-configure-saml-2.png)

# Experimente
1. Copie o link para o seu navegador para acessar o aplicativo Pickup-Dispatch: http://localhost.com:8080/saml2-web-app-pickup-dispatch.com
2. Clique em Login para acessar a página de autenticação.

    ![7](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-dispatch-login.png)
3. Insira uma das seguintes credenciais para entrar no aplicação.
                
        Senior Manager --> Username: cameron | Password: cameron123
        Junior Manager --> Username: alex    | Password: alex123

    ![8](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-login-credentials.png)

4. Selecione os atributos que você concorda em compartilhar com o aplicativo **Pickup-Dispatch** e clique em **Continuar**.

    ![9](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-consent.png)

- A obtenção do consentimento do utilizador é um requisito fundamental do Regulamento Geral de Proteção de Dados (RGPD). O WSO2 Identity Server facilita isso por meio de seus recursos de **Gerenciamento de Consentimento**. Para saber mais sobre o GDPR e como o WSO2 Identity Server lida com o consentimento, consulte [Gerenciamento de consentimento](https://is.docs.wso2.com/en/latest/references/concepts/consent-management/).

Observe que a tela inicial do aplicativo Pickup-Dispatch é exibida.

![10](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-dispatch-home.png)

5. Da mesma forma, copie o link para o seu navegador para acessar o aplicativo Pickup-Manager: http://localhost.com:8080/saml2-web-app-pickup-manager.com
6. Clique em **Login** para acessar o aplicativo.
![11](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-manager-login.png)

Observe que o aplicativo Pickup-Manager é aberto sem precisar inserir as credenciais do usuário novamente.

![12](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-manager-home.png)

# Experimente o SSO com o OIDC
Siga as etapas abaixo para experimentar o cenário em que os dois aplicativos usam o OIDC como autenticação protocolo:

# Executar o cenário de exemplo
Primeiro, vamos configurar e executar os aplicativos de exemplo.

1. Siga as instruções sobre como configurar os exemplos.
- Uma mensagem é exibida para escolher um cenário. 
![13](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-sso.png) 
2. Insira **2** como o número do cenário no prompt de comando.
- Observe que uma mensagem com os detalhes do usuário e do aplicativo é exibida.
![14](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-sso-2.png)

# Experimente
Vamos acessar os aplicativos Pickup-Dispatch e Pickup-Manager e continuar o acesso.

1. Copie para o navegador o link para acessar o aplicativo Pickup Dispatch: http://localhost.com:8080/pickup-dispatch
2. Clique em **Login** para acessar a página de autenticação.
![15](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-dispatch-login.png)
3. Insira uma das seguintes credenciais para entrar no aplicação.

        Senior Manager --> Username: cameron | Password: cameron123
        Junior Manager --> Username: alex    | Password: alex123

    ![16](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-login-credentials.png)
4. Selecione os atributos que você concorda em compartilhar com o aplicativo Pickup-Dispatch e clique em **Continuar**.

    ![17](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-consent.png)

- A obtenção do consentimento do utilizador é um requisito fundamental do Regulamento Geral de Proteção de Dados (RGPD). O WSO2 Identity Server facilita isso por meio de seus recursos de **Gerenciamento de Consentimento**. Para saber mais sobre o GDPR e como o WSO2 Identity Server lida com o consentimento, consulte [Gerenciamento de consentimento](https://is.docs.wso2.com/en/latest/references/concepts/consent-management/).
  
Observe que a tela inicial do aplicativo Pickup-Dispatch é exibida.
![18](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-dispatch-home.png)

5. Da mesma forma, copie o link para um navegador para acessar o aplicativo Gerenciador de Coleta: http://localhost:8080/pickup-manager

- Observe que o aplicativo Pickup-Manager é aberto sem precisar inserir as credenciais do usuário.

    ![19](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-manager-home.png) 

Você configurou o SSO e seus funcionários só precisam fornecer credenciais uma vez para acessar os aplicativos Pickup-Dispatch e Pickup-Manager.

# O que vem a seguir?
Para experimentar outros cenários, navegue de volta para a linha de comando onde você executou o exemplo de início rápido e insira **y** para limpar a instalação.

![20](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-cleanup.png)

# Autenticação Multifator
Siga as instruções fornecidas aqui para experimentar a autenticação multifator.

# Cenário
A Pickup deseja aprimorar os padrões de segurança introduzindo um segundo nível de autenticação quando os usuários entrarem nos aplicativos. A autenticação multifator (MFA) está habilitada no WSO2 Identity Server usando os seguintes fatores:

- Primeiro fator: nome de usuário/senha
- Segundo fator: CHAVE DE HARDWARE

Vamos usar a linha de comando para verificar a funcionalidade MFA.

# Pré-requisitos
Antes de começar, faça o seguinte:

1. Instale o WSO2 Identity Server.
2. Implante a dependência do autenticador do exemplo e sua aplicação Web no WSO2 Identity Server.

   1. Pare o Servidor de Identidades se já estiver em execução.
   2. Baixe o arquivo **org.wso2.carbon.identity.sample.extension.authenticator.jar** e copie-o para a pasta **<IS_HOME>/repository/components/dropins** .
   3. Baixe o arquivo [sample-auth.war](https://github.com/wso2/samples-is/releases/download/v4.5.2/sample-auth.war) e copie-o para a pasta **<IS_HOME>/repository/deployment/server/webapps** .

- Este arquivo **.war** contém a interface do usuário WEB para os autenticadores usados neste tutorial.

  4. Abra o arquivo na pasta **deployment.toml<IS_HOME>/repository/conf** e adicione a seguinte configuração:

            [[resource.access_control]]
            context = "(.*)/sample-auth/(.*)"
            secure = false
            http_method = "all" 

3. Inicie o WSO2 Identity Server.

# Executar o cenário
Vamos executar os aplicativos Pickup-Dispatch e Pickup-Manager.

Siga as instruções sobre como [configurar os exemplos](https://is.docs.wso2.com/en/latest/get-started/sample-use-cases/sample-scenario/#set-up-the-sample-apps).

- Uma mensagem é exibida para escolher um cenário.

    Insira **3** como o número do cenário no prompt de comando.
    ![21](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-sso.png)

    Insira **y** para confirmar que você já fez as etapas a seguir.

    ![22](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-setup.png)

# Experimente
Vamos acessar o aplicativo Pickup-Dispatch e continuar o acesso.

1. Copie a URL para o navegador da Web para acessar o aplicativo Pickup-Dispatch: http://localhost:8080/saml2-web-app-pickup-dispatch.com
2. Clique em Efetuar login para acessar a primeira etapa de autenticação fornecida pelo WSO2 Identity Server.
   ![23](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-dispatch-login.png)
3. Insira uma das seguintes credenciais para entrar no aplicação:
        
        Manager  --> Username: cameron | Password: cameron123
        Employee --> Username: alex    | Password: alex123 
    ![24](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-login-credentials.png)

   - A página de login HARDWARE KEY que aparece como HARDWARE KEY é o segundo fator de autenticação.
4. Insira a chave DEMO que aparece no navegador e clique em Entrar.
![25](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/hardware-key.png)
   - Após a autenticação bem-sucedida, a página Consentimento do Usuário do aplicativo Pickup-Dispatch será exibida.
5. Selecione os atributos que você concorda em compartilhar com o aplicativo Pickup-Dispatch e clique em Continuar.
![26](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-consent.png)

   - A obtenção do consentimento do utilizador é um requisito fundamental do Regulamento Geral de Proteção de Dados (RGPD). O WSO2 Identity Server facilita isso por meio de seus recursos de **Gerenciamento de Consentimento**. Para saber mais sobre o GDPR e como o WSO2 Identity Server lida com o consentimento, consulte [Gerenciamento de consentimento](https://is.docs.wso2.com/en/latest/references/concepts/consent-management/).

- Observe que a tela inicial do aplicativo Pickup-Dispatch é exibida.
![27](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-dispatch-home.png)

# O que vem a seguir?
Para experimentar outros cenários, navegue de volta para a linha de comando onde você executou o exemplo de início rápido e insira **y** para limpar a instalação.

![20](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-cleanup.png)

# Autenticação federada
Siga as instruções fornecidas aqui para experimentar a autenticação federada.

# Cenário
A Pickup trabalha com uma equipe de consultores externos. No entanto, é um incômodo continuar adicionando e mantendo suas contas no banco de dados de funcionários, pois esses consultores são temporários e empregados de forma contínua.

Portanto, o Pickup decide usar a ferramenta de federação de identidades do WSO2 Identity Server. Isso permite que consultores externos usem suas credenciais de Conta do Google para fazer login nos aplicativos **Pickup**.

# Pré-requisitos
Instale o [WSO2 Identity Server](https://is.docs.wso2.com/en/latest/get-started/sample-use-cases/set-up/) e inicie o servidor.

# Configurar um aplicativo do Google OAuth 2.0
Siga estas instruções para registrar um aplicativo OAuth 2.0 no Google.

1. Acesse o console do [Google Developer](https://console.developers.google.com/apis/credentials), crie um novo projeto ou selecione um projeto existente.
2. Se a página **APIs e serviços** ainda não estiver aberta, faça o seguinte:
   1. Abra o menu de navegação e clique em **Exibir todos os produtos**.
![28](https://is.docs.wso2.com/en/6.0.0/assets/img/samples/google-view-all-products.png) 
   2. Em **Gerenciamento**, clique em **APIs e Serviços**.
![29](https://is.docs.wso2.com/en/6.0.0/assets/img/samples/google-apis-and-services.png)   
3. Vá para a página **Credenciais**, clique em **Criar Credenciais** e selecione **ID do cliente OAuth**.
![30](https://is.docs.wso2.com/en/6.0.0/assets/img/samples/google-oauth-client-id.png)   
4. Configure sua tela de consentimento clicando em **Configurar Tela de Consentimento** e retorne à tela **Criar ID do cliente OAuth** assim que terminar.
- Para obter mais informações, consulte [Consentimento do usuário](https://support.google.com/googleapi/answer/6158849#userconsent&zippy=%2Cuser-consent).
5. Selecione **Aplicativo Web** como o tipo de aplicativo.
6. Forneça um nome para seu aplicativo e especifique a seguinte URL como a **URI de Redirecionamento Autorizado** do aplicativo:

        https://localhost.com:9443/commonauth`
7. Anote a **API key** e **secret** para uso posterior.
![31](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/create-client-id.png)

- Para evitar receber a seguinte mensagem de erro, adicione **localhost.com** à lista de domínios autorizados.

        If Invalid Redirect: domain must be added to the authorized domains list before submitting.

    ![32](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/authorized-domains-list.png)

# Executar o cenário de exemplo
Vamos executar os aplicativos de exemplo Pickup-Dispatch e Pickup-Manager.

1. Siga as instruções sobre como [configurar os exemplos](https://is.docs.wso2.com/en/latest/get-started/sample-use-cases/sample-scenario/#set-up-the-sample-apps).
- Uma mensagem é exibida para escolher um cenário.
 ![33](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-sso.png)
2. Insira **4** como o número do cenário no prompt de comando para executar o cenário de autenticação federada.
3. Insira **y** para confirmar que você já concluiu as etapas a seguir.
   ![34](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-federated-auth.png)
4. Insira o **client-id** e **secret** do Google no aplicativo quando solicitado.
- Observe que uma mensagem com os detalhes do usuário e do aplicativo é exibida.
![35](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-federated-auth-3.png)

# Experimente
Vamos acessar o aplicativo Pickup-Dispatch e continuar o acesso.

1. Copie a URL para o navegador da Web para acessar o aplicativo **Pickup-Dispatch**: http://localhost:8080/saml2-web-app-pickup-dispatch.com .
2. Clique em **Login** para acessar a página de autenticação.
![36](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-dispatch-login.png)
   - Você será direcionado para a página de login do Google.
3. Digite seu nome de usuário e senha do Google e clique em **Entrar**.
   - Após a autenticação bem-sucedida, o formulário de **Consentimento do Usuário** do aplicativo **Pickup-Dispatch** será exibido.
4. Selecione os atributos que você concorda em compartilhar com o aplicativo **Pickup-Dispatch** e clique em **Continuar**.
![37](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-consent.png)

- A obtenção do consentimento do utilizador é um requisito fundamental do Regulamento Geral de Proteção de Dados (RGPD). O WSO2 Identity Server facilita isso por meio de seus recursos de **Gerenciamento de Consentimento**. Para saber mais sobre o GDPR e como o WSO2 Identity Server lida com o consentimento, consulte [Gerenciamento de consentimento](https://is.docs.wso2.com/en/latest/references/concepts/consent-management/).
  
- Observe que a tela inicial do aplicativo Pickup-Dispatch é exibida.
![38](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-dispatch-home.png)

Você fez login com êxito no aplicativo **Pickup-Dispatch** como consultor externo usando suas credenciais do Google.

# O que vem a seguir?
Para experimentar outros cenários, navegue de volta para a linha de comando onde você executou o exemplo de início rápido e insira **y** para limpar a instalação.

![20](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-cleanup.png)

# Auto-inscrição
Siga as instruções dadas aqui para experimentar a auto-inscrição do usuário.

# Cenário
Cameron percebe que permitir que novos funcionários se inscrevam nos aplicativos Web da **Pickup** pode acelerar o processo de integração. Como resultado, Cameron define a auto-inscrição para o RH da **Pickup** usando o WSO2 Identity Server.

# Pré-requisitos
Antes de começar, faça o seguinte:

1. Instale o WSO2 Identity Server.
2. Habilite as [configurações de envio de email](https://is.docs.wso2.com/en/latest/deploy/configure-email-sending/) do WSO2 IS.
3. Reinicie o WSO2 IS.

# Executar o cenário
Primeiro, vamos configurar e executar os aplicativos de exemplo.

1. Siga as instruções sobre como configurar os exemplos.

- Uma mensagem é exibida para escolher um cenário.
![39](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-sso.png)

2. Insira **5** como o número do cenário no prompt de comando. Um prompt é exibido para escolher a abordagem de inscrição do usuário.

    Habilitar o registro automático de usuário (sem qualquer configuração) | Isso permite a auto-inscrição sem ter que fazer configurações adicionais. Uma vez registrado, o usuário recebe um e-mail para o endereço de e-mail fornecido.
    |:--:|:--:|
    Habilitar o bloqueio de conta na criação|Isso bloqueia a conta de usuário durante o registro do usuário. O usuário só pode entrar no aplicativo depois de clicar no link de verificação enviado para o endereço de e-mail fornecido pelo usuário. Um e-mail de confirmação é enviado ao usuário, mas a conta de usuário é bloqueada até que o usuário confirme a conta clicando no e-mail de confirmação da conta enviado pelo WSO2 Identity Server.

    ![40](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-self-sign-up.png)

3. Digite o ***número** que corresponde à abordagem que você gostaria de tentar.
   ![41](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-configure-self-sign-up-2.png)

# Experimente
Siga as instruções abaixo para concluir o auto-registo e para iniciar sessão.

# Auto-registo
Vamos acessar o aplicativo **Pickup-Dispatch** e nos auto-registrar como um novo usuário.

1. Copie a URL em um navegador da Web para acessar o aplicativo Pickup Dispatch: http://localhost.com:8080/pickup-dispatch .

2. Clique em Login para acessar a página de autenticação.
![42](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-dispatch-login.png)
3. Clique em Criar Conta para iniciar o processo de auto-inscrição.
![43](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-self-sign-up-register.png)
4. Insira um **nome de usuário** para sua conta de usuário e clique em Prosseguir para o auto-registro. 
![44](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-self-sign-up-username.png)

- Se você quiser que um usuário se registre automaticamente para um locatário específico, forneça no seguinte formato:username<USERNAME>@<TENAND_DOMAIN>.

5. Forneça os detalhes do perfil de usuário, concorde com a **Política de Privacidade** e clique em **Registrar**. 
![45](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-self-sign-up-new-account.png)

- Uma mensagem de confirmação é exibida.
![46](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-self-sign-up-confirmation.png) 

6. Clique em **Fechar** para concluir o registro.

# Iniciar sessão
Para tentar fazer login com sua nova conta de usuário, siga as instruções abaixo:

- Se você selecionou **Habilitar Registro de Usuário (sem nenhum configuração)** durante a configuração, volte para o aplicativo **Pickup-Dispatch** e entre usando as novas credenciais de usuário.

- Se você selecionou **Bloqueio de conta na criação** durante a configuração, acesse sua conta de e-mail para exibir o e-mail de confirmação de registro da conta.

1. Acesse seu e-mail e clique em **Confirmar Registro** no e-mail ou copie o link no e-mail para o seu navegador e confirme a criação da conta.

- A conta é desbloqueada e um e-mail é enviado.

2. Volte para o aplicativo **Pickup-Dispatch** e entre usando as novas credenciais de usuário.
![47](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-login-credentials.png)

- Observe que a tela inicial do aplicativo Pickup-Dispatch é exibida.
    ![48](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-dispatch-home.png)
Você se inscreveu com êxito no aplicativo Web Pickup-Dispatch.

# O que vem a seguir?
Para experimentar outros cenários, navegue de volta para a linha de comando onde você executou o exemplo de início rápido e insira **y** para limpar a instalação.

![20](https://is.docs.wso2.com/en/6.0.0/assets/img/get-started/qsg-sso-cleanup.png)
