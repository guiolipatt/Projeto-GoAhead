# Autenticação - Visão Geral
O WSO2 Identity Server é um provedor de identidade que permite autenticar os usuários da sua organização quando eles fazem logon em seus aplicativos. Você pode usar o protocolo de autenticação necessário para seus aplicativos e configurar o fluxo de entrada necessário. Você também pode habilitar a autenticação forte usando a autenticação multifator (MFA) e a autenticação adaptável.

# Login
Você pode integrar facilmente seus aplicativos com o WSO2 Identity Server (WSO2 IS) e habilitar a autenticação básica. Com esse método, os usuários que fazem login em seus aplicativos são solicitados com a tela de login do WSO2 IS, onde podem inserir suas credenciais para fazer login com segurança.

## Aplicações Web

### [OIDC (OpenID Connect)](https://is.docs.wso2.com/en/6.0.0/references/concepts/authentication/intro-oidc)
#### Pré-requisitos

1. Baixe o [Apache Tomcat 8.x](https://tomcat.apache.org/download-80.cgi) e instale-o. O local de instalação do servidor Tomcat será posteriormente referido como **<TOMCAT_HOME>** neste guia.

2. É recomendável que você use um nome de host que não seja **localhost** para evitar erros do navegador. Modifique a entrada **/etc/hosts** da sua máquina para refletir isso.

- Observe que é usado **wso2is.local** nesta documentação como um exemplo, mas você deve modificá-lo ao configurar os autenticadores ou conectores com este aplicativo teste.

3. Baixe a versão mais recente do [aplicativo OIDC pickup dispatch](https://github.com/wso2/samples-is/releases/download/v4.5.2/pickup-dispatch.war).

#### Registrar um provedor de serviços

Para configurar o provedor de serviços:

1. No Management Console, vá para **Main > Identity > Service Providers** e clique em **Add**.

2. Insira **pickup-dispatch** como o Service **Provider Name** e clique em **Register**.

3. Expanda a seção **Inbound Authentication Configuration > OAuth/OpenID Connect Configuration** e clique em **Configure**.

4. Selecione os tipos de concessão relevantes que você deseja experimentar na lista **Allowed Grant Types**.

5. Insira *http://wso2is.local:8080/pickup-dispatch/oauth2client* como a **Callback Url** e clique em **Add**.

- Anote a **OAuth Client Key** e o **Client Secret**. Você precisará deles ao implantar o aplicativo teste.

- Para obter mais informações sobre o campo **Callback URL** e outras configurações avançadas, consulte [Configurações avançadas do OpenID Connect](https://is.docs.wso2.com/en/latest/guides/login/oauth-app-config-advanced/).

6. Clique em **Register** para adicionar o provedor de serviço e salve as configurações. 

#### Implantar o aplicativo Web teste

Para implantar o aplicativo Web de exemplo em um web container:

1. Extraia o arquivo **pickup-dispatch.war** e abra o **dispatch.properties** na pasta **<EXTRACT>/WEB-INF/classes**.

2. Substitua os valores **consumerKey** e **consumerSecret** pela **OAuth Client Key** e **Client Secret** obtidos ao configurar o provedor de serviços.

![oidc1](https://is.docs.wso2.com/en/6.0.0/assets/img/samples/pickup-key-secret.png)

3. Copie o **pickup-dispatch** modificado para o diretório **webapps** da pasta Tomcat.

4. Inicie o servidor Tomcat.

#### Teste

1. Inicie o servidor Tomcat e acesse a seguinte URL no seu navegador: *http://localhost:8080/pickup-dispatch/home.jsp* .
2. Clique em **Login** e insira suas credenciais de usuário.
3. Forneça o consentimento necessário. Você será redirecionado para a página inicial do aplicativo Pickup Dispatch.

Você configurou com êxito a autenticação para um aplicativo SAML.

### [SAML](https://is.docs.wso2.com/en/latest/references/concepts/authentication/intro-saml/)

#### Pré-requisitos

1. Baixe o [Apache Tomcat 8.x](https://tomcat.apache.org/download-80.cgi) e instale-o. O local de instalação do servidor Tomcat será posteriormente referido como **<TOMCAT_HOME>** neste guia.

2. É recomendável que você use um nome de host que não seja **localhost** para evitar erros do navegador. Modifique a entrada **/etc/hosts** da sua máquina para refletir isso.

- Observe que é usado **wso2is.local** nesta documentação como um exemplo, mas você deve modificá-lo ao configurar os autenticadores ou conectores com este aplicativo teste.

3. Baixe a versão mais recente do [aplicativo SAML pickup dispatch](https://github.com/wso2/samples-is/releases/download/v4.5.2/saml2-web-app-pickup-dispatch.com.war).

#### Implantar o aplicativo Web teste
Para implantar o aplicativo Web de exemplo em um Web container:

1. Copie o arquivo **.war** baixado do aplicativo SAML para o diretório **webapps** da pasta Tomcat.

2. Inicie o servidor Tomcat.

#### Adicionar configuração CORS
A SAML2 POST Binding requer que as configurações do CORS sejam definidas.

Antes de configurar o provedor de serviços, adicione as seguintes configurações ao arquivo **deployment.toml** encontrado no **<IS_HOME>/repository/conf/**. Adicionar essa configuração permite requisições **HTTP POST**.

    ``` toml
    [cors]
    allow_generic_http_requests = true
    allow_any_origin = false
    allowed_origins = [
        "http://localhost:8080"
    ]
    allow_subdomains = false
    supported_methods = [
        "GET",
        "POST",
        "HEAD",
        "OPTIONS"
    ]
    support_any_header = true
    supported_headers = []
    exposed_headers = []
    supports_credentials = true
    max_age = 3600
    tag_requests = false
    ```
#### Registrar um provedor de serviços
1. No **Management Console**, vá para **Main > Identity > Service Providers** e clique em **Add**.

2. Insira *saml2-web-app-pickup-dispatch* como o **Service Provider Name** e clique em **Register**.

3. Expanda a seção **Inbound Authentication Configuration > SAML2 Web SSO Configuration** e clique em **Configure**.

4. Insira os seguintes valores nos campos mencionados.

Nome do Campo|Valor
:-:|:-:|
Issuer|	saml2-web-app-pickup-dispatch.com
Assertion Consumer URL|	http://localhost.com:8080/saml2-web-app-pickup-dispatch.com/home.jsp

- Clique em **Yes** na caixa de diálogo que aparece depois de adicionar a **Assertion Consumer URL**. Essa caixa de diálogo aparece quando você adiciona uma **http URL**.
  
5. Habilite marcando as caixas de seleção correspondentes:
-  Enable Response Signing
- Enable Signature Validation in Authentication Requests and Logout Requests
- Enable Single Logout
- Enable Attribute Profile
    - Include Attributes in the Response Always

Para obter mais informações sobre as configurações avançadas, consulte [Configurações SAML avançadas](https://is.docs.wso2.com/en/latest/guides/login/saml-app-config-advanced).

#### Teste
Agora, vamos fazer login no aplicativo.

1. Inicie o servidor Tomcat e acesse a seguinte URL no seu navegador: *http://localhost:8080/saml2-web-app-pickup-dispatch.com* .
2. Clique em **Login** e insira suas credenciais de usuário.
3. Forneça o consentimento necessário. Você será redirecionado para a página inicial do aplicativo Pickup Dispatch.

Você configurou com êxito a autenticação para um aplicativo SAML.

### WS-Federation
- O **serviço de token de segurança passivo** (Passive STS) do WSO2 Identity Server é usado como a implementação do WS-Federation. O STS passivo é capaz de emitir tokens de segurança SAML 1.1 e 2.0. Para solicitar um token de segurança SAML 2.0, o **Request Security Token** (RST) deve ser enviado para o endpoint do STS passivo com o TokenType **SAMLV2.0** ao enviar a requisição de token. Se nenhum RST for especificado, o WSO2 Identity Server emitirá um token **SAML 1.1** por padrão.

#### Pré-requisitos

1. Baixe o [Apache Tomcat 8.x](https://tomcat.apache.org/download-80.cgi) e instale-o. O local de instalação do servidor Tomcat será posteriormente referido como **<TOMCAT_HOME>** neste guia.

2. É recomendável que você use um nome de host que não seja **localhost** para evitar erros do navegador. Modifique a entrada **/etc/hosts** da sua máquina para refletir isso.

- Observe que é usado **wso2is.local** nesta documentação como um exemplo, mas você deve modificá-lo ao configurar os autenticadores ou conectores com este aplicativo teste.

3. Baixe a versão mais recente do [aplicativo PassiveSTSSample](https://github.com/wso2/samples-is/releases/download/v4.5.2/PassiveSTSSampleApp.war).

#### Implantar o aplicativo teste
Para implantar o aplicativo Web de exemplo em um Web container:

1. Copie o arquivo **.war** baixado do aplicativo para o diretório **webapps** da pasta Tomcat.

2. Inicie o servidor Tomcat.

#### Configurar propriedades
Para configurar propriedades adicionais para o aplicativo de teste:

1. Adicione as seguintes configurações ao arquivo **web.xml** no **<TOMCAT_HOME>/apache-tomcat-<version>/webapps/PassiveSTSSampleApp/WEB-INF**.

- Especifique **idpUrl** como Passive STS URL do Identity Server.

        <init-param>
            <param-name>idpUrl</param-name>
            <param-value>https://localhost:9443/passivests</param-value>
        </init-param> 

- Especifique **replyURL** como a URL do aplicativo Web.

        <init-param>
            <param-name>replyUrl</param-name>
            <param-value>http://localhost:8080/PassiveSTSSampleApp/index.jsp</param-value>
        </init-param>

- Especifique **realm** como identificador único para o aplicativo Web. 

        <init-param>
            <param-name>realm</param-name>
            <param-value>PassiveSTSSampleApp</param-value>
        </init-param> 

- Especifique **tenantDomain** para os logins de usuários tenant. 

        <init-param>
            <param-name>requestParams</param-name>
            <param-value>tenantDomain=tenant4.com</param-value>
        </init-param>

2. Reinicie o servidor tomcat.

#### Configurar o provedor de serviços

1. No **Management Console**, vá para **Main > Identity > Service Providers** e clique em **Add**.

2. Insira **PassiveSTSSampleApp** como o **Service Provider Name** e clique em **Register**.

3. Expanda a seção **Inbound Authentication Configuration > WS-Federation (Passive) Configuration** e insira os seguintes valores nos campos mencionados.

Nome do campo|	Valor|	Descrição|
:-:|:-:|:-:|
Passive STS Realm|	PassiveSTSSampleApp|	Esse deve ser um identificador único para o aplicativo Web. Forneça o mesmo realm name dado ao aplicativo Web para o qual você está configurando o WS-Federation.|
Assertion Consumer URL|	http://localhost:8080/PassiveSTSSampleApp/index.jsp	| Forneça a URL do aplicativo Web para o qual você está configurando o WS-Federation. Essa URL de endpoint lidará com a resposta do token.|

4. Expanda **Claim Configuration**, clique em **Add Claim URI** ao lado de **Requested Claims** e adicione as seguintes declarações:

   - http://wso2.org/claims/username
   - http://wso2.org/claims/emailaddress

5. Selecione *http://wso2.org/claims/emailaddress* como **Subject Claim URI**.

5. Clique em **Update** para salvar suas configurações.

- Atualmente, o algoritmo *signing* usado para STS passivo por padrão é **rsa-sha1**, e o algoritmo *digest* usado é **sha1**. Para alterar os algoritmos padrões, adicione a seguinte configuração no arquivo **deployment.toml** encontrado no diretório **<IS_HOME>/repository/conf**. O exemplo dado abaixo define o algoritmo *signing* como **rsa-sha256** e o algoritmo *digest* como **sha256**.

        [sts]
        signature_algorithm = "http://www.w3.org/2001/04/xmldsig-more#rsa-sha256"
        digest_algorithm = "http://www.w3.org/2001/04/xmlenc#sha256"

#### Teste
Ao redirecionar os usuários para o endpoint do STS passivo WSO2 IS, os seguintes parâmetros (opcionais) são enviados na requisição do aplicativo teste.

**wa=wsignin1.0**: especifica se o WSO2 IS deve emitir um token para a terceira parte confiável (essa é a ação padrão).

**wa=wsignout1.0**: especifica se o WSO2 IS deve fazer logout do usuário.

**wreply={replyUrl}**: especifica para onde a resposta deve ser enviada.

O uso de um rastreador de rede, como um rastreador SAML, é recomendável para analisar a requisição HTTP e as respostas nesse cenário. Com um rastreador, você poderá visualizar os parâmetros mencionados acima e também ver o token SAML emitido pelo WSO2 IS.

1. Acesse um dos links a seguir em seu navegador e clique em Login.

   - Para obter um token SAML 1.1: http://localhost:8080/PassiveSTSSampleApp/index.jsp
   - Para obter um token SAML 2.0: http://localhost:8080/PassiveSTSSampleApp?samlv=2-0

2. Faça login usando suas credenciais.

3. Forneça o consentimento necessário. Você será redirecionado para o WSO2 IS Passive STS Service e, em seguida, redirecionado de volta para a **replyUrl** configurada.

Você verá a resposta passiva do STS com as declarações solicitadas na tela.

## Aplicações SaaS

### Google
Você precisa ter um domínio do Google. Clique [aqui](https://www.bettercloud.com/monitor/the-academy/create-google-apps-domain-three-easy-steps/) para obter mais informações sobre como criar o domínio.

#### Configurar o Google
1. Acesse o console de administração do seu domínio por meio https://admin.google.com .

2. Clique em **Security**.

- Caso não consiga ver a seção Security clique na barra **MORE CONTROLS** na parte inferior e você poderá ver a seção Security.
![google1](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/security-google.png)

3. Clique em **Set up single sign-on (SSO) with a third party IdP**.
![google2](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/setup-sso-google.png)

4. Insira as seguintes URLs para seu Provedor de Identidade de terceiros (IdP).

- URL da página de **Sign-in**: https://<IS_HOSTNAME>:<IS_PORT>/samlsso

- URL da página de **Sign-out**: https://<IS_HOSTNAME>:<IS_POST>/samlsso
![google3](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/sso-fill-google.png)

5. Faça o upload do certificado do Identity Server:

- O arquivo de certificado deve conter a chave pública para o Google verificar as requisições de **sign-in**.

  1. Navegue até o diretório **<IS_HOME>/repository/resources/security** através do terminal.
  2. Execute o comando fornecido abaixo para importar o certificado público do keystore para um arquivo **.pem**.

            keytool -export -alias wso2carbon  -keystore wso2carbon.jks -storepass wso2carbon -file mycert.pem

    - O arquivo **mycert.pem** é criado no mesmo diretório mencionado na etapa acima. Se você quiser alterar o nome do arquivo que está sendo gerado, digite outro nome em vez de **mycert** no comando acima.

    3. Clique em Substituir certificado e carregue o arquivo que você acabou de gerar..pem

    4. Clique em Salvar.

#### Configurar o endereço de e-mail como o nome de usuário


Configurar o endereço de e-mail como o nome de usuário em um Identity Server já em execução não é recomendado. Portanto, certifique-se de configurá-lo antes de começar a trabalhar com o WSO2 IS.

1. Faça login no **Management Console** e clique em **Claims > List > http://wso2.org/claims**.

2. Clique no link **Edit** correspondente à **Username** e configure a propriedade **Mapped Attribute** como **mail**.
![google4](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/email-as-username-attribute-mapping.png)
e-mail como nome de usuário-atributo-mapeamento

3. Clique em **Update** para salvar as alterações.

4. Abra o arquivo **<IS_HOME>/repository/conf/deployment.toml**.

5. Adicione a seguinte configuração para habilitar a autenticação de email.

        [tenant_mgt]
        enable_email_domain= true

6. Configure o seguinte conjunto de parâmetros na configuração da userstore, dependendo do tipo de userstore que você está conectado (LDAP/Active Directory/JDBC).

Parâmetro|Descrição|
:-:|:-:|
UserNameAttribute | Define o atributo de email do usuário. **LDAP/Active Director only** 

    [user_store] 
    user_name_attribute = "mail"

Parâmetro|Descrição|
:-:|:-:|
UserNameSearchFilter |	Usa o atributo de email do usuário em vez de **cn** ou **uid**. **LDAP/Active Directory only**

Por exemplo:

    In LDAP,
    [user_store]
    user_name_search_filter = "(&amp;(objectClass=person)(mail=?))"
 
    In Active Directory, 
    [user_store]
    user_name_search_filter = "(&amp;(objectClass=user)(mail=?))"

Parâmetro|Descrição|
:-:|:-:|
UserNameListFilter |	
Usa o atributo de email do usuário, **se necessário**. **LDAP/Active Directory only**

Por exemplo:

     In LDAP,
    [user_store]
    user_name_list_filter = "(&amp;(objectClass=person)(!(sn=Service)))"
 
    In Active Directory, 
    [user_store]
    user_name_list_filter = "(&amp;(objectClass=user)(!(sn=Service)))"

Parâmetro|Descrição|
:-:|:-:|    
UsernameJavaScriptRegEx|Altere essa propriedade que está sob a tag relevante do gerenciador de userstore relevante da seguinte maneira. Essa propriedade permite que você adicione caracteres especiais como "@" no nome de usuário.

    [user_store]
    username_java_script_regex = '^[a-zA-Z0-9.-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$'

Parâmetro|Descrição|
:-:|:-:|
UsernameJavaRegEx|	Esta é uma expressão regular para validar nomes de usuário. Por padrão, as cadeias de caracteres têm um comprimento de 5 a 30. Somente caracteres não vazios são permitidos. Você pode fornecer intervalos de alfabetos, números e também intervalos de valores ASCII nas propriedades RegEx.

    [user_store]
    username_java_regex = '^[a-zA-Z0-9.-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}'

Parâmetro|Descrição|
:-:|:-:|
Realm Configurations	|O nome de usuário deve usar o atributo de email do usuário administrador.

    [super_admin]
    username = "admin@wso2.com"
    password = "admin"

Antes dessa configuração, o usuário que tinha o nome de usuário **admin** e a senha **admin** era considerado o superadministrador. O usuário superadministrador não pode ser excluído.
Após essa configuração, o usuário que tiver o nome de usuário *admin@wso2.com* é considerado o superadministrador. O usuário que tem o nome de usuário admin é considerado um administrador normal.
![google5](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/super-admin.png)

- Com essas configurações, os usuários podem fazer login no super tenant com ambos nome de usuário de e-mail (*alex@gmail.com*) ou nomes de usuário que não são de e-mail (*larry*). No entanto, para tenants, somente nomes de usuário de email são permitidos: **(tod@gmail.com@wso2.com)**.

- Você pode configurar o nome de usuário de e-mail sem habilitar a propriedade **enable_email_domain** (passo 5). Então os usuários podem fazer login tanto no super tenant e no tenant usando nomes de usuário de email e não email. No entanto, os usuários super tenant devem sempre usar **@carbon.super** no final dos nomes de usuário.

7. Reinicie o servidor.

#### Criar o provedor de serviços
Você precisa registrar seu aplicativo como um provedor de serviços no WSO2 Identity Server.

1. Faça login no Management Console do WSO2 Identity Server (https://<IS_HOST>:<PORT>/carbon) usando credenciais de administrador (admin:admin).

2. Navegue até **Main > Identity > Service Providers > Add**.
3. Insira um **Service Provider Name**. Opcionalmente, insira uma **Description**.
4. Clique em **Register**.

#### Configurações SAML
Faça as seguintes alterações no provedor de serviços criado.

1. Expanda **Inbound Authentication Configuration > SAML Configuration** e clique em **Configure**.

2. Preencha o valor para **Issuer** e **Assertion consumer URL** conforme mostrado abaixo:

Campo|Valor|Descrição
:-:|:-:|:-:|
Issuer|	google.com |Esse é o elemento **\<saml:Issuer>** que contém o identificador exclusivo do provedor de serviços. 
Assertion Consumer URL|	https://www.google.com/a/<ENTER_YOUR_DOMAIN>/acs|Essa é a URL para a qual o navegador deve ser redirecionado após a autenticação ser bem-sucedida. Esta é a URL do ACS (Assertion Consumer Service) do provedor de serviços. O provedor de identidade redireciona a resposta SAML2 para essa URL ACS. No entanto, se a solicitação SAML2 for assinada e a solicitação SAML2 contiver a URL ACS, o Servidor de Identidade honrará a URL ACS da requisição SAML2.

3. Selecione **Enable Response Signing** para assinar as Respostas SAML2 retornadas após o processo de autenticação.

4. Selecione **Enable Attribute Profile** e **Include Attributes in the Response Always** para que o provedor de identidade sempre inclua os valores de atributo relacionados às declarações selecionadas na instrução de atributo SAML2.

5. Clique em **Register**.

#### Teste
Agora, você configurou com êxito o Google e o WSO2 Identity Server.

Os usuários administradores do seu Google domain não são redirecionados para o WSO2 IS. Portanto, para experimentar o tutorial, você precisa usar um usuário que não seja um admin na sua Conta do Google.

1. Crie um usuário no WSO2 Identity Server. Certifique-se de que o mesmo usuário existe no seu domínio do Google. Neste exemplo, **alex@wso2support.com** está no domínio do Google. Portanto, precisamos criar o mesmo usuário no WSO2 Identity Server.

   1. Faça login no Management Console do WSO2 Identity Server (https://<IS_HOST>:<PORT>/carbon) usando credenciais de administrador (admin:admin).

2. Navegue até **Main > Identity > Users and Roles > Add**.

3. Clique em **Add New User** e insira o nome de usuário e a senha. Ao adicionar um novo usuário, use um endereço de e-mail como nome de usuário. Uma vez que não é obrigatório para atribuir uma role a um usuário neste tutorial, clique em **Finish**.

4. Navegue até https://google.com/a/<ENTER_YOUR_DOMAIN>/acs e insira o endereço de e-mail (nome de usuário) do usuário que você criou e insira. Você será direcionado até a tela de login do WSO2 Identity Server.

5. Insira o nome de usuário e a senha do usuário que você criou. Você será redirecionado até o G-Suite desse domínio e pode selecionar o aplicativo que você precisa usar.

Se você quiser acessar apenas o Gmail, navegue até **mail.google.com**, insira o nome de usuário do usuário, insira o nome de usuário e a senha do usuário na tela de acesso do WSO2 Identity Server e você será redirecionado até a conta de email do usuário.

### Wordpress
O WordPress é um popular sistema de gerenciamento de conteúdo de código aberto. Este tópico fornece instruções sobre como configurar o WordPress e WSO2 Identity Server (WSO2 IS) para permitir que os usuários façam login no WordPress usando suas credenciais WSO2 IS.

Neste tutorial, o WSO2 Identity Server atua como o provedor de identidade e o plugin de third party miniOrange SAML Single Sign on (SSO) atua como o provedor de serviços SAML 2.0 que pode ser configurado para estabelecer a confiança entre o plugin e o WSO2 IS para autenticar com segurança o usuário no site WordPress.

#### Fluxo
O diagrama abaixo demonstra o fluxo de como o WordPress usa o WSO2 Identity Server como um autenticador federado SAML2 para autenticar um usuário.

- Você precisa ter o [WordPress](https://wordpress.org/support/article/how-to-install-wordpress/) instalado.

#### Configurar a extensão SAML SSO no WordPress
1. No painel de administração do WordPress, no painel de navegação esquerdo, clique em **Plugins > Add New**.

2. Instale o miniOrange SSO usando a extensão SAML 2.0.

3. No painel de navegação esquerdo, clique em **miniOrange SAML 2.0 SSO > Plugin Configuration**.

4. Navegue até a aba **Service Provider Metadata**. Aqui você verá os detalhes de configuração que serão necessários mais tarde para configurações do Provedor de Identidade.

5. Na aba **Service Provider Setup**, clique em **Upload IDP Metadata** e insira os seguintes valores.

- Identity Provider Name: WSO2
- Insira a URL dos metadados: https://localhost:9443/identity/metadata/saml2

Procure o arquivo **<IS_HOME>/repository/resources/conf/templates/repository/conf/identity/identity.xml.j2** e adicione a seguinte configuração como uma sub tag da tag **ResourceAccessControl**.
        
    <Resource context="(.*)/identity/metadata/(.*)" secured="false" http-method="all"/>

6. Clique em **Fetch Metadata**. Dadas abaixo estão as informações de metadados IdP buscadas.
7. Para adicionar o widget SSO ao site WordPress, faça login como administrador e clique em **Customize** no menu no canto superior esquerdo canto.
8. Selecione **Wdigets** e adicione o widget SSO a qualquer local preferido do site.
9. Publique as alterações.

#### Configurando o provedor de serviços no WSO2 Identity Server

1. Entre no **Management Console** do WSO2 Identity Server.

2. No menu **Main**, clique em **Identity > Service Providers > Add**.

3. Preencha o **Service Provider Name** e forneça uma breve **Description** do provedor de serviços. Somente **Service Provider Name** é um campo obrigatório e você pode usar o WordPress-SP como o nome para este exemplo.

4. Expanda **Claim Configuration**.

   1. Selecione **Use Local Claim Dialect**.
   2. Para **Requested Claims**, adicione **https://wso2.org/claims/emailaddress** como URI claim.
   3. Defina o **Subject Claim URI** como **https://wso2.org/claims/nickname** .

5. Expanda a seção **Inbound Authentication Configuration > SAML2 Web SSO Configuration** e clique em **Configure**. No formulário exibido, preencha os seguintes detalhes de configuração necessários para o **single sing-on**. Para obter mais detalhes sobre esses atributos, consulte [Configuração de SSO da Web SAML2](https://is.docs.wso2.com/en/6.0.0/learn/configuring-inbound-authentication-for-a-service-provider#configuring-inbound-authentication-with-saml2-web-sso).

   1. Para o valor de **Issuer**, forneça a **SP Entity ID** obtida como **Service Provider Metadata** ao configurar a extensão SAML SSO no WordPress.
   2. Para o valor de **Assertion Consumer URL**, forneça a URL do ACS obtida como **Service Provider Metadata** ao configurar a extensão SAML SSO no WordPress.
   3. Desmarque **Enable Signature Validation in Authentication Requests and Logout Requests**.
   4. Marque **Enable Attribute Profile** e **Include Attributes in the Response Always.**.
   5. Marque **Enable Audience Restriction**. Insira a **Audience URL** obtida como **Service Provider Metadata** ao configurar a extensão SAML SSO no WordPress e clique em **Add Audience**.
   6. Marque **Enable Recipient Validation**. Insira a **Recipient URL** obtida como **Service Provider Metadata** ao configurar a extensão SAML SSO no WordPress e clique em **Add Recipient**.
   7. Salve a configuração.

#### Teste
1. Visite o site WordPress e clique no widget SSO.
2. Você será redirecionado para a página de login do WSO2 Identity Server. Faça login fornecendo credenciais de um usuário no WSO2 IS.
3. Após o login bem-sucedido, você será logado no WordPress.

### OpenCart
OpenCart é uma popular plataforma de código aberto que facilita a negociação de produtos on-line, tornando-se uma solução one-stop para empresas de comércio eletrônico. Este tópico fornece instruções sobre como configurar o OpenCart e o WSO2 Identity Server (WSO2 IS) para permitir que os usuários façam login no OpenCart usando suas credenciais do WSO2 Identity Server. Neste tutorial, o WSO2 Identity Server atua como o provedor de identidade e o plug-in third party miniOrange SAML Single Sign on (SSO) atua como o provedor de serviços SAML 2.0 que pode ser configurado para estabelecer a confiança entre o plug-in e o WSO2 IS para autenticar com segurança o usuário na loja Opencart.

#### Fluxo
- O diagrama abaixo demonstra o fluxo de como o OpenCart usa o WSO2 Identity Server como um autenticador federado SAML2 para autenticar um usuário.

- Você precisa ter o [OpenCart](https://docs.opencart.com/installation/) instalado.

#### Configurar o OpenCart

1. Instalar a extensão SAML SSO
   1. Visite a [loja de extensões OpenCart](https://www.opencart.com/index.php?route=marketplace/extension) e faça o download da extensão do provedor de serviços miniorange saml.
   2. Faça login no painel do OpenCart como administrador.
   3. Navegue até **Extensions > Installer** no painel de administração.
   4. Clique no botão **Upload** e selecione a extensão *miniorange saml sp*.
   5. Navegue até **Extensions > Extensions** e escolha o tipo de extensão como **Modules**.
   6. Na lista de módulos, você verá MiniOrange SAML SP. Clique no botão de instalação: [ + ] .

2. Configurar a extensão SAML SSO
   1. Clique no ícone **Edit** para começar a configurar a extensão.
   2. Forneça um nome de aplicativo.
   3. Na aba **Service Provider Metadata**, você encontrará a **SP Entity ID** e a **ACS Url** que serão necessárias mais tarde para configurações de provedor de identidade.
   4. Na aba **Identity Provider Setup**, forneça os valores para **Entity ID, Single Login URL** e **SAML x509 Certificate**. Esses valores devem corresponder aos valores de metadados SAML disponíveis no provedor de identidade.

3. Extrair valores de metadados SAML
   1. Faça login no WSO2 IS como administrador.
   2. Na aba **Main**, selecione **Resident Identity Provider** sob **Identity Providers**.
   3. Expanda a seção **Inbound Authentication Configuration**.
   4. Selecione **SAML2 Web SSO Configuration** e **Download SAML Metadata**.
   5. O arquivo xml baixado contém as informações relevantes necessárias para a configuração do provedor de identidade.

4. Adicione os atributos IdP relevantes navegando até a aba **Attribute Mapping**.
    - First name: http://wso2.org/claims/givenname
    - Last name: http://wso2.org/claims/lastname

5. Salve as configurações.

#### Adicionar a extensão SAML SSO para exibir o layout
1. Navegue até **Design > Layouts** no painel de administração. Selecione o ícone **Edit** adjacente a **Account**.
2. Escolha uma posição de exibição preferida para o módulo e adicione-a selecionando o MiniOrange SAML SP da lista suspensa.
3. Salve as configurações depois de adicionar o módulo à tela.

#### Configurando o provedor de serviços no WSO2 Identity Server
1. Entre no **Management Console** do WSO2 Identity Server.
2. No menu **Main**, clique em **Identity > Service Providers > Add**.
3. Preencha o **Service Provider Name** e forneça uma breve **Description** do provedor de serviços. Somente **Service Provider Name** é um campo obrigatório e você pode usar **Opencart-SP** como o nome para este exemplo.
4. Expanda **Claim Configuration**.
   1. Selecione **Use Local Claim Dialect**.
   2. Para **Requested Claims**, adicione os seguintes URIs de declaração.
      - https://wso2.org/claims/lastname
      - https://wso2.org/claims/givenname
   3. Defina **Subject Claim URI** como **https://wso2.org/claims/emailaddress** .
5. Expanda a seção **Inbound Authentication Configuration > SAML2 Web SSO Configuration** e clique em **Configure**. No formulário exibido, preencha os seguintes detalhes de configuração necessários para o **single sign-on**. Para obter mais detalhes sobre esses atributos, consulte [Configuração de SSO da Web SAML2](https://is.docs.wso2.com/en/6.0.0/learn/configuring-inbound-authentication-for-a-service-provider#configuring-inbound-authentication-with-saml2-web-sso).

   1. Para o valor de **Issuer**, forneça a **SP Entity ID** obtida como **Service Provider Metadata** ao configurar a extensão SAML SSO extensão no OpenCart.
   2. Para o valor de **Assertion Consumer URL**, forneça a URL ACS obtida como Metadados do Provedor de Serviços ao configurar a extensão SAML SSO no OpenCart.
   3. Desmarque **Enable Signature Validation in Authentication Requests and Logout Requests**.
   4. Marque **Enable Attribute Profile** e **Include Attributes in the Response Always**.
   5. Salve a configuração.

#### Teste
1. Visite o site do OpenCart e clique em login.
2. Na próxima visualização, clique em **Login with \$app**, onde **$app** é o nome da aplicação que você forneceu ao configurar a extensão SSO.
3. Você será redirecionado para a página de login do WSO2 Identity Server. Faça login fornecendo credenciais de um usuário no WSO2 IS.
4. Após o login bem-sucedido, você será logado no OpenCart.
5. Os atributos de perfil de usuário configurados no WSO2 Identity Server serão preenchidos nos **Personal details** da seu conta.

### Workday
Os tópicos a seguir orientam você na configuração do Workday e do WSO2 Identity Server (IS) para habilitar o logon no Workday por meio do WSO2 IS.

#### Pré-requisitos
1. Uma conta de administrador do [Workday](http://www.workday.com/).

2. O certificado público extraído do WSO2 (wso2carbon.jks).
   1. Extraia e imprima o certificado público.
   2. Abra a janela do terminal e navegue até o diretório **<IS_HOME>/repository/resources/security/** .
   3. Execute o seguinte comando keytool para extrair o certificado público do arquivo **wso2carbon.jks**, localizado no diretório mencionado acima. A senha do keystore é wso2carbon.

            keytool -export -alias wso2carbon -file key.crt -keystore wso2carbon.jks

- Em um ambiente de produção, você não deve usar o padrão **wso2carbon.jks** que acompanha o WSO2 Identity Server.

  1. Execute o seguinte comando para imprimir o certificado público extraído.

            openssl x509 -text -inform DER -in key.crt 
  2. Você receberá uma resposta semelhante ao exemplo abaixo. 

            -----BEGIN CERTIFICATE-----
            MIICNTCCAZ6gAwIBAgIES343gjANBgkqhkiG9w0BAQUFADBVMQswCQYDVQQGEwJV
            UzELMAkGA1UECAwCQ0ExFjAUBgNVBAcMDU1vdW50YWluIFZpZXcxDTALBgNVBAoM
            BFdTTzIxEjAQBgNVBAMMCWxvY2FsaG9zdDAeFw0xMDAyMTkwNzAyMjZaFw0zNTAy
            MTMwNzAyMjZaMFUxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJDQTEWMBQGA1UEBwwN
            TW91bnRhaW4gVmlldzENMAsGA1UECgwEV1NPMjESMBAGA1UEAwwJbG9jYWxob3N0
            MIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQCUp/oV1vWc8/TkQSiAvTousMzO
            M4asB2iltr2QKozni5aVFu818MpOLZIr8LMnTzWllJvvaA5RAAdpbECb+48FjbBe
            0hseUdN5HpwvnH/DW8ZccGvk53I6Orq7hLCv1ZHtuOCokghz/ATrhyPq+QktMfXn
            RS4HrKGJTzxaCcU7OQIDAQABoxIwEDAOBgNVHQ8BAf8EBAMCBPAwDQYJKoZIhvcN
            AQEFBQADgYEAW5wPR7cr1LAdq+IrR44iQlRG5ITCZXY9hI0PygLP2rHANh+PYfTm
            xbuOnykNGyhM6FjFLbW2uZHQTY1jMrPprjOrmyK5sjJRO4d1DeGHT/YnIjs9JogR
            Kv4XHECwLtIVdAbIdWHEtVZJyMSktcyysFcvuhPQK8Qc/E/Wq8uHSCo=
            -----END CERTIFICATE-----   

#### Configurando o Workday
1. Faça login na conta Workday como administrador.
2. Abra a opção **Edit Tenant Setup** e clique em **Security**.
3. Marque a caixa de seleção **Enable SAML Authentication**.
4. Insira o nome do provedor de identidade e o issuer da seguinte maneira.

- **Identity Provider Name**: wso2_is
- **Issuer**: localhost

O nome do **issuer** deve ser igual ao valor do **issuer** que vem com a SAML Response do provedor de identidade.

5. Adicione o certificado público do Identity Provider (que foi extraído no pré-requisito).

6. Clique em **Create** e inserir **Name**, **Valid to**, **Valid from** e o certificado na interface que aparecerá.

Você pode obter as informações do certificado e validá-lo [aqui](https://www.sslshopper.com/certificate-decoder.html).

7. Habilite o logout iniciado no Workday como visto abaixo.

8. Defina os seguintes ambientes.

9. Gere um par de chaves privadas se você ainda não tiver um. Este certificado será usado dentro do WSO2 IS para validar a entrada as requisições de autenticação e logout do Workday.

Você pode importar um certificado para o **WSO2 trust store** usando o seguinte comando (pw: wso2carbon).

        keytool -import -alias workday -file workday.crt -keystore client-truststore.jks

Reinicie o WSO2 Identity Server após a importação do certificado.

10. Insira os seguintes detalhes e clique em **OK**. Por fim, clique em **Done**.

Campo | Valor|
:-:|:-:
Service Provider ID| http://www.workday.com/ test_app

A ID do provedor de serviços deve começar com http://www.workday.com/ .

Campo | Valor|
:-:|:-:
Enable SP initiated SAML authentication | Marcado (enabled)
IdP SSO Service URL	| https://localhost:9443/samlsso
Sign SP-initiated Authentication Request | Marcado (enabled)

Permita isso para assinar a requisição de login

Campo | Valor|
:-:|:-:
Do Not Deflate SP-initiated Authentication Request | Marcado

Marque essa caixa de seleção para desabilitar a deflação de requisições

Campo | Valor|
:-:|:-:
Authentication Request Signature Method | SHA1

#### Configurando o WSO2 IS
1. Inicie o servidor IS e efetue login no management console.
2. Navegue até **Service Providers > Add** no menu **Main** e adicione um novo provedor de serviços.
3. Expanda a seção **Inbound Authentication Configuration** e, em seguida, a seção de **SAML2 Web SSO Configuration** e clique em **Configure**.
4. No formulário exibido, preencha os seguintes detalhes de configuração necessários para **single sign-on** e clique em **Register**.

Consulte a tabela a seguir para obter os detalhes.

Campo | Valor Exemplo | Descrição
:-:|:-:|:-:
Issuer|	https://workday.com/test_app | Esse é o elemento \<saml:Issuer> que contém o identificador único do provedor de serviços. Esse também é o valor do issuer especificado na SAML Authentication Request emitida pelo provedor de serviços. Verifique se esse valor é igual à ID do **Service Provider ID** definida na configuração do Workday.
Assertion Consumer URL | https://www.workday.com/your.tenant/login-saml.flex | Essa é a URL para a qual o navegador deve ser redirecionado após a autenticação ser bem-sucedida. Esta é a URL do ACS (Assertion Consumer Service) do provedor de serviços. O provedor de identidade redireciona a resposta SAML2 para essa URL ACS. No entanto, se a solicitação SAML2 for assinada e a solicitação SAML2 contiver a URL ACS, o Servidor de Identidade honrará a URL ACS da solicitação SAML2.

A URL do ACS deve estar no seguinte formato: https://www.myworkday.com/<Nome do tenant do workday>/ login-saml.flex

Campo | Valor Exemplo | Descrição
:-:|:-:|:-:
NameID Format | O valor padrão pode ser usado aqui. | Isso define os formatos de identificador de nome suportados pelo provedor de identidade. O provedor de serviços e o provedor de identidade geralmente se comunicam entre si em relação a um assunto específico. Esse assunto deve ser identificado por meio de um Name-Identifier (NameID), que deve estar em algum formato para que seja fácil para a outra parte identificá-lo com base no formato. Os identificadores de nome são usados para fornecer informações sobre um usuário.
Certificate Alias | wso2carbon.cert | Selecione o alias do certificado público do provedor de serviços (Consulte a etapa 8 da configuração do Workday) na lista suspensa. Isso é usado para validar a assinatura de solicitações SAML2 e é usado para gerar criptografia. Basicamente, o certificado do provedor de serviços deve ser selecionado aqui. Observe que esse também pode ser o certificado público do tenant do Servidor de Identidade em um cenário em que você está fazendo uma configuração específica do tenant.
Enable Response Signing | Selecionado | Selecione **Enable Response Signing** para assinar as Respostas SAML2 retornadas após o processo de autenticação.
Enable Signature Validation in Authentication Requests and Logout Requests | Selecionado | Isso especifica se o provedor de identidade deve validar a assinatura da solicitação de autenticação SAML2 e a solicitação de logout SAML2 enviadas pelo provedor de serviços.
Enable Single Logout | Selecionado | Selecione **Enable Single Logout** para que todas as sessões sejam encerradas assim que o usuário sair de um servidor. Se o single logout estiver habilitado, o provedor de identidade enviará solicitações de logout para todos os provedores de serviços. Basicamente, o provedor de identidade age de acordo com o perfil de single logout. Se o provedor de serviços oferecer suporte a uma URL diferente para logout, você poderá inserir uma **SLO Response URL** e uma **SLO Request URL** para fazer logout. Essas URLs indicam para onde a solicitação e a resposta devem ir. Se você não especificar essa URL, o provedor de identidade usará a URL do ACS (Assertion Consumer Service).

A URL de single logout deve estar no seguinte formato: https://www.myworkday.com/<Nome do tenant do Workday>/logout-saml.flex

5. Clique em **Update** para salvar.

6. Acesse a URL do ACS a partir do seu navegador para efetuar login no Workday usando o WSO2 Identity Server: https://www.myworkday.com/ \<Seu nome de tenant Workday> /login-saml2.flex.

Para alterar o valor do **Issuer** que vem com a resposta SAML por meio do Identity Server, faça o seguinte:

1. Faça login no management console e clique em **Resident** sob **Identity Providers** no menu **Main**.

2. Expanda a seção **Inbound Authentication Configuration** e, em seguida, a seção **SAML2 Web SSO Configuration**.

3. Altere o valor do **Identity Provider Entity ID** para o valor do **Issuer** requerido e clique em **Update**.

### SimpleSAMLphp
Esta página orienta você usando o WSO2 Identity Server para efetuar login no SimpleSAMLphp.

#### Configurar o SimpleSAMLphp como um provedor de serviços
1. Instale o Apache.

        # apt-get install apache2 

2. Instale o PHP e as extensões relacionadas.

        # apt-get install php5  
        # apt-get install php5-cli  
        # apt-get install php5-common  
        # apt-get install php5-curl  
        # apt-get install php-pear  
        # apt-get install php5-mcrypt 

- Se você é um usuário do Ubuntu, instale a seguinte extensão também: 
        
        # apt-get install php5-json

3. Instale o [SimpleSAMLphp](https://simplesamlphp.org/) usando os seguintes comandos.

        # sudo mkdir /var/simplesamlphp/
        # cd /var/simplesamlphp/  
        # wget https://github.com/simplesamlphp/simplesamlphp/releases/download/simplesamlphp-1.11.0/simplesamlphp-1.11.0.tar.gz  
        # tar xvf simplesamlphp-1.11.0.tar.gz  
        # mv simplesamlphp-1.11.0 simplesamlphp  
        # cd simplesamlphp  
        # cp -r metadata-templates/*.php metadata/  
        # cp -r config-templates/*.php config 

4. Configure o SimpleSAMLphp web no Apache.

        # cd /var/www/html
        # ln -s /var/simplesamlphp/simplesamlphp/www simplesaml 
5. Inicie o Apache.

        # apachectl start  

6. Acesse o aplicativo Web SimpleSAMLphp usando a seguinte URL: **http://localhost/simplesaml** .

7. Defina a configuração de login do administrador do SimpleSAMLphp da seguinte maneira:

        # cd /var/simplesamlphp/simplesamlphp  

        # vi config/config.php  

   1. Procure por ' **auth.adminpassword** ' e altere seu valor do padrão e salve o arquivo.
   2. Clique em ' **Login as administrator** ' na página da Web **http://localhost/simplesaml** para testar o valor configurado.

8. Adicione um provedor de serviços ao SimpleSAMLphp.

        # cd /var/simplesamlphp/simplesamlphp  
        # vi config/authsources.php 

   1. Adicione a seção a seguir ao arquivo e salve.

            'wso2-sp' => array(  
            
            'saml:SP',  

            // The entity ID of this SP.  

            // Can be NULL/unset, in which case an entity ID is generated based on the metadata URL.  

            'entityID' => 'simplesaml',  

            // The entity ID of the IdP this should SP should contact.  

            // Can be NULL/unset, in which case the user will be shown a list of available IdPs.  

            'idp' => 'https://localhost:9443/samlsso',  

            // The URL to the discovery service.  

            // Can be NULL/unset, in which case a builtin discovery service will be used.  

            'discoURL' => NULL,  

            ),

Por padrão, o WSO2 IS é executado em localhost:9443. Se você estiver usando um nome de host diferente ou tiver configurado um deslocamento de porta, ajuste as configurações acima de acordo.

9. Adicione os metadados do provedor de identidade.

        # cd /var/simplesamlphp/simplesamlphp  
        # vi metadata/saml20-idp-remote.php 

   1. Adicione a seção a seguir ao arquivo e salve.

            $metadata['https://localhost:9443/samlsso'] = array(  

                'name' => array(  

                'en' =>  'WSO2 IS',  

                'no' =>  'WSO2 IS',  

            ),  

                'description'   =>  'Login with WSO2 IS SAML2 IdP.',  

                'SingleSignOnService'  =>  'https://localhost:9443/samlsso',  

                'SingleLogoutService'  => 'https://localhost:9443/samlsso',  

                'certFingerprint'      => '6bf8e136eb36d4a56ea05c7ae4b9a45b63bf975d'  

            );

   2. Observe que os metadados [' **https://localhost:9443/samlsso** '] devem corresponder ao valor de 'idp' na etapa 8.

   3. Note que "6bf8e136eb36d4a56ea05c7ae4b9a45b63bf975d" é a impressão digital do certificado padrão fornecido pelo WSO2 IS. O SAML2  Response é assinado com este certificado.

#### Configurar o provedor de serviços no WSO2 IS
Você precisa registrar seu aplicativo como um provedor de serviços no WSO2 Identity Server.

1. Faça login no Management Console do WSO2 Identity Server (**https://<IS_HOST>:<PORT>/carbon**) usando credenciais de administrador (**admin:admin**).

2. Navegue até **Main > Identity > Service Providers > Add**.

3. Insira um **Service Provider Name**. Opcionalmente, insira uma **Description**.

4. Clique em **Register**.

5. Expanda **Inbound Authentication Configuration > SAML Configuration** e clique em **Configure**.

6. Insira os detalhes a seguir e mantenha os valores do restante dos campos como estão.

   - **Issuer**:simplesaml
   - **Assertion Consumer URL**: http://localhost/simplesaml/module.php/saml/sp/saml2-acs.php/wso2-sp
   - **Enable Single Logout**: True
   - **SLO Response URL**: http://localhost/simplesamlphp/www/module.php/saml/sp/saml2-logout.php/wso2-sp

7. Clique em **Register**.
![simplesaml1](https://is.docs.wso2.com/en/6.0.0/assets/img/fragments/simplesamlphp-sp.png)

#### Configurar um provedor de identidade residente no WSO2 IS
1. No menu **Main** do Management Console (https://<IS_HOST>:<PORT>/carbon), clique em **Resident** sob **Identity Providers**.

2. Na página exibida, abra a seção **SAML2 Web SSO Configuration** em **Inbound Authentication Configuration**.

3. Torne o valor do campo ****Identity Provider Entity ID** igual ao endpoint SAML do WSO2 Identity Server: https://{yourhost}:{port}/samlsso
![simplesaml2](https://is.docs.wso2.com/en/6.0.0/assets/img/fragments/simplesamlphp-resident.png)

#### Teste o SimpleSAMLphp
1. Acesse http://localhost/simplesaml e, em seguida, para **Authentication**  e clique em **Test configured authentication sources**.
2. Escolha " **wso2-sp** ". Você será redirecionado para WSO2 IS SAML2 IdP para login.

Para obter mais informações sobre SimpleSAMLphp, clique em https://simplesamlphp.org/docs/stable/

### Salesforce
### Salesforce IS
Esta página orienta você durante o uso do WSO2 Identity Server para efetuar login no Salesforce.

#### Configurar o Salesforce
1. Inscreva-se como um desenvolvedor do Salesforce.

   1. Preencha as informações relevantes na seguinte URL: https://developer.salesforce.com/signup
   2. Clique em **Sign me up**.
   3. Clique em **Allow** para permitir que o Salesforce acesse sua informação básica. Essa mensagem aparece somente quando você faz login no Salesforce pela primeira vez.
   4. Você será transferido para o tema lightening do Salesforce.
   ![salesforceis1](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/welcome-to-lightening.png)

   Este documento é explicado usando o tema do Salesforce lightning. Se você estiver usando o tema clássico, clique em **Switch to Lightning Experience** no painel superior.
   ![salesforceis2](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/switch-to-lightening.png)

2. Depois de fazer login, crie um novo domínio e acesse-o. Para fazer isso, execute as etapas a seguir.

   1. Procurar **My Domain** na barra de pesquisa que está à esquerda do painel de navegação.
    ![salesforceis3](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/my-domain-salesforce.png)
    2. Clique em **My Domain**.
    3. Na página exibida, crie um nome para o seu domínio. Você pode verificar se o domínio está disponível clicando no botão **Check Availability**.

    Para que a página abaixo seja carregada no seu navegador, certifique-se de que os cookies do Salesforce não foram bloqueados.
    ![salesforceis4](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/domain-available-salesforce.png)
    
   4. Se o domínio estiver disponível, clique em **Register Domain** para registrar seu novo domínio.

   5. A verificação pode levar alguns minutos. Após a verificação bem-sucedida, você prosseguirá para a etapa 3, onde poderá testar seu login.

   6. Clique em **Log in**.

3. No menu de navegação esquerdo, procure por **Single Sign-On Settings** e clique nele.

4. Na página exibida, clique em **Edit** e selecione a caixa de seleção **SAML Enabled** para habilitar o single sign-on federado usando SAML.
![salesforceis5](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/enable-saml-salesforce.png)
5. Clique em **Save**.
6. Clique em **New** sob **SAML Single Sign-On Settings**. A tela seguinte aparecerá:
![salesforceis6](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/saml-sso-salesforce.png)

Certifique-se de configurar as seguintes propriedades.

Campo | Valor
:-:|:-:|
Name | SSO
API Name | SSO
Issuer | localhost
Entity Id | https://saml.salesforce.com
Identity Provider Certificate | wso2.crt

Para criar o Identity Provider Certificate, abra o terminal, vá até o diretório **<IS_HOME>/repository/resources/security**. Em seguida, execute o seguinte comando.

    keytool -export -alias wso2carbon -file wso2.crt -keystore wso2carbon.jks -storepass wso2carbon

Uma vez que este comando é executado, o arquivo **wso2.crt** é gerado e pode ser encontrado no diretório **<IS_HOME>/repository/resources/security**. Clique em **Choose File** e navegue até este local para obter e carregar esse arquivo.

Campo | Valor
:-:|:-:|
Request Signing Certificate |	Default Certificate
Request Signature Method |	RSA-SHA1
Assertion Decryption Certificate |	Assertion not encrypted
SAML Identity Type	| Assertion contains user's salesforce username
SAML Identity Location	|
Identity is in the NameIdentifier element of the Subject statement
Service Provider Initiated Request Binding |	HTTP POST
Identity Provider Login URL |	https://localhost:9443/samlsso
Custom Logout URL |	https://localhost:9443/samlsso
Custom Error URL |	Deixar em branco
User Provisioning Enabled |	Deixar em branco

Clique em **Save** para salvar suas configurações.

7. Navegue até **Company Settings** no painel de navegação esquerdo e clique em **My Domain**.

8. Clique em **Deploy to Users**. Clique em **Ok** para a mensagem de confirmação que aparecerá.

9. Na página exibida, você deve configurar a seção **Authentication Configuration**. Role para baixo até esta seção e clique em **Edit**.

10. Em **Authentication Service**, selecione **SSO** em vez de **Login Page**.
![salesforceis7](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/auth-config-salesforce.png)
11. Clique em **Save**.

#### Configurar o endereço de e-mail como o nome de usuário

Configurar o endereço de e-mail como o nome de usuário em um Identity Server já em execução não é recomendado. Portanto, certifique-se de configurá-lo antes de começar a trabalhar com o WSO2 IS.

1. Faça login no Management Console e clique em **Claims > List > http://wso2.org/claims** .

2. Clique no link **Edit** correspondente à **Username** claim e configure a propriedade **Mapped Attribute** como **mail** .
![salesforceis8](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/email-as-username-attribute-mapping.png)

3. Clique em **Update** para salvar as mudanças.
4. Abra o arquivo **<IS_HOME>/repository/conf/deployment.toml** .

5. Adicione a seguinte configuração para habilitar a autenticação de email.

        [tenant_mgt]
        enable_email_domain= true

6. Configure o seguinte conjunto de parâmetros na configuração do userstore, dependendo do tipo de userstore que você esteja conectado (LDAP/Active Directory/JDBC).

Parâmetro | Descrição
:-:|:-:
UserNameAttribute | Defina o atributo de mail do usuário. Somente para **LDAP/Active Directory**.

    [user_store]
    user_name_attribute = "mail"

Parâmetro | Descrição
:-:|:-:
UserNameSearchFilter | Use o atributo de email do usuário em vez de **cn** ou **uid** . Somente para **LDAP/Active Directory**.

Por exemplo:

    In LDAP,
        [user_store]
        user_name_search_filter = "(&amp;(objectClass=person)(mail=?))"
 
    In Active Directory, 
        [user_store]
        user_name_search_filter = "(&amp;(objectClass=user)(mail=?))"

Parâmetro | Descrição
:-:|:-:
UserNameListFilter | Use o atributo de email do usuário, se necessário. Somente **LDAP/Active Directory**.

Por exemplo:

     In LDAP,
        [user_store]
        user_name_list_filter = "(&amp;(objectClass=person)(!(sn=Service)))"
 
    In Active Directory, 
        [user_store]
        user_name_list_filter = "(&amp;(objectClass=user)(!(sn=Service)))"

Parâmetro | Descrição
:-:|:-:
UsernameJavaScriptRegEx | Altere essa propriedade que está sob a tag responsável na userstore do management da seguinte maneira. Essa propriedade permite que você adicione caracteres especiais como "@" no nome de usuário.

    [user_store]
    username_java_script_regex = '^[a-zA-Z0-9.-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$'

Parâmetro | Descrição
:-:|:-:
UsernameJavaRegEx | Esta é uma expressão regular para validar nomes de usuário. Por padrão, as cadeias de caracteres têm um comprimento de 5 a 30. Somente caracteres não vazios são permitidos. Você pode fornecer intervalos de alfabetos, números e também intervalos de valores ASCII nas propriedades RegEx.

    [user_store]
    username_java_regex = '^[a-zA-Z0-9.-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}'

Parâmetro | Descrição
:-:|:-:
Realm configurations | O nome de usuário deve usar o atributo de email do usuário administrador.

    [super_admin]
    username = "admin@wso2.com"
    password = "admin"

Antes dessa configuração, o usuário que tinha o nome de usuário admin e a senha admin era considerado o superadministrador. O usuário superadministrador não pode ser excluído.

Após essa configuração, o usuário que tiver o nome de usuário admin@wso2.com é considerado o superadministrador. O usuário que tem o nome de usuário admin é considerado um administrador normal.
![salesforceis9](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/super-admin.png)

- Com essas configurações, os usuários podem fazer log in no super tenant com ambos nome de usuário de e-mail (alex@gmail.com) ou nomes de usuário que não são de e-mail (larry). No entanto, para tenants, somente nomes de usuário de email são permitidos. (larrytod@gmail.com@wso2.com).
- Você pode configurar o nome de usuário de e-mail sem habilitar a propriedade **enable_email_domain** (etapa 5). Em seguida, os usuários podem fazer login no super tenant e no tenant usando nomes de usuário de email e não email. No entanto, os usuários super tenant devem sempre usar **@carbon.super** no final dos nomes de usuário.

7. Reinicie o servidor.

#### Criar o provedor de serviços
Você precisa registrar seu aplicativo como um provedor de serviços no WSO2 Identity Server.

1. Faça login no WSO2 Identity Server Management Console (**https://<IS_HOST>:<PORT>/carbon**) usando credenciais de administrador (**admin:admin**).

2. Navegue até **Main > Identity > Service Providers > Add**.
3. Insira um **Service Provider Name**. Opcionalmente, insira uma Descrição.
4. Clique em **Register**.

#### Configurações SAML
Faça as seguintes alterações no provedor de serviços criado.

1. Expanda **Inbound Authentication Configuration > SAML Configuration** e clique em **Configure**.

2. Insira o **Issuer** como **https://saml.salesforce.com** .

O **Issuer** é o identificador exclusivo do provedor de serviços. Esse também é o valor do **issuer** especificado na SAML Authentication Request emitida pelo provedor de serviços.

3. Insira a **Assertion Consumer URL** e clique em **Add**.

A **Assertion Consumer URL** é a URL da página para a qual o navegador é redirecionado após a autenticação bem-sucedida. Para obter a **Assertion Consumer URL** do Salesforce, siga as etapas fornecidas abaixo.
    
      1. Navegue até Identity > Single Sign-On Settings no painel do lado esquerdo.
      2. Clique no nome do componente SAML SSO criado.
      3. Anote o URL de login.

4. Selecione **Enable Response Signing** para assinar as SAML2 Responses retornadas após o processo de autenticação.

5. Selecione **Enable Attribute Profile** e **Include Attributes in the Response Always** para que o provedor de identidade sempre inclua os valores de atributo relacionados às declarações selecionadas na instrução de atributo SAML2.

6. Clique em **Register**.

Para configurações mais avançadas, consulte [Configurações SAML avançadas](https://is.docs.wso2.com/en/6.0.0/guides/login/saml-app-config-advanced).

#### Testar as configurações
Execute as etapas a seguir para testar as configurações de um novo usuário no Salesforce e no Identity Server.

1. Crie um usuário no WSO2 IS.
   1. Faça login no WSO2 Identity Server Management Console (**https://<IS_HOST>:<PORT>/carbon**) usando credenciais de administrador (**admin:admin**).
2. Navegue até **Main > Identity > Users and Roles > Add**.

3. Clique em **Add New User** e insira o nome de usuário e a senha. Ao adicionar um novo usuário, use um endereço de e-mail como nome de usuário. Uma vez que não é obrigatório atribuir uma função a um usuário neste tutorial, clique em **Finish**.

4. Crie um usuário no Salesforce. Este usuário deve ter o mesmo endereço de e-mail como o usuário no WSO2 IS

   1. Faça login na conta de desenvolvedor do Salesforce: https://login.salesforce.com/.
   2. No painel de navegação esquerdo, em **ADMINISTRATION**, clique em **Users** em **Users**.
   3. Na página exibida, clique no botão **New User** para criar um novo usuário.
   4. Crie um usuário com o mesmo nome de usuário que você criou no WSO2 Identity Server. Clique em **Save** para salvar as alterações. Um e-mail será enviado para o endereço de e-mail que você forneceu para o utilizador.

Isso é principalmente para fins de teste. Em um real cenário de negócios, seria mais provável que você usasse o provisionamento Just-In-Time (JIT) para provisionar um usuário ao Salesforce.

5. Acesse sua URL de login do Salesforce em um navegador anônimo ou privado.

- A URL de login do salesforce é exclusiva do seu aplicativo Salesforce. Siga os passos abaixo para obter este URL:

    1. Procurar por **My Domain** na barra de pesquisa que está à esquerda do painel de navegação.
    2. Clique em **My Domain** e você será redirecionado para o domínio que você criou na seção "Configurar Salesforce".
    3. Clique em **Edit** em **Authentication Configurations** e você será direcionado para uma nova página com a seguinte URl:  https://<DOMAIN_NAME>/domainname/EditLogin.apexp .
    4. No menu de navegação esquerdo, expanda **Security Controls** e clique em **Single Sign-On Settings**.
    5. Clique no nome do **Single Sign-On Setting** criado. Para esse teste, clique em **SSO**. ![salesforcesi10](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/single-sign-on-setting.png)
    6. Copie a URL que está definida no **Login URL** para acessar Salesforce. ![salesforceis11](https://is.docs.wso2.com/en/6.0.0/assets/img/guides/login-url-for-salesforce.png)

1. Faça login usando as novas credenciais do usuário que você acabou de criar. Você, em seguida, será redirecionado de volta para o Salesforce.

#### Solução de problemas
Informações adicionais de solução de problemas relacionadas a qualquer SSO do lado do Salesforce podem ser recuperadas usando o Salesforce SAML Assertion Validator. Mais informações sobre as etapas estão disponíveis [aqui](https://developer.salesforce.com/docs/atlas.en-us.sso.meta/sso/sso_saml_validation_errors.htm#!).

### Salesforce Facebook
Este tópico fornece instruções sobre como fazer login no Salesforce usando suas credenciais do Facebook. Nesse caso o Salesforce é o provedor de serviços, enquanto o Facebook é o provedor de identidade. Se um usuário precisar fazer login no Salesforce, o WSO2 Identity Server enviará os detalhes do usuário para o Facebook. O Facebook autentica as credenciais do usuário e, se o usuário sair do Facebook, o usuário terá permissão para fazer login no Salesforce.

- Ao fazer login no Salesforce, você normalmente usa um endereço de e-mail. Então, para integrar isso com o Identity Server, você precisa configurar o WSO2 IS para permitir que os usuários façam login usando seus endereços de e-mail.

Configurar o endereço de e-mail como o nome de usuário em um Identity Server já em execução não é recomendado. Portanto, certifique-se de configurá-lo antes de começar a trabalhar com o WSO2 IS.

1. Abra o arquivo **<IS_HOME>/repository/conf/deployment.toml**.
2. Adicione **enable_email_domain** como mostrado abaixo.

        [tenant_mgt]
        enable_email_domain= true
3. Abra o arquivo **<IS_HOME>/repository/conf/claim-config.xml** e configure a propriedade **AttributeID** da declaração de ID **http://wso2.org/claims/username** que está sob **<Dialect dialectURI="http://wso2.org/claims">mail**.

Esse arquivo é verificado somente quando o WSO2 IS está sendo iniciado pela primeira vez. Portanto, se você não tiver configurado essa propriedade no momento da inicialização do servidor pela primeira vez, você receberá erros na inicialização.

    <Claim>
    <ClaimURI>http://wso2.org/claims/username</ClaimURI>
    <DisplayName>Username</DisplayName>
    <AttributeID>mail</AttributeID>
    <Description>Username</Description>
    </Claim>
4. Abra o arquivo **<IS_HOME>/repository/conf/identity/identity-mgt.properties** e defina a seguinte propriedade como **true**.

Esta etapa é necessária devido a um problema conhecido que impede que os códigos de confirmação sejam removidos depois que eles são usados quando os nomes de usuário de email estão habilitados. Isso ocorre porque o caractere '@' (e alguns caracteres especiais) não são permitidos no registry. Para superar esse problema, habilite nomes de usuário com hash ao salvar os códigos de confirmação configurando as propriedades abaixo.

    UserInfoRecovery.UseHashedUserNames=true

Opcionalmente, você também pode configurar a propriedade a seguir para determinar qual algoritmo de hash usar.

    UserInfoRecovery.UsernameHashAlg=SHA-1

5. Configure o seguinte conjunto de parâmetros na configuração de user store, dependendo do tipo de repositório do usuário ao qual você está conectado (LDAP/Active Directory/JDBC).

Parâmetro | Descrição
:-:|:-:
user_name_attribute | Defina o atributo de email do usuário. **Somente LDAP/Active Directory**.

    [user_store]
    user_name_attribute = "mail"


Parâmetro | Descrição
:-:|:-:
user_name_search_filter | Use o atributo de email do usuário em vez de **cn** ou **uid**. **Somente LDAP/Active Directory**.

    [user_store]
    user_name_search_filter = "(&(objectClass=identityPerson)(mail=?))"

Parâmetro | Descrição
:-:|:-:
user_name_list_filter | Use o atributo de email do usuário. **Somente LDAP/Active Directory**.

    [user_store]
    user_name_list_filter = "(&(objectClass=identityPerson)(mail=*))"

Parâmetro | Descrição
:-:|:-:
username_javas_cript_regex | Altere essa propriedade que está sob a tag de gerenciador de user store relevante da seguinte maneira. Essa propriedade permite que você adicione caracteres especiais como "@" no nome de usuário.

    [user_store]
    username_javas_cript_regex="^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+.[a-zA-Z]{2,4}"

Parâmetro | Descrição
:-:|:-:
username_java_regex | Esta é uma expressão regular para validar nomes de usuário. Por padrão, as cadeias de caracteres têm um comprimento de 5 a 30. Somente caracteres não vazios são permitidos. Você pode fornecer intervalos de alfabetos, números e também intervalos de valores ASCII nas propriedades RegEx.

    [user_store]
    username_java_regex="^[a-zA-Z0-9._-]+@[a-zA-Z0-9.-]+.[a-zA-Z]{2,4}$"

Parâmetro | Descrição
:-:|:-:
Realm configurations | 	O nome de usuário **super_admin** deve usar o atributo de email do usuário administrador.

    [super_admin]
        username="admin@wso2.com"
        Password= "admin"

Antes dessa configuração, o usuário que tinha o nome de usuário **admin** e a senha **admin** era considerado o superadministrador. O usuário superadministrador não pode ser excluído.

Após essa configuração, o usuário que tiver o nome de usuário **admin@wso2.com** é considerado o superadministrador. O usuário que tem o nome de usuário admin é considerado um administrador normal.

Se você alterou a senha do usuário admin para algo diferente de 'admin', inicie o servidor WSO2 IS usando o parâmetro -Dsetup, conforme mostrado no comando abaixo.

    sh wso2server.sh -Dsetup

Com essas configurações, os usuários podem fazer log in no super tenant com ambos nome de usuário de e-mail ( alex@gmal.com ) ou nomes de usuário que não sejam de e-mail (larry). Mas para nomes de usuário de email somente para tenant permitido (tod@gmail.com@wso2.com)

Você pode configurar o nome de usuário de e-mail sem habilitar a propriedade **EnableEmailUserName**, os usuários podem fazer login no supertenant e no tenant usando email e nomes de usuário que não são de e-mail. Mas os usuários super tenants devem sempre usar @carbon.super no final dos nomes de usuário.

6. Reinicie o servidor.

Para obter mais informações sobre como configurar o usuário primário e secundário armazena, consulte [Configurando User Stores](https://is.docs.wso2.com/en/6.0.0/setup/configuring-user-stores).

#### Configurando o Salesforce

1. Inscreva-se como desenvolvedor do Salesforce se você não tiver uma conta. Se você já tem uma conta, passe para a etapa 2 e faça login no Salesforce.
   1. Preencha as informações relevantes encontradas na seguinte URL: https://developer.salesforce.com/signup
   2. Clique em **Sign me up**.
   3. Você receberá um token de segurança por e-mail para confirmar sua novo conta. Se você não recebeu o e-mail com sucesso, você vai ser capaz de redefini-lo, seguindo os passos dados [aqui](https://help.salesforce.com/apex/HTViewHelpDoc?id=user_security_token.htm&language=en_US).
2. Faça login com suas novas credenciais como desenvolvedor do Salesforce. Faça isso clicando no link **Login** no canto superior direito do https://login.salesforce.com/ .

Este documento é explicado usando o tema do Salesforce lightning. Se você está usando o tema clássico, siga os passos abaixo para alternar para o tema lightning:
   1. Clique no seu nome de usuário para expandir a lista suspensa.
   2. Clique em **Switch to Lightning Experience.**.
   3. Clique no ícone de configurações no canto superior direito e clique em **Set Up**.

Agora você será encaminhado para o tema lightening do Salesforce. 


3. Clique em **Allow** para permitir que o Salesforce acesse sua informação básica.

4. Depois de fazer login, crie um novo domínio e acesse-o. Para fazer isso, execute as etapas a seguir.

   1. Procurar **My Domain** na barra de pesquisa que está à esquerda do painel de navegação.
   2. Clique em **My Domain**.
   3. Na página exibida, crie um nome para o seu domínio. Você pode verificar se o domínio está disponível clicando no botão **Check Availability**.

- Para que a página abaixo seja carregada no seu navegador, certifique-se de que os cookies do Salesforce não estão bloqueados.

   4. Se o domínio estiver disponível, selecione **I agree to Terms and Conditions** e clique em **Register Domain** para registrar seu novo domínio.
   5. Depois que o domínio for registrado em sua conta, clique no botão **Click here to login** para testá-lo.

5. No menu de navegação esquerdo, procure **Single Sign-On Settings**, e clique nele.
6. Na página exibida, clique em **Edit** e selecione a caixa de seleção **SAML Enabled** para habilitar o **single sign-on** federado usando SAML.
7. Clique em **Save** para salvar essa alteração de configuração.
8. Obtenha o certificado do Salesforce. Você precisa enviá-lo para o Identity Server mais tarde. Siga os passos abaixo para obter o certificado.

A solicitação de validação enviada pelo Salesforce deve ser validada pelo Identity Server. Para isso, o certificado público do Salesforce deve ser carregado no Identity Server e ser usado para validar a requisição.

   1. No menu de navegação esquerdo, vá para **Security Controls** e clique em **Certificate and Key Management**.
   2. Se você ainda não tiver feito isso, você deve criar o certificado primeiro. Execute as etapas a seguir para criar isso.
      - Clique em **Create Self-Signed Certificate**.
      - Insira o **Label** e um **Unique Name** e clique em **Save**. O certificado será gerado.
      - Clique no botão **Download Certificate** para baixar o certificado.

9. Clique em **New** em **SAML Single Sign-On Settings**.

- Se você quiser saber mais sobre as configurações de SAML Single Sign-On do Salesforce , consulte a [documentação de desenvolvedores do Salesforce](https://developer.salesforce.com/docs/atlas.en-us.sso.meta/sso/sso_saml.htm).

- Certifique-se de configurar as seguintes propriedades.

Campo | Valor
:-:|:-:
Name | SSO
API Name | SSO
Issuer | localhost

Nesse caso, temos localhost como o **Issuer**, pois este tópico é um exemplo de como isso deve funcionar. Em um ambiente de produção em que você precisa executar esse cenário, você deve ter o nome de domínio ou o nome de host do servidor que estará hospedando o WSO2 Identity Server.

Campo | Valor
:-:|:-:
Entity Id | https://saml.salesforce.com
Identity Provider Certificate | Gere o arquivo **wso2.crt** e carregue-o. Siga os passos dados na nota abaixo:

Para criar o Certificado do Provedor de Identidade, abra o terminal de comando, vá para o diretório **/repository/resources/security/**. Em seguida, você deve executar o seguinte comando

    keytool -export -alias wso2carbon -file wso2.crt -keystore wso2carbon.jks -storepass wso2carbon

Uma vez que este comando é executado, o arquivo **wso2.crt** é gerado e pode ser encontrado no diretório **<IS_HOME>/repository/resources/security/**. Clique em **Choose File** e navegue até este local para obter e carregar o arquivo.

Campo | Valor
:-:|:-:
Request Signing Certificate | Na lista suspensa, você deve selecionar o certificado público Loggingie do Salesforce que você criou na etapa 8. Se você ainda não tiver criado isso, siga as etapas fornecidas na etapa 8 acima. Depois de criar o certificado, você precisa começar a preencher o formulário de Configuração de SAML Single Sign-On a partir do início novamente.
Request Signature Method | RSA-SHA1
Assertion Decryption Certificate | Assertion not encrypted
SAML Identity Type | Assertion contains User's salesforce.com username
SAML Identity Location | Identity is in the NameIdentifier element of the Subject statement
Service Provider Initiated Request Binding | HTTP POST
Identity Provider Login URL | https://localhost:9443/samlsso

Nesse caso, temos localhost como URL, pois este tópico é um exemplo de como isso deve funcionar. Em um ambiente de produção em que você precisa executar esse cenário, você deve ter o nome de domínio ou o nome de host do servidor que você está hospedando no WSO2 Identity Server.

Campo | Valor
:-:|:-:
Custom Logout URL | Deixar em branco
Custom Error URL | Deixar em branco
Single Logout Enabled | Opcionalmente, se você quiser ter o single sing-on habilitado, você pode selecionar essa opção. Com o Single Log Out, você pode sair do Facebook e ser desconectado do Salesforce ao mesmo tempo.
User Provisioning Enabled | Deixar em branco

Se você quiser habilitar o provisionamento Just In Time, será necessário selecionar essa configuração. Quando essa configuração está habilitada, o WSO2 Identity Server cria um usuário no Salesforce, se o usuário não tiver uma conta do FB e se inscreve no Facebook. Portanto, você não precisa se preocupar em criar um usuário no Salesforce toda vez que um novo usuário precisar ser adicionado.

10. Clique em **Save** para salvar as alterações.
11. Procure por **My Domain** na barra de pesquisa que fica no painel de navegação esquerdo e clique em **My Domain**.
12. Vá até o **Domain Management** no painel de navegação esquerdo e clique em **My Domain**.
13. Clique em **Deploy to Users**. Clique em **Ok** quando a mensagem de confirmação aparecer.
14. Na página que aparecerá, você deve configurar a seção **Authentication Configuration**. Role para baixo nessa seção e clique em **Edit**.
15. Sob **Authenticate Service**, selecione **SSO** e desselecione **Login Page**.

- SSO é o método de autenticação de usuário SAML que você criou em salesforce.com, na etapa 9 acima. Ele está configurado para direcionar os usuários para o WSO2 Identity Server, que por sua vez direciona a solicitação para o Facebook, pois o Facebook atua como o IdP.

16. Clique em **Save**.

#### Configurando o provedor de serviços
1. Entre. Insira o seu nome de usuário e senha para iniciar sessão no management console.
2. Navegue até o menu **Main** para acessar o menu **Identity**. Clique em **Add** sob **Service Providers**.
3. Preencha o **Service Provider Name** e forneça uma breve **Descrição** do provedor de serviços. Somente **Service Provider Name** é um campo obrigatório e usamos Salesforce como o nome para este exemplo.
4. Clique em **Register**.
5. Configurando o calim mapping para o Salesforce:

   1. Expanda a seção **Claim Configuration**.
   2. Selecione a opção **Define Custom Claim Dialect** em **Select Claim mapping Dialect**.
   3. Clique em **Add Claim URI** para adicionar mapeamentos de declaração personalizados como segue. Adicione as seguintes URIs de declaração.

Service Provider Claim	| Local Claim
:-:|:-:
email |	http://wso2.org/claims/emailaddress
first_name | http://wso2.org/claims/givenname
last_name | http://wso2.org/claims/lastname

   4. Selecione todas essas declarações como **Requested Claims**.
   5. Selecione o **email** na lista suspensa **Subject Claim URI**. O **Subject Claim URI** é importante definir, pois é o valor único usado para identificar o usuário. Nos casos em que você tem uma user store conectado ao Identity Server, o valor desta **Subject Claim URI** é usado para procurar o usuário na user store.

Para obter mais informações sobre claim mapping, consulte [Claim Management](https://is.docs.wso2.com/en/6.0.0/learn/claim-management).

6. Expanda a **Inbound Authentication Configuration** e o **SAML2 Web SSO Configuration** e clique em **Configure**.

7. No formulário exibido, preencha os seguintes detalhes de configuração necessários para o single sign-on.
Consulte a tabela a seguir para obter detalhes.

Campo |	Valor | Descrição
:-:|:-:|:-:
**Issuer**	| https://saml.salesforce.com	| Esse é o elemento \<saml:Issuer> que contém o identificador exclusivo do provedor de serviços. Esse é o mesmo valor inserido como Entity-ID ao criar o aplicativo salesforce. Esse também é o valor do emissor especificado na Solicitação de Autenticação SAML emitida pelo provedor de serviços. Ao configurar o logon único em servidores Carbon, verifique se esse valor é igual ao valor de service_provider_id mencionado em [admin_console.authenticator.saml_sso_authenticator] no arquivo  <IS_HOME>/repository/conf/deployment.toml.
Assertion Consumer URL| | Essa é a URL para a qual o navegador deve ser redirecionado após a autenticação ser bem-sucedida. Esta é a URL do ACS (Assertion Consumer Service) do provedor de serviços. O provedor de identidade redireciona a resposta SAML2 para essa URL ACS. No entanto, se a solicitação SAML2 for assinada e a solicitação SAML2 contiver a URL ACS, o Servidor de Identidade honrará a URL ACS da solicitação SAML2. Nesse caso, você deve usar sua URL de login do Salesforce. No Salesforce, clique em **Security Controls** no menu esquerdo e, em seguida, clique em **Single Sign-On Settings**. Na página que aparecerá, clique em **SSO settings** que você criou para exibir os detalhes. Use a **Salesforce Login URL** listada lá para esse valor.

- Siga as etapas abaixo para obter a URL do Salesforce:

  1. Faça login na conta de desenvolvedor do Salesforce: https://login.salesforce.com/.
  2. Procure por **My Domain** na barra de pesquisa que está no painel de navegação esquerdo.
  3. Clique em **My Domain** e você navegará até o domínio criado na seção Configurando o Salesforce.
  4. Clique em **Edit** em **Authentication Configurations** e você será redirecionado para uma nova página com o seguinte URl: https://<DOMAIN_NAME>/domainname/EditLogin.apexp
  5. No menu de navegação esquerdo, procure **Single Sign-On Settings** e clique nela.
  6. Clique no nome da **Single Sign-On Setting** que você criou. Nesse caso, clique em **SSO**.
  7. Copie a URL definida como **Login URL** para acessar o Salesforce.

Campo |	Valor | Descrição
:-:|:-:|:-:
NameID Format |	O valor padrão pode ser usado aqui.	| Isso define os formatos de identificador de nome suportados pelo provedor de identidade. O provedor de serviços e o provedor de identidade geralmente se comunicam entre si em relação a um assunto específico. Esse assunto deve ser identificado por meio de um Name-Identifier (NameID), que deve estar em algum formato para que seja fácil para a outra parte identificá-lo com base no formato. Os identificadores de nome são usados para fornecer informações sobre um usuário.
Enable Response Signing | Selecionado |	
Selecione **Enable Response Signing** para assinar as SAML2 Responses retornadas após o processo de autenticação.
Enable Attribute Profile | Selecionado | Selecione **Enable Attribute Profile** para habilitar e adicionar uma declaração inserindo o link de declaração e clicando no botão **Add Claim**. O Identity Server fornece suporte para um perfil de atributo básico em que o provedor de identidade pode incluir os atributos do usuário nas SAML Assertions como parte da instrução de atributo. Depois de marcar a caixa de seleção **Include Attributes in the Response Always**, o provedor de identidade sempre inclui os valores de atributo relacionados às declarações selecionadas na instrução de atributo SAML.

8. Clique em **Register** para salvar suas configurações.

#### Configurando o aplicativo do Facebook
1. Vá em https://developers.facebook.com/ e inicie sua sessão utilizando suas credenciais do Facebook.
2. Clique em **Create App**.
3. Insira um **Display Name**, **Contact Email** e clique em **Create App ID**.
4. Insira o código de verificação de segurança e clique em **Submit**.
5. Na página **Select Product**, clique em **Set up** em **Facebook Login**.
6. Selecione **Website** como a plataforma para o aplicativo usado neste teste.
7. Insira **https://localhost:9443/** como a URL do site e clique em **Save**.

- Se você configurou o WSO2 Identity Server para ser executado usando o IP ou hostname, você precisa fornecer o IP ou o nome do host em vez de **localhost**.

8. Em **Products** no painel de navegação esquerdo, clique em **Facebook Login**.
9. Você pode definir as **Client OAuth Settings** na janela que Aparecerá.
   1. O **Client OAuth Login** deve ser definido como **Yes**. O **Client OAuth Login** é o switch on-off global para usar fluxos de tokens de cliente OAuth. Isso ajuda a proteger seu aplicativo e evitar abusos, bloqueando quais URIs de redirecionamento de token são permitidos.
   2. O **Web OAuth Login** deve ser definido como **Yes**. As configurações Web OAuth Login habilitam qualquer fluxo de token de cliente OAuth que usam a caixa de diálogo de login Web do Facebook para retornar tokens ao seu site próprio.
   3. **Valid OAuth redirect URIs** devem ser definidos como **https://localhost:9443/commonauth**. Insira a URL do ACS (URL do Consumidor de Asserção), que é o endpoint no WSO2 Identity Server que aceita a resposta enviada pelo facebook.

10. Role para baixo e clique no botão **Save Changes** para salvar as alterações.
11. Clique em **Dashboard**. Você pode ver o **App ID** e o **App Secret**. Clique em **Show** para exibir o **App Secret**.

- O **App ID** é a ID do Cliente e o **App Secret** é a senha do Cliente na terminologia OAuth. A versão da API é a API do Facebook que é usada para criar a aplicação.

12. Clique em **Settings** no menu à esquerda e navegue até a aba **Basic**. Adicione os **App Domains** (já que o WSO2 IS está sendo executado no localhost, você pode adicionar localhost como o **App Domain**).

13. Clique em **Save Changes**.

Agora você terminou de configurar o Facebook como um Provedor de Identidade.

- O aplicativo ainda não está disponível para o público em geral. Para disponibilizar o aplicativo para cada usuário do Facebook, você tem que enviar o aplicativo para revisão. Depois de uma revisão, o Facebook disponibiliza o aplicativo para todos os usuários do Facebook. É possível encontrar mais informações sobre o processo de revisão clicando em **App Review** no menu de navegação esquerdo do painel do seu aplicativo.

- O processo de revisão pode levar algum tempo, portanto, para os fins deste exemplo, você pode especificar alguns usuários do Facebook como desenvolvedores ou testadores. Somente os usuários especificados aqui podem usar este aplicativo para fazer login com o Facebook até que o aplicativo se torne público. Para fazer isso, clique em **Roles** à esquerda do menu de navegação do painel e especificar os usuários necessários do Facebook como Desenvolvedores ou Testadores.

#### Configurando o provedor de identidade
Agora você precisa configurar o WSO2 Identity Server adicionando o Facebook como um novo provedor de identidade.

1. Faça login no management console como administrador.
2. Na seção **Identity** sob a aba **Main** do console de gerenciamento, clique em  **Add** em **Identity Providers**.
3. Dê um nome adequado para o **Identity Provider Name**. Neste caso podemos ter o Facebook como o nome do provedor de identidade para maior clareza.

- Para obter informações detalhadas sobre as configurações do Provedor de Identidade, consulte [Adicionando e configurando um  Provedor de Identidade](https://is.docs.wso2.com/en/6.0.0/learn/adding-and-configuring-an-identity-provider).

4. Escolha o certificado do salesforce que você baixou na etapa 8 em Configurando o Salesforce como certificado público do provedor de identidade.
5. Configure o calim mapping para o Facebook:
   1. Expanda **Claim Configuration**, vá para **Basic Claim Configuration**.
   2. Selecione a opção **Define Custom Claim Dialect** em **Select Claim mapping Dialect**.
   3. Clique em **Add Claim Mapping** para adicionar mapeamentos de declaração personalizados como a seguir.

Identity Provider Claim URI | Local Claim URI | Descrição|
:-:|:-:|:-:
email |	http://wso2.org/claims/emailaddress |	Aqui mapeamos o valor no Facebook com a URI de declaração no Identity Server. Nesse caso, é uma correlação direta de declarações em que o atributo de e-mail dos usuários do Facebook é mapeado para o atributo de **e-mail** usado no Identity Server.
first_name |	http://wso2.org/claims/givenname |	Aqui mapeamos o valor no Facebook com a URI de declaração no Identity Server. Nesse caso, é uma correlação direta de declarações em que o atributo first_name dos usuários do Facebook é mapeado para o atributo **givenname** usado no Identity Server.
last_name |	http://wso2.org/claims/lastname	|Aqui mapeamos o valor no Facebook com a URI de declaração no Identity Server. Nesse caso, é uma correlação direta de declarações em que o atributo last_name dos usuários do Facebook é mapeado para o atributo de **lastname** usado no Identity Server.

- A **User ID Claim** é importante de se definir, pois é o único valor usado para identificar o usuário. Nos casos em que você tem um user store conectado ao Identity Server, esse valor de User ID Claim é usado para procurar o usuário no user store. Você pode definir ao configurar as declarações para o provedor de identidade ou ao configurar as declarações para o provedor de serviços. Neste caso isso é configurado para o provedor de serviços configurando a **Subject Claim URI**.

- Se o WSO2 Identity Server envia funções em vez de usuários e se você deseja usar essas funções para serem provisionadas pelo JIT para os usuários de o userstore local, você precisa configurar o **Role Claim URI**. Essa configuração não é necessária para este tutorial.

Você pode recuperar todas as informações públicas do usuário e do endereço eletrônico. A seguir estão alguns nomes de atributos comuns.

- id
- email
- name
- first_name
- last_name
- link
- gender
- locale
- age_range
 
Mais informações estão disponíveis no seguinte link: https://developers.facebook.com/docs/facebook-login/permissions/v2.0. Você pode mapear esses atributos para qualquer **Local Claim URI** adequada.

Para obter mais informações sobre mapeamento de declaração, consulte [Claim Management](https://is.docs.wso2.com/en/6.0.0/learn/claim-management).

6. Acesse **Facebook Configuration** em **Federated Authenticators**.

7. Marque as duas caixas de seleção para **Enable Facebook Authenticator** e torne-a **Default**.

8. Insira os valores de **App ID** e **App Secret** do Facebook que você criou nos campos **Client ID** e **Client Secret** respectivamente.

- Navegue até o [console de desenvolvedor do Facebook] (https://developers.facebook.com/)e clique no seu aplicativo que está na lista suspensa **My App**.

Campo	| Descrição |	Valor de exemplo
:-:|:-:|:-:
Client ID |	Isso se refere ao **App ID** que você recebeu do aplicativo do Facebook que você criou.	| \<Application ID of the Facebook App>

-----------------------
Segredo do cliente	Isso se refere ao Segredo do Aplicativo que você recebeu do aplicativo do Facebook que você criou.	
<App Segredo do aplicativo do Facebook>

Âmbito	Define a permissão para acessar informações específicas de um perfil do Facebook. Consulte a Referência de permissões para obter uma lista dos diferentes grupos de permissões nas APIs do Facebook.	Email
Campos de informações do usuário	Estas são as reivindicações relacionadas à conta de usuário no Facebook. O WSO2 Identity Server solicita esses campos do Facebook quando um usuário é autenticado no Facebook por meio do IS. Consulte public_profile permissão para obter mais informações sobre esses campos.	id,e-mail,first_name,last_name,
URL de retorno de chamada	Esta é a URL para a qual o navegador deve ser redirecionado após a autenticação ser bem-sucedida. Ele deve ter este formato: https://(nome do host):(porta)/acs.	https://localhost:9443/commonauth
Clique em Registrar.

Agora você adicionou o provedor de identidade.

Configurando o autenticador federado para o provedor de serviços¶
A próxima etapa é configurar o autenticador federado para o fornecedor de serviços. Nesse caso, o provedor de serviços é o Salesforce

Retorne ao console de gerenciamento.

Na seção Identidade, na guia Principal, clique em Lista em Provedores de Serviços.

Vá para o provedor de serviços que você criou e clique em Editar.

Vá para a seção Configuração de Autenticação Local e de Saída.

Selecione o Provedor de Identidade que você criou na lista suspensa em Autenticação Federada.

Verifique se o botão de opção Autenticação Federada está selecionado e selecione Facebook na lista suspensa. Este é o nome do provedor de identidade que você configurou.

Clique em Atualizar para salvar as alterações.

Agora você adicionou o provedor de identidade como autenticador federado para o Salesforce.

Testando as configurações¶
Execute as etapas a seguir para testar as configurações de um novo usuário em Salesforce e o Identity Server.

Crie um usuário no Salesforce. Este usuário deve ter o mesmo e-mail endereço como sua conta do Facebook.

Faça login na conta de desenvolvedor do Salesforce: https://login.salesforce.com/.
No painel de navegação esquerdo, clique em Usuários em Gerenciar Usuários.
Na página exibida, clique no botão Novo usuário para criar um novo usuário.
Criar um usuário com o mesmo endereço de e-mail que o usuário em Facebook.

Nota

Defina a Licença de usuário como Salesforce para este tutorial. Durante mais informações sobre a licença de usuário do Salesforce, consulte o desenvolvedor do Salesforce documentação .
Defina qualquer tipo de perfil para o usuário. Para mais informações nos perfis de usuário do Salesforce, consulte o Salesforce revelador documentação.
Clique em Salvar para salvar as alterações. Um e-mail será enviado para o endereço de e-mail que você forneceu para o usuário.

Logout do Salesforce.

Acesse sua URL de login do Salesforce em um navegador anônimo ou privado.

Informação

A URL de login do salesforce é exclusiva do seu aplicativo Salesforce. Siga os passos abaixo para obter este URL:

Procurar Meu Domínio na barra de pesquisa que está à esquerda painel de navegação.

Clique em Meu Domínio e você será navegado para o domínio que você criou na seção Configurando Salesforce .

Clique em Editar em Configurações de Autenticação e você estará navegado para uma nova página com o seguinte URl: https://<DOMAIN_NAME>/domainname/EditLogin.apexp

No menu de navegação esquerdo, expanda Controles de Segurança e clique em Configurações de Logon Único.

Clique no nome da Configuração de Logon Único que você criou. Em neste caso de uso, clique em SSO.
Copie a URL definida para que a URL de Login acesse Força-venda.
Você é direcionado para a tela de Login do Facebook.
Faça login usando suas credenciais do Facebook. Você é então redirecionado de volta para o Salesforce.
Lembre-se de usar o mesmo endereço de e-mail que o usuário no Salesforce conta.

Agora você configurou com êxito o servidor de identidade WSO2 para poder fazer login no Salesforce usando o Facebook como o provedor de identidade.
