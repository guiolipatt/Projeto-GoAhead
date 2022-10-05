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
    - [Cenário 9: Realtime Data com WebSocket API](#cenário-9-realtime-data-com-websocket-api)
    - [Cenário 10: Notificações Utilizando Webhooks](#cenário-10-notificações-utilizando-webhooks)
    - [Cenário 11: Suporte GraphQL](#cenário-11-suporte-graphql)
    - [Cenário 12: Entrega de Mensagem Garantida](#cenário-12-entrega-de-mensagem-garantida)
    - [Cenário 13: Integração com Serviços via Conectores](#cenário-13-integração-com-serviços-via-conectores)
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





### Cenário 9: Realtime Data com WebSocket API
### Cenário 10: Notificações Utilizando Webhooks
### Cenário 11: Suporte GraphQL
### Cenário 12: Entrega de Mensagem Garantida
### Cenário 13: Integração com Serviços via Conectores
### Cenário 14: Suporte de Gerenciamento de Chaves Externas

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
