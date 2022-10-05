# Documentação API Manager 4.1.0
- [Documentação API Manager 4.1.0](#documentação-api-manager-410)
  - [Tutoriais - Visão Geral](#tutoriais---visão-geral)
  - [Tutoriais de Cenário](#tutoriais-de-cenário)
    - [Cenário 1: Criar uma REST API através de uma OpenAPI Definition](#cenário-1-criar-uma-rest-api-através-de-uma-openapi-definition)
      - [Contexto](#contexto)
      - [Passo 1: Testando o backend](#passo-1-testando-o-backend)
      - [Passo 2: Expondo a API através do WSO2 API Manager](#passo-2-expondo-a-api-através-do-wso2-api-manager)
      - [Passo 3: Removendo autenticação do recurso](#passo-3-removendo-autenticação-do-recurso)
      - [Passo 4: Implantar a API em Gateway](#passo-4-implantar-a-api-em-gateway)
      - [Passo 5: Testando a API](#passo-5-testando-a-api)
      - [Passo 6: Publicar a API](#passo-6-publicar-a-api)
    - [Cenário 2: Permitir Controle de Acesso para a API](#cenário-2-permitir-controle-de-acesso-para-a-api)
      - [Contexto](#contexto-1)
      - [Passo 1: Criando uma API com Restrições de Função](#passo-1-criando-uma-api-com-restrições-de-função)
      - [Passo 2: Configurando Controle de Acesso para Recursos](#passo-2-configurando-controle-de-acesso-para-recursos)
      - [Passo 3: Experimentando a API](#passo-3-experimentando-a-api)
    - [Cenário 3: Implementando uma API](#cenário-3-implementando-uma-api)
      - [Contexto](#contexto-2)
      - [Passo 1: Criando um Serviço utilizando Micro Integrator](#passo-1-criando-um-serviço-utilizando-micro-integrator)
      - [Passo 2: Verifique a API no Developer Portal](#passo-2-verifique-a-api-no-developer-portal)
    - [Cenário 4: Inscrevendo um Novo Usuário](#cenário-4-inscrevendo-um-novo-usuário)
      - [Contexto](#contexto-3)
      - [Passo 1: Aplicando o fluxo de Auto-Registro](#passo-1-aplicando-o-fluxo-de-auto-registro)
      - [Passo 2: Testando o Fluxo](#passo-2-testando-o-fluxo)
      - [Passo 3: Aprovando a Requuisição de Registro](#passo-3-aprovando-a-requuisição-de-registro)
    - [Cenário 5: Envolvendo a Comunidade de Desenvolvedores](#cenário-5-envolvendo-a-comunidade-de-desenvolvedores)
      - [Contexto](#contexto-4)
      - [Passo 1: Configurando e Experimentando Recursos da Comunidade de Desenvolvedores](#passo-1-configurando-e-experimentando-recursos-da-comunidade-de-desenvolvedores)
    - [Cenário 6: Integrando com Data Sources](#cenário-6-integrando-com-data-sources)
      - [Contexto](#contexto-5)
      - [Passo 1: Desenvolvendo um serviço no Micro Integrator](#passo-1-desenvolvendo-um-serviço-no-micro-integrator)
      - [Passo 2: Expondo um dado via API Manager](#passo-2-expondo-um-dado-via-api-manager)
      - [Passo 3: Invocando a API](#passo-3-invocando-a-api)
    - [Cenário 7: Analytics](#cenário-7-analytics)
      - [Contexto](#contexto-6)
      - [Passo 1: Configurando Analytics](#passo-1-configurando-analytics)
      - [Passo 2: Teste](#passo-2-teste)
    - [Cenário 8: Limitação de Taxa](#cenário-8-limitação-de-taxa)
      - [Contexto](#contexto-7)
      - [Passo 1: Aplicando uma Apólice de Limitação de Taxa](#passo-1-aplicando-uma-apólice-de-limitação-de-taxa)
      - [Passo 2: Definindo Taxa de Transferência Máxima](#passo-2-definindo-taxa-de-transferência-máxima)
    - [Cenário 9: Realtime Data com WebSocket API](#cenário-9-realtime-data-com-websocket-api)
      - [Contexto](#contexto-8)
      - [Passo 1: Desenvolvendo um Serviço no Streaming Integrator](#passo-1-desenvolvendo-um-serviço-no-streaming-integrator)
      - [Passo 2: Expondo a WebSocket via API Manager](#passo-2-expondo-a-websocket-via-api-manager)
    - [Cenário 10: Notificações Utilizando Webhooks](#cenário-10-notificações-utilizando-webhooks)
      - [Contexto](#contexto-9)
      - [Passo 1: Subscrevendo em uma API](#passo-1-subscrevendo-em-uma-api)
      - [Passo 2: Configurando Notificações](#passo-2-configurando-notificações)
      - [Passo 3: Enviando Notificações](#passo-3-enviando-notificações)
    - [Cenário 11: Suporte GraphQL](#cenário-11-suporte-graphql)
      - [Contexto](#contexto-10)
      - [Passo 1: Criando uma API GraphQL](#passo-1-criando-uma-api-graphql)
      - [Passo 2: Publicando e Testando a API](#passo-2-publicando-e-testando-a-api)
    - [Cenário 12: Entrega de Mensagem Garantida](#cenário-12-entrega-de-mensagem-garantida)
      - [Contexto](#contexto-11)
      - [Passo 1: Invocando a API](#passo-1-invocando-a-api)
      - [Passo 2: Assegurando Entrega Bem-Sucedida](#passo-2-assegurando-entrega-bem-sucedida)
    - [Cenário 13: Integração com Serviços via Conectores](#cenário-13-integração-com-serviços-via-conectores)
      - [Contexto](#contexto-12)
      - [Passo 1: Criando e Configurando o Serviço](#passo-1-criando-e-configurando-o-serviço)
    - [Cenário 14: Suporte de Gerenciamento de Chaves Externas](#cenário-14-suporte-de-gerenciamento-de-chaves-externas)
  - [Tutoriais API Management](#tutoriais-api-management)
    - [Criar e Publicar uma GraphQL API](#criar-e-publicar-uma-graphql-api)
    - [Criar e Publicar uma AWS Lambda API](#criar-e-publicar-uma-aws-lambda-api)
    - [Expor um Serviço SOAP como uma REST API](#expor-um-serviço-soap-como-uma-rest-api)
    - [Criar e Publicar uma WebSocket API](#criar-e-publicar-uma-websocket-api)
    - [Criar e Publicar um WebSub API (WebHook API)](#criar-e-publicar-um-websub-api-webhook-api)
    - [Criar e Publicar uma SSE API](#criar-e-publicar-uma-sse-api)
    - [Editar uma API Modificando a Definição da API](#editar-uma-api-modificando-a-definição-da-api)
  - [Tutoriais de Integração](#tutoriais-de-integração)
    - [Enviando uma Mensagem Simples para um Serviço](#enviando-uma-mensagem-simples-para-um-serviço)
    - [Roteando Requests baseados em Cabeçalhos de Mensagem](#roteando-requests-baseados-em-cabeçalhos-de-mensagem)
    - [Traduzindo Formatos de Mensagem](#traduzindo-formatos-de-mensagem)
    - [Expondo Serviços Diversos como Serviço Único](#expondo-serviços-diversos-como-serviço-único)
    - [Guardar e Encaminhar Mensagens para Entrega Garantida](#guardar-e-encaminhar-mensagens-para-entrega-garantida)
    - [Expondo Datasources como um Serviço](#expondo-datasources-como-um-serviço)
    - [Processamento de Arquivo](#processamento-de-arquivo)
    - [Execução Periódica de Processo de Integração](#execução-periódica-de-processo-de-integração)
    - [Utilizando Inbound Endpoints](#utilizando-inbound-endpoints)
    - [Reutilizando Sequências de Mediação](#reutilizando-sequências-de-mediação)
    - [Enviando Emails por um Serviço de Integração](#enviando-emails-por-um-serviço-de-integração)
    - [Expondo um Serviço de Integração como uma API Gerenciada](#expondo-um-serviço-de-integração-como-uma-api-gerenciada)
    - [Expondo um Serviço de Integração SOAP como uma API Gerenciada](#expondo-um-serviço-de-integração-soap-como-uma-api-gerenciada)
    - [Integrando com SAP](#integrando-com-sap)
  - [Tutoriais de Integração Streaming](#tutoriais-de-integração-streaming)
    - [Expondo um Kafka Stream como um WebSocket API Gerenciada](#expondo-um-kafka-stream-como-um-websocket-api-gerenciada)
    - [Executando Mudança de Captura de Dado em Tempo Real com MySQL](#executando-mudança-de-captura-de-dado-em-tempo-real-com-mysql)
    - [Executando ETL em Tempo Real com Arquivos](#executando-etl-em-tempo-real-com-arquivos)
    - [Criando uma Aplicação ETL via SI Tooling](#criando-uma-aplicação-etl-via-si-tooling)
    - [Trabalhando com Kafka](#trabalhando-com-kafka)
    - [Trabalhando com Business Rules](#trabalhando-com-business-rules)
    - [Integrando Stores](#integrando-stores)
    - [Expondo Processed Data como API](#expondo-processed-data-como-api)
    - [Tratamento de Erro com Data Stream](#tratamento-de-erro-com-data-stream)
    - [Engatilhando Fluxos de Intregração](#engatilhando-fluxos-de-intregração)
    - [Operando o Streaming Integrator em Ambientes Conteinerizados](#operando-o-streaming-integrator-em-ambientes-conteinerizados)

## Tutoriais - Visão Geral
Os tutoriais da WSO2 API Manager guiam o usuário a experimentar as capacidades do produto.

## Tutoriais de Cenário
Os tutoriais de cenário fornecem exemplos reais que podem ser resolvidos utilizando API Manager. São tutoriais curtos e que podem ser experimentados fácil e rapidamente, cobrindo as principais capacidades do produto.

### Cenário 1: Criar uma REST API através de uma OpenAPI Definition
Este tutorial é parte de uma série de tutoriais que guia o usuário por todas as capacidades de API Manager. Este envolve a criação de uma REST API através de uma OpenAPI Definition. Para mais detalhes sobre o cenário e pré-requisitos, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 10 minutos.
#### Contexto
Coltrain é uma companhia ferroviária em parceria com a GOGO Train para oferecer um melhor serviço para seus clientes. Coltrain já possui algumas APIs implantadas in-house gerenciadas internamente por seu time de desenvolvedores. Uma delas é uma API para requisição de cronograma do trem, a qual foi projetada para o acesso do público aos cronogramas da Coltrain. Atualmente, essa API é exposta ao público e o time de desenvolvedores da Coltrain enfrenta dificuldades para manter e manejar a alta procura pela API.

Ao expor essa API através da WSO2 API Manager, Coltrain espera receber todos os benefícios da solução de Gerenciamento de API, como gerenciamento de ciclo de vida da API, segurança, limitação de taxas, etc, por fim, dissociando a sobrecarga de manutenção do seu time de desenvolvedores internos.

WSO2 API Manager oferece a capacidade de importar definições OAS para criação da API.

![scenarioone1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario1.png)

#### Passo 1: Testando o backend
Primeiramente, testa-se o backend. O usuário pode tentar o comando curl abaixo para receber uma resposta com os itens do cronograma.

    curl "http://localhost:8082/train-operations/v1/schedules"

O usuário então receberá a seguinte resposta.

    [{"entryId":"1","startTime":"14:50","endTime":"19:59","from":"London","to":"Glasgow","trainType":"Standard"},{"entryId":"2","startTime":"14:30","endTime":"19:20","from":"London","to":"Edinburgh","trainType":"1st class"},{"entryId":"3","startTime":"11:10","endTime":"12:59","from":"London","to":"Cardiff","trainType":"Standard"},{"entryId":"4","startTime":"08:30","endTime":"10:50","from":"London","to":"Manchester","trainType":"1st class"}]

Isso indica que o backend funciona bem. Próximo passo é expor essa API através do WSO2 API Manager.

#### Passo 2: Expondo a API através do WSO2 API Manager
1. Logue em https://localhost:9443/publisher/apis utilizando o usuário publisher da Coltrain. Utilize o usuário como apiprovider@coltrain.com e a senha como *user 123*.
2. Selecione a opção **Import Open API** sob a seção **REST API**.

![scenearioone2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/create-api-oas-def.png)

3. Selecione **OpenAPI File/Archive** botão e importe a definição **coltrain-public-openapi.yaml** localizada em */resources*.

![scenarionone3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/import-oas-def.png)
4. Adicione o contexto (/coltrain) e crie a API mantendo o endpoint como ele está. O usuário pode selecionar a caixa em frente ao endpoint para checar o status da URL do backend.

![scenarioone4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/create-coltrain-public-api.png)

Já que essa API é projetada para a o acesso público de usuários, os provedores de API da Coltrain querem remover qualquer autenticação para esse recurso, dessa forma qualquer pessoa poderá acessar o serviço sem uso de credenciais.

#### Passo 3: Removendo autenticação do recurso
Para a implementação disso, o usuário deve seguir os passos abaixo.

1. Vá até a aba **Develop → API Configuration → Resources**.
2. Expanda o recurso.
3. Sob a seção **Operation Governance**, desative o botão para **Segurança**.
   
![scenarioone5](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/resource-security.png)

4. Salve a API.

Antes de publicar a API, os desenvolvedores da Coltrain querem testar essa API. WSO2 API Manager oferece uma plataforma de teste para testagem de API enquanto ela está em estágio de desenvolvimento.

#### Passo 4: Implantar a API em Gateway
Antes de começar a testar a API, o usuário deve implantar a API em Gateway. Primeiro, o usuário deve selecionar um plano de negócio para a API. Para isso, vá até a seção **Develop → Subscriptions**, selecione **Unlimited** e salve. Após isso, vá até a seção **Deploy → Deployment** e selecione **Deploy**. Isso implantará a API em Gateway mas a API não estará visível aos outros ainda.

![scenarioone6](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/deploy-coltrain-public.png)

#### Passo 5: Testando a API
Agora o usuário está pronto para utilizar a API. Vá até **Test → Try out**. Isso oferece uma plataforma de API no portal Publisher para a testagem da API.

![scenarioone7](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/tryout.png)
Expanda o recurso */schedules* e invoque a API. O usuário não necessita clicar em **Generate Key** já que a segurança desse recurso foi removida. Apenas será necessária a geração de uma caso o usuário queira testar o recurso */schedules/{id}*.

![scenarioone8](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/tryout-result.png)

Agora a testagem está feita sobre o ponto de vista do publisher.

#### Passo 6: Publicar a API
A API precisa ser publicada para que possa ser acessada pelo portal Developer. Para isso, vá até a seção **Lifecycle** e selecione **Publish**.

Agora que a API foi publicada, para visualizá-la vá até o portal Developer em https://localhost:9443/devportal/ e selecione o domínio da hospedagem de **Coltrain**. Isso irá redirecionar o usuário para o portal Developer da Coltrain.

Selecione a **ColTrainScheduleCommunityAPI** e aperte o botão **Try-out** no menu da esquerda. Isso abrirá um console in-built para essa API. O usuário poderá agora experimentar a API clicando nos recursos.

![scenarioone9](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/coltrain-public-dev.png)
- [Índice](#documentação-api-manager-410)
  
### Cenário 2: Permitir Controle de Acesso para a API
Este tutorial é parte de uma série de tutoriais que guia o usuário por todas as capacidades de API Manager. Este envolve a criação de uma REST API através de uma OpenAPI Definition. Para mais detalhes sobre o cenário e pré-requisitos, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 7 minutos.

#### Contexto
ColTrain tem uma API separada de gerenciamento de horários para sua equipe interna. Essa API precisa ter níveis de permissão de acesso mais elevadas do que suas API públicas. Todos os funcionários na companhia ColTrain têm acesso à aplicação do usuário final onde eles podem ver detalhes dos horários dos trens usando essa API. Toda a equipe da ColTrain deve estar apta a checar os horários disponíveis enquanto somente a equipe com privilégios de administradores podem adicionar, editar ou remover os horários existentes. Nenhum outro usuário público ou registrado poderá ver essa API já que ela é apenas para tarefas internas. ColTrain quer ter uma clara separação entre quem pode ver e quem pode acessar suas APIs. Eles perceberam que poderia ser uma tarefa massante se tiverem que implantar do começo para o backend de suas APIs diretamente. Já que eles agora usam uma plataforma de API Management, eles querem mover todas essas tarefas de autenticações e autorizações de suas APIs internas. Isso seria benéfico para seus times internos pois assim teriam que prestar atenção apenas à lógica de suas APIs de negócio.

O usuário WSO2 pode configurar a API para ficar visível para um grupo de usuários. Por exemplo, essa API deve ficar visível apenas aos usuários do Developer Portal com a função **coltrain_employess**.

![scenariotwo1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario2.png)

WSO2 API Manager também oferta a capacidade de prover controle de acesso aos recursos da API utilizando extensões OAuth2. Requisições contendo tokens de acesso com o escopo correto estarão aptas a acessar esses recursos.

![scenariotwo2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario2a.png)

*Observação: Essa configuração contém funções **schedule_admin** e **coltrain_employee** já criados no domínio de hospedagem da ColTrain. As funções **schedule_admin** e **coltrain_employee** estão designadas ao usuário **jenny@coltrain.com** e somente a função **coltrain_employee** está desginada a **george@coltrain.com**.*

#### Passo 1: Criando uma API com Restrições de Função
Vamos criar uma API separada denominada de **ColTrainInternalTimeTableAPI** e aplicar a visibilidade dessa API baseada em funções.

1. Logue no Publisher Portal novamente *https://localhost:9443/publisher/*. Utilize credenciais de usuário tipo *apiprovider@coltrain.com* e senha tipo *user123*.
2. Crie uma nova API utilizando a definição de OpenAPI **coltrain-openapi.yaml** disponível no local */resources*. Vamos utilizar */coltrain-schedule* como no contexto. Use o endpoint fornecido ao arquivo como ele está.

![scenariotwo3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/coltrain-internal-api-create.png)

3. Vá para **Develop → Portal Configurations → Basic Info** e sob **Develop portal visibility** selecione **Restrict by role(s)**. Isso permitirá um novo campo para definir a função. Utilize **coltrain_employee** e pressione enter e salve.

![scenariotwo4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/set-visibility.png)

A visibilidade do Developer Portal está configurada para a API. Usuários com a função **coltrain_employee** agora podem ver a API no Developer Portal.

#### Passo 2: Configurando Controle de Acesso para Recursos
A próxima tarefa é configurar o controle de acesso para os recursos. Para fazê-lo, o usuário deve seguir os seguintes passos:

1. Criar uma competência selecionando **Develop → API Configurations → Local Scopes** e gerar uma competência utilizando os detalhes abaixo. Utilize **schedule_admin** como a função.

![scenariotwo5](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/create-scope.png)

2. Vá até a seção **Develop → API Configurations → Resources** e aplique a função para o recurso relevante. Por exemplo, configure a competência **schedule_admin** para o recurso *POST /schedule*, selecione esse recurso para expandir e selecione a competência do menu **Operation scope**.

![scenariotwo6](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/set-scope.png)

3. Defina um plano de negócio para a API. Para isso, vá até **Develop → Portal Configurations → Subscriptions** e selecione um plano de negócio (ex: *Unlimited*).
4. Implante a API. Para isso, vá até a seção **Develop → Deployments** e clique **deploy**.
5. Publique a API utilizando a opção **Publish → Lifecycle**.

Agora vá até o Developer Portal e siga para o domínio ColTrain. O usuário não estará apto a visualizar a API **ColTrainInternalTimeTableAPI**.

![scenariotwo7](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/not-visible.png)

Vamos logar utilizando *jenny@coltrain.com*. Use *user123* como a senha. Agora o usuário estará apto a visualizar a API.

![scenariotwo8](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/visible.png)

Jenny possui a função **coltrain_employee** e como resultado ela pode ver a API.

#### Passo 3: Experimentando a API
Agora vamos experimentar a API.

1. Logue no Developer Portal utilizando o usuário *jenny@coltrain.com* e a senha *user123*.
2. Vá em **Applications → Add new Application**, crie uma aplicação e gere chaves.
3. Copie a chave e o segredo. O segredo pode ser visto ao clicar no ícone próximo a seção **Consumer Secret**.

![scenariotwo9](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/gen-keys.png)

4. Inscreva-se na API utilizando essa aplicação.

Agora nós tentaremos o acesso a essa API utilizando dois diferentes tokens de acesso gerado por dois usuários diferentes. O usuário **jenny@coltrain.com** que tem a função **schedule_admin** associada e **george@coltrain.com** que não tem essa função associada.

Já que o recurso *POST /schedule* é protegida usando a competência **schedule_admin**, vamos criar tokens de acesso com esse escopo utilizando clientid e segredo previamente geradas. Utilize os seguintes comandos:

Para Jenny:

    curl -k -X POST https://localhost:9443/oauth2/token -d "grant_type=password&username=jenny@coltrain.com&password=user123&scope=schedule_admin" -H "Authorization: Basic Base64(consumer-key:consumer-secret)"

Para George:

    curl -k -X POST https://localhost:9443/oauth2/token -d "grant_type=password&username=george@coltrain.com&password=user123&scope=schedule_admin" -H "Authorization: Basic Base64(consumer-key:consumer-secret)"

Se o usuário checar as respostas para as duas requisições acima, ele verá que para a primeira resposta, haverá uma competência **schedule_admin** no payload da resposta.

Invoque o recurso POST utilizando cada token.

    curl -X POST "https://localhost:8243/t/coltrain.com/coltrain-schedule/1.0.0/schedules" -H  "Content-Type: application/json" -H  "Authorization: Bearer <token>" -d "{\"entryId\":\"10\",\"startTime\":\"18:30\",\"endTime\":\"20.30\",\"from\":\"London\",\"to\":\"Oxford\",\"trainType\":\"Standard\"}" -v

O usuário notará que pode acessar o recurso utilizando o token do usuário jenny@coltrain.com, mas que receberá uma mensagem de erro ao utilizar o token de George.

    {"code":"900910","message":"The access token does not allow you to access the requested resource","description":"User is NOT authorized to access the Resource: /schedules. Scope validation failed."}

O usuário pode testar os mesmos comandos utilizando a coleção Postman provida no local **resources/Access_Control_Demo.postman_collection.json**. O usuário precisa adicionar o client_id e client_secret sob a seção **Variables** para usá-lo.

![scenariotwo10](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/postman.png)
- [Índice](#documentação-api-manager-410)

### Cenário 3: Implementando uma API
Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como implementar uma API. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 8 minutos.

#### Contexto
RailCo tem uma parceria com companhias de Telecom para vender seus ingressos de trem como serviços agregadores de valor. Atualmente RailCo tem parceria com três companhias do ramo (Nexus, Wishque e Tenet). RailCo possui um requerimento para angariar as estatísticas de reservas dessas empreas em uma base diária. Todas as 3 companhias estão expondo esses dados mas elas estão expondo em diferentes formatos. RailCo quer desenvolver um serviço que capte todos esses dados e os exponha com uma API apenas. Eles primeiramente decidiram criar seu prórpio backend para chamar cada uma dessas APIs internamente e escrever a lógica de consumo de cada serviço para gerar uma saída requerida. Entretanto, eles rapidamente perceberam a complexidade de desenvolvimento da tarefa eles tinham empenhado. Por exemplo, cada um desses serviços externos usa diferentes protocolos e formatos de mensagem. Isso iria requerer habilidades especiais de seus times de desenvolvimento e aumentaria a carga de manutenção também. RailCo percebeu que utilizando o WSO2 API Manager e WSO2 Micro Integrator, eles poderiam fazer sua integração em pouco tempo e expor a API com recursos QoS adicionais.

Há três exemplos diferentes de backend implementados que providenciam as métricas em formatos diferentes. Quando o usuário as invoca diretamente, pode ver as métricas relacionadas a uma companhia Telecom.

    curl -X GET 'http://localhost:8082/telecom-rest-service/nexus/v1/metrics' 

Com Micro Integrator e Integration Studio, o usuário pode implementar a lógica de negócio para chamar esses três backends, agregando a resposta, e apresentar ao cliente como uma só resposta.

![scenariothree1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario3.png)

#### Passo 1: Criando um Serviço utilizando Micro Integrator
Para desenvolver um serviço no Micro Integrator, o usuário necessitará usar Integration Studio. Enquanto estiver desenvolvendo o usuário pode experimentar no Embedded Micro Integrator dentro do Studio. Uma vez que o desenvolvimento estiver completo, o usuário poderá exportá-lo como uma Compose Application e adicioná-lo ao Micro Integrator runtime.

![scenariothree2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/integration_studio_view.png)

Aqui, para simplificar, o serviço já está criado e foi exportado como uma Composite Application, além de ter sido adicionado à instância Micro Integrator no tutorial de instalação. O usuário pode testar o serviço do Micro Integrator o invocando diretamente.

    curl -X GET 'http://localhost:8290/metrics' 

Se o catálogo de serviço estiver habilitado no Micro Integrator, ele automaticamente impulsionará os artefatos da API, definição de Swagger para o API Manager durante a inicialização, a qual o usuário poderá ver no Catálogo de Serviço API Manager.

Para habilitar o catálogo de serviço, descomente a seção seguinte no Dockerfile encontrado dentro de *<REPO_HOME>/dockerfiles/micro-integrator/*.

    COPY *deployment.toml ${WSO2_SERVER_HOME}/conf/*.

Isso adicionará o novo arquivo de configuração para montagem. Para aplicar a configuração, reinicie o Micro Integrator rodando o seguinte comando. Isso reiniciará o container do Micro Integrator.

    docker-compose up -d --build mi-runtime

Uma vez iniciado, o usuário poderá observar que o seguinte log no Micro Integrator.

    {ServiceCatalogUtils} - Successfully updated the service catalog

O usuário poderá ver a entrada da API no API Manager ao visitar a seguinte URL. Logue com jill@railco.com.

https://localhost:9443/publisher/service-catalog

![scenariothree3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/service_catalog_view.png)

![scenariothree4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/service_catalog_detail_view.png)

#### Passo 2: Verifique a API no Developer Portal
Nessa configuração, a API já está implantada através do Publisher e o usuário poderá visualizá-la no Developer Portal.

1. Vá até Developer Portal https://localhost:9443/devportal/ e selecione RailCo domínio de hospedagem. Isso irá direcionar o usuário para o Developer Portal da RailCo.
2. Inscreva-se com um usuário do Developer Portal de hospedagem da RailCo. Utilize um usuário como *tom@railco.com* e senha *user123*.
3. Clique em TelecomMetricsAPI e vá para a seção Subscribe, e se inscreva utilizando a aplicação Default, gerando o token de acesso.
4. Uma vez gerada o token de aceso, o usuário poderá testar a seguinte requisição Curl.
   
        curl -k -X GET 'https://localhost:8243/t/railco.com/operations/bookings/1.0.0/' \
        --header 'Accept: application/json' \
        --header 'Authorization: Bearer <Access Token>'
- [Índice](#documentação-api-manager-410)

### Cenário 4: Inscrevendo um Novo Usuário
Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como inscrever um novo usuário. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 3 minutos.

#### Contexto
Quantis permite usuários externos acessarem suas APIs. Para conseguir todos os benefícios dessas APIs, eles decidiram abrir o registro para usuários externos já que pode ser um fardo entrar em todos os detalhes para cada usuário/consumidor. Para isso, eles requerem um fluxo de trabalho para aprovação de registro de usuário de forma que os usuários sejam registrados ao sistema quando um usuário com privilégios administrativos aprovar seu registro após uma validadeção manual do usuário. Ao permitir grupos externos registrando-se ao sistema sob uma supervisão, Quantis espera aumento de receita no futuro.

![scenariofour1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario4.png)

#### Passo 1: Aplicando o fluxo de Auto-Registro

O WSO2 API Manager traz pontos de extensão para engatilhar tarefas de fluxo para diversas operações tal qual criação de aplicação, criação de inscrição, inscrição de usuário, etc. Por padrão, o WSO2 API Manager vem com um fluxo de aprovação simples.

Essa configuração de demonstração vem com o fluxo de auto-registro e registro habilitado para o domínio de hospedagem da Quantis. Se o usuário precisa checar como configurá-la, deve checar a documentação de [habilitação de auto-registro](https://apim.docs.wso2.com/en/latest/reference/customize-product/customizations/customizing-the-developer-portal/enabling-or-disabling-self-signup/) e [habilitação de fluxo de registro](https://apim.docs.wso2.com/en/latest/reference/customize-product/customizations/adding-a-user-signup-workflow/).

*Observação: O usuário pode ver que **UserSignUpApprovalWorkflowExecutor** já está engatado se logar em  https://localhost:9443/carbon utilizando as credenciais de administrador da Quantis (admin@quantis.com:admin) e navegando até o local /_system/governance/apimgt/applicationdata/workflow-extensions.xml.*

![scenariofour2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/signup-config.png)

#### Passo 2: Testando o Fluxo
Para testar, faça o seguinte.

1. Vá para o Developer Portal https://localhost:9443/devportal/ e selecione o domínio de hospedagem Quantis.
2. Selecione o botão Sign In no canto superior direito. Assim mostrará a página de acesso.
3. Selecione o link **Create Account**.
4. Adicione o nome de usuário desejado (com o domínio de hospedagem) e prossiga para o auto registro. Digamos que seja *raj@quantis.com*.

![scenariofour3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/signup-start-pg.png)

5. Complete os campos requisitados e prossiga com o registro.
6. Se o usuário tentar o login usando essas credenciais, será mostrado uma página de acesso não autorizado.

![scenariofour4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/login-forbidden.png)

#### Passo 3: Aprovando a Requuisição de Registro
Para aprovar a requisição de registro, faça o seguinte:

1. Logue no Admin Portal em https://localhost:9443/admin/ utilizando *admin@quantis.com* e senha *admin*.
2. Sob **Task → User Creation**, o usuário poderá notar uma tarefa pendente. Aprove-a.

![scenariofour5](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/approve.png)

3. Agora o usuário estará apto a logar no Developer Portal utilizando o usuário *raj@quantis.com* e sua senha.

- [Índice](#documentação-api-manager-410)

### Cenário 5: Envolvendo a Comunidade de Desenvolvedores
Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como envolver a comunidade de desenvolvedores. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 4 minutos.

#### Contexto
Quantis permite que usuários aleatórios acessem suas APIs. Já que eles habilitaram o Developer Portal para o registro de usuários externos para o seu sistema, agora eles esperam que a comunidade de desenvolvedores interaja com eles na construção de suas próprias aplicações utilizando seus serviços. Quantis quer prover um lugar onde desenvolvedores de aplicação podem se comunicar com os desenvolvedores de API Quantis com consultas relacionadas as suas API. Dessa maneira desenvolvedores de aplicações e usuários externos podem entender mais sobre as APIs Quantis, podendo ter uma melhor experiência de desenvolvimento.

O Developer Portal da WSO2 API Manager fornece diversas ferramentas para auxiliar desenvolvedores a utilizarem APIs publicadas. Por exemplo:
- Geração SDK para APIs;
- Documentação para APIs;
- Classificações e Comentários;
- Console de API para experimetação de API.

#### Passo 1: Configurando e Experimentando Recursos da Comunidade de Desenvolvedores
Essa demonstração de configuração contem um exemplo de API para a elucidação das ferramentas. Logue no Developer Portal da Quantis utilizando um usuário Quantis **sindy@quantis.com** com a senha **user123** e cheque a **QuantisTrainAPI**.

![scenariofive1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/dev-portal-community.png)

O usuário poderá gerar SDKs do lado do cliente para diferentes linguagens de programação, podendo buscar mais informações a respeito na [documentação oficial](https://apim.docs.wso2.com/en/latest/consume/generating-sdks/write-a-client-application-using-the-sdk/) da WSO2. A WSO2 oferece um exemplo de programa em Java criado utilizando o Java SDK baixado do **QuantisTrainAPI**.

1. Inscreva-se na **QuantisTrainAPI** utilizando uma aplicação e gerando um token de acesso.
2. Vá até o local */resources* e invoque a a API utilizando o *sdk-demo-1.0.0.jar* com o token de acesso.
  
        java -jar sdk-demo-1.0.0.jar <access_token>

![scenariofive2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/sdk-response.png)

Info: **Sdk-demo-1.0.0.jar** *é montado utilizando o Java SDK baixado do Developer Portal. O usuário poderá checar o código fonte para esse programa no local /resources/sdk-demo*.

*Ao baixar o SDK direto do Developer Portal (ex: Java SDK), o usuário estará apto a montá-lo e utilizá-lo como uma dependência de seu próprio projeto. Nessa demonstração, o Java SDK para **QuantisTrainAPI** (QuantisTrainAPI_1.0.0_java.zip) foi usado e construído utilizando Apache Maven.*

*Então poderá ser adicionada a seguinte dependência ao projeto para importar o SDK.*

    <dependency>
    <groupId>org.wso2</groupId>
    <artifactId>org.wso2.client.QuantisTrainAPI</artifactId>
    <version>1.0.0</version>
    </dependency>

*O código de exemplo para invocar a API utilizando esse SDK pode ser encontrado em resources/sdk-demo/src/main/java/org/wso2/carbon/apimgt/tutorial/App.java.*

- [Índice](#documentação-api-manager-410)

### Cenário 6: Integrando com Data Sources
Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como integrar com Data Sources. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 5 minutos.

#### Contexto
O departamento de RH da RailCo está planejando desenvolver um sistema de planilha. Portanto, RailCo quer criar APIs REST para expor o banco de dados de funcionários como um serviço que os usuários podem adicionar, deletar, atualizar e ver detalhes dos empregados.

Com o Serviço de Dados WSO2 Micro Integrator, usuários podem integrar com diferentes fontes de dados e extrair dados de sua infraestrutura. Em outras palavras, quando o usuário criar um serviço de dados no WSO2 Micro Integrator, o dado que está armazenado no sistema de armazenamento (tipo os RDBMS) pode ser exposto na forma de um serviço. Isso permite que usuários (que podem estar em qualquer aplicação ou sistema) acessem o dado sem interagir com a fonte original do dado.

#### Passo 1: Desenvolvendo um serviço no Micro Integrator
Para desenvolver um serviço em Micro Integrator, o usuário poderá usar o WSO2 Integration Studio.

![scenariosix1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/integration_studio_dataservice.jpg)

#### Passo 2: Expondo um dado via API Manager
Uma vez desenvolvido, o usuário poderá expor dados via API Manager para um acesso seguro. Para simplificar, o serviço de dados já está desenvolvido e adicionado ao API Manager. Uma base de dados já foi criada com o nome fictício Employee Data que pode ser consultado e modificado.

![scenariosix2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/employee_database.png)

#### Passo 3: Invocando a API
Para invocar a API do API Manager:

1. Vá até o Developer Portal  https://localhost:9443/devportal/ e selecione o domínio de hospedagem RailCo. Isso irá redirecionar o usuário para o Developer Portal da RailCo.
2. Logue com um usuário do Developer Portal hóspede da RailCo. Utilize um usuário como *toma@railco.com* e senhar *user123*.
3. Clique em **RailCoEmployeeAPI** e clique em **Subscribe** usando uma apólice, e gere um token de acesso.
4. Após isso, o usuário poderá testar as operações CRUD na EmployeeAPI.

![scenariosix3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/employee_resources_apim.png)

Por exemplo, o usuário pode testar a seguinte requisição Curl:

    curl -k -X GET 'https://localhost:8243/t/railco.com/operations/data/employees/1.0.0/employees/2' \
    --header 'Accept: application/json' \
    --header 'Authorization: Bearer <Access Token>'

- [Índice](#documentação-api-manager-410)

### Cenário 7: Analytics
Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como instalar e visualizar análises para uma API. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 5 minutos.

#### Contexto
GOGO Transit identificou uma nova oportunidade de mercado, afinal o dado de chegada do trem contém o número de passageiro em cada chegada, assim o dado pode ser usado para prever a multidão de passageiros na estação em certo período do dia. Portanto, os serviços construídos ao redor da estação como lojas e serviços de transporte poderiam utilizar esse dado para otimizar o número de funcionários necessários para os serviços a cada dia. De ante disso, GOGO Transit decidiu fornecer a API com detalhes de passageiros para o público com a capacidade de inscrição que gere receita baseado no número de requerimentos bem sucedidos dentro de um período de tempo.

Choreo API-M Analytics pode ser usado para preencher as necessidades estatíticas e analíticas do API Manager. É uma oferta de análises na nuvem para o Choreo API Manager e implantações On-Prem API Manager.

![scenarioseven1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario7.png)

#### Passo 1: Configurando Analytics
*Antes de começar: O usuário precisa ser registrado para seguir os passos abaixo. Para instruções refira-se ao [Guia de Iniciação em Analytics](https://apim.docs.wso2.com/en/latest/api-analytics/getting-started-guide/).

Para configurar analíticas:
1. Inscreva-se em https://console.choreo.dev/login/.
2. Vá até https://console.choreo.dev/user-settings/onpremkeys e gere uma chave.
3. Abra o arquivo */dockerfiles/conf/apim/repository/conf/deployment.toml* e atualize a configuração [apim.analytics] como em seguida:

        [apim.analytics]
        enable = true
        config_endpoint = "https://analytics-event-auth.choreo.dev/auth/v1"
        auth_token = "<on prem key>"

4. Reinicie o container api-manager utilizando o seguinte comando:
  
        docker-compose restart api-manager

#### Passo 2: Teste
Vamos gerar algum tráfego. A API (**PassengerInfoAPI) foi implantada em um domínio de super hospedagem.
1. Vá até https://localhost:9443/devportal/ e selecione **carbon.super tenant domain**.
2. Logue usando usuário *peter* e senha *user123*, inscreva-se na API **PassengerInfoAPI** e gere um token de acesso.
3. Invoque a API usando o token.

        curl -X GET "https://localhost:8243/info/1.0.0/passenger-count" -H "accept: application/json" -H "Authorization: Bearer <token>" -k

Vá até [Choreo Insights](https://console.choreo.dev/insights) e veja as estatísticas. Abaixo seguem alguns gráficos.
![scenarioseven2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/usage-graph.png)
![scenarioseven3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/usage-ot-graph.png)
![scenarioseven4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/resp-time-graph.png)

- [Índice](#documentação-api-manager-410)

### Cenário 8: Limitação de Taxa
Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como configurar limitação de taxas para uma API. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 5 minutos.

#### Contexto
Enquanto analisava os dados de padrões de tráfego, o time de desenvolvedores da GOGO notou que o backend estava recebendo uma alta demanda de requisições e graças a essa alta demanda, os números de latência tinham aumentado. O time de desenvolvedores fez alguns testes de performance em seu backend de informações do usuário e identificou que os serviços de backend lidavam com o máximo de 1000 TPS. Então os gerenciadores da GOGO decidiram introduzir uma taxa limítrofe para coordenar seus usuários gratuitos.

![scenarioeight1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario8.png)

#### Passo 1: Aplicando uma Apólice de Limitação de Taxa
O WSO2 API Manager oferece vários níveis de limtação de rateio. Para esse caso, vamos aplicar **Subscription Rate Limiting Policy** e **Maximum Throughput** para o backend da PassengerInfoAPI.

Para cirar uma política de limitação de taxa em inscrição, faça o seguinte:

1. Logue no Admin Portal https://localhost:9443/admin utilizando *admin* e senha *admin*.
2. Navegue até **Rate Limiting Policies → Subscription Policies** e crie uma nova política. Em seguida um exemplo de apólice.

![scenarioeight2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/sample-policy.png)

3. Uma vez que a apólice é criada, para aplicá-la à API, logue no Publisher Portal utilizando *apiprovider* com a senha *user123* e vá até a seção **Develop → Portal Configuration → Subscription**.
4. Aplique a apólice para a PassengerInfoAPI e salve a API.

![scenarioeight3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/apply-policy.png)

5. Agora logue no Developer Portal e tente se subsescrever na API. Será notável que ela terá a nova apólice criada.
6. Inscreva-se na API utilizando essa apólice e invoque a API usando o token gerado.

![scenarioeight4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/subscribe-policy-api.png)

![scenarioeight5](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/invoke-policy-api.png)

7. Quando requisitar mais de 10 vezes, o usuário receberá uma mensagem de throttled-out.

![scenarioeight6](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/throttleout-api.png)

#### Passo 2: Definindo Taxa de Transferência Máxima
O usuário pode definir uma taxa de transferência máxima para o backend assim protegendo o backend de uma sobrecarga de requisições.

1. Logue no Publisher Portal e selecione a API, navegue até a seção **Develop → API Configurations → Runtime**.
2. Sob a seção **Backend**, o usuário pode definir o máximo de TPS para seu backend. Para essa demonstração, para ver o resultado rapidamente, vamos configurar para 1 TPS e salvar a API.

![scenarioeight7](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/max-throughput.png)

3. Para essa configuração surgir, o usuário precisa criar uma nova revisão para essa API. Para isso, vá até **Deploy → Deployments** e implante uma nova revisão.
4. Invoque a API em sucessão rápida (mais do que uma requisição por minuto). O usuário poderá usar tokens prévios para isso.

O usuário deve ver as requisições sendo impedidas com a seguinte mensagem.

    {
      "code": "900801",
      "message": "API Limit Reached",
      "description": "API not accepting requests"
    }

![scenarioeight8](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/throttleout-backend.png)

Isso demonstra que o API Manager está limitando as requisições ao backend.

- [Índice](#documentação-api-manager-410)

### Cenário 9: Realtime Data com WebSocket API

Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como trabalhar com dados em tempo real com um WebSocket API. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 5 minutos.

#### Contexto
Quantis quer promover uma localização em tempo real de seus trens para seus clientes. Os sensores nos trens vão fornecer eventos em tempo real e Quantis quer convertê-los para WebSockets e expor como uma Streaming API para que aplicações de aparelhos móveis de clientes possam se inscrever e receber tais eventos em tempo real.

![scenarionine1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario9.png)

WSO2 Streaming Integrator (SI) é um servidor de processamento de dado em streaming que integra dados em transmissão e toma ações baseado em dados em trasmissão. Quantis está planejando usar o Streaming Integrator para processar dados de eventos em tempo real.

#### Passo 1: Desenvolvendo um Serviço no Streaming Integrator
Para desenvolver um serviço no Streaming Integrator, o usuário necessitará usar as ferramentas Streaming Integrator. **Siddhi** é a ferramenta de processamento de evento que é usada dentro do Streaming Integrator. Para processar os WebSockets o usuário pode escrever o serviço em **linguagem Siddhi Query**. O usuário pode testar o serviço na própria ferramenta. Uma vez que o desenvolvimento estiver completo, o usuário poderá exportá-lo como um Siddhi app e aplicá-lo ao Streaming Integrator runtime.

![scenarionine2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/streaming_api_tooling.png)

Aqui, para simplificar, o serviço já está criado e exportado como SiddhiApp, e adicionado à instância do Streaming Integrator na configuração do tutorial. O usuário pode testar o serviço do Streaming Integrator ao invocá-lo diretamente. O usuário começa a receber eventos Realtime ao conectar um cliente WebSocket (o usuário pode utilizar [wscat](https://www.npmjs.com/package/wscat)).

      wscat -c ws://localhost:8025/ 

#### Passo 2: Expondo a WebSocket via API Manager

Uma vez que o usuário expôs os eventos via servidor WebSocket, ele pode expor as WebSockets com o API Manager como faria com outras APIs que oferecem **acesso seguro, limitação de rateio, throttling, monetização, analíticas**, etc. A API já está publicada no Developer Portal. Para invocar a API, o usuário pode seguir os passos abaixo:

1. Para se subscrever à WebSocket API, vá ao Developer Portal em https://localhost:9443/devportal/ e selecionando o domínio de hospedagem da Quantis (é necessário deslogar dos domínios prévios). Isso irá redirecionar o usuário para o Developer Portal da Quantis.
2. Inscrever-se com um usuário do Developer Portal da Quantis. Utilize o usuário tipo *bob@quantis.com* e senha tipo *user123*.
3. Clique em **TrainRealLocationAPI**, clique em **Subscribe** utilizando uma apólice e gere um token de acesso.

![scenarionine3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/realtime_api_devportal.png)
![scenarionine4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/realtime_api_subscriptions.png)

4. O usuário pode usar o token de acesso buscado acima para subscrever-se na localização do trem 456 (Topic: loc-train-qnt-456), utilizando um WebSocket client. Por exemplo, o usuário pode usar uma ferramenta wscat, subscreva-se como abaixo:

        wscat -c ws://localhost:9099/t/quantis.com/train/location/1.0.0/loc-train-qnt-456/ -H "Authorization: Bearer <Access Token>"

- [Índice](#documentação-api-manager-410)

### Cenário 10: Notificações Utilizando Webhooks
Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como trabalhar com notificações utilizando Webhooks. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 5 minutos.

#### Contexto
De tempos em tempos GOGO Transit oferece notificações para as companhias de trem (por exemplo, indisponibilidade de plataformas, taxas revisadas, etc). GOGO Transit está planejando oferecer essas informação como WebHooks para que as companhias de trem possam se subescrever nessas notificações sem requisitar continuosamente.

WebHooks permitem somente comunicações de uma via, de um app chamada web para outro app de chamada web. O cliente que intenciona receber os eventos do servidor/web app/publisher precisa registrar essa URL nos interessados pelo evento no publisher. Quando um evento ocorre, se um cliente está registrado para esse evento, o publisher fará uma requisição HTTP POST para a URL registrada do cliente assim notificando o evento.

![scenarioten1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario10.png)

O usuário pode ver a WebHook API criada na WSO2 API Manager indo no publisher (Super tenant - admin) https://localhost:9443/publisher/apis.

O usuário pode publicar notificações sob diferentes tópicos.

![scenarioten2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/notification_api_topics.png)

#### Passo 1: Subscrevendo em uma API
Para se subscrever na API, o usuário precisa ir ao Developer Portal.
1. Vá até o Developer Portal em  https://localhost:9443/devportal/ e selecione o tenant domain **Carbon.super**. Isso irá redirecioná-lo ao super tenant Developer Portal.
2. Inscreva-se com um usuário Super tenant no Developer Portal. Utilize um usuário como *peter* e senha *user123*.
3. Clique em **NotificationAPI**, clique em **Subscribe** utilizando uma apólice e gere um token de acesso.

#### Passo 2: Configurando Notificações
Para receber notificações, o usuário necessitará se registrar a um serviço que será chamado para cada evento.
1. Pode ser utilizado https://webhook.site/ para esse propósito. O usuário pode usar a URL única no site WebHook para subscrever a si mesmo no **general topic**.
2. Vá para a aba **Try out** e insira os seguintes detalhes sob o tópico **general**.

![scenarioten3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/notification_subscribe_devportal.png)

3. Clique em **Generate Curl**, copie o comando Curl, rode-o no seu terminal. Isso irá subscrever seu cliente (WebHook site) no API Manager. O usuário pode verificccar se a subscrição foi bem-sucedida ao checar o evento que foi recebido no WebHook site.

#### Passo 3: Enviando Notificações
Para enviar uma notificação, o usuário precisa reaver a URL de callback para um tópico do publisher.
1. Inscreva-se no publisher novamente com credenciais de usuário admin e selecione NotificationAPI.
2. O usuário pode conseguir a Callback URL ao visitar a aba de Tópicos, selecionando o tópico requerido. Já que foi subscrito ao tópico **general** acima, vamos reaver a URL para esse tópico.

![scenarioten4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/notification_topic_configuration.png)

3. Depois, o usuário precisa ir na seção do topo **Subscribe Configuration** e habilitá-la. Clique no botão **Generate** e gere um segredo. O usuário precisará desse segredo para calcular o valor hmac que poderá enviar no cabeçalho de requisição.

![scenarioten5](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/notification_topic_secret.png)

4. Digamos que iremos enviar esse payload abaixo:

       {"Message" : "Platform 12 on Braybrooke station will be closed for 2 hours on 2021-09-07T-15:50+00"}

5. O usuário necessitará calcular o valor para o payload acima utilizando o segredo que foi gerado no publisher. Isso pode ser feito no seguinte website: https://www.freeformatter.com/hmac-generator.html (Use SHA1).
6. Com o valor hmac derivado acima, o usuário pode invocar a requisição abaixo que enviará um evento no tópico **general**. Esse evento será recebido no WebHook site.

       curl -X POST 'http://localhost:9021/notification/1.0.0/webhooks_events_receiver_resource?topic=/general' \
        --header 'Accept: application/json' \
        --header 'x-hub-signature: sha1=<hmac value>' \
        --header 'Content-Type: application/json' \
        --data-raw '{"Message" : "Platform 12 on Braybrooke station will be closed for 2 hours on 2021-09-07T-15:50+00"}'

- [Índice](#documentação-api-manager-410)

### Cenário 11: Suporte GraphQL
Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como trabalhar com GraphSQL. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 5 minutos.

#### Contexto
Quantis está mais focada em oferecer maior capacidade para a comunidade de desenvolvedores. Eles esperam que a comunidade construa suas próprias aplicações móveis e web apps para usar suas APIs. Para tornar esse processo mais fácil, Quantis quer expor API GraphQL para o público.

![scenarioeleven1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario11.png)

#### Passo 1: Criando uma API GraphQL
WSO2 API Manager suporta a criação de APIs GraphQL utilizando o esquema GraphQL. Os passos seguintes podem ser usados para criar uma API de exemplo.

1. Logue no Publisher Portal  https://localhost:9443/publisher utilizando *apiprovider@quantis.com* e a senha *user123*.
2. Selecione **Create API → Import GraphQL SDL**.

![scenarioeleven2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/select-graphql.png)

3. Importe o **train.graphql** em **/resources** e crie a API. Use http://backend-service:8080/train-operations/graphql como a URL de endpoint para o backend.

![scenarioeleven3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/import-graphql.png)

#### Passo 2: Publicando e Testando a API
1. Implemente a API e a publique.
2. Vá ao Developer Portal e navegue até o domínio de hospedagem da Quantis. O usuário verá a API GraphQL no Developer Portal.

![scenarioeleven4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/view-graphql.png)

3. Logue no Developer Portal da Quantis usando *bob@quantis.com* com a senha *user123* e subscreva na API GraphQL utilizando uma aplicação e receba o token de acesso.
4. O usuário pode usar a aba **Try out** para testar essa API GraphQL. Em seguida está um exemplo de requisição de payload.

        schedules {
          entryId
          from
          to
          trainType 
          }
        }

O usuário receberá uma resposta como a mostrada abaixo:

![scenarioeleven5](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/response-graphql.png)

- [Índice](#documentação-api-manager-410)

### Cenário 12: Entrega de Mensagem Garantida
Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como garantir a entrega de mensagem. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 6 minutos.

#### Contexto
RailCo quer realizar uma parceria com a catering, um serviço de fornecimento de comida para passageiros de primeira classe. Para cada registro eles querem enviar uma entrada para o sistema de serviço da Catering. Entretanto, eles notaram que o sistema de serviço Catering fica indisponível de tempos em tempos. Para ter certeza que as entradas alcançarão o sistema da Catering, eles estão planejando implementar um sistema de Garantia de Entrega de Mensagens.

Armazenamento e envio de mensageria padrão é utilizado para assegurar a entrega garantida de mensagens. Mensagens nunca serão perdidas se elas estiverem armazenadas no armazém de mensagens e disponíveis para futura referência.

Isso será implementado com Message Store e Message Processor no Micro Integrator. Quando o sistema Catering estiver fora do ar, as mensagens serão armazenadas no Message Store. Quando o sistema voltar a ficar disponível novamente, as mensagens armazenadas serão enviadas ao sistema Catering.

![scenariotwelve1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario12.png)

Se o usuário observar o arquivo *docker-compose.yml* poderá notar que *CATERING_SERVICE_EP* está definido como *‘http://www.urldoesnotexist.com’* sob  *mi-runtime service*. Se o usuário enviar uma requisição para esse endpoint, ela falhará e a mensagem será armazenada na base de dados da Message Store.

#### Passo 1: Invocando a API
Para invocar a API, o usuário pode usar a seguinte curl:

    curl -X POST 'http://localhost:8290/catering/register' \
    --header 'Content-Type: application/json' \
    --data-raw '{
      "passengerId": "241241d",
      "class": "first",
      "train": "RLC-5051",
      "departure": {
        "time": "2021-07-16 11:45",
        "station": "King Cross"
      },
      "arrival": {
        "time": "2021-07-16 16:40",
        "station": "Edinburgh"
      },
      "duration": "4h 55m",
      "food": [
        {
          "serving": "lunch",
          "type": "Asian",
          "comments": [
            "Not too spicy"
            ]
          },
          {
          "serving": "snacks",
          "type": "Normal",
          "comments": []
          }
        ]
      }'

Se o usuário checar os logs do Micro Integrator, poderá ver que a invocação do backend falhou.

    “Message processor [CateringServiceForwardingProcessor] failed to forward message 4 times. Moved failed message to fail-messages-store and continue”

Após algum tempo, o Micro Integrator tentará enviar novamente a mensagem para o backend. Esse processo continuará até que a mensagem seja entregue com sucesso ao backend.

#### Passo 2: Assegurando Entrega Bem-Sucedida
Para obter sucesso na entrega, o usuário poderá providenciar um endpoint funcional e reiniciar o Micro Integrator. Isso irá enviar a mensagem acima para o backend.

Para testar esse fluxo o usuário poderá fazer o seguinte:

1. Criar um novo endpoint em  https://hookbin.com/ e fornecer o endpoint no arquivo *docker-compose.yml* sob *CATERING_SERVICE_EP*.
2. Reiniciar a execução do Micro Integrator usando o seguinte comando:

        docker-compose up -d --build mi-runtime

Agora se os logs do Micro Integrator forem checados, poderá ser avistado que a invocação foi bem sucedida.

    _Response = CateringServiceEP Reply Sequence Invoked, Payload: {"success":true}_

O usuário pode atualizar o site hookbin e ver que a mensagem agora foi captada.

- [Índice](#documentação-api-manager-410)

### Cenário 13: Integração com Serviços via Conectores
Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como usar conectores. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 10 minutos.

#### Contexto
RailCo está mantendo uma garagem para trens para sua manutenção de checagem rotineira de seus trens. Quando um trem vai para a garagem, um arquivo de entrada é criado em formato CSV. RailCo quer gerar um email a partir desse arquivo, e eles planejam usar o Micro Integrator e seu conector de email para conseguir isso.

Quando o usuário integra os sistemas de sua organização, ele também necessariamente integra com sistemas de terceiros e suas capacidades para elevar seus serviços. WSO2 Micro Integrator usa Conectores para o propósito de referenciamento para APIS de sistemas de terceiros.

![scenariothirteen1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario13.png)

Para desenvolver o serviço o usuário pode usar o Integrator Studio, onde ele poderá importar e compactar o conector com a aplicação Composite. Para buscar por um arquivo, ele pode usar um Inbound Endpoint, que estará escoltando uma locação em particular já fornecida. Uma vez que o arquivo é adicionado a essa locação ele irá puxar o arquivo e processá-lo. Inbound Endpoints suportam diversos protocolos tais quais HTTP, JMS, RabbitMQ, WebSocket, etc.

Enquanto desenvolve, o usuário pode testar no Embedded Micro Integrator dentro do Studio. Uma vez que o desenvolvimento está completo, ele pode exportá-lo como uma aplicação Compose e adicioná-lo ao Micro Integrator runtime.

#### Passo 1: Criando e Configurando o Serviço
![scenariothirteen2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/integration_studio_connectors.png)

Aqui, para simplificar, o serviço já foi criado e exportado como uma aplicação Compose junto com o conector. Antes de adicionar o serviço ao sistema, o usuário precisa fazer o seguinte:

1. Criar um diretório temporário na sua máquina e criar três subdiretórios dentro dele chamados **in, out** e **error**.
2. Apague a seção volume sob *mi-runtime* em *docker-compose.yml* e forneça o local do diretório temporário mudando a tag *<SourceLocation\>*.

        # volumes:
        #   - <SourceLocation>:/home/wso2carbon/sample

3. Para enviar um email, o usuário precisa ter um servidor SMTP. Apague as seguintes variáveis de ambiente sob *_mi-runtime_* e preencha os detalhes:

        #   SMTP_HOST: <SMTP_Host>
        #   SMTP_PORT: <SMTP_Port>
        #   SMTP_USERNAME: <SMTP_Server_Username>
        #   SMTP_PASSWORD: <SMTP_Server_Password>
        #   EMAIL_TO: <To_Address>
        #   EMAIL_FROM: <From_Address>

4. Após 










- [Índice](#documentação-api-manager-410)
### Cenário 14: Suporte de Gerenciamento de Chaves Externas
- [Índice](#documentação-api-manager-410)

## Tutoriais API Management
A lista de tutoriais seguinte guia o usuário a criar pela primeira vez uma API gerenciada e expô-la ao mercado de APIs.

### Criar e Publicar uma GraphQL API
### Criar e Publicar uma AWS Lambda API
### Expor um Serviço SOAP como uma REST API
### Criar e Publicar uma WebSocket API
### Criar e Publicar um WebSub API (WebHook API)
### Criar e Publicar uma SSE API
### Editar uma API Modificando a Definição da API

## Tutoriais de Integração
Os tutoriais de integração guiam o usuário através das principais capacidades e ferramentas de Micro Integrator, auxiliando o entendimento sobre a construção de um sistema integrado.

### Enviando uma Mensagem Simples para um Serviço
### Roteando Requests baseados em Cabeçalhos de Mensagem
### Traduzindo Formatos de Mensagem
### Expondo Serviços Diversos como Serviço Único
### Guardar e Encaminhar Mensagens para Entrega Garantida
### Expondo Datasources como um Serviço
### Processamento de Arquivo
### Execução Periódica de Processo de Integração
### Utilizando Inbound Endpoints
### Reutilizando Sequências de Mediação
### Enviando Emails por um Serviço de Integração
### Expondo um Serviço de Integração como uma API Gerenciada
### Expondo um Serviço de Integração SOAP como uma API Gerenciada
### Integrando com SAP

## Tutoriais de Integração Streaming
Os tutoriais de streaming guiam o usuário através das principais capacidades e ferramentas do Streaming Integrator, auxiliando o entendimento sobre a construção com aplicações Streaming.

### Expondo um Kafka Stream como um WebSocket API Gerenciada
### Executando Mudança de Captura de Dado em Tempo Real com MySQL
### Executando ETL em Tempo Real com Arquivos
### Criando uma Aplicação ETL via SI Tooling
### Trabalhando com Kafka
### Trabalhando com Business Rules
### Integrando Stores
### Expondo Processed Data como API
### Tratamento de Erro com Data Stream
### Engatilhando Fluxos de Intregração
### Operando o Streaming Integrator em Ambientes Conteinerizados
