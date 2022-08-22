# Gerenciamento de Identidade Lab Kit
- [Gerenciamento de Identidade Lab Kit](#gerenciamento-de-identidade-lab-kit)
  - [WSO2 IS Configurações](#wso2-is-configurações)
  - [Recuperação de Senha](#recuperação-de-senha)
    - [Recuperação de senha via email](#recuperação-de-senha-via-email)
    - [Recuperação de senha via perguntas secretas](#recuperação-de-senha-via-perguntas-secretas)
  - [Recuperação de Username](#recuperação-de-username)
  - [Trava e Desabilitação de Conta](#trava-e-desabilitação-de-conta)
    - [**Trava de Conta através de um administrador**](#trava-de-conta-através-de-um-administrador)
    - [Travamento de Conta baseado em falhas em tentativas de login](#travamento-de-conta-baseado-em-falhas-em-tentativas-de-login)
    - [Desabilitando Conta](#desabilitando-conta)
  - [Políticas de Senhas](#políticas-de-senhas)
    - [Padrões de Senha](#padrões-de-senha)
    - [Histórico de Senhas](#histórico-de-senhas)

## WSO2 IS Configurações
1. Abra o arquivo deplyment.toml no diretório <IS_HOME>/repository/conf
2. Cheque se as seguintes configurações estão em ordem

        [event.default_listener.identity_mgt]
        priority= "50"
        enable = false

        [enable.default_listener.governance_identity_mgt]
        priority= "95"
        enable = true

        [event.default_listener.governance_identity_store]
        priority= "97"
        enable = true

3. Configure as seguintes configurações de email no arquivo deployment.toml

        [output_adapter.email]
        from_address=""
        username=""
        password=""
        hostname="smtp.gmail.com"
        port=587
        enable_start_tls=true
        enable_authentication=true

4. Vá para <IS_HOME>/bin e inicie o servidor executando os seguintes comandos

        Linux: sh wso2server.sh
        Windows: wso2server.bat

5. Logue no *management console* e dê ao admin tanto o nome de usuário quanto a senha
6. Crie um usuário
   - Clique em **Manage > Users**
   - Clique em **New User**
   - Complete os campos obrigatórios para criar um novo usuário

[Tabela de Conteúdos](#gerenciamento-de-identidade-lab-kit)
***

## Recuperação de Senha
Quando o usuário esquece sua senha há uma maneira de resetá-las. WSO2 Identity Server pode resetar senhas de duas maneiras:

1. Recuperação de senha via email
2. Recuperação de senha via perguntas secretas

### Recuperação de senha via email
- **Introdução**
    
    Uma das maneiras de resetar sua senha é via notificação por email. Se o usuário esquecer sua senha, ele pode recuperá-la verificando a si mesmo usando o email enviado a ele.

- **Configurando**
1. Clique em **Manage > Account Management**
2. Na aba **Account Recovery**, ative a caixa de **Notification Based Password Recovery**
3. CLique em **update**

- **Teste**
1. Vá ao **user portal** e clique em **forgot password**
2. Insira o nome do usuário e selecione **Recover with Email**.
3. Clique em **Submit**

![1](https://user-images.githubusercontent.com/110742899/186028466-536fab36-30e9-4851-82df-0acad9168463.png)


4. Uma notificação de email é enviada  para o endereço de email do usuário.
5. Clique no botão **Reset Password** no email.

![2](https://user-images.githubusercontent.com/110742899/186028492-f05ea77e-8020-4412-81bd-0f7a22466ded.png)


6. Insira uma nova senha e clique em **Submit**

### Recuperação de senha via perguntas secretas

- **Introdução**

    Caso o usuário esqueça sua senha, ele pode recuperá-la respondendo  *challenge questions* salvas para sua conta.

- **Configurando**
1. CLique em **Manage > Account Management**
2. Na aba **Account Recovery**, ative a caixa **Enable the Security Questions Based Password Recovery**
3. Configure o número de perguntas em **Number of Questions Required for Password Recovery**

![3](https://user-images.githubusercontent.com/110742899/186028534-8d655a51-c3b3-4294-84b1-6c7f26ad8adb.png)


4. Logue no **user portal**
5. CLique em **Update Account Security** sob **Account Security**
6. Clique em **'+'** sob **Security > Account Recovery**

![4](https://user-images.githubusercontent.com/110742899/186028598-2464ab8b-b9e2-416f-bca8-ce816d9c0aef.png)


7. Configure as perguntas e respostas para a conta do usuário

![4](https://user-images.githubusercontent.com/110742899/186028800-ff5b2944-faaf-449a-816e-6cfaa07bfcff.png)


8. Clique em salvar
9. Deslogue do portal do usuário

- **Teste**
  
1. Vá ao **user portal**
2. Clique em **Forgot Password**
3. Insira o nome de usuário selecione **Recover with Security Questions**

![5](https://user-images.githubusercontent.com/110742899/186028817-9c4f870e-c35f-4844-ad96-a6e0de05e7de.png)

4. Clique em **Submit**
5. Insira as respostas para as perguntas secretas e submeta

![6](https://user-images.githubusercontent.com/110742899/186028854-da72ba2f-d78f-4cd4-b57b-2dc11c05fc84.png)


6. Uma vez que sejam inseridas as respostas corretas, será encaminhado ao formulário para resetar a senha
7. Insira a nova senha e confirme

![7](https://user-images.githubusercontent.com/110742899/186028873-42d98bda-2c3c-4dc3-b395-fe6f6af3c5ca.png)


8. Clique em **Submit** e você receberá uma mensagem ao resetar com sucesso

## Recuperação de Username

- **Configurando**
 
1. Clique em **Manage > Account Management**
2. Na aba **Account Recovery**, ative as caixas de **Enable Username Recovery** e de **Enable Manage notifications sending internally**

![8](https://user-images.githubusercontent.com/110742899/186028888-d197b49f-a8a3-4a9a-a946-325b52f2104f.png)


- **Teste**

1. Vá ao **user portal**
2. Clique em **username**
3. Complete os campos obrigatórios e clique em **Submit**

![9](https://user-images.githubusercontent.com/110742899/186028909-aab4879c-6e10-4e5b-9255-8b294aa0b989.png)


4. Uma notificação de email será enviada ao endereço de email do usuário recuperando o nome do usuário
5. O email de recuperação pode ser customizado

## Trava e Desabilitação de Conta

- **Introdução**
  
  Trava e desabilitação de conta são alguns dos recursos de segurança oferecidos no WSO2 Identity Server. 
  
  A trava de conta é utilizada para bloquear **temporariamente** um usuário de logar, e a desabilitação de conta é uma medida de segurança a longo prazo que desabilita a conta por uma quantia de tempo significativa.

### **Trava de Conta através de um administrador**

- **Configurando**
1. Clique em **Manage > Login Attempts Security**
2. Selecione a caixa **Lock user accounts**

![10](https://user-images.githubusercontent.com/110742899/186028931-f10cdb0e-4070-4556-bae1-9bdd896da9e0.png)


3. CLique em **update**

- **Teste**

1. Clique em **Manage > Users**, a partir de agora você pode ver todos os usuários listados
2. Vá até o usuário que deseja travar e clique no **User Profile**
3. Ative a caixa **Lock user**

![11](https://user-images.githubusercontent.com/110742899/186028956-f021889e-d016-48ea-81f2-adff90947350.png)


4. Clique em **update**
5. Vá ao **user portal** e tente logar com o usuário bloqueado
6. A tentativa de login deve falhar

### Travamento de Conta baseado em falhas nas tentativas de login

- **Configurando**

1. Clique em **Manage > Login Attempts Security**
1. Selecione a caixa **Lock user accounts**
2. Especifique o **Maximun failed login attempts** e **Account Unlock time** como segue
        
        a. Maximum Failed Login Attempts: 3
        b. Initial account lock duration: 15


![12](https://user-images.githubusercontent.com/110742899/186028984-d4003c85-e4bf-4aec-b064-75e2108629e7.png)


4. CLique em **update**

- **Teste**

1. Vá ao **user portal** e tente logar inserindo senhas incorretas mais do que três vezes
2. Depois tente logar usando as credenciais corretas, sua tentativa deve falhar
3. Um email informando sobre a trava da conta é enviado para o endereço de email relacionado

![13](https://user-images.githubusercontent.com/110742899/186029002-401d972b-f911-4946-8ce2-77ac74cf1e4d.png)


4. Aguarde por quinze minutos e tente logar novamente com as credenciais corretas
5. A tela inicial do WSO2 Identity Server Dashboard

### Desabilitando Conta

- **Configurando**
  
1. Clique em **Manage > Account Management**
2. Selecione a caixa **Enable Account Disabling**
3. Clique em **update**

- **Teste**
  
1. Clique em **Manage > Users**,  a partir de agora você poderá visualizar todos os usuários listados
2. Acesse o usuário a ser desabilitado
3. Ative a caixa **Account Disabled**
4. Clique em **update**
5. Vá ao **user portal**, e tente logar como o usuário desabilitado
6. A tentativa de login deve falhar

[Tabela de Conteúdos](#gerenciamento-de-identidade-lab-kit)
***

## Políticas de Senhas

As políticas de senhas formam um número de regras que incentivam o usuário a utilizar senhas mais seguras. WSO2 Identity Server auxilia a customização dos padrões de senha para reforçar as políticas de senha.

### Padrões de Senha

- **Introdução**
  
  A Política de Padronização de Senha auxilia a customização de padrões de senhas de usuários. Usando essa medida, organizações podem reforçar aos usuários a respeito da mínima e máxima extensão das senhas e seus padrões **RegEx**

- **Configurando**

1. Clique em **Manage > Account Management**
2. Clique na aba **Password Policies > Password Patterns**
3. Selecione **Enable Validate passwords based on policy pattern** e edite os recursos tais quais mínima extensão, máxima extensão da senha, formato **RegEx** e mensagem de erro

![14](https://user-images.githubusercontent.com/110742899/186029031-ae092f95-f63b-4af6-83f7-168896615929.png)


4. Clique em **update** 

- **Teste**
  
1. Vá ao **user portal**
2. Clique em **Forgot Password**
3. Insira o nome do usuário, selecione **Recover with Email**, e então clique em **Submit**
4. Uma notificação de email será enviada ao endereço de email do usuário, clique em **Reset Password** no botão anexado ao email
5. Insira a senha que viola o padrão especificado de senhas, será retornado o erro especificado

![15](https://user-images.githubusercontent.com/110742899/186029055-b703a39b-3649-423d-806e-11b4ef5b1e9b.png)


### Histórico de Senhas

- **Introdução**
  
  Esse recuruso auxilia na prevenção da utilização e configuração de senhas recentes por usuários. Por exemplo, se alguém tentar configurar uma conta com a senha igual as duas anteriores, será impedido de reutilizá-la como senha atual

- **Configurando**
  
1. Clique em **Manage > Account Management**
2. Clique em **Enable Validate password history** e poderão ser configurados os recursos em **Password History validation to count**

- **Teste**

1. Vá ao **user portal**
  2. CLique em **Forgot Password**
  3. Insira o nome de usuário, selecione **Recover with Email**, e então clique em **Submit**
  4. Uma notificação de email é enviada ao endereço de email do usuário. Clique no botão **Reset Password** anexado ao email
  5. Insira a senha antiga novamente como nova senha e clique em **Submit**, será requerida a utilização de uma senha diferente da que foi usada previamente

[Tabela de Conteúdos](#gerenciamento-de-identidade-lab-kit)
***
