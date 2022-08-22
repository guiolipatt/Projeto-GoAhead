# Gerenciamento de Usuário Lab Kit
- [Gerenciamento de Usuário Lab Kit](#gerenciamento-de-usuário-lab-kit)
  - [Introdução](#introdução)
  - [Lab 01: Gerenciamento de Usuário via *Management Console*](#lab-01-gerenciamento-de-usuário-via-management-console)
    - [Roles](#roles)
    - [Grupos](#grupos)
    - [Usuários](#usuários)
  - [Lab 02: Auto Registro de Usuário via User Portal](#lab-02-auto-registro-de-usuário-via-user-portal)
  - [Lab 03: Configurando uma Secudanry User Store](#lab-03-configurando-uma-secudanry-user-store)
## Introdução

Nesse tutorial, nós vamos testar o Usuário, Role e Gerenciamento de Grupo in WSO2 Identity Server. Usuário, *Role* e Gerenciamento de Grupo envolve gerenciamento de usuário, *roles* de usuários, grupos de usuário, permissões associadas com *roles*, atribuindo *roles* em grupos e usuários em *roles*. Essas tarefas de gerenciamento de usuário podem ser performadas de várias maneiras incluindo o uso do *Console Management*, utilizando *APIs* ou *User Portal*.

[Tabela de Conteúdos](#gerenciamento-de-usuário-lab-kit)
***

## Lab 01: Gerenciamento de Usuário via *Management Console*
![1](https://user-images.githubusercontent.com/110742899/185948723-e3b45eb6-4717-401d-a51e-fc14b35fe73b.png)


1. Vá para <IS_HOME>/bin e inicialize o servidor executando um dos seguintes,

         - Linux: sh wso2server.sh
         - Windows: wso2server.bat

2. Adicione host - IP mapping. Abra o arquivo etc/host e mapeie localhost.com com IP 127.0.0.1

3. Logue no *management console* e dê ao "admin" tanto um nome de usuário quanto uma senha.

### Roles

- Adicionar Novo User Role
  - Clique em **Manage > Roles**
  - Clique em **New Role**
  - Especifique os valores requeridos para criar um novo *role*.

    ![2](https://user-images.githubusercontent.com/110742899/185950658-7562304d-5bdb-4f4d-8934-4baa6a7f8133.png)

  - Clique em **Finish**

- Atualizar User Role Existente
  - Clique em **Manage > Roles**
  - Edite o nome do *role* ao clicar no respectivo nome do *role*
  - Clique **Update**

- Deletar User Roles
  - Clique em **Manage > Roles**
  - Clique **Delete Role**

-  Atribuir Permissões para o User Role criado
   - Clique em **Manage > Roles**
   - Edite o nome do *role* ao clicar no respectivo nome do *role*
   - Clique em **Permissions**
   - Selecione as permissões da lista de permissões
    
      ![3](https://user-images.githubusercontent.com/110742899/185950708-9407ab24-c4ca-4802-9df8-be4f55c6237d.png)

    - Clique em **Update**

### Grupos
- Adicionar Novo Grupo de Usuário
  - Clique em **Manage > Groups**
  - Clique em **New Group**
  - Especifique os valores requeridos para criar um novo grupo.

    ![4](https://user-images.githubusercontent.com/110742899/185950743-eb2029b0-c2be-4166-bc6a-4671a05f2789.png)

  - Clique em **Finish**

- Deletar Grupo de Usuários
  - Clique em **Manage > Groups**
  - Clique em **Delete Group**

- Atribuir Roles para grupo de usuário criado
  - Clique em **Manage > Groups** 
  - Edite o nome do grupo clicando no respectivo nome do grupo
  - Clique em **Roles** e clique em **Assign Role**
  - Selecione os *roles* da lista de *roles*
  
    ![5](https://user-images.githubusercontent.com/110742899/185953019-f71efc93-1d3e-408c-b86c-b054967bf7bf.png)


  - Clique em **Save**

### Usuários

- Adicionar Novos Usuários
  - Clique em **Manage > Users**
  - Clique em **New User**
  - Especifique os valores requeridos para criar um novo usuário

    ![6](https://user-images.githubusercontent.com/110742899/185952880-c1e9151e-813e-4e21-94b0-0c33bc13b835.png)


- Clique em **Next > Next > Finish**
  
  (Nota: Grupos e *Roles* são opcionais ao criar um usuário)

- Atribuir *roles* de usuário para os usuários
  - Clique em **Manage > Users**
  - Edite o usuário clicando no respectivo nome de usuário
  - Clique em **Roles** e clique no botão **edit**
  - Selecione os *roles* de usuário para o usuário

    ![7](https://user-images.githubusercontent.com/110742899/185950849-e8b87f9b-cee4-4ec5-9732-023419019a65.png)

  - Clique em **Save**

[Tabela de Conteúdos](#gerenciamento-de-usuário-lab-kit)
***

## Lab 02: Auto Registro de Usuário via User Portal

- Ativar Auto Registro
1. Vá até o arquivo deployment.toml no diretório /repository/conf
2. Certifique-se que as seguintes configurações de estão no lugar:

        [identity_mgt.user_onboarding]
        enable_email_verification = true
        lock_on_creation=true
3. Adicione o seguinte para configurar o servidor de email para enviar emails, especificando lavores para fromAddress, userName e Password:
   
        [output_adapter.email]
        from_address=""
        username=""
        password=""
        hostname="smtp.gmail.com"
        port= 587
        enable_start_tls= true
        enable_authentication= true
4. Reinicie o WSO2 Identity Server
5. Habilite o auto registro de usuário no *resident identity provider*
   - Logue no *management console* e insira tanto o "admin" quanto o nome de usuário
   - Na seção **Manage**, clique em **User Onboarding**
   - Marque a caixa para **User self registration** sob **Self Registration**
  
      ![8](https://user-images.githubusercontent.com/110742899/185950917-ed9e2a75-384b-46ae-9158-eaf2b11de567.png)

    - Clique em **Update** para salvar as configurações

Teste:
- Vá ao portal do usuário e clique em **Create New Account**
- Especifique um nome de usuário
    
    ![9](https://user-images.githubusercontent.com/110742899/185950963-2596cddd-0226-48ac-90ee-145b3577ba77.png)

- Clique em **Proceed with Self Register**
- Especifique os valores para a conta do usuário
    
    ![10](https://user-images.githubusercontent.com/110742899/185950995-97bb61b1-1c27-4e81-bf8e-0e75e94e0eb5.png)

- Clique em **Register**
- Agora vá para a conta do email registrado e cheque a caixa de entrada
- Clique no link no email recebido para a ativar a conta criada
- Depois vá ao *management console* e **View Users**
- O usuário criado deve estar listado sob usuários e *roles*
- Vá ao portal do usuário e logue utilizando credenciais de usuários criados
- Assim estará apto a logar

[Tabela de Conteúdos](#gerenciamento-de-usuário-lab-kit)
***

## Lab 03: Configurando uma Secudanry User Store

Através desse lab configuraremos **Mysql JDBC Database** como um **Secondary User store** em WSO2 IAM.

- Configurando
1. Primeiramente crie um banco de dado Mysql
2. Execute <IS_HOME>/dbscripts/mysql.sql em oposição ao banco de dados criado para criar as tabelas do banco de dados
3. Baixe o Mysql driver e o localize sob a pasta <IS_HOME>/repository/componets/lib
4. Reinicie o WSO2 Identity Server
5. Logue no *management console*
6. Clique em **Manage > Userstores**
7. Clique em **New Userstores** e clique em **JDBC**
8. Defina um nome e demais propriedades de conexão
   - Connection URL:

            jdbc:mysql://localhost:3306/{Database_Name}/?useSSL=false&allowPublicKeyRetrieval=true
   - Driver Name:

            com.mysql.jdbc.Driver

    ![11](https://user-images.githubusercontent.com/110742899/185951036-46c791f2-a348-4489-a782-eb5684a92531.png)


9. Cheque o status do *DB connection* clicando em **Test Connection**
10. Clique em **Next > Next > Finish** para salvar o *secundary user store*
11. Atualize a página após alguns segundos para checar o status 
    - Se o *store* do novo usuário foi adicionado com sucesso, ele aparecerá na página *User Stores*
    - Ele pode ser visto a qualquer momento clicando em **List** sob **User Stores** no menu principal

Teste:
- No *Management Console*, clique em **Manage > Users > New User**
- Selecione o *Userstore* do *secondary user store* criado

    ![12](https://user-images.githubusercontent.com/110742899/185954059-a6850844-61bd-42b6-808b-92b5fc0bf53a.png)

- Especifique os valores requeridos para criar um novo usuário
- Clique em **Next > Next > Finish**
- Agora um usuário foi adicionado ao *secundary user store*
- Então examine a tabela **UM_USER** no banco de dados MySql, reparando que o novo usuário foi criado

[Tabela de Conteúdos](#gerenciamento-de-usuário-lab-kit)
***
