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
      - [Contexto](#contexto-13)
      - [Passo 1: Configurando o Keycloak](#passo-1-configurando-o-keycloak)
      - [Passo 2: Configurando a Conexão ao Keycloak](#passo-2-configurando-a-conexão-ao-keycloak)
      - [Passo 3: Invocando a API](#passo-3-invocando-a-api-1)
  - [Tutoriais API Management](#tutoriais-api-management)
    - [Criar e Publicar uma GraphQL API](#criar-e-publicar-uma-graphql-api)
      - [Passo 1: Iniciando o Servidor Backend do GraphQL](#passo-1-iniciando-o-servidor-backend-do-graphql)
      - [Passo 2: Criando uma GraphQL API](#passo-2-criando-uma-graphql-api)
      - [Passo 3: Implantando uma GraphQL API](#passo-3-implantando-uma-graphql-api)
      - [Passo 4: Publicando a GraphQL API](#passo-4-publicando-a-graphql-api)
      - [Passo 5: Invocando a GraphQL API](#passo-5-invocando-a-graphql-api)
      - [Passo 5.1: Experimentando uma Query operation](#passo-51-experimentando-uma-query-operation)
      - [Passo 5.2: Experimentando uma Subscription Operation](#passo-52-experimentando-uma-subscription-operation)
    - [Criar e Publicar uma AWS Lambda API](#criar-e-publicar-uma-aws-lambda-api)
      - [Passo 1: Criando uma REST API](#passo-1-criando-uma-rest-api)
      - [Passo 2: Adicionando uma AWS Lambda Endpoint](#passo-2-adicionando-uma-aws-lambda-endpoint)
      - [Passo 3: Mapeando Função ARNs para Recursos](#passo-3-mapeando-função-arns-para-recursos)
      - [Passo 4: Implantando e Publicando a AWS Lambda API](#passo-4-implantando-e-publicando-a-aws-lambda-api)
    - [Expor um Serviço SOAP como uma REST API](#expor-um-serviço-soap-como-uma-rest-api)
      - [Passo 1: Criando um serviço SOAP como uma REST API](#passo-1-criando-um-serviço-soap-como-uma-rest-api)
      - [Passo 2: Invocando um serviço SOAP como uma REST API](#passo-2-invocando-um-serviço-soap-como-uma-rest-api)
    - [Criar e Publicar uma WebSocket API](#criar-e-publicar-uma-websocket-api)
      - [Passo 1: Criando uma WebSocket API](#passo-1-criando-uma-websocket-api)
      - [Passo 2: Publicando a WebSocket API](#passo-2-publicando-a-websocket-api)
      - [Passo 3: Iniciando o WebSocket Server](#passo-3-iniciando-o-websocket-server)
      - [Passo 4: Invocando a WebSocket API](#passo-4-invocando-a-websocket-api)
      - [Soluções de Problemas](#soluções-de-problemas)
    - [Criar e Publicar uma WebSub/WebHook API](#criar-e-publicar-uma-websubwebhook-api)
      - [Passo 1: Criando uma WebSub/WebHook API](#passo-1-criando-uma-websubwebhook-api)
      - [Passo 2: Encaminhando uma URL Pública](#passo-2-encaminhando-uma-url-pública)
      - [Passo 3: Adicionando uma WebHook para o seu Repositório GitHub](#passo-3-adicionando-uma-webhook-para-o-seu-repositório-github)
      - [Passo 4: Publicando a API WebSub/WebHook](#passo-4-publicando-a-api-websubwebhook)
      - [Passo 5: Criando uma Callback URL](#passo-5-criando-uma-callback-url)
      - [Passo 6: Invocando a API WebSub/WebHook](#passo-6-invocando-a-api-websubwebhook)
    - [Criar e Publicar uma Server Sent Events API](#criar-e-publicar-uma-server-sent-events-api)
      - [Passo 1: Criando a SSE API](#passo-1-criando-a-sse-api)
      - [Passo 2: Publicando a SSE API](#passo-2-publicando-a-sse-api)
      - [Passo 3: Iniciando o SSE Server](#passo-3-iniciando-o-sse-server)
      - [Passo 4: Invocando a SSE API](#passo-4-invocando-a-sse-api)
    - [Editar uma API Modificando a Definição da API](#editar-uma-api-modificando-a-definição-da-api)
  - [Tutoriais de Integração](#tutoriais-de-integração)
    - [Enviando uma Mensagem Simples para um Serviço](#enviando-uma-mensagem-simples-para-um-serviço)
      - [Contexto](#contexto-14)
      - [Conceitos e Artefatos Usados](#conceitos-e-artefatos-usados)
      - [Passo 1: Configurar o Workspace](#passo-1-configurar-o-workspace)
      - [Passo 2: Desenvolva os Artefatos de Integração](#passo-2-desenvolva-os-artefatos-de-integração)
      - [Passo 3: Empacotar os Artefatos](#passo-3-empacotar-os-artefatos)
      - [Passo 4: Construir e Rodar os Artefatos](#passo-4-construir-e-rodar-os-artefatos)
      - [Passo 5: Teste o Estudo de Caso](#passo-5-teste-o-estudo-de-caso)
    - [Roteando Requests baseados em Cabeçalhos de Mensagem](#roteando-requests-baseados-em-cabeçalhos-de-mensagem)
      - [Contexto](#contexto-15)
      - [Conceitos e Artefatos Usados](#conceitos-e-artefatos-usados-1)
      - [Passo 1: Configurar o Workspace](#passo-1-configurar-o-workspace-1)
      - [Passo 2: Desenvolva os Artefatos de Integração](#passo-2-desenvolva-os-artefatos-de-integração-1)
      - [Passo 3: Empacotar os Artefatos](#passo-3-empacotar-os-artefatos-1)
      - [Passo 4: Construa e Rode os Artefatos](#passo-4-construa-e-rode-os-artefatos)
      - [Passo 5: Teste o Estudo de Caso](#passo-5-teste-o-estudo-de-caso-1)
    - [Traduzindo Formatos de Mensagem](#traduzindo-formatos-de-mensagem)
      - [Contexto](#contexto-16)
      - [Passo 1: Configurar o Workspace](#passo-1-configurar-o-workspace-2)
      - [Passo 2: Desenvolva os Artefatos de Integração](#passo-2-desenvolva-os-artefatos-de-integração-2)
      - [Passo 3: Empacotar os Artefatos](#passo-3-empacotar-os-artefatos-2)
      - [Passo 4: Construa e Rode os Artefatos](#passo-4-construa-e-rode-os-artefatos-1)
      - [Passo 5: Teste o Estudo de Caso](#passo-5-teste-o-estudo-de-caso-2)
    - [Expondo Serviços Diversos como Serviço Único (Orquestração de Serviço)](#expondo-serviços-diversos-como-serviço-único-orquestração-de-serviço)
      - [Contexto](#contexto-17)
      - [Conceitos e Artefatos Usados](#conceitos-e-artefatos-usados-2)
      - [Passo 1: Configurar o Workspace](#passo-1-configurar-o-workspace-3)
      - [Passo 2: Desenvolva os Artefatos de Integração](#passo-2-desenvolva-os-artefatos-de-integração-3)
      - [Passo 3: Empacotar os Artefatos](#passo-3-empacotar-os-artefatos-3)
      - [Passo 4: Construa e Rode os Artefatos](#passo-4-construa-e-rode-os-artefatos-2)
      - [Passo 5: Teste o Estudo de Caso](#passo-5-teste-o-estudo-de-caso-3)
    - [Guardar e Encaminhar Mensagens para Entrega Garantida](#guardar-e-encaminhar-mensagens-para-entrega-garantida)
      - [Contexto](#contexto-18)
      - [Passo 1: Configurar o Workspace](#passo-1-configurar-o-workspace-4)
      - [Passo 2: Desenvolva os Artefatos de Integração](#passo-2-desenvolva-os-artefatos-de-integração-4)
      - [Passo 3: Empacotar os Artefatos](#passo-3-empacotar-os-artefatos-4)
      - [Passo 4: Inicie o RabbitMQ Broker](#passo-4-inicie-o-rabbitmq-broker)
      - [Passo 5: Construa e Rode os Artefatos](#passo-5-construa-e-rode-os-artefatos)
      - [Passo 6: Teste o Estudo de Caso](#passo-6-teste-o-estudo-de-caso)
    - [Expondo Datasources como um Serviço](#expondo-datasources-como-um-serviço)
      - [Contexto](#contexto-19)
      - [Passo 1: Configurar o Workspace](#passo-1-configurar-o-workspace-5)
      - [Passo 2: Criando um Data Service](#passo-2-criando-um-data-service)
      - [Passo 3: Empacotar os Artefatos](#passo-3-empacotar-os-artefatos-5)
      - [Passo 4: Configurando o Servidor Micro Integrator](#passo-4-configurando-o-servidor-micro-integrator)
      - [Passo 5: Construa e Rode os Artefatos](#passo-5-construa-e-rode-os-artefatos-1)
      - [Passo 6: Testando o Data Service](#passo-6-testando-o-data-service)
    - [Processamento de Arquivo](#processamento-de-arquivo)
      - [Contexto](#contexto-20)
      - [Passo 1: Configurar o Workspace](#passo-1-configurar-o-workspace-6)
      - [Passo 2: Desenvolva os Artefatos de Integração](#passo-2-desenvolva-os-artefatos-de-integração-5)
      - [Passo 3: Empacotar os Artefatos](#passo-3-empacotar-os-artefatos-6)
      - [Passo 4: Configure o Servidor Micro Integrator](#passo-4-configure-o-servidor-micro-integrator)
      - [Passo 5: Construa e Rode os Artefatos](#passo-5-construa-e-rode-os-artefatos-2)
      - [Passo 6: Teste o Estudo de Caso](#passo-6-teste-o-estudo-de-caso-1)
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

4. Após isso, é necessário adicionar o *EmailService* CApp ao Micro Integrator no setup. Para fazer isso descomente a seguinte linha no arquivo Dockerfile encontrado dentro de *<REPO_HOME>/dockerfiles/micro-integrator/.*

        # # Uncomment when trying out Guaranteed Message Delivery Scenario
        # COPY carbonapps/RailCoFileEmailServiceCompositeExporter_1.0.0-SNAPSHOT.car ${WSO2_SERVER_HOME}/repository/deployment/server/carbonapps/

5. Agora é possível reiniciar o Micro Integrator:
        
        docker-compose up -d --build mi-runtime

6. Uma vez reiniciado, o usuário pode colocar o arquivo .csv dentro do diretório \*\*in*\* dentro de sua locação temporária. É possível usar o arquivo *train-entry-sample.csv* encontrado no diretório <REPO_HOME>/resources para esse propósito. Uma vez adicionado, o arquivo será selecionado pelo Micro Integrator e enviado como um email para o endereço que foi configurado acima.

- [Índice](#documentação-api-manager-410)

### Cenário 14: Suporte de Gerenciamento de Chaves Externas
Esse tutorial é parte de uma série e pode ser utilizado como um tutorial por si só em como configurar um Key Manager. Para mais detalhes nesse cenário e pré-requisitos gerais, acesse a [página da visão geral de cenário](https://apim.docs.wso2.com/en/latest/tutorials/scenarios/scenario-overview/).

- Tempo Estimado: 5 minutos.

#### Contexto
RailCo tem usuários em seu sistema de gerenciamento de identidade interno. Eles não querem ter duplicatas de informações de usuários em dois sistemas. RailCo quer usar seu IDP para gerar tokens de acesso para consumir suas APIs sem ter que importar seus usuários para a plataforma de API da GOGO train.

WSO2 API Manager vem com conectores de gerenciadores de chaves externas prontos para uso para vários provedores de identidade como Okta, Auth0, Keycloak, etc. Além disso, ele oferece interfaces para escrever implementações personalizadas ao Key Manager para plugar qualquer solução Key Manager de terceiros.

Para esse cenário, nós assumimos que RailCo tem Keycloak IDP como seu provedor de identidade interno. Em seguida estão os passos para configurar o Keycloak IDP como o gerenciador de chave externo para a RailCo.

![scenariofourteen1](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenario-tutorials/scenario14.png)

#### Passo 1: Configurando o Keycloak
O passos a passo detalhado em como configurar o Keycloak pode ser encontrando na [Documentação WSO2](https://apim.docs.wso2.com/en/latest/administer/key-managers/configure-keycloak-connector/). Adicionalmente, o usuário pode usar como referência esse [vídeo](https://www.youtube.com/watch?v=xuZ6DPhXNX8). Abaixo segue o passo a passo simplificado para a instalação.

1. Download o Keycloak Server através de https://www.keycloak.org/downloads. A versão usada nesse tutorial é keycloak 12.0.4.
2. Extraia para o local de instalação e navegue até *\<keycloak>/bin* e rode *./standalone.sh* para iniciar o servidor.
3. Vá até http://localhost:8080/. Se essa é a primeira vez, crie u usuário admin inicial do formulário dado nessa página.
4. Rode o seguinte comando. Mude o usuário admin e a senha. Isso rodará um script no keycloak para gerar aplicação no keycloak.
          
        docker run -e USER=<admin_username> -e PASSWORD=<admin_password> chamilaadhi/keycloak-apim-script:1.0.0

Se a execução tiver sucesso, o usuário receberá uma client ID e um client secret para usar com o WSO2 API Manager:

    client id    :  apim-client

    client secret:  221f10b7-d169-45e0-851e-e1b017052162



**Observação:** *O script usado nesse Docker container para criar as credenciais pode ser encontrado no arquivo /resource/setup-keycloak.sh*.

#### Passo 2: Configurando a Conexão ao Keycloak
Agora iremos configurar a conexão entre o API-M e Keycloak

1. Logue no Admin Portal https://localhost:9443/admin/ utilizando o usuário admin RailCo. Use *admin@railco.com* e *admin* como senha.
2. Vá até **Key Managers** e selecione **Add Keymanagers**.
3. Adicione um nome compatível e nome de exibição.
4. Selecione o **Key Manager Type** como **Keycloak** do menu.
5. Use http://host.docker.internal:8080/auth/realms/master/.well-known/openid-configuration no campo **Well-known URL** e clique em **Import**. Isso irá preencher os outros campos requeridos.
6. Coloque http://host.docker.internal:8080/auth/realms/master/protocol/openid-connect/revoke em **Revoke Endpoint** se esse campo estiver vazio.
7. Sob a seção **Connector Configurations**, coloque o **client id** e **secret** dados na execução do script.

![scenarionfourteen2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/connector-config.png)

Agora o Key Manager está configurado.

#### Passo 3: Invocando a API
Vamos invocar uma API usando um token gerado pelo Keycloak.

1. Logue no domínio de hospedaem no Developer Portal da RailCo  https://localhost:9443/devportal/ utilizando *tom@railco.com* e a senha *user123*.
2. Vá até a página de **Aplications** e selecione **KeyCloakAPP**. Essa aplicação já está subscrita na **RailCoTrainAPI**.
3. Selecione **Production Keys → OAuth2 Tokens**. O usuário verá uma aba para **Keycloak**.

![scenariofourteen3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/scenarios/keycloak-app.png)

4. Clique em **Generate Keys** para gerar um token. Valores pré definididos devem bastar para gerar um token de acesso para esse cenário.
5. Invoque a API usando esse token.

- [Índice](#documentação-api-manager-410)

## Tutoriais API Management
A lista de tutoriais seguinte guia o usuário a criar pela primeira vez uma API gerenciada e expô-la ao mercado de APIs.

### Criar e Publicar uma GraphQL API
Siga as instruções nesse tutorial para criar, publicar e invocar uma GraphQL API.

**Observação**: Para mais informações sobre GraphQL APIs, veja em [Criando uma GraphQL API](https://apim.docs.wso2.com/en/latest/design/create-api/create-a-graphql-api/).

#### Passo 1: Iniciando o Servidor Backend do GraphQL
Vamos usar o exemplo do servidor backend de Star Wars como o backend para a GraphQL API.

1. Clone o repositório [WSO2 API Manager Samples](https://github.com/wso2/samples-apim).

        git clone https://github.com/wso2/samples-apim

2. Navegue até o diretório *graphql-backend*.

        cd samples-apim/graphql-backend

3. Execute *npm install* para instalar os módulos de node necessários.
4. Rode *npm start* para iniciar o servidor.
5. Uma vez completados os passos acima, o servidor Star Wars estará rodando em http://localhost:8080. ![tam1-1](https://apim.docs.wso2.com/en/latest/assets/img/learn/cli-output.png) O usuário poderá usar o http://localhost:8080/graphql como endpoint quando criar a GraphQL API.
#### Passo 2: Criando uma GraphQL API
1. Logue na API Publisher Portal (https://\<hostname>:9443/publisher). Como exemplo: https://localhost:9443/publisher
Vamos utilizar *admin* como nome de usuário e senha para se inscrever.
2. Clique em **Create API** e então clique em **Import GraphQL SDL**.![tam1-2](https://apim.docs.wso2.com/en/latest/assets/img/learn/create-graphql-schema-option.png)
3. Importe o esquema ao arrastar e soltar o arquivo ou upando o arquivo, então clique em **Next**. Vamos utilizar as [definições de esquema da StarWars API](https://apim.docs.wso2.com/en/latest/assets/attachments/learn/schema_graphql.graphql).

    **Observação:**
   - O usuário precisa definir o SDL Schema baseado no [GraphQL schema design best practices](https://leapgraph.com/graphql-schema-design-best-practices). 
   - A extensão do arquivo pode ser tanto *.graphql* , *txt* , ou *.json*.
   - O nome do arquivo pode ser qualquer um da preferência do usuário. ![tam1-3](https://apim.docs.wso2.com/en/latest/assets/img/learn/import-graphql-schema-via-file.png)

4. Entre nos detalhes relativos a GraphQL API e clique em **Create**. Vamos criar uma API chamada **StarWarsAPI** utilizando os dados seguintes como exemplo.

    Field | Description |
    :---: |:---:|
    Name | StarWarsAPI
    Context | */swapi*
    Version | 1.0.0
    Endpoint | http://localhost:8080/graphql

    **Observação:**
    - Quando você provê a HTTP URL como o endpoint do backend, WSO2 API-M vai internamente derivar a WebSocket URL correspondente *ws://localhost:8080/graphql* .
   - Portanto, o API Gateway vai utilizar essa WebSocket URL como endpoint subscrito do backend da GraphQL API. ![tam1-4](https://apim.docs.wso2.com/en/latest/assets/img/learn/create-graphql-api-details.png)
5. Opcionalmente, modifique o esquema de definição da GraphQL existente.
   1. Navegue até **Develop → API Configurations** e clique em **Schema Definition**.
   2. Clique em **Download Definition**. O esquema de GraphQL API existente será baixado. ![tam1-5](https://apim.docs.wso2.com/en/latest/assets/img/learn/download-schema-definition.png) 
   3. Atualize a definição de esquema como requerido.
   4. Clique em **Import Definition** para importar o esquema de definição atualizado.
6. Atualize as operações GraphQL API como requisitado. Invés de recursos, que ficam populadas em REST APIs, operações ficam populadas em GraphQL APIs.
    1. Clique em **Show More** sob a seção **Operations** na página **Overview** para navegar até a página de operações. ![tam1-6](https://apim.docs.wso2.com/en/latest/assets/img/learn/operations.png)
    2. Atualize as operações como requisitado. O Publisher pode adicionar políticas de limitação de taxas, escopos e habilitar/desabilitar segurança para cara operação da GraphQL API.
7. Criando Scopes

   Repita o seguintes passos abaixo para criar dois escopos nomeados de *adminScope* e *FilmSubscriberScope* .        
     1. Clique em **Local Scopes**, e então clique em **Create Scopes**. ![tam1-6](https://apim.docs.wso2.com/en/latest/assets/img/learn/add-scope.png)
     2. Entre com os detalhes requisitados.
      
        **Observação:**
        - A função que o usuário entrará deve ser uma função válida que já existe no WSO2 API Manager. Tenha certeza que designou uma função ao seu usuário.
        - Para mais informações, veja [Adicionando Usuários](https://apim.docs.wso2.com/en/latest/administer/managing-users-and-roles/managing-users/) e [Adicionando Funções a Usuários](https://apim.docs.wso2.com/en/latest/administer/managing-users-and-roles/managing-user-roles/).
      
     3. Entre com os detalhes seguintes para esse cenário de exemplo.

        Name | Role |
        :--: |:--: |
        *FilmSubscriber*|*FilmSubscriber
        adminScope|admin
      
        ![tam1-7](https://apim.docs.wso2.com/en/latest/assets/img/learn/create-scope.png)
      4. Pressione **Enter** para adicionar cada função.
      5. Clique em **Save**.![tam1-8](https://apim.docs.wso2.com/en/latest/assets/img/learn/starwars-scope-list.png)
8. Definindo as Configurações de Nível de Operação
   1. Clique em **Operations**.
   2. Clique em **Operation Level** para aplicar Rate Limiting para operações.![tam1-9](https://apim.docs.wso2.com/en/latest/assets/img/learn/update-operations.png)
   3. Selecione uma Rate Limiting Policy, Scope, e habilite ou desabilite a segurança para cada uma das operações. Aplique os seguintes escopos para as respectivas operações:
  
      Operation | Scope
      :--:|:---:
      *allDroids*|*FilmSubscriber*
      *allCharacters*|*adminScope*|
   
   4. Clique em **Save**. Se o usuário checar a lista de escopos, ela deve aparecer dessa forma: ![tam1-10](https://apim.docs.wso2.com/en/latest/assets/img/learn/scope-list.png) Dessa forma a GraphQL API foi criada e configurada com sucesso.

#### Passo 3: Implantando uma GraphQL API
1. Navegue até **Deploy** e clique em **Deployments** para navegar até a página **Deploy the API**.
2. Clique em **Deploy** para implantar a API no API Gateway, o portal padrão.![tam1-11](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/deploy-graphql-api.png)
3. A página de **Deployments** aparecerá:![tam1-12](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/graphql-api-revision-1.png)

#### Passo 4: Publicando a GraphQL API
1. Navegue até **Publish** e clique em **Lifecycle**. A página **API Lifecycle** aparecerá.
2. Clique em **Publish** para publicar a API no **API Developer Portal**. ![tam1-13](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/publish-graphql-api.png)
 
#### Passo 5: Invocando a GraphQL API

1. Se inscreva no **Developer Portal**: (https://\<hostname>:9443/devportal). Por exemplo https://localhost:9443/devportal . Utilize *admin* como nome de usuário e senha para se inscrever.![tam1-14](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/starwars-in-dev-portal.png)
2. Clique na GraphQL API. A visão geral da API aparecerá:![tam1-15](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/create-and-publish-a-graphql-api/api-overview.png)
  
  **Observação:**
  - Note que tanto as URLs HTTP quanto a WebSocket do Gateway são mostradas pelas GraphQL API.
  - A URL HTTP do Gateway serve para invocar a query e mutation operations da GraphQL API.
  - A URL Websocket do Gateway serve para invocar as subscription operations da GraphQL API.
3. Subscreva na API.
   1. Clique em **Try out**. Isso criará a subscrição para a aplicação nomeada *DefautlApplication* e gerar uma consumer key e um par de consumer secret para *DefaultApplication*. Clique em **TRY OUT** no menu pop-up para navergar até o **Try Out Console**.

![tam1-16](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/create-and-publish-a-graphql-api/try-out-graphql-popup.png)

4. Experimente as operações.
   1. Clique em **GET TEST KEY**. 

![tam1-17](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/get-test-key-starwars.png)

#### Passo 5.1: Experimentando uma Query operation

  **Observação:**
   - Se você invocará uma operação de consulta, você deve iniciar o payload com a palavra chave "query".
   - Se você invocará uma operação de mutação, vocẽ deve iniciar o payload com a palavra chave "mutation".
  
  1. Entre com o seguinte payload de exemplo como request da StarWarsAPI. Então clique no botão de execução como segue abaixo: 
           
         query{
          human(id:1000){
            id
            name
          }
          droid(id:2000){
            name
            friends{
              name
              appearsIn
            }
          }
          
![tam1-18](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/create-and-publish-a-graphql-api/graphql-console-execute-query.png)

2. Clique em **Execute**. 

![tam1-19](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/graphql-response-query.png)

#### Passo 5.2: Experimentando uma Subscription Operation
**Observação:**
Se você invocará uma operação de subscrição, você deve iniciar o payload com a palavra chave *subscription*.

1. Entre com o exemplo seguinte payload com a request de subscrição na *reviewAdded* da StarWarsAP para receber atualizações em tempo real sobre a adição de novas reviews.
 
        subscription {
          reviewAdded(episode: JEDI) {
            stars
            episode

            commentary
           }
        }

2. Prepare-se para inspecionar as chamadas de network pelas ferramentas de desenvolvedores de seu navegador. Por exemplo, se estiver usando o navegador Google Chrome.
   1. Clique com o botão direito no navegador e clique em **Inspect**.
   2. Clique em **Network** para ver as chamadas network via ferramentas de desenvolvedores do navegador.
3. Clique em **Executar**. Se você inspecionar as chamadas network das ferramentas de desenvolvedores do seu navegador, você poderá ver as mensagens passarem entre o cliente GraphQL e o backend. 
  ![tam1-20](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/create-and-publish-a-graphql-api/graphql-sub-init-response.png)
  Como pode ser visto, uma conexão WebSocket bem sucedida é estabelecida entre o client e o backend via WSO2 API Gateway.
4. Enquanto a página do navegador é mantida aberta no Developer Portal, separadamente abra um termina e invoque diretamente a mutação de operação *createReview* do backend da API ao executar o seguinte comando:

       curl -X POST "http://localhost:8080/graphql" -H  "accept: application/json" -H  "Content-Type: application/json" -d '{"query":"mutation {createReview(episode: JEDI, review: { stars: 3, commentary: \"Excellent\"}) { stars   episode   commentary }}","variables":null}' -k
    Quando a mutação tiver sucesso, a seguinte resposta será enviada ao backend da GraphQL:

        {"data":{"createReview":{"stars":3,"episode":"JEDI","commentary":"Excellent"}}}
5. Agora retorne à página do navegador do Developer Portal. Você poderá ver que recebeu a resposta ao evento de subscrição que corresponde à operação de mutação feita em passos anteriores. 
![tam1-21](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/create-and-publish-a-graphql-api/try-out-sub-event.png)
Você criou com suceso e publicou sua primeira GraphQl APi, se subscreveu nela, obteve um token de acesso para testá-la, e testou operações de query e subscription da sua API com o token de acesso.
- [Índice](#documentação-api-manager-410)

### Criar e Publicar uma AWS Lambda API
Ao utilizar o AWS Lambda, você pode executar seu código sem ter que gerenciar ou prover servidores. Para mais informações sobre AWS Lambda, veja [O Que é AWS Lambda?](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html). WSO2 API Manager tem integrado o suporte para a invocação de funções AWS Lambda através do WSO2 API Gateway para receber os benefíios da AWS Lambda. Siga os passos abaixo para criar e publicar uma API AWS Lambda.
#### Passo 1: Criando uma REST API
1. Inscreva-se no Publisher Portal da API em https://\<hostname>:9443/publisher .
2. Clique em **CREATE API** e então clique em **Start From Scratch**. ![tam2-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/create-lambda-api.png)
3. Entre com os detalhes da API sem um endpoint URL, e clique em **Create**. ![tam2-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/create-lambda-api-details.png)
#### Passo 2: Adicionando uma AWS Lambda Endpoint
1. Clique em **Endpoints** para navegar até a página Endpoints.
2. Navegue até o tipo **AWS Lambda Endpoint** e clique em **ADD**. ![tam2-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/endpoint-select-awslambda-endpoint.png)
3. Selecione o **Access Method** preferido. AWS SDK necessita de credenciais AWS e região AWS para invocar funções AWS Lambda. O método de acesso define como você proverá essas credenciais AWS. Há duas maneiras que você pode selecionar isso:
    - **Usando credenciais AWS temporárias IAM role-supplied**: se o API Manager está rodando em uma instância AWS EC2 ou ECS, é recomendado selecionar esse método. Você precisa anexar uma função IAM com as permissões *AWSLambda_ReadOnlyAccess* e *AWSLambdaRole* para a instância para assim garantir permissão para a aplicação listar e invocar funções Lambda. Para mais informações em como anexar uma função IAM para EC2, veja [Usando uma IAM Role para Garantir Permissões a Aplicações Rodando em Instâncias Amazon EC2](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_use_switch-role-ec2.html).
    - **Usando credenciais AWS armazenadas**: se o API Manager não está rodando em uma instância AWS, selecione esse método. Note que ele não é recomendado para entrar em credenciais root da conta AWS. Invés disso, crie uma conta de usuário separada com as permissões *AWSLambda_ReadOnlyAccess* e *AWSLambdaRole* e entre com as credenciais dessa conta. Para mais informações, veja [Boas Práticas para Gerenciar Chaves de Acesso AWS](https://docs.aws.amazon.com/general/latest/gr/aws-access-keys-best-practices.html).
    
4. Habilite STS AssumeRole **(Opcional)**
      
      **Observação**: Nas duas opções acima, a função Lambda deve pertencer a mesma conta AWS. Você precisa habilitar STS AssumeROle para invocação de função Lambda entre contas. Note que, suporte para AWS STS AssumeRole foi introduzido no WSO2 API Managar 4.1.0 via uma atualização U2 (Update level 20) e sua efetividade vem de 27 de Julho de 2022.

      Se suas funções Lambda existem em uma diferente conta AWS, você pode usar a ferramenta AWS STS AssumeRole. Para mais informações veja [AWS STS AssumeRole](https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole.html). Entretanto, você deve configurar as requeridas políticas em ambas contas para assumir uma role.
      - Para o método **Usando credenciais temporárias AWS IAM role-supplied**, IAM role com permissão *AWS_AssumeRolePolicy* deve estar anexada a instância EC2 invés de uma role com permissões *AWSLambda_ReadOnlyAccess* e *AWSLambdaRole*.
      - De forma similar, para o método **Usando credenciais armazenadas AWS**, use credenciais de uma conta de usuário separada com *AWS_AssumeRolePolicy invés de uma contade usuário com permissões *AWSLambda_ReadOnlyAccess* e *AWSLambdaRole*. Também insira a região da AWS STS endpoint na **Region**. Para mais informações veja [Gerenciando AWS STS em uma Região AWS](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_temp_enable-regions.html).
      
      Após isso marque *Enable STS AssumeRole* e insira os valores requeridos para configurar o STS AssumeRole.

      Field|Value
      :--:|:--:|
      Role ARN|ARN da função a ser assumida
      Role Session Name| Valor da String par identificar unicamente a sessão
      Region|Região das funções AWS Lambda
5. Clique em **Save**. ![tam2-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/endpoint-awslambda-save.png)
 **Observação**: Você receberá uma mensagem de erro se você não configurar o Método de Acesso apropriadamente.   
#### Passo 3: Mapeando Função ARNs para Recursos
**Observação**: Para mais informações sobre ARNs, veja [Amazon Resource Names(ARNs)](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html).
1. Clique em **Resources** para navegar até a página de Recursos.
2. Configure os recursos. Por padrão a API terá cinco recursos com /* como o padrão URL.
    - Clique em deletar, como mostrado abaixo, para remover todos os recursos existentes. ![tam2-5](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/delete-all-existing-resources.png)
    - Adicione um novo recurso.
       1. Selecione um HTTP Verb.
       2. Insira um nome para a URL Pattern (Você pode adicionar um path parameter também).
       3. Clique em + para adicionar um novo recurso. ![tam2-6](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/resource-add-post-lambda.png)
3. Sob AWS Lambda Settings, selecione ou digite um Amazon Resource Name (ARN) para o recurso. ![tam2-7](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/resource-add-amazon-resource-name.png)
4. Opcionalmente, mude o AWS SDK Client Execution Timeout ao mudar a opção **Set Timeout**. O AWS SDK Client Execution Timeout padrão é de 50 segundos.
    - Min Timeout - 1 segundo
    - Max Timeout - 15 minutos

    ![tam2-8](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/resource-set-amazon-resource-timeout.png)
5. Clique em **SAVE**. ![tam2-9](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/resource-save-lambda.png)
**Observação**: WSO2 API Manager 4.1.0 suporta o conceito padrão Lambda Proxy Integration. Você pode passar path parameters, query parameters, e headers junto com o payload para o backend do Lambda. Essas propriedades pode ser acessadas via object parameter *event* da função Lambda. Por exemplo, veja o seguinte exemplar de objeto *event*.
    
        {
          "headers":{
            "Host":"localhost:8243",
            "Origin":"https://localhost:9443",
            "Referer":"https://localhost:9443/",
          },
          "pathParameters":{
            "id":"7"
          },
          "queryStringParameters":{
            "lastName":"Doe",
            "firstName":"John"
          },
          "httpMethod":"POST",
          "path":"/user/{id}",
          "body":{
            "message":"Hello, World!"
          }
        }
#### Passo 4: Implantando e Publicando a AWS Lambda API
1. Vá até a página **Deployment** e clique no botão **Deploy** para implantar a API no Gateway.
2. Vá até a página **Lifecycle** e clique em **PUBLISH** para publicar a API no Developer Portal.
Você publicou a AWS Lambda API com sucesso. Experimente invocar a Lambda API no Developer Portal.
- [Índice](#documentação-api-manager-410)
 
### Expor um Serviço SOAP como uma REST API
WSO2 API Manager suporta o gerenciamento de serviços existentes baseados em SOAP e WSDL expostas como REST APIs. As organizações que tem serviços baseados em SOAP/WSDL podem facilmente criar pontes entre os serviços existentes para REST sem o custo de uma maior migração. WSO2 API Manager suporta dois tipos de serviços com um performando uma travessia da mensagem SOAP para o backend e outro gerando uma [RESTful API do serviço de backend SOAP](https://apim.docs.wso2.com/en/latest/design/create-api/create-rest-api/generate-rest-api-from-soap-backend/).  
#### Passo 1: Criando um serviço SOAP como uma REST API
1. Inscreva-se no API Publisher e clique em **CREATE API**. ![tam3-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/create-soap-api.jpg)
2. Selecione a opção **Pass Through** e depois selecione uma das seguintes opções:
    - WSDL URL - se você selecionar essa opção, você vai precisar prover um URL endpoint.
    - WSDL Archive/File - se você selecionar essa opção, clique em **Browse** e carregue tanto um arquivo individual WSDL ou um conjunto de arquivo WSDL, que é um projeto WSDL contendo múltiplos WSDLs.
    
    **Observação**:
    Ao carregar um arquivo WSDL, todos os wsdlls/xsds que estão referidos no arquivo pai WSDL deve residir dentro do arquivo. Se não, a validação falhará no ponto da criação da API.

    Esse exemplo utiliza o WSDL *http://ws.cdyne.com/phoneverify/phoneverify.asmx?wsdl* da CDYNE como o endpoint aqui, mas você pode utilizar qualquer backend SOAP de sua escolha. ![tam3-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/generate-rest-api-from-soap-backend.jpg)
3. Clique no botão  **NEXT** para prosseguir à próxima fase, insira as informações da tabela abaixo e clique no botão **CREATE**.

    Field | Sample Value
    :--:|:--:|
    Name|PhoneVerification
    Context|/phoneverify
    Version|1.0
    Endpoint|http://ws.cdyne.com/phoneverify/phoneverify.asmx

    ![tam3-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/create-soap-api-form.jpg)
4. A API criada aparecerá no publisher como abaixo. ![tam3-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/created-soap-api.jpg)
5. A definição da API do esquema criado será mostrada na aba **API Definition**. ![tam3-5](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/api-definition-of-soap-api-created-by-passthrough-mode.jpg)

    **Observação**: Se você deseja adicionar escopos aos recursos que foram criados, navegue até **Resources** e expanda os recursos. Depois, crie novos escopos e especifique-os sob operation scope. Se você especificar um escopo, você precisará usar o mesmo escopo quando gerar tokens de acessos para a aplicação subscrita para invocar a API. Para mais informações em como trabalhar com scopes, veja [OAuthscopes](https://apim.docs.wso2.com/en/latest/design/api-security/oauth2/oauth2-scopes/fine-grained-access-control-with-oauth-scopes/).

    /* ![tam3-6](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/add-scope-for-passthrough-soap-api.jpg)

    **Observação**: Note que ao criar essa API, a opção padrão de **Rate Limiting level** foi selecionada para **API Level**. Para mais informações em configurações avançadas de throttling policies, veja [Reforçando Políticas de Throttling e Acesso de Recursos](https://apim.docs.wso2.com/en/latest/design/rate-limiting/setting-throttling-limits/).
6. Navegue até **LifeCycle** e clique no botão **Publish**. ASsim, você publicou a SOAP API no Developer Portal.
#### Passo 2: Invocando um serviço SOAP como uma REST API
1. Inscreva-se no Developer Portal, navegue para a aba **Subscriptions** e subscreva-se para uso da API (ex DefaultApplication). ![tam3-7](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/subscribed-to-api.jpg)
2. Clique no botão **MANAGE APP** após selecionar **View Credentials**. ![tam3-8](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/view-credentials.jpg)
3. Clique em **GENERATED ACCESS TOKEN** e aparecerá uma janela para criar um token de acesso para a aplicação. ![tam3-9](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/generate-accesstoken.jpg)
4. Clique em **GENERATE**. O JSON Web Token (JWT) gerado aparecerá na janela. Tenha certeza que o copiou. ![tam3-10](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/generate-access-token-popup.jpg) Vamos invocar a API.
5. Navegue até a aba **TryOut** e cole o token no campo de inserção **Access token**. ![tam3-11](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/soap-tryout.jpg)
6. Expanda o método POST e clique em **Try it out**. Insira as informações seguintes e clique em **Execute** para invocar a API.

        SOAP Request
        <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
                <soap:Body>
                    <CheckPhoneNumber xmlns="http://ws.cdyne.com/PhoneVerify/query">
                    <PhoneNumber>18006785432</PhoneNumber>
                    <LicenseKey>18006785432</LicenseKey>
                    </CheckPhoneNumber>
                </soap:Body>
            </soap:Envelope>

            SOAP Action
            http://ws.cdyne.com/PhoneVerify/query/CheckPhoneNumber
      ![tam3-12](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/soap-response.png)
7. Note que a resposta da API deve aparecer no console.
    
    **Observação**: Você também pode invocar a API utilizando uma ferramenta de terceiros tipo SOAP UI. Para mais informações em como invocar uma API utilizando um cliente SOAP, veja [Invocando uma API utilizando um Cliente SOAP](https://apim.docs.wso2.com/en/latest/consume/invoke-apis/invoke-apis-using-tools/invoke-an-api-using-a-soap-client/)
- [Índice](#documentação-api-manager-410)
 
### Criar e Publicar uma WebSocket API
Esse tutorial te guiará na implementação de uma aplicação de chat baseada em WebSocket utilizando o WSO2 API Manager. Siga as instruções nesse tutorial para criar e publicar API via um backend de WebSocket, e então invocar a WebSocket API utilizando o cliente WebSocket **wscat**.

Isso demonstrará uma sala de chat com comandos simples de linha que tem dois canais: **rooms** e **notifications**.

**Observação:**
Ao criar uma API WebSocket Streaming ela é exposta via protocolos *ws* e *wss*. Por padrão, o transporte *ws* utiliza a porta 9099, e o transporte *wss* utiliza a porta 8099.

#### Passo 1: Criando uma WebSocket API
1. Inscreva-se no Publisher (https://\<hostname>:9443/publisher). Para o propósito de testagenm você poderá usar https://localhost:9443/publisher e *admin* como nome de usuário e senha.
2. Clique em **Criar API**, vá até **Streaming API** e clique em **WebSocket API**.
   
   **Observação**: O botão **Create** só aparecerá para um usuário que tem a permissão de função *creator*.
   ![tam4-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/design/create-api/streaming-api/design-new-streaming-api.png)
3. Entre com os detalhes da nova WebSocket API.
   Field | Sample Value
   :---:|:---:
   Name| Chats
   Context | /chats
   Version | 1.0.0
   Protocol | WebSocket
   Endpoint |ws://localhost:8080
   
   **Observação**:
   - Ao criar uma API WebSocket Streaming ela é exposta via protocolos *ws* e *wss*. Por padrão, o transporte *ws* utiliza a porta 9099, e o transporte *wss* utiliza a porta 8099.
   - Para WebSockets não asseguradas entre com o protocolo *ws://* no endpoint, ou para WebSockets asseguradas entre com o protocolo *wss://* . 
4. Clique em **CREATE**. A página de visão geral da WebSocket API criada aparecerá: 
  ![tam4-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websocket-api-overview.png)
5. Adicione tópicos relacionados ao WebSocket API.
    1. Clique em **Topics** e navegue até a página **Topics**.
    2. Delete o tópico padrão existente, que terá o nome /\* .
    3. Adicione os tópicos seguintes um por um. Selecione **pub** e **sub** como os **Types**, adicione o **Topic Name** e clique em + para adicionar cada tópico.
        - /notifications
        - /rooms/{roomID} 
       ![tam4-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websocket-api-add-topics.png)
      4. Expanda cada tópico, complete URL Mappings como segue, e clique em **Save**. 
       
      Topics | URL Mapping
      :--:|:--:|
      /notifications|/notifications
      /rooms/{roomID}|/rooms?room={uri.var.roomID}
  
      5. A URL Mapping provida para cada tópico será adicionada a URL endpoint da WebSocket, que será foi dada ao criar a API, e o tráfego via tópico será enviada e recebida do dessa URL resultante. ![tam4-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websocket-api-topic-url-mapping.png)
      
      6. Para adicionar os business plans para sua WebSocket API.
         1. Clique em **Subscriptions** e navegue até a página Business Plan.
         2. Selecione **AsyncGold** e clique em **Save**. ![tam4-5](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websocket-api-subscriptions.png)
         Agora você terminou de criar e configurar com sucesso a  WebSocket API.
#### Passo 2: Publicando a WebSocket API
1. Clique em **Lifecycle** para naevagar até o ciclo de vida da API, clique em **Publish** para publicar a API no Developer Portal.
2. Clique em **Deployments** para navegar até a página de desenvolvimentos e cliquem em **Deploy New Revision**.
3. Selecione **Production and Sandbox**, escolha **localhost** como o VHost e clique em **Deploy**. ![tam4-6](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/streaming-api-deploy-new-revision.png)
#### Passo 3: Iniciando o WebSocket Server
1. Download o exemplar de WebSocket server do [repositório WSO2 APIM Samples - GitHub](https://github.com/wso2/samples-apim/tree/master/streaming-api-backends/websocket-backend) .
2. Vá até o diretório *streaming-api-backends/websocket-backend* e instale as dependências requeridas.
      
       npm install
3. Inicie o servidor.
      
        npm start
#### Passo 4: Invocando a WebSocket API
1. Inscreva-se no Developer Portal (https://\<hostname>:9443/devportal). Para o propósito de testagem, você pode utilizar https://localhost:9443/devportal e *admin* como nome de usuário e senha.
2. Clique na WebSocket API. A visão geral da API aparecerá.
3. Subscreva-se na API.
    - Clique em **Subscriptions** para ir até a página de subscrições e clique em **Subscription & Key Generation Wizard**. Esse wizard levará você ao passo a passo da criação de uma nova aplicação, subscrição, geração de chaves e geração de token de acesso para invocar a API.
     
      **Observação**:  Você pode usar qualquer aplicação (ex: JWT ou OAuth) para subscrever na API. ![tam4-7](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/streaming-api-key-generation-wizard.png)
    - Copie o token de autorização que aparecerá e clique em **Finish**. ![tam4-8](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/streaming-api-subscription-token.png)
4. Experimente as operações.
    - Instale o cliente **wscat**.
          
          npm install -g wscat
    -  Invoque o tópico */notifications* da API com um authorization header ao executar o seguinte comando:
      
    
            WS
            wscat -c ws://localhost:9099/chats/1.0.0/notifications -H "Authorization: Bearer [accesstoken]"


            WSS
            wscat -n -c wss://localhost:8099/chats/1.0.0/notifications -H "Authorization: Bearer [accesstoken]"
        Quando a conexão tiver sucesso, o servidor WebSocket enviará:

            Subscribed to notifications!
    - Em um terminal separado, invoque o tópico */rooms/{roomID}* da API com um authorization header ao executar o seguinte comando:
    
          WS 
          wscat -c ws://localhost:9099/chats/1.0.0/rooms/room1 -H "Authorization: Bearer [accesstoken]" 
    

          WSS
          wscat -n -c wss://localhost:8099/chats/1.0.0/rooms/room1 -H "Authorization: Bearer [accesstoken]"
      Quando a conexão tiver sucesso, o servidor WebSocket enviará:
        
          You joined room1!

        Isso denota que o primeiro usuário se conectou a *room1*. Com isso, a seguinte mensagem será mostrada no terminal por onde você invocou o tópico */notifications . Isso é o que denota a notificação para o evento acima:

          Someone joined room1!
   - Em outro terminal, invoque o tópico */rooms/{roomID} da API novamente. Isso denota o segundo usuário, que irá conectar a *room1* .

          WS
          wscat -c ws://localhost:9099/chats/1.0.0/rooms/room1 -H "Authorization: Bearer [accesstoken]" 

          WSS
          wscat -n -c wss://localhost:8099/chats/1.0.0/rooms/room1 -H "Authorization: Bearer [accesstoken]"
        Você receberá a mensagem: *You joined room1!* nesse terminal, junto com a correspondente notificação no terminal *notifications*. 
        
        Como há dois usuários conectados a *room1*, ambos podem receber e enviar conversas via *room1*. Experimente enviar mensagens de ambos terminais.

        **Observação**:
        Há clientes (especialmente navegadores) que não permitem a adição de headers para handshake da WebSocket. Em tais casos, você pode enviar o token de acesso para a invocação da WebSocket API como um parâmetro de query nomeado de *access_token* ao utilizar o comando abaixo:

          WS
          wscat -c "ws://localhost:9099/chats/1.0.0/notifications?access_token=[accesstoken]" 

          WSS
          wscat -n -c "wss://localhost:8099/chats/1.0.0/notifications?access_token=[accesstoken]"

        **Observação**: *BasicAuth* e *API Key* não funcionam para a segurança das WebSocket APIs.
  
Você criou com sucesso e publicou sua primeira WebSocket API, subscreveu nela, obteve um token de acesso para testagem e testou sua API com o token de acesso.

#### Soluções de Problemas
Se você necessita de logs mais detalhados de desenvolvimento de WebSocket API para soluções de problemas e debugar um erro de cenário, veja [Soluções de Problemas WebSocket APIs](https://apim.docs.wso2.com/en/latest/troubleshooting/troubleshooting-websocket-api/).
- [Índice](#documentação-api-manager-410)

### Criar e Publicar uma WebSub/WebHook API
Esse tutorial te guiará na criação de uma WebHook API a qual dará atenção para as issues criadas no GitHub. Siga as instruções nesse tutorial para criar e publicar uma API WebSub/WebHook e registrar uma WebHook para ela.

Esse tutorial demonstrará uma API WebSub/WebHook simples que monitora seu repositório GitHub para novas issues e recebe eventos quando uma issue é criada.
#### Passo 1: Criando uma WebSub/WebHook API
1. Inscreva-se no Publisher (https://\<hostname>:9443/publisher). Para o propósito de testagem, você pode usar https://localhost:9443/publisher e *admin* como nome de usuário e senha.
2. Clique em **Create API**, vá para **Streaming API** e clique em **WebHook API**. ![tam5-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/design/create-api/streaming-api/design-new-streaming-api.png)
  
    **Observação**: O botão **CREATE** só aparecerá se o usuário tiver a permissão de função *creator*.
3. Entre com os detalhes da nova WebSub/WebHook API.
 
    Field | Sample Value
    :--:|:--:|
    Name|RepoWatcher
    Context|/repo-watcher
    Version|1.0.0
    Protocol|WebSub
4. Clique em **CREATE**. A página de visão geral da API WebSub/WebHook criada aparecerá:![tam5-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websub-api-overview.png)
5. Adicione um tópico a API WebSub/Webhook:  
    - Clique em **Topics** e navegue até a página Topics.
    - Clique en **Add Topic**, adicione um tópico com o nome **/issues**, cliquem em **Add** e finalmente clique em **Save**. ![tam5-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websub-api-add-topic.png)
6. Gere um secret:
    - Expanda a seção **Subscription Configuration** na página **Topics**. ![tam5-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websub-api-runtime-configurations.png)
    - Selecione **SHA1** como a **Signing Algorithm**.
    - Clique em **Generate** para gerar um secret. ![tam5-5](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websub-api-generate-secret.png)
    - Copie o secret gerado. Vamos nos referir ao secret gerado como *[generated_secret]* .
    - Clique em **Save**.
7. Adicione business plans para a API WebSub/Webhook:
   - Clique em **Subscriptions** e navegue até a página Business Plans.
   - Selecione **AsyncWHGold** e clique em **Save**. ![tam5-6](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websub-api-subscriptions.png)
   Agora você criou e configurou a API WebSub/WebHook com sucesso.
#### Passo 2: Encaminhando uma URL Pública
Uma URL Pública deve ser encaminhada para o *localhost:9021*, então dessa forma o seu servidor local pode ficar acessível ao provedor WebHook (GitHub). [ngrok](https://ngrok.com/) pode ser utilizado para esse propósito.
1. Download [ngrok](https://ngrok.com/download), e o inicie. Isso encaminhará uma URL pública para o *localhost:9021* .

        ./ngrok http 9021

2. Copie a URL HTTP que será encaminhada para o *localhost:9021* , como demonstrado no terminal do ngrok. No exemplo a seguida, ele é *http://3b1-------c9.ngrok.io* .

        Forwarding                    http://3b1*******c9.ngrok.io -> http://localhost:9021
        Forwarding                    https://3b1*******c9.ngrok.io -> http://localhost:9021
#### Passo 3: Adicionando uma WebHook para o seu Repositório GitHub
**Observação**: Você pode usar um repositório existente em seu GitHub ou criar um novo para esse propósito.
1. Vá até **Settings** de seu repositório GitHub.
2. Clique **WebHooks**, navegue até a página da WebHook e clique em **Add WebHook**. ![tam5-7](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/github-webhooks-page.png)
3. Configure a WebHook.
     - Retorne ao WSO2 API Publisher, clique em **Topics** para navegar até a página de Tópicos e expanda o tópico **/issues** .
     - Copie a Callback URL.

            https://{GATEWAY_HOST}:9021/repo-watcher/1.0.0/webhooks_events_receiver_resource?topic=/issues
      - Retorne à página da WebHook do repositório GitHub. Insira os seguintes valores:
    
        |Field|Value|
        :--:|:--:|
        Payload| http://3b1*******c9.ngrok.io/repo-watcher/1.0.0/webhooks_events_receiver_resource?topic=/issues
        Content Type|application/json
        Secret|[generated_secret]
        Which events would you like to trigger this WebHook?| Selecione **Let me select individual events**, e então marque **Issues**.
        
        ![tam5-8](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/github-webhooks-select-issues.png)

        **Observação**: 
        - A URL Payload é obtida ao trocar a parte *https://{GATEWAY_HOST}:9021* do tópico **/issues** da Callback URL, com a URL HTTP de encaminhamento da ngrock (por exemplo, *http://3b1*******c9.ngrok.io* ).
        - O secret é obtido através da seção **Subscription Configuration** em **Topics** das APIs WebSub/WebHook.
4. Clique em **Add WebHook**.
#### Passo 4: Publicando a API WebSub/WebHook
1. Vá até WSO2 API Publisher.
2. Clique em **Lifecyle** para navegar até o ciclo de vida da API.
3. Clique em **PUBLISH** para publicar a API no Developer Portal.
4. Clique em **Deployments** para navegar até a página de implantação.
5. Clique em **Deploy New Revision**.
6. Selecione **Production and Sandbox**, escolha o **localhost** como o VHost e clique em **Deploy**. ![tam5-9](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/streaming-api-deploy-new-revision.png)
#### Passo 5: Criando uma Callback URL
1. Vá até https://webhook.site.org .
2. Clique em **New**, deixe os valores padrões e clique em **Create**. Uma URL única será criada para você. ![tam5-10](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websub-api-create-callback-url.png)
3. Clique em **Copy to clipboard**, que fica ao lado de **Your unique URL**. ![tam5-11](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websub-api-copy-callback-url.png)
4. Codifique a URL única que você copiou. Vamos nos referir à URL única codificada como *[encoded_hub_callback]*.
5. Deixe a página web aberta pois será necessário retornar a ela depois.
#### Passo 6: Invocando a API WebSub/WebHook
1. Inscreva-se no Developer Portal (https://\<hostname>:9443/devportal). Para o propósito de testagem, você pode usar https://localhost:9443/devportal e *admin* como o nome de usuário e senha.
2. Clique na API WebSub/WebHook. A visão geral da API aparecerá.
3. Inscreva-se na API.
    - Clique em **Subscriptions** para ir até a página de subscrições e clique em **SUBSCRIPTION & KEY GENERATION WIZARD**. Esse wizard levará você através do passo a passo da criação de uma nova aplicação, inscrição, geração de chaves e geração de token de acesso para invocar a API.
     
    **Observação**: Você pode usar qualquer aplicação (ex: JWT or OAuth) para inscrever-se na API. ![tam5-12](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/streaming-api-key-generation-wizard.png)
    
    - Copie o token de autorização que aparece e clique em **FINISH**. ![tam5-13](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/streaming-api-subscription-token.png)
4. Experimente as operações:
    - Subscreva-se ao tópico **/issues** .
      - Subscreva a callback URL com o tópico **/issues** ao executar o seguinte comando cUrl:
                
            curl -X POST 'http://localhost:8280/repo-watcher/1.0.0?hub.callback=[encoded_hub_callback]&hub.mode=subscribe&hub.secret=newValue&hub.lease_seconds=50000000&hub.topic=/issues' -H "Authorization: Bearer [accesstoken]"
        **Observação**: Modifique os valores de *[encoded_hub_callback]* e *accesstoken* com os valores que você obteve.
       - Clique em **Subscriptions** para ir até a página de subscrição da sua aplicação no Developer Portal.
       - Clique no acesso de subscrição da API WebSub. Isso irá listar a subscrição que você acabou de fazer.
       - Vá até seu repositório GitHub e crie uma nova issue. Isso irá engatilhar o WebHook do GitHub que você criou.
       - Retorne a página da web https://webhook.site.org onde você criou a callback URL. Um novo request que denota a issue criada deverá aparecer. ![tam5-14](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/websub-api-received-event.png)
       - Cancele a inscrição do tópico **/issues** ao executar o seguinte comando cURL:

              curl -X POST 'http://localhost:8280/repo-watcher/1.0.0?hub.callback=[encoded_hub_callback]&hub.mode=unsubscribe&hub.secret=newValue&hub.lease_seconds=50000000&hub.topic=/issues' -H "Authorization: Bearer [accesstoken]"
          **Observação**: Modifique os valores de *[encoded_hub_callback]* e *accesstoken* com os valores que você obteve.
  
Você criou e publicou com sucesso sua primeira API WebSub/WebHook, inscreveu-se nela, obteve um token de acesso para testagem, criou uma subscrição para uma WebHook e testou sua API com um token de acesso.
  - [Índice](#documentação-api-manager-410)

### Criar e Publicar uma Server Sent Events API
Esse tutorial te guiará na criação de uma SSE Streaming API que estará conectada ao backend que observa a memória de seu sistema e te entrega os valores de maneira contínua. Siga as instruções desse tutorial para desenhar e publicar uma API com um backend SSE, e então invocá-la usando um comando cUrl.
#### Passo 1: Criando a SSE API
1. Inscreva-se no Publisher (https://\<hostname>:9443/publisher). Para o propósito de testagem, você pode usar https://localhost:9443/publisher e *admin* como nome de usuário e senha.
2. Clique em **CREATE API**, vá até **Streaming API** e clique em **SEE API**. ![tam6-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/design/create-api/streaming-api/design-new-streaming-api.png)
 **Observação**: O botão **CREATE** só aparecerá se para o usuário que tiver a permissão de função *creator*.
3. Entre com os detalhes da nova **SEE API**.

    Field|Sample Value
    :--:|:--:|
    Name|Observer
    Context|/observer
    Version|1.0.0
    Protocol|SSE
    Endpoint|http://localhost:8080
4. Clique em **CREATE**. A página de visão geral da API SSE criada aparecerá: ![tam6-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/sse-api-overview.png)
5. Adicione business plans para a SSE API.
 - Clique em **Subscriptions** e navegue até a página de Business Plans.
 - Selecione **AsyncGold** e clique em **Save**. ![tam6-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/sse-api-subscriptions.png)
Agora você terminou de criar e configurar a API SSE com sucesso.
#### Passo 2: Publicando a SSE API
1. Clique em **Lifecycle** e navegue até a página do ciclo de vida da API.
2. Clique em **Publish** e publique a API no Developer Portal.
3. Clique em **Deployments** para navegar até a página de implantação e clique em **Deploy New Revision**.
4. Selecione **Production and Sandbox**, escolha o **localhost** como VHost e clique em **Deploy**. ![tam6-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/streaming-api-deploy-new-revision.png)
#### Passo 3: Iniciando o SSE Server
1. Download o exemplar de servidor SSE do [repositório GitHub - WSO2 APIM Samples](https://github.com/wso2/samples-apim/raw/master/streaming-api-backends/sse/target/sse-server-1.0.0.jar).
2. Vá até o diretório onde você baixou o SSE server e rode o seguinte comando:

        java -jar sse-server-1.0.0.jar --time=5000 --interval=1000
#### Passo 4: Invocando a SSE API
1. Inscreva-se no Developer Portal (https://\<hostname>:9443/devportal). Para o propósito de testagem use https://localhost:9443/devportal e *admin* como nome de usuário e senha.
2. Clique na SEE API. A visão geral da API aparecerá.
3. Subscreva-se na API.
    - Clique em **Subscriptions** para ir até a página de subscrição e clique em **SUBSCRIPTION & KEY GENERATION WIZARD**. Esse wizard levará você através do passo a passo para a criação de uma nova aplicação, subscrição, geração de chaves e geração de um token de acesso para a invocação da API.
    
      **Observação**: Você pode usar qualquer aplicação (ex. JWT ou OAuth) para se inscrever na API. ![tam6-5](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/streaming-api-key-generation-wizard.png)
    
    - Copie o token de autorização que aparecerá e clique em **FINISH**. ![tam6-6](https://apim.docs.wso2.com/en/4.1.0/assets/img/tutorials/streaming-api/streaming-api-subscription-token.png)
4. Experimente as operações. Invoque a API com um authorization header ao executar o seguinte comando cURL.
    
        curl http://localhost:8280/observer/1.0.0/memory -H "Authorization: Bearer [accesstoken]"
    Você receberá contínuos fluxos de eventos mostrando a sua utilização de memória através do server.

        data:{"heap":67893392,"nonHeap":36260800,"ts":1614803952066,"identifier":"ram_222"}

        data:{"heap":72591160,"nonHeap":37250808,"ts":1614803953067,"identifier":"ram_223"}

        data:{"heap":72591160,"nonHeap":37251544,"ts":1614803954064,"identifier":"ram_224"}
Você criou e publicou sua primeira SSE API com sucesso, subscreveu nela, obteve um token de acesso para testagem e testou sua API com um token de acesso.
- [Índice](#documentação-api-manager-410) 

### Editar uma API Modificando a Definição da API
WSO2 API Manager tem um Editor Swagger Integrado, o que faz parte do projeto Swagger.

Swagger é 100% open source, padronizado, com especificação de linguagem agnóstica e um framework completo para descrição, produção, consumo e visualização de RESTful APIs, sem a necessidade de proxy or serviços de terceiros. Swagger permite que consumidores entendam as capacidades de um serviço remoto sem acessar seu código fonte, e interagir com o serviço com o mínimo de implementação lógica. Swagger auxilia a descição de um serviço da mesma maneira que a interface descreve o código de programação de baixo nível.

O [Editor Swagger](https://github.com/swagger-api/swagger-editor) é uma coleção de dependência livre de HTML, JavaScript e CSS que geram dinamicamente de APIs compatíveis com Swagger. APIs compatíveis com Swagger fornecem documentação interativa, geração de cliente SDK, e mais descobertas. O Editor Swagger tem código JSON e sua UI facilita a identação de códigos mais fáceis, realça palavras-chave e mostra erros de sintaxe automaticamente. Você pode adicionar parâmetros de recursos, sumários e descrições para suas APIs usando o Editor Swagger.

API Manager suporta especificações Open API 3.0 e Open API 2.0 e você pode simplesmente criar, importar, editar e consumir as APIs definidas em ambas especificações.

Nesse tutorial, vamos ver como você pode adicionar documentação interativa a uma API ao editar diretamente o código Swagger via API Publisher UI.

**Observação**: Esse tutorial utiliza a API *PizzaShack* criada na seção [Criando uma REST API](https://apim.docs.wso2.com/en/latest/design/create-api/create-rest-api/create-a-rest-api/) e publicada na seção [Publicando uma API](https://apim.docs.wso2.com/en/latest/deploy-and-publish/publish-on-dev-portal/publish-an-api/).

1. Acesso o API Publisher, clique em **CREATE API** e selecione **Design a New REST API**. (https://\<hostname>:9443/publisher) ![tam7-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/create-a-rest-api.jpg)
2. Na página **Create an API**, nomeie a API, dê um contexto, uma versão e um endpoint como segue abaixo e clique em **Create**.

Field|SampleValue|
:---:|:---:|
Name|PizzaShack
Version|1.0.0
Context|/pizzashack
Endpoint|https://localhost:9443/am/sample/pizzashack/v1/api/ (O endpoint que você adiciona é automaticamente adicionado como endpoints da produção e sandbox)

![tam7-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/tutorials/create-a-rest-api-pizzashack.png)
A **Overview** da API criada será mostrada. ![tam7-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/overviewpage-rest-api.jpg)
3. Clique em **API Definition** para ver a definição da API na UI da swagger. O Swagger UI abrirá. ![tam7-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/tutorials/rest-api-definition-pizzashack.png)

4. Adicione os seguintes métodos GET e PUT para a API
     1. Sob o objeto *path*, remova o *{}* e adicione o seguinte código como está demonstrado abaixo.
            
            /order/{orderId}: 
              get:
                description: Get details of an Order
                parameters:
               - name: orderId
                in: path
                description: Order Id
                required: true
                schema:
                  type: string
                  format: string
                responses:
                200:
              description: OK Requested Order will be returned
              content:
              application/ json:
                schema:
                  $ref: '#/components/schemas/Order'
              security:
               - default: []
              x-auth-type: Application & Application User
              x-throttling-tier: Unlimited                    
    
              put: 
                description: Update an existing Order
                parameters:
                - name: orderId
                in: path
                description: Order Id
                required: true
                schema:
                type: string
                format: string
                requestBody:
                description: Order object that needs to be added
                content:
                application/json:
                schema:
                  $ref: '#/components/schemas/Order'
                  required: true
                responses:
                200:
                description: OK. Successful response with updated Order
                headers:
                Location:
                description: The URL of the newly created resource.
                schema:
                  type: string
                Content-Type:
                description: The content type of the body.
                schema:
                type: string
                content:
                application/json:
                schema:
               $ref: '#/components/schemas/Order'
              security: 
                - 
                default: []
              x-auth-type: "Application & Application User"
              x-throttling-tier: "Unlimited"
  
    **Observação**: No código acima, note que você definiu o recurso com o padrão URL */order/{orderId}* sob o objeto *path*. Isso é seguido pelos métodos HTTP GET e PUT. Para cada método HTTP os seguintes parâmetros foram definidos.
     - responses: Um objeto para segurar as respostas que podem ser usadas entre operações. Veja as especificações Swagger para detalhes.
     - x-auth-type: Objeto específico WSO2 para definir o tipo de autenticação do método.
     - x-throtlling-tier: Objeto específico WSO2 para definir a camada throtlling do método. 
  
    2. Defina o schema *Order*. Adicione o seguinte código na API Definition abaixo da seção *Paths*.
      
      
             definitions: 
              Order: 
            required: 
              - "orderId"
            properties: 
            customerName: 
            type: "string"
            delivered: 
            type: "boolean"
            address: 
            type: "string"
            pizzaType: 
            type: "string"
            creditCardNumber: 
            type: "string"
            quantity: 
            type: "number"
            orderId: 
            type: "string"
            title: "Pizza Order"

    **Observação**: O método PUT tem o parâmetro path definido com referência ao schema *Order*

        parameters: 
        - 
        name: "orderId"
        in: "path"
        description: "Order Id"
        required: true
        type: "string"
        format: "string"
        - 
        in: "body"
        name: "body"
        description: "Order object that needs to be added"
        required: true
        schema: 
            $ref: "#/definitions/Order"

     3. Clique em **Update Content**. Isso adicionará um recurso com dois métodos HTTP dentro da API, o que estará visível na aba **Resources** no API Publisher junto com os parâmetros definidos. ![tam7-5](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/tutorials/create-rest-api-pizzashack-resources.png) Vamos assumir que o backend dessa API manda a resposta em formato XML. Vamos documentar isso sob o método GET no recurso que acabamos de adicionar.
   
    **Info**:
    
      Troubleshooting: se você receber um error após a adição da definição da API no Swagger UI, primeiro cheque a identação do código que você adicionou, o que define a API, porque o Swagger fornece erros se a identação não estiver correta. ![tam7-6](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/tutorials/rest-api-definition-pizzashack-indentation.png)

5. Adicione um sumário e descrição para o método GET.
     1. Clique em **Edit Source** e adicione o seguinte código, o que definirá um sumário e descrição ao método GET. 

            summary: "Get Order details"
            description: "Get details of an order by order Id"
        ![tam7-7](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/tutorials/pizzashack-api-get-summary-and-descrption.png)

      2. Clique em **Aply Changes**. O sumário e descrição do método GET que você adicionou estará visível quando você expandir o método GET no API Publisher. ![tam7-8](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/tutorials/pizza-shack-api-get-summary-and-description-updated.png)

6. Mude o título da API
    1. Clique em **Edit Source** e adicione o seguinte código no Swagger UI. Esse é o título que estará visível aos consumidores no Developer Portal depois que a API for publicada.

            info:
            title: PizzaShackAPI 
          ![tam7-9](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/tutorials/pizza-shack-api-change-api-title.png) Agora você pode ver como a mudança se reflete no Developer Portal.
    2. Clique em **Apply Changes** e complete a processo de criação da API.
 1. Complete o restante do processo de criação da API. Para mais informações veja a seção [Criando uma REST API](https://apim.docs.wso2.com/en/latest/design/create-api/create-rest-api/create-a-rest-api/) e na seção [Publicando uma API](https://apim.docs.wso2.com/en/latest/deploy-and-publish/publish-on-dev-portal/publish-an-api/).
 2. Clique em **View in Developer Portal** e a API que você acabou de publicar aparecerá.
 3. Clique em **Try Out**. Note que as mudanças que você fez previamente aparecerão no Developer Portal para os consumidores. ![tam7-10](https://apim.docs.wso2.com/en/4.1.0/assets/img/learn/tutorials/pizza-shack-api-put-dev-portal.png)

Nesse tutorial você viu quão integrado o Editor Swagger é ao ser usado no desenho, descrição, e documentação de sua API, assim os consumidores da API melhor entederão as funcionalidades da API.
- [Índice](#documentação-api-manager-410) 

## Tutoriais de Integração
Os tutoriais de integração guiam o usuário através das principais capacidades e ferramentas de Micro Integrator, auxiliando o entendimento sobre a construção de um sistema integrado.

### Enviando uma Mensagem Simples para um Serviço
#### Contexto
Vamos experimentar um cenário simples onde um paciente faz uma consulta especificando a especialização do médico (categoria) para recceber uma lista de médicos que condizem com a especialização. A informação requerida está disponível em um microsserviço backend.

Para implementar esse caso de uso, você criará um recurso REST API e outros artefatos utilizando WSO2 Integration Studio, e então os implantará na instância embutida WSO2 Micro Integrator. O recurso de API padrão estará configurado para receber o pedido do cliente no lugar do serviço backend, ou seja separando o cliente do serviço de backend. A mensagem de resposta com os detalhes do médico requisitado vai ser devolvida ao cliente através do mesmo recurso da API.

#### Conceitos e Artefatos Usados
- REST API;
- Endpoint HTTP;
- Call Mediator;
- Respond Mediator.

#### Passo 1: Configurar o Workspace
Baixe o [WSO2 Integration Studio](https://wso2.com/api-management/tooling/) baseado no seu sistema operacional.
#### Passo 2: Desenvolva os Artefatos de Integração
Siga as instruções dadas nessa seção para criar e configurar os artefatos necessários.

- Criando um projeto de integração
  
  Um projeto de integração é um projeto especializado multimodular, o que conterá todos os módulos necessários para uma solução de integração.
  
  1. Abra o **WSO2 Integration Studio**.
  2. Cliqe em **New Integration Project** na aba **Getting Started** como mostrado abaixo. ![ti1-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/create-integration-project.jpg) Isso abrirá a caixa de diálogo do **New Integration Project**. ![ti1-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/create-simple-message-project.jpg)
  3. Insira *SampleServices* como o nome do projeto e selecione as seguintes caixas para criar os módulos necessários.
      - **Create ESB Configs**.
      - **Create Composite Exporter**.
  4. Clique em **Finish**.

Agora você verá o projeto listado no **Project Explorer**.

- Criando um Endpoint
  
  Um artefato Endpoint é necessário para o propósito de expor a URL que conecta o serviço backend.
  
  1. Clique com o botão direito em **SampleServiceConfigs** no project explorer e clique em **New → Endpoint**.
  2. Assegure-se que **Create a New Endpoint** está selecionado e clique em **Next**.
  3. Adicione as informações dadas abaixo para criar o novo endpoint.
   
   Property|Value|Description|
   :---:|:---:|:---:|
   Endpoint Name|QueryDoctorEP|O nome do Endpoint.
   Endpoint Type|HTTP Endpoint|Indica que o serviço backend é HTTP.
   URI Template|http://localhost:9090/healthcare/{uri.var.category}|O template para a URL de request esperada pelo serviço de backend. Nesse caso, a variável 'category' que precisa ser incluída no request para os médicos consultados é representado por {uri.var.category} no template.
   Method|GET|Indica que nós estamos criando esse endpoint para requests de GET que serão enviados ao serviço de backend.
   Save Endpoint in|SampleServicesConfigs|Esse é o módulo **ESB Config** onde o artefato será salvo.

   ![ti1-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132413/create-endpoint-artifact.png)
  
  4. Clique em **Finish**. O endpoint **QueryDoctorEP** está salvo na pasta *endpoints* dentro do módulo do projeto de integração **ESB Config**.  

- Criando uma REST API
  
  Uma REST API é necessária para o recebimento da resposta do cliente e o recurso REST dentro da API vai definir a mediação lógica que enviará os pedidos ao serviço de backend de saúde e retornará a informação disponível sobre o médico.
  1. No Project Explorer, clique como o botão direito em **SampleServicesConfigs** e clique em **Next → REST API**.
  2. Assegure-se que **Create a New API Artifact** foi selecionado e clique em **Next**.
  3. Entre com os detalhes abaixo para criar uma nova REST API.
  
   Property|Value|Description|
  :---:|:---:|:---:|
  Name|HealthcareAPI|O nome da REST API
  Context|/heatlhcare|Aqui você ancora a API no contexto */healthcare*. Isso se tornará parte do nome da URL gerada usada pelo cliente quando enviar os requests ao serviço de saúde. Por exemplo, definindo o contexto como */healthcare* significa que a API somente lidará com requests HTTP que o caminho da URL começa com *http://host:port/healthcare.*
  Save location|SampleServicesConfigs|Esse é o módulo **ESB Config** onde o artefato será salvo.
  
  ![ti1-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132413/create-rest-api.png)
  
  4. Clique em **Finish**.

- Definindo o Fluxo de Mediação
  
  Uma vez que o recurso API foi criado, a tela de design do arquivo *HealthcareAPI.xml* aparecerá como mostrado abaixo.
![ti1-5](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132413/119132425.png)

  **Observação**:
    - A parte de cima da tela é a **In sequence**, o que controla como as mensagens serão mediadas.
    - A parte do meio da tela é a **Out sequence**, o que controla como respostas serão lidadas. Nesse caso, o mediador **Send** já está colocada para enviar de volta respostas aos clientes requerentes.
    - A parte de baixo da tela é a **Fault sequence**, o que permite que você configure como lidar com mensagens quando um erro ocorre.

Agora você pode configurar o recurso da API.
  1. Clique duas vezes no ícone **Resource** no lado esquerdo da tela. As propriedades para o recurso da API aparecerão na aba **Properties** na parte de baixo da janela. Se elas não aparecerem, clique com o botão direito no ícone **Resources** e clique em **Show Properties View**.
  2. Na aba **Properties**, insira o seguinte como **Basic Properties**

  Property|Description|
  :--:|:-:|
  Url Style|Clique no respectivo campo **Value**, clique na seta para baixo e selecione **URI_TEMPLATE** da lista.
  URI-Template|Insira */querydoctor/{category}*. Isso definirá o formato URL do request. Nesse caso, o formato inteiro da URL de request é *http://host:port/querydoctor/{category}* onde *{category}* é uma variável.
  Methods|Veja que a caixa de seleção **Get** está selecionada. Isso define que o recurso da API só lidará com requests onde o método HTTP é GET.
  
  ![ti1-6](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132413/119132424.png)
  
  3. Você agora pode configurar a **In sequence** para lidar com requests de um cliente.
      1. Na paleta **Mediators**, clique e arraste o mediador **Log** para a **In sequence** (o topo da tela). 
   
      **Observação**: O mediador Log loga mensagens quando o request é recebido pela In sequence do recurso da API. Nesse cenário, vamos configurar o mediador Log para mostrar a seguinte mensagem: "Bem vindo ao HealthcareService".
      
      2. Com o mediador **Log** selecionado, acesse a aba **Property** e insira as informações da tabela abaixo:
        
         Field|Value|Description
          :-:|:-:|:-:|
          Log Category|INFO|Indica que o log contém uma mensagem informacional.
          Log Level|Custom|Quando o *custom* está selecionado só propriedades especificadas vai ser logadas por esse mediador.
          Log Separator|(blank)|Já que há apenas uma propriedade que está sendo logada, você não necessita de um separador. Portanto deixe esse campo em branco.
          Properties||Para extrair o símbolo de estoque do request e imprimir uma mensagem de bem vindo ao log, clique no botão com ícone de mais (+) na seção **Properties**, e então adicione os seguintes valores: **Name**: Log Property Message / **Type**: LITERAL (Nós selecionamos LITERAL porque a mensagem de log requerida é um valor estático) / **Value/Expression**: "Welcome to HealthcareService" ![ti1-7](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132413/119132423.png)
          Description|Request Log|O campo **Description** oferece o nome que aparece para o ícone de mediador de Log na visão de design.
        
          ![ti1-8](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132413/119132422.png) 
    
      3. Clique em **OK** para salvar a configuração do mediador **Log**.
      4. Configure o mediador **Call** para enviar a mensagem de request para o endpoint *HealthService* e receber a mensagem de resposta.
         1. Na paleta **Mediators**, clique e arraste o mediador **Call** para a **In sequence** adjacente ao mediador **Log** que você adicionou antes.
         2. Na paleta **Defined EndPoints**, clique e arraste o endpoint **QueryDoctorEP**, que já foi criada, bem ao lado do espaço vazio do mediador **Call**. ![ti1-9](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/sending-simple-message/add-call-mediator.png)
      5. Adicione um mediador **Respond** no final da **In sequence** para enviar a mensagem de resposta do serviço de backend de saúde para o cliente. ![ti1-10](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/sending-simple-message/add-respond-mediator.png)

Você criou com sucesso todos os artefatos que são necessários para enviar um request através do Micro Integrator ao serviço de backend.

#### Passo 3: Empacotar os Artefatos
Empactoe os artefatos no módulo **composite explorer** para estar apto a implantar os artefatos no servidor.
1. Abra o arquivo *pom.xml* do módulo **SampleServicesCompositeExporter**.
2. Assegure-se que os seguintes artefatos estão selecionados no arquivo PIM. 
    - HealthcareAPI
    - QueryDoctorEP
3. Salve as mudanças.

#### Passo 4: Construir e Rodar os Artefatos
Para testar os artefatos, implante os artefatos empacotados no Micro Integrator embutido.
1. Clique com o botão direito no módulo **composite explorer** e clique em **Export Project Artifacts and Run**.
2. Na caixa de diálogo que abrirá, confirme que os artefatos necessários do módulo **composite explorer** estão selecionados.
3. Clique em **Finish**.

Os artefatos estarão implantados no Micro Integrator embutido e o servidor iniciará.
- Veja o log de inicialização na aba **Console**.
- Veja as URLs dos serviços implantados e APIs na aba **Runtime Services**.

#### Passo 5: Teste o Estudo de Caso
Vamos testar o estudo de caso enviando um request simples de cliente que invocará o serviço.

- Inicie o serviço backend
  1. Baixe o arquivo JAR do serviço de backend [aqui](https://github.com/wso2-docs/WSO2_EI/blob/master/Back-End-Service/Hospital-Service-JDK11-2.0.0.jar)
  2. Abra um terminal, navegue até o local onde você salvou o serviço de backend.
  3. Execute o seguinte comando para iniciar o serviço:
        
          java -jar Hospital-Service-JDK11-2.0.0.jar

- Envie o request do cliente

  Vamos enviar o request para API. Você pode usar o **HTTP Client** embutido do WSO2 Integration Studios, como segue abaixo:
  1. Abra a aplicação Postman. Se você não tem a aplicação, baixe [aqui](https://www.postman.com/downloads/).
  2. Adicione a informação de request como dada abaixo e clique no botão **Send**.
   
      Method| GET
      :-:|:-:|
      URL|http://localhost:8290/healthcare/querydoctor/surgery

Se você quiser enviar o request do cliente de seu terminal:
1. Instale e configure o [cUrl](https://curl.haxx.se) como seu cliente REST.
2. Execute o seguinte comando.
        
        curl -v http://localhost:8290/healthcare/querydoctor/surgery

- Analise a resposta
  
  Você verá a mensagem de resposta da HealthcareService com uma lista de médicos disponíveis e detalhes relevantes.

      [
        {"name":"thomas collins",
          "hospital":"grand oak community hospital",
          "category":"surgery",
          "availability":"9.00 a.m - 11.00 a.m",
          "fee":7000.0},
        {"name":"anne clement",
          "hospital":"clemency medical center",
          "category":"surgery",
          "availability":"8.00 a.m - 10.00 a.m",
          "fee":12000.0},
        {"name":"seth mears",
          "hospital":"pine valley community hospital",
          "category":"surgery",
          "availability":"3.00 p.m - 5.00 p.m",
          "fee":8000.0}
      ]

Agora cheque a aba **Console** do WSO2 Integration Studio e você verá a seguinte mensagem: 

    INFO - LogMediator message = "Welcome to HealthcareService"

Você acabou de criar e implantar um recurso de API no Micro Integrator, o qual recebe requests, loga uma mensagem usando um mediador de Log, enviar o pedido ao serviço de backend utilizando um mediador Send, e retorna uma resposta ao cliente requerente.
- [Índice](#documentação-api-manager-410) 

### Roteando Requests baseados em Cabeçalhos de Mensagem
#### Contexto
Nesse tutorial, nós criaremos os artefatos de mediação que podem rotear uma mensagem para um endpoint relevante dependendo do conteúdo do payload da mensagem.

Quando o cliente enviar um pedido de agendamento de consulta ao Micro Integrator, o payload da mensagem com o request contém o nome do hospital onde a consulta precisa ser confirmada. O método de request HTTP que é usado para isso é POST. Baseado no nome do hospital enviado na mensagem de request, o Micro Integrator deve rotear o agendamento da consulta ao serviço de backend do hospital relevante.

#### Conceitos e Artefatos Usados
- REST API;
- HTTP Endpoint;
- Property Mediator;
- Call Mediator.

#### Passo 1: Configurar o Workspace
Download o [WSO2 Integration Studio](https://wso2.com/api-management/tooling/)  relevante baseado em seu sistema operacional.

#### Passo 2: Desenvolva os Artefatos de Integração
Siga as instruções dadas nessa seção para criar e configurar os artefatos necessários.

- Criando um projeto de integração
  
  Um projeto de integração é um projeto especializado multimodular, o que conterá todos os módulos necessários para uma solução de integração.
  1. Abra o **WSO2 Integration Studio**.
  2. Clique em **New Integration Project** na aba **Getting Started** como mostrado abaixo. ![ti2-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/create-integration-project.jpg) Isso abrirá a caixa de diálogo **New Integration Project**. ![ti2-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/create-simple-message-project.jpg)
  3. Insira *SampleServices* como o nome do projeto e marque as seguintes caixas de seleção para criar os módulos necessários.
      - **Create ESB Configs**
      - **Create Composite Exporter**
  4. Clique em **Finish**.

  Agora você verá os projetos listados no **Project Explorer**.

- Criando Endpoints
  
  Nesse tutorial, nós temos três serviços de hospital hospedados como backend:
  - Grand Oak Community Hospital: *http://localhost:9090/grandoaks/*
  - Clemency Medical Center: *http://localhost:9090/clemency/*
  - Pine Valley Community Hospital: *http://localhost:9090/pinevalley/*
  
  O método de request é POST e o formato da URL de request esperado pelos serviços backend é *http://localhost:9090/grandoaks/categories/{category}/reserve* .

  Vamos criar três endpoints HTTP diferentes para os serviços acima.
  1. Clique com o botão direito em **SampleServiceConfigs** no **Project Explorer** e clique em **New → Endpoint**.
  2. Assegure-se que **Create a New Endpoint** está selecionado e clique em **Next**.
  3. Insira as informações dadas abaixo para criar o novo endpoint.

  Property|Value|Descrição
  :-:|:-:|:-:
  Endpoint Name| GrandOakEP|O nome do endpoint representando o serviço do Hospital Grand Oaks.
  Endpoint Type|HTTP Endpoint|Indica que o serviço de backend é HTTP.
  URI Template|http://localhost:9090/grandoaks/categories/{uri.var.category}/reserve|O template para a URL de request esperado pelo serviço de backend.
  Method|POST|O método REST do HTTP do endpoint.
  Save Endpoint in|SampleServicesConfigs|Esse é o módulo ESB Config que nós criamos na última seção.

  ![ti2-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/119132166.png)

  4. Clique em **Finish**.
  5. De forma similar, crie os endpoints HTTP para os dois outros serviços de hospital utilizando as templates URI dadas abaixo:
      -  ClemencyEP: http://localhost:9090/clemency/categories/{uri.var.category}/reserve
      -  PineValleyEP: http://localhost:9090/pinevalley/categories/{uri.var.category}/reserve
  
  Agora terminamos de cirar os três endpoints para os serviços de backend do hospital que serão usados para fazer agendamentos de consultas.

  **Dica**: 
  Você também pode criar apenas um endpoint onde a diferenciação do nome do hospital pode ser lidado utilizando uma variável no template da URI. Veja o tutorial em [Expondo Diversos Serviços como um Serviço Só](https://apim.docs.wso2.com/en/latest/page-not-found/).  Utilizar três endpoints diferentes é vantajoso quando os serviços de backend são muito diferentes um do outro e ou quando há uma necessidade de configurar um erro de direcionamento diferente para cada um deles.

- Criando uma REST API
  1. No **Project Explorer**, clique com o botão direito em **SampleServicesConfigs** e vá para **New → REST API**.
  2. Assegure-se que **Create a New API Artifact** está selecionado e clique em **Next**.
  3. Insira os detalhes dados abaixo para criar uma nova REST API.
   
  Property|Value|Descrição
  :-:|:-:|:-:|
  Name|HealthcareAPI|O nome da REST API.
  Context|/healthcare|Aqui você está ancorando a API no contexto /healthcare. Isso se tornará parte do nome da URL gerada usada pelo cliente ao enviar a requisição para o serviço de saúde. Por exemplo, configurando o contexto como /healthcare significa que a API vai apenas lidar com requisições HTTP onde o caminho da URL começa com *http://host:port/healthcare* .
  Save location|SampleServicesConfigs|Esse é o módulo **ESB Config** onde o artefato será salvo.

  4. Clique no API Resource padrão e acesse a aba **Properties** e insira as seguintes informações.
  
  Property|Descrição
  :-:|:-:|
  Url Style|Clique no campo **Value**, clique na seta pra baixo e selecione da lista **URI_TEMPLATE**.
  URI-Template|Insira */categores/{category}/reserve* .
  Methods|Da lista de métodos, selecione **POST**.

  ![ti2-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/119132164.png)

- Defina o Mediation Flow

  Você pode começar a configurar o recurso da API.
  1. Arraste o mediador **Property** da paleta **Mediators** para a In Sequence do recurso da API e nomeie-o **Get Hospital**.
  
  **Info**: Isso é usado para extrair o nome do hospital que é enviado no payload da requisição.
  
  2. Com o mediador **Property** selecionado, acesse a aba **Properties** e insira os detalhes seguintes:
   
  Property|Descrição
  :-:|:-:|
  Property Name|Insira *New Property...* .
  New Property Name|Insira *Hospital* .
  Property Action|Insira *set* .
  Property Scope|Insira *defautl* .
  Value| Siga os passos abaixo para especificar o valor da expressão: ![ti2-5](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/expression-value.png) 1. Clique no botão **Ex** antes do campo **Value**. Isso especificará o tipo de valor como *expression*. 2. Agora clique o botão **f** para abrir a caixa de diálogo do **Expression Selector**. 3. Insira *json-eval($.hospital)* como o valor da expressão. **Observação**: Essa é a expressão JSONPath que vai extrair o hospital do payload da requisição.

  3. Arraste o mediador **Switch** da paleta **Mediator** logo após o mediador **Property**.
  4. Clique com o botão direito no mediador Switch que você acabou de adicionar e selecione **Add/Remove Case** para adicionar o número de casos que você quer especificar.![ti2-6](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/119132163.png) Nós temos três endpoints diferentes de hospitais, o que correspondem aos três casos de switch. Insira 3 para o **Number of branches** e clique em **OK**. ![ti2-7](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/switch-cases-dialog.png)
  5. Como o mediador Switch selecionado, vá até a aba **Properties** e insira os seguintes detalhes:
  
  Property|Descrição
  :-:|:-:|
  Source XPath| O campo **Source XPath** é onde nós especificamos a expressão XPath, o que obtém o valor do Hospital que nós armazenamos no mediador Property. Siga os passos abaixo para especificar a expressão: 1. Clique na caixa de texto da propriedade **Source XPath**. isso abrirar a caixa de diálogo **Expression Selector**. 2. Selecione **Expression** da lista. 3. Insira *get-property('Hospital')* para substituir a expressão padrão. 4. Clique em **OK**.
  Case Branches|Siga os passos abaixo para adicioanr os case branches: 1. Clique duas vezes em **case regex** (correspondendo a cada branch) que está listado. Isso abrirá a caixa de diálogo **SwitchCaseBranchOutputConnector**. 2. Mude os valores RegEx para os switch cases como segue: a) Case 1: grand oak community hospital. b) Case 2: clemency medical center. c) Case 3: pine valley community hospital. 3. Clique em **OK**.

  6. Arraste o mediador Log para a primeira caixa Case do mediador Switch e nomeie-o **Grand Oak Log**.
  
  **Info**: Isso imprimirá uma mensagem indicando a qual hospital a mensagem de requisição está sendo roteada.
  
  7. Com o mediador Log selecionado, acesse a aba **Properties** e insira os seguintes detalhes:
  
  Property|Value|Descrição
  :-:|:-:|:-:|
  Log Category| INFO|Indica que o log contém uma mensagem informativa.
  Log Level|CUSTOM|Somente propriedades especificadas serão logadas por esse mediador.
  Log Separator|(em branco)|Já que há apenas uma propriedade sendo logada, nós não necessitamos de um separador. Portanto, esse campo pode ser deixado em branco.
  Properties||Siga os passos abaixo para extrair o símbolo de estoque do request e imprima uma mensagem de boas vindas no log: 1. Clique no ícone de mais (+) para começar a definir uma propriedade. Isso abrirá a caixa de diálogo **LogProperty**. 2. Adicione os seguintes valores na caixa de diálogo **LogProperty**: **Name**: message / **Type**: EXPRESSION . (nós selecionamos EXPRESSION porque as propriedades necessárias para a mensagem de log deve ser extraídas do request, o que nós podemos fazer usando uma expressão XPath)./ **Property Expression**: Clique em **browse(...)** no campo **Property Expression** e insira *fn:concat('Routing to ', get-property('Hospital'))* . **Observação**: Esse valor de expressão XPath recebe o valor armazenado no mediador Property e concatena as duas strings para mostrar o log de mensagem: *Routing to \<hospital name>* . 3. Clique em **OK**.
  
  8.  Arraste o mediador **Call** da paleta **Mediators** depois do mediador Log e adicione o **GrandOakEP endpoint** da paleta **Defined Endpoints** para a caixa vazia adjacente ao mediador Call.
  9.  Adicione **Log mediators** nas duas outras **Case boxes** no mediador Switch e então insira as mesmas propriedades. Confirme se nomeou os dois mediadores Logs como segue:
      - Clemency Log
      - Pine Valley Log  
  10. Adicione os mediadores **Call** após os esses mediadores de log e adicione os endpoints **ClemencyEP** e **PineValleyEP** respectivamente da paleta **Defined Endpoints**.
  
      **Info**: Você agora configurou o mediador Switch para logar a mensagem *Routing to \<Hospital Name>* quando uma requisição for mandada para o recurso da API. A mensagem de requisição será então encaminhada para o serviço de backend do hospital relevante baseado no nome do hospital que será enviadao no payload da requisição.
  
  11. Adicione um **Log mediator** para o **Default** (a caixa de baixo) do mediador Switch e configure-a da mesma maneira como os mediadores Log anteriores.
  **Observação**: Certifique-se de nomear como **Fault Log** e mudar sua **Property Expression** para *fn:concat('Invalid hospital - ', get-property('Hospital'))* .
  
      O case padrão do mediador Switch lida com a requisição de hospital inválida que é enviada para payload de requisição. Isso logará a mensagem (*Invalid hospital - \<Hospital Name>) para requisições que têm o nome de hospital inválido.
  12. Arraste um **Respond mediator** ao lado do mediador **Switch** para retornar as respostas do serviço de backend de saúde ao cliente.
  
  Você criou com sucesso todos os artefatos que são necessários para encaminhar mensagens para um serviço de backend dependendo do conteúdo do payload de uma requisição.

#### Passo 3: Empacotar os Artefatos
Empacote os artefatos em seu módulo **composite application** (SampleServicesCompositeExporter) para estar apto a implantar os artefatos no servidor.
1. Abra o arquivo *pom.xml* no módulo **composite exporter**.
2. Assegure-se que os artefatos seguintes estão selecionados no arquivo POM.
    - HealthcareAPI
    - ClemencyEP
    - GrandOakEP
    - PineValleyEP
3. Salve as mudanças.

#### Passo 4: Construa e Rode os Artefatos
Para testar os artefatos, implante o artefatos empacotados acima embutidos no Micro Integrator:
1. Clique com o botão direito no módulo **composite exporter** e clique em **Export Project Artifacts and Run**.
2. Na caixa de diálogo que abrirá, confirme que os artefatos requeridos do módulo **composite exporter** estão selecionados.
3. Clique em **Finish**.

Os artefatos serão implantados no Micro Integrator embutido e o servidor será iniciado.
   - Veja o log de inicialização na aba **Console**.
   - Veja as URLs dos serviços implantados e as APIs na aba **Runtime Services**.

#### Passo 5: Teste o Estudo de Caso
Vamos testar o estudo de caso enviando uma requisição de cliente simples que invoca o serviço. 

- Inicie o serviço backend
   1. Baixe o arquivo JAR do serviço de backend [aqui](https://github.com/wso2-docs/WSO2_EI/blob/master/Back-End-Service/Hospital-Service-JDK11-2.0.0.jar).
   2. Abra o terminal, navegue até o local onde seu serviço de backend está salvo.
   3. Execute o seguinte comando para iniciar o serviço:
   
          java -jar Hospital-Service-JDK11-2.0.0.jar 

- Envie a requisição do cliente

  Vamos enviar a requisição para o recurso da API fazer o agendamento. Você pode usar uma aplicação Postman como segue:
  1. Abra a aplicação Postman. Se você não tiver a aplicação, baixe-a [aqui](https://www.postman.com/downloads/).
  2. Adicione a informação do requerida como dada abaixo e clique no botão **Send**.
  
  Method|POST
  :-:|:-:
  Headers|Content-Type=application/json
  URL|http://localhost:8290/healthcare/categories/surgery/reserve . O Formato da URI-Template que é usado nessa URL foi definida durante a criação do recurso da API: http://host:port/categories/{category}/reserve.
  Body|{ "patient": { "name": "John Doe", "dob": "1940-03-19", "ssn": "234-23-525", "address": "California", "phone": "8770586755", "email": "johndoe@gmail.com" }, "doctor": "thomas collins", "hospital_id": "grandoaks", "hospital": "grand oak community hospital", "appointment_date": "2025-04-02" } . Esse JSON payload contém detalhes do agendamento da consulta, o que inclui detalhes do paciente, médico, hospital e data da consulta.

  Se você quiser enviar a requisição do cliente de seu terminal:
  1. Instale e configure [cUrl](https://curl.haxx.se) como seu cliente REST.
  2. Crie um arquivo JSON chamado *request.json* com o seguinte payload de requisição. 
   
          {
            "patient": {
            "name": "John Doe",
            "dob": "1940-03-19",
            "ssn": "234-23-525",
            "address": "California",
            "phone": "8770586755",
            "email": "johndoe@gmail.com"
            },
            "doctor": "thomas collins",
            "hospital_id": "grandoaks",
            "hospital": "grand oak community hospital",
            "appointment_date": "2025-04-02"
          }
  3. Abra um terminal e navegue até o diretório onde você salvou o arquivo *request.json* .
  4. Execute o seguinte comando.
  
          curl -v -X POST --data @request.json http://localhost:8290/healthcare/categories/surgery/reserve --header "Content-Type:application/json" 

- Analise a resposta

  Você verá a seguinte resposta recebida em seu **HTTP Client**: 

      {"appointmentNumber":1,
        "doctor":
          {"name":"thomas collins",
            "hospital":"grand oak community hospital",
            "category":"surgery","availability":"9.00 a.m - 11.00 a.m",
            "fee":7000.0},
        "patient":
          {"name":"John Doe",
            "dob":"1990-03-19",
            "ssn":"234-23-525",
            "address":"California",
            "phone":"8770586755",
            "email":"johndoe@gmail.com"},
        "fee":7000.0,
      "confirmed":false,
      "appointmentDate":"2025-04-02"}

  Agora cheque a aba **Console** do WSO2 Integration Studio e você verá a seguinte mensagem:

      INFO - LogMediator message = Routing to grand oak community hospital
  Essa é a mensagem impressa pelo mediador Log quando a mensagem do cliente é encaminhada para o endpoint relevante no mediador Switch.

Você completou com sucesso esse tutorial e viu como as requisições recebidas pelo Micro Integrator pode ser roteadas para o endpoint relevante usando o mediador Switch.

- [Índice](#documentação-api-manager-410) 

### Traduzindo Formatos de Mensagem
#### Contexto
A transformação de mensagem é necessária quando o formato da mensagem enviada pelo cliente é diferente do formato de mensagem esperado pelo serviço de backend. O padrão de arquitetura **Message Translator** no WSO2 Micro Integrator descreve como traduzir de um formato de dado para outro. 

Nesse tutorial, você enviará uma mensagem de requisição para um serviço de backend onde o formato do payload da requisição será diferente do que é esperado pelo serviço de backend. O mediador **Data Mappter** é usado para transformar o payload da mensagem de requisição para o formato esperado pelo serviço de backend.

Vamos assumir que esse é o formato do request enviado pelo cliente:

    {
      "name": "John Doe",
      "dob": "1940-03-19",
      "ssn": "234-23-525",
      "address": "California",
      "phone": "8770586755",
      "email": "johndoe@gmail.com",
      "doctor": "thomas collins",
      "hospital_id": "grandoaks",
      "hospital": "grand oak community hospital",
      "cardNo": "7844481124110331",
      "appointment_date": "2017-04-02"
    }

Porém o formato compatível com o serviço de backend é esse que segue:

    {
      "patient": {
        "name": "John Doe",
        "dob": "1990-03-19",
        "ssn": "234-23-525",
        "address": "California",
        "phone": "8770586755",
        "email": "johndoe@gmail.com",
        "cardNo": "7844481124110331"
      },
      "doctor": "thomas collins",
      "hospital_id": "grandoaks",
      "hospital": "grand oak community hospital",
      "appointment_date": "2017-04-02"
    }

O formato da mensagem do cliente deve ser transformado para o formato de mensagem do serviço de backend dentro da **In sequence**.

#### Passo 1: Configurar o Workspace
Download o [WSO2 Integration Studio](https://wso2.com/api-management/tooling/) relevante baseado em seu sistema operacional.

#### Passo 2: Desenvolva os Artefatos de Integração
Siga as instruções dadas nessa seção para criar e configurar os artefatos necessários.

- Criando um projeto de integração
  
  Um projeto de integração é um projeto especializado multimodular, o que conterá todos os módulos necessários para uma solução de integração.
  1. Abra o **WSO2 Integration Studio**. 
  2. Clique em **New Integration Project** na aba **Getting Started** como mostrado abaixo. ![ti3-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/create-integration-project.jpg) Isso abrirá a caixa de diálogo **New Integration Project**. ![ti3-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/create-simple-message-project.jpg)
  3. Insira *SampleServices* como o nome do projeto e marque as seguintes caixas de seleção para criar os módulos necessários.
      - **Create ESB Configs**
      - **Create Composite Exporter**
  4. Clique em **Finish**.

  Agora você verá os projetos listados no **Project Explorer**.

- Criando uma REST API
  1. No **Project Explorer**, clique com o botão direito em **SampleServicesConfigs** e vá para **New → REST API**.
  2. Assegure-se que **Create a New API Artifact** está selecionado e clique em **Next**.
  3. Insira os detalhes dados abaixo para criar uma nova REST API.
   
  Property|Value|Descrição
  :-:|:-:|:-:|
  Name|HealthcareAPI|O nome da REST API.
  Context|/healthcare|Aqui você está ancorando a API no contexto /healthcare. Isso se tornará parte do nome da URL gerada usada pelo cliente ao enviar a requisição para o serviço de saúde. Por exemplo, configurando o contexto como /healthcare significa que a API vai apenas lidar com requisições HTTP onde o caminho da URL começa com *http://host:port/healthcare* .
  Save location|SampleServicesConfigs|Esse é o módulo **ESB Config** onde o artefato será salvo.

  4. Clique no API Resource padrão e acesse a aba **Properties** e insira as seguintes informações.
  
  Property|Descrição
  :-:|:-:|
  Url Style|Clique no campo **Value**, clique na seta pra baixo e selecione da lista **URI_TEMPLATE**.
  URI-Template|Insira */categores/{category}/reserve* .
  Methods|Da lista de métodos, selecione **POST**.

  ![ti3-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/119132164.png)

- Criando Novo Endpoint
  
  Vamos criar um Endpoint para representar o serviço de backend do Hospital.
  
  1. Clique com o botão direito em **SampleServiceConfigs** no **Project Explorer** e clique em **New → Endpoint**.
  2. Assegure-se que **Create a New Endpoint** está selecionado e clique em **Next**.
  3. Vamos criar o endpoint do serrviço do hospital (**HospitalServicesEP**) usando os seguintes valores:

  Property|Value|Descrição
  :-:|:-:|:-:
  Endpoint Name| HospitalServicesEP|Esse é um endpoint único configurado para encaminhar requisições para o hospital relevante ao ler o hospital especificado no payload da requisição.
  Endpoint Type|HTTP Endpoint|Indica que o serviço de backend é HTTP.
  URI Template|http://localhost:9090/{uri.var.hospital}/categories/{uri.var.category}/reserve|O template para a URL de request esperado pelo serviço de backend. As seguintes duas variáveis serão trocadas pelos respectivos valores correspondentes na mensagem de requisição: 1. {uri.var.hospital} 2. {uri.var.category}
  Method|POST|O método REST do HTTP do endpoint.
  Save Endpoint in|SampleServicesConfigs|Esse é o módulo ESB Config que nós criamos na última seção.

  4. Clique em **Finish**.

- Defina o Mediation Flow

  Vamos configurar o recurso da API com a lógica de transformação de dados.

  1. Arraste o mediador **Property** da paleta **Mediators** para a In Sequence do recurso da API e nomeie-o **Get Hospital**.
  
  **Info**: Isso é usado para extrair o nome do hospital que é enviado no payload da requisição.
  
  2. Com o mediador **Property** selecionado, acesse a aba **Properties** e insira os detalhes seguintes:
   
  Property|Value|Descrição
  :-:|:-:|:-:|
  Property Name|*New Property...* .|Especifica que uma nova propriedade foi criada.
  New Property Name|*uri.var.hospital* .|O nome que vai ser usado para se referir aos valores dessa propriedade.
  Property Action|*set* . | A ação da propriedade.
  Property Scope| *default* .| O escopo do propriedade.
  Value (Expression)|*json-eval($.hospital_id)* |Siga os passos abaixo para especificar o valor da expressão: ![ti3-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/expression-value.png) 1. Clique no botão **Ex** antes do campo **Value**. Isso especificará o tipo de valor como *expression*. 2. Agora clique o botão **f** para abrir a caixa de diálogo do **Expression Selector**. 3. Insira *json-eval($.hospital_id)* como o valor da expressão. **Observação**: Essa é a expressão JSONPath que vai extrair o hospital do payload da requisição.

  3. Adicione um mediador **Data Mapper** logo após o mediador **Property** na In Sequence do recurso da API. ![ti3-5](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/message-transformation/add-data-mapper.png)
  4. Clique duas vezes no ícone do mediador Data Mapper e especifique os seguintes detalhes:
   
   Property|Descrição
   :-:|:-:
   Configuration Name| Insira *RequestMapping* como nome.
   Save in project| Especifique o **Registry Resource module** onde a configuração do data mapper deve ser salva. O módulo **SampleServicesRegistryResources** criado no momento da criação do projeto de integração será selecionado como padrão.

   ![ti3-6](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132196/119132224.png)
   Clique **OK**. Você poderá visualizar o editor data mapping. ![ti3-7](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/message-transformation/data-mapper-canvas.png)
  
  5. Crie um arquivo JSON (ex: *input.json) copiando o conteúdo do exemplar em seguida da mensagem de requisição enviada ao recurso da API e salve na sua pasta local do sistema.
   
          { "name": "John Doe",
            "dob": "1990-03-19",
            "ssn": "234-23-525",
            "address": "California",
            "phone": "8770586755",
            "email": "johndoe@gmail.com",
            "doctor": "thomas collins",
            "hospital_id": "grandoaks",
            "hospital": "grand oak community hospital",
            "cardNo": "7844481124110331",
            "appointment_date": "2025-04-02"
          }
  
  **Observação**: Você pode criar um esquema JSON manualmente para input e output utilizando o editor **Data Mapper Diagram**.

  6. Clique em **Load Input File** na caixa **Input** e abra a caixa de diálogo **Load Input**.

  7. Selecione **JSON** como **Resource Type**.
  
  8.  Clique no link do **file system** em **Select resource from**, selecione o arquivo JSON (ex: *input.json*) que você salvou na sua pasta local do sistema, clique em **Open**. Você poderá ver o formato de input carregado na caixa **Input** do editor como mostrado abaixo: ![ti3-8](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/message-transformation/load-data-input-data-mapper.png)
  
  9.  Crie outro arquivo JSON (ex: *output.json*) copiando o conteúdo do exemplar de mensagem de requisição sequinte esperado pelo serviço backend e salve na pasta local de seu sistema. 
  
          {
            "patient": {
              "name": "John Doe",
              "dob": "1990-03-19",
              "ssn": "234-23-525",
              "address": "California",
              "phone": "8770586755",
              "email": "johndoe@gmail.com"
            },
              "doctor": "thomas collins",
              "hospital_id": "grandoaks",
              "hospital": "grand oak community hospital",
              "appointment_date": "2025-04-02"
          }
  10. Clique em **Load Output File** na caixa **Output** para abrir a caixa de diálogo **Load Output**.
  11. Selecione **JSON** como o **Resource Type**.
  12. Clique no link **file system** em **Select resource from**, selecione o arquivo JSON salvo na pasta local de seu sistema, clique em **Open**. Você poderá visualizar o formato de input carregado na caixa **Output** no editor como mostrado abaixo: ![ti3-9](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/message-transformation/load-data-output-data-mapper.png)

  **Info**: Cheque as caixas **Input** e **Output** com as mensagens de exemplo para ver se os tipos de elementos (ex valores de Arrays, Objects e Primitive) estão definidos corretamente. Os símbolos seguintes te ajudarão a identificá-los corretamente.
  - (): representa elementos de object.
  - []: representa elementos array.
  - <>: representa valores de campo primitivos.
  - A: representa valor do atributo XML. 
  
  Você criou com sucesso todos os artefatos que são necessários para encaminhar mensagens para um serviço de backend dependendo do conteúdo do payload de uma requisição.

  13. Agora, você precisa mapear a mensagem de input com a mensagem de output. Há duas maneiras de fazer o mapeamento:
      - Se você clicar em **Apply**, o mapeamento vai ser gerado pelo **AI Data Mapper**. Você terá a opção de mudar manualmente o mapeamento depois de ser gerado.
      -  Você pode desenhar manualmente o mapeamento ao arrastar as setas dos valores na caixa **Input** para os valores relevantes na caixa **Output**. ![ti3-10](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/message-transformation/input-output-data-mapper.png) O mapeamento completo vai parecer como o seguinte: ![ti3-11](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/message-transformation/mapping-data-input-output.png) 
  14. Salve e feche a configuração.
  15. Volte ao **Design View** do API Resource e selecione o mediador **Data Mapper** e edite o seguinte na aba **Properties**:
  
      Property|Descrição
      :-:|:-:|
      Input Type| Selecione **JSON**
      Output Type|Selecione **JSON**  
  
      ![ti3-12](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/message-transformation/data-mapper-properties.png)
  16. Adicione um mediador **Call** da paleaa de **Mediators** e adicione ao endpoint HospitalServicesEP da paleta **Defined Endpoints** para a caixa vazia adjunta do mediador **Call**. ![ti3-13](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/message-transformation/add-call-mediator-for-transformation.png) 
  17. Adicione um **Respond mediator** ao lado do mediador **Call** para retornar a resposta do serviço de saúde de volta ao cliente. ![ti3-14](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/message-transformation/add-respond-mediator-for-transformation.png)
  18. Salve a configuração da REST API.
  
  Você criou com sucesso todos os artefatos necessários para esse estudo de caso.

#### Passo 3: Empacotar os Artefatos
Empacote os artefatos em seu módulo **composite application** (SampleServicesCompositeExporter) para estar apto a implantar os artefatos no servidor.
1. Abra o arquivo *pom.xml* no módulo **composite exporter**.
2. Assegure-se que os artefatos seguintes estão selecionados no arquivo POM.
    - HealthcareAPI
    - HospitalServicesEP
3. Salve as mudanças.

#### Passo 4: Construa e Rode os Artefatos
Para testar os artefatos, implante os artefatos empacotados acima embutidos no Micro Integrator:
1. Clique com o botão direito no módulo **composite exporter** e clique em **Export Project Artifacts and Run**.
2. Na caixa de diálogo que abrirá, confirme que os artefatos requeridos do módulo **composite exporter** estão selecionados.
3. Clique em **Finish**.

Os artefatos serão implantados no Micro Integrator embutido e o servidor será iniciado.
   - Veja o log de inicialização na aba **Console**.
   - Veja as URLs dos serviços implantados e as APIs na aba **Runtime Services**.

#### Passo 5: Teste o Estudo de Caso
Vamos testar o estudo de caso enviando uma requisição de cliente simples que invoca o serviço. 

- Inicie o serviço backend
   1. Baixe o arquivo JAR do serviço de backend [aqui](https://github.com/wso2-docs/WSO2_EI/blob/master/Back-End-Service/Hospital-Service-JDK11-2.0.0.jar).
   2. Abra o terminal, navegue até o local onde seu serviço de backend está salvo.
   3. Execute o seguinte comando para iniciar o serviço:
   
          java -jar Hospital-Service-JDK11-2.0.0.jar 

- Envie a requisição do cliente

  Vamos enviar a requisição para o recurso da API fazer o agendamento. Você pode usar um cliente HTTP embutido do WSO2 Integration Studio como segue:
  1. Abra a aplicação Postman. Se você não tiver a aplicação, baixe-a [aqui](https://www.postman.com/downloads/).
  2. Adicione a informação do request como dada abaixo e clique no botão **Send**.
  
  Method|POST
  :-:|:-:
  Headers|Content-Type=application/json
  URL|http://localhost:8290/healthcare/categories/surgery/reserve . O Formato da URI-Template que é usado nessa URL foi definida durante a criação do recurso da API: http://host:port/categories/{category}/reserve.
  Body|{ "patient": { "name": "John Doe", "dob": "1940-03-19", "ssn": "234-23-525", "address": "California", "phone": "8770586755", "email": "johndoe@gmail.com" }, "doctor": "thomas collins", "hospital_id": "grandoaks", "hospital": "grand oak community hospital", "appointment_date": "2025-04-02" } . Esse JSON payload contém detalhes do agendamento da consulta, o que inclui detalhes do paciente, médico, hospital e data da consulta.

  Se você quiser enviar a requisição do cliente de seu terminal:
  1. Instale e configure [cUrl](https://curl.haxx.se) como seu cliente REST.
  2. Crie um arquivo JSON chamado *request.json* com o seguinte payload de requisição. 
   
          {
            "name": "John Doe",
            "dob": "1990-03-19",
            "ssn": "234-23-525",
            "address": "California",
            "phone": "8770586755",
            "email": "johndoe@gmail.com",
            "doctor": "thomas collins",
            "hospital_id": "grandoaks",
            "hospital": "grand oak community hospital",
            "cardNo": "7844481124110331",
            "appointment_date": "2025-04-02"
          }
  3. Abra um terminal e navegue até o diretório onde você salvou o arquivo *request.json* .
  4. Execute o seguinte comando.
  
          curl -v -X POST --data @request.json http://localhost:8290/healthcare/categories/surgery/reserve --header "Content-Type:application/json" 

- Analise a resposta

  Você verá a seguinte resposta recebida em seu **HTTP Client**: 

      {"appointmentNumber":1,
        "doctor":
          {"name":"thomas collins",
            "hospital":"grand oak community hospital",
            "category":"surgery","availability":"9.00 a.m - 11.00 a.m",
            "fee":7000.0},
        "patient":
          {"name":"John Doe",
            "dob":"1990-03-19",
            "ssn":"234-23-525",
            "address":"California",
            "phone":"8770586755",
            "email":"johndoe@gmail.com"},
        "fee":7000.0,
      "confirmed":false,
      "appointmentDate":"2025-04-02"}

Você agora descobriu como o Micro Integrator pode receber uma mensagem em um formato e transformá-lo dentro do formato esperado pelo serviço de backend usando o mediador Data Mapper.

- [Índice](#documentação-api-manager-410)

### Expondo Serviços Diversos como Serviço Único (Orquestração de Serviço)
#### Contexto
Quando a informação de vários serviços são requeridas para construir uma resposta à requisição do cliente, o encadeamento de serviço precisa ser implementado. Ou seja, diversos serviços serão integrados baseado em alguma lógica de negócio e exposta como apenas um serviço agregado.

Nesse tutorial, quando o cliente enviar uma requisição para uma consulta médica, o Micro Integrator performará diversas chamadas de serviço para múltiplos serviços de backend para construir a resposta que inclua todos os detalhes necessários. O mediador **Call** permite que você especifique todas as invocações de serviço uma após a outra em apenas uma sequência.

Você também usará o mediador **PayloadFactory** para pegar a resposta de um serviço de backend e mudá-la para o formato que é aceito para o outro serviço de backend.

#### Conceitos e Artefatos Usados
- REST API;
- HTTP Endpoint;
- Property Mediator;
- Call Mediator;
- PayloadFactory Mediator.

#### Passo 1: Configurar o Workspace
Download o [WSO2 Integration Studio](https://wso2.com/api-management/tooling/) relevante baseado em seu sistema operacional.

#### Passo 2: Desenvolva os Artefatos de Integração
Siga as instruções dadas nessa seção para criar e configurar os artefatos necessários.

- Criando um projeto de integração
Um projeto de integração é um projeto especializado multimodular, o que conterá todos os módulos necessários para uma solução de integração.
1. Abra o **WSO2 Integration Studio**.
2. Clique em **New Integration Project** na aba **Getting Started** como mostrado abaixo. ![ti4-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/create-integration-project.jpg) Isso abrirá a caixa de diálogo **New Integration Project**. ![ti4-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/create-simple-message-project.jpg)
3. Insira *SampleServices* como o nome do projeto e marque as seguintes caixas de seleção para criar os módulos necessários.
   - **Create ESB Configs**
   - **Create Composite Exporter**
4. Clique em **Finish**.

    Agora você verá os projetos listados no **Project Explorer**.

- Criando Novos Endpoints
  
  Vamos criar três endpoints HTTP para representar todos os três serviços backend: Hospital Service, Channeling Service, Payment Service.

  1. Clique com o botão direito em **SampleServiceConfigs** no **Project Explorer** e clique em **New → Endpoint**.
  2. Assegure-se que **Create a New Endpoint** está selecionado e clique em **Next**.
  3. Vamos criar o endpoint do serviço do hospital (**HospitalServicesEP) utilizando os seguintes valores.

  Property|Value|Descrição
  :-:|:-:|:-:
  Endpoint Name| HospitalServicesEP|Esse é apenas um endpoint configurado para encaminhar requisições para o hospital relevante ao ler os hospitais especificados no payload da requisição
  Endpoint Type|HTTP Endpoint|Indica que o serviço de backend é HTTP.
  URI Template|http://localhost:9090/{uri.var.hospital}/categories/{uri.var.category}/reserve|O template para a URL de request esperado pelo serviço de backend. As seguintes duas variáveis serão trocadas pelos valores correspondentes na mensagem de requisição 1. {uri.var.hospital} 2. {uri.var.category}
  Method|POST|O método REST do HTTP do endpoint.
  Static Endpoint||Selecione essa opção pois nós utilizaremos esse endpoint apenas nesse módulo ESB Config e não será reutilizado em outros projetos. **Observação**: Se você precisar criar um endpoint reutilizável, salve-o como **Dynamic Endpoint** tanto na **Configuration** quanto na **Governance Registry**.
  Save Endpoint in|SampleServicesConfigs|Esse é o módulo ESB Config que nós criamos na última seção.

  4. Clique em **Finish**.
  5. Crie outro endpoint para o serviço de backend Channeling e especifique os detalhes dados abaixo:

    Property|Value|Descrição
    :-:|:-:|:-:
    Endpoint Name| ChannelingFeeEP|O nome do endpoint.
    Endpoint Type|HTTP Endpoint|Indica que o serviço de backend é HTTP.
    URI Template|http://localhost:9090/{uri.var.hospital}/categories/appointments/{uri.var.appointment_id}/fee|O template para a URL de request esperado pelo serviço de backend. As seguintes duas variáveis serão trocadas pelos valores correspondentes na mensagem de requisição 1. {uri.var.hospital}: Essa vai ser a ID do hospital extraída do payload de resposta que é recebida pelo serviço do hospital 2. {uri.var.appointment_id}: Essa vai ser a ID do appointment extraída do payload de resposta que é recebida pelo serviço do hospital.
    Method|GET|O artefato endpoint vai ser usado para conseguir a informação do serviço de backend.
    Static Endpoint||Selecione essa opção pois nós utilizaremos esse endpoint apenas nesse módulo ESB Config e não será reutilizado em outros projetos. **Observação**: Se você precisar criar um endpoint reutilizável, salve-o como **Dynamic Endpoint** tanto na **Configuration** quanto na **Governance Registry**.
    Save Endpoint in|SampleServicesConfigs|Esse é o módulo ESB Config que nós criamos na última seção.
  6. Clique em **Finish**.
  7. Crie um outro endpoint para o serviço de backend Settle Payment e especifique os detalhes dados abaixo:
  
    Property|Value|Descrição
    :-:|:-:|:-:
    Endpoint Name| SettlePaymentEP|O nome do endpoint.
    Endpoint Type|HTTP Endpoint|Indica que o serviço de backend é HTTP.
    URI Template|http://localhost:9090/healthcare/payments|O template para a URL de request esperado pelo serviço de backend.
    Method|POST|O artefato endpoint vai ser usado para postar informações para o serviço backend.
    Static Endpoint||Selecione essa opção pois nós utilizaremos esse endpoint apenas nesse módulo ESB Config e não será reutilizado em outros projetos. **Observação**: Se você precisar criar um endpoint reutilizável, salve-o como **Dynamic Endpoint** tanto na **Configuration** quanto na **Governance Registry**.
    Save Endpoint in|SampleServicesConfigs|Esse é o módulo ESB Config que nós criamos na última seção.
  8. Clique em **Finish**.
   
   Você acabou de criar os endpoints necessários para esse tutorial. 

- Criando uma REST API
  1. No **Project Explorer**, clique com o botão direito em **SampleServicesConfigs** e vá para **New → REST API**.
  2. Assegure-se que **Create a New API Artifact** está selecionado e clique em **Next**.
  3. Insira os detalhes dados abaixo para criar uma nova REST API.
   
  Property|Value|Descrição
  :-:|:-:|:-:|
  Name|HealthcareAPI|O nome da REST API.
  Context|/healthcare|Aqui você está ancorando a API no contexto /healthcare. Isso se tornará parte do nome da URL gerada usada pelo cliente ao enviar a requisição para o serviço de saúde. Por exemplo, configurando o contexto como /healthcare significa que a API vai apenas lidar com requisições HTTP onde o caminho da URL começa com *http://host:port/healthcare* .
  Save location|SampleServicesConfigs|Esse é o módulo **ESB Config** onde o artefato será salvo.

  4. Clique no API Resource padrão e acesse a aba **Properties** e insira as seguintes informações.
  
  Property|Value|Descrição
  :-:|:-:|:-:|
  Url Style|URI_TEMPLATE|Você pode agora especificar variáveis dinâmicas para extrair valores da URL de request.
  URI-Template|Insira */categories/{category}/reserve* .|A URL de request deve ser compatível com esse template. A variável {category} vai ser trocada pelo valor enviado no request. 
  Methods|POST|O recurso da API aceitará requisições POST.

- Atualize o Mediation Flow

  Você pode começar a atualizar o recurso da API com o fluxo de mediação.
  1. Abra o recurso da REST API. Você verá a tela para a in sequence e out sequence. 
  2. Arraste o mediador **Property** da paleta **Mediators** para a In Sequence do recurso da API e nomeie-o **Get Hospital**. Isso é usado para extrair o nome do hospital que é enviado no payload da requisição.
  3. Com o mediador **Property** selecionado, acesse a aba **Properties** e insira os detalhes seguintes:
  
      Property|Value|Descrição
      :-:|:-:|:-:|
      Property Name|New Property...|Especifica que a nova propriedade foi criada.
      New Property Name|uri.var.hospital|O nomve que será usado para se referir aos valores da propriedade.
      Property Action|set|A ação da propriedade.
      Property Scope|default|O escopo da propriedade.
      Value (Expression)|json-eval($hospital_id)| Siga os passos abaixo para especificar o valor da expressão: ![ti4-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/expression-value.png) 1. Clique no botão **Ex** antes do campo **Value**. Isso especificará o tipo de valor como *expression*. 2. Agora clique o botão **f** para abrir a caixa de diálogo do **Expression Selector**. 3. Insira *json-eval($.hospital_id)* como o valor da expressão. **Observação**: Essa é a expressão JSONPath que vai extrair o hospital do payload da requisição.

  4. Adicione um novo mediador **Property** logo após o mediador de propriedade **Get Hospital** e nomeie-o **Get Card Number**. Isso vai retornar e armazenar o número do cartão que é enviado no payload da requisição.
  5. Com o mediador Propriety selecionado, acesse a aba Properties e especifique os seguintes detalhes:
 
      Property|Value|Descrição
      :-:|:-:|:-:|
      Property Name|New Property...|Especifica uma nova propriedade.
      New Property Name|card_number|O nome da propriedade, que será usado para se referir à propriedade.
      Property Action|set|A ação da propriedade.
      Value (Expression)|json-eval($.cardNo)| Siga os passos abaixo para especificar o valor da expressão: ![ti4-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/expression-value.png) 1. Clique no botão **Ex** antes do campo **Value**. Isso especificará o tipo de valor como *expression*. 2. Agora clique o botão **f** para abrir a caixa de diálogo do **Expression Selector**. 3. Insira *json-eval($.hospital_id)* como o valor da expressão. **Info**: Essa é a expressão JSONPath que vai extrair o hospital do payload da requisição.
      Description|Get Card Number|A descrição da propriedade.

  6. Adicione um mediador Call da paleta **Mediators** e adicione o endpoint HospitalServicesEP da paleta **Defined Endpoints** para a caixa vazia adjunta ao mediador Call.
  
      **Info**: Usar um mediador Call permite-nos definir outras invocações de serviço seguindo esse mediador.

      **Observação**: A seguinte resposta será retornada de GrandOakEP, ClemencyEP ou PineValleyEP.

         {"appointmentNumber":1,   "doctor":
            {"name":"thomas collins",
             "hospital":"grand oak community hospital",
             "category":"surgery","availability":"9.00 a.m - 11.00 a.m",
             "fee":7000.0},
            "patient":
              {"name":"John Doe",
                "dob":"1990-03-19",
                "ssn":"234-23-525",
                "address":"California",
                "phone":"8770586755",
                "email":"johndoe@gmail.com"},
             "fee":7000.0,
             "confirmed":false}

      Vamos usar os mediadores de Propriedade para receber e armazenar os valores que você conseguirá das respostas que você receberá de GrandOakEP, ClemencyEP ou PineValleyEP.  
  7. Adicione um mediador Property para resgatar e armazenar o valor enviado como *appointmentNumber*.
  8. Com o mediador Property selecionado, acesse a aba Properties e especifique os seguintes detalhes:

  Property|Value|Descrição
  :-:|:-:|:-:
  Property Name|**New Property**|Especifica uma nova propriedade.
  New Property Name|uri.var.appointment_id| Esse valor é usado quando invocamos **ChannelingFeeEP**.
  Property Action|Selecione **set**|A ação da propriedade.
  Value (Expression)|json-eval($.appointmentNumber)|Siga os passos abaixo para especificar a expressão: ![4-5](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132228/expression-value.png) 1. Cloque no botão **Ex** antes do campo **Value**. Isso especifica o tipo de valor como *expression*. 2. Agora, clique no botão **f** para abrir a caixa de diálogo **Expression Selector**. 3. Insira json-eval($.appointmentNumber) como o valor da expressão. **Observação**: Essa é a expressão JSONPath que vai extrair o número de agendamento do payload da requisição.
  Description|Get Appointment Number|
  
  9. De forma similar, adicione mais dois mediadores de Propriedade. Eles vão receber e armazenar os detalhes *doctor* e *pacient* respectivamente da resposta que é recebida de GrandOakEP, ClemencyEP ou PineValleyEP.
     - Para armazenar os detalhes de *doctor* :
     
     Property|Value|Description
     :-:|:-:|:-:
     Property Name|**New Property**|Uma nova propriedade será definida.
     New Property Name|doctor_details|O nome da propriedade será usado para referir-se a essa propriedade.
     Property Action|**set**|O nome da ação da propriedade.
     Value (Expression)|json-eval($.doctor)|Siga os passos abaixo para especificar a expressão: ![4-6](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132228/expression-value.png) 1. Cloque no botão **Ex** antes do campo **Value**. Isso especifica o tipo de valor como *expression*. 2. Agora, clique no botão **f** para abrir a caixa de diálogo **Expression Selector**. 3. Insira json-eval($.doctor) como o valor da expressão. **Observação**: Essa é a expressão JSONPath que vai extrair o número de agendamento do payload da requisição.
     Description|Get Doctor Details| A descrição da propriedade.

     - Para armazenar os detalhes de *patient* :
     
     Property|Value|Description
     :-:|:-:|:-:
     Property Name|**New Property**|Uma nova propriedade será definida.
     New Property Name|patient_details|O nome da propriedade será usado para referir-se a essa propriedade.
     Property Action|**set**|O nome da ação da propriedade.
     Value (Expression)|json-eval($.patient)|Siga os passos abaixo para especificar a expressão: ![4-7](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132228/expression-value.png) 1. Cloque no botão **Ex** antes do campo **Value**. Isso especifica o tipo de valor como *expression*. 2. Agora, clique no botão **f** para abrir a caixa de diálogo **Expression Selector**. 3. Insira json-eval($.patient) como o valor da expressão. **Observação**: Essa é a expressão JSONPath que vai extrair o número de agendamento do payload da requisição.
     Description|Get Patient Details| A descrição da propriedade.
  10. Adicione um mediador Call e adicione o endpoint ChannelingFeeEP da paleta **Defined Endpoints** para a caixa vazia adjunta ao mediador Call.
  
      **Observação**: A seguinte resposta será recebida de ChannelingFeeEP:

          {"patientName":" John Doe ", 
          "doctorName":"thomas collins", 
          "actualFee":"7000.0"}

  11. Adicione um mediador Property adjunto à caixa do mediador Call para receber e armazenar o valor enviado como *actualFee* .
  12. Acesse a aba de Property do mediador e especifique os seguintes detalhes.
  
  Property|Value|Description
     :-:|:-:|:-:
     Property Name|**New Property**|Uma nova propriedade será definida.
     New Property Name|actual_fee|O nome da propriedade será usado para referir-se a essa propriedade.
     Property Action|**set**|O nome da ação da propriedade.
     Value (Expression)|json-eval($.patient)|Siga os passos abaixo para especificar a expressão: ![4-8](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132228/expression-value.png) 1. Cloque no botão **Ex** antes do campo **Value**. Isso especifica o tipo de valor como *expression*. 2. Agora, clique no botão **f** para abrir a caixa de diálogo **Expression Selector**. 3. Insira json-eval($.patient) como o valor da expressão. **Observação**: Essa é a expressão JSONPath que vai extrair o número de agendamento do payload da requisição.
     Description|Get Actual Fee| A descrição da propriedade.
   
    13. Vamos usar o mediador **PayloadFactory** para construir a mensagem de payload seguinte para a requisição enviada para SettlePaymentEP.
    
      {"appointmentNumber":2,
        "doctor":{
          "name":"thomas collins",
          "hospital":"grand oak community hospital",
          "category":"surgery",
          "availability":"9.00 a.m - 11.00 a.m",
          "Fee":7000.0
        },
        "patient":{
          "name":"John Doe",
          "Dob":"1990-03-19",
          "ssn":"234-23-525",
          "address":"California",
          "phone":"8770586755",
          "email":"johndoe@gmail.com"
        },
        "fee":7000.0,
        "Confirmed":false,
        "card_number":"1234567890"
      } 
  14. Adicione um mediador PayloadFactory (da paleta **mediators**) ao lado do mediador Property para construir a mensagem de payload acima.
  15. Com o mediador PayloadFactory selecionado, acesse a aba properties do mediador e especifique os seguintes detalhes:
  
  Property|Description
  :-:|:-:
  Payload Format|Insira **Inline**
  Media Type|Selecione **json**
  Payload|{"appointmentNumber":$1, "doctor":$2, "patient":$3, "fee":$4, "confirmed":"false", "card_number":"$5"} Essa é o payload da mensagem para enviar com a requisição para SettlePaymentEP. Nesse payload $1, $2, $3, $4 e $5 indicam variáveis.

  16. Para adicionar os argumentos para o mediador PayloadFactory:
  
        - Clique no ícone de mais (+) no campo **Args** para abrir o diálogo **PayloadFactoryArgument**.
        - Insira as informações a seguir na caixa de diálogo **PayloadFactoryArgument**. Isso oferece o argumento que define o valor atual da primeira variável (utilizada no definição de formato dado no passo anterior).
        
        **Dica**: Para evitar o recebimento de mensagens de erro, primeiro selecione **Media Type** antes de adicionar o **Payload**.

        Property|Description
        :-:|:-:
        Argument Type|Selecione *Expression*
        Argument Expression| Siga os passos dados abaixo para especificar a expressão: 1. Clique na caixa de texto para o campo **Argument Expression**. Isso abrirá o diálogo **Expression Selector**. 2. Selecione **Expression** da lista. 3. Insira *$ctx:uri.var.appointment_id* . Observe que o método *$ctx* é similar a utilização do método *get-property*. Esse método checa no contexto da mensagem. 4. Clique em **OK**.
        Evaluator|Selecione *xml.* . Isso indica que a expressão é fornecida em XML.
   17. De forma similar, clique em **Add** e adicione mais argumentos para definir as outras variáveis que são usadas na definição de formato do payload da mensagem. Use os seguintes como **Value** para cada uma delas:
       - $ctx:doctor_details
       - $ctx:patient_details
       - $ctx:actual_fee
       - $ctx:card_number
   18. Adicione um mediador Call e adicione SettlePaymentEP da paleta Defined Endpoints para a caixa vazia adjunta ao mediador Call.
   19. Adicione um mediador **Respond** para enviar a resposta ao cliente.

#### Passo 3: Empacotar os Artefatos
Empacote os artefatos em seu módulo **composite application** (SampleServicesCompositeExporter) para estar apto a implantar os artefatos no servidor.
1. Abra o arquivo *pom.xml* no módulo **composite exporter**.
2. Assegure-se que os artefatos seguintes estão selecionados no arquivo POM.
    - HealthcareAPI
    - HospitalServicesEP
    - ChannelingFeeEP
    - SettlePaymentEP
3. Salve as mudanças.

#### Passo 4: Construa e Rode os Artefatos
Para testar os artefatos, implante o artefatos empacotados acima embutidos no Micro Integrator:
1. Clique com o botão direito no módulo **composite exporter** e clique em **Export Project Artifacts and Run**.
2. Na caixa de diálogo que abrirá, confirme que os artefatos requeridos do módulo **composite exporter** estão selecionados.
3. Clique em **Finish**.

Os artefatos serão implantados no Micro Integrator embutido e o servidor será iniciado.
   - Veja o log de inicialização na aba **Console**.
   - Veja as URLs dos serviços implantados e as APIs na aba **Runtime Services**.

#### Passo 5: Teste o Estudo de Caso
Vamos testar o estudo de caso enviando uma requisição de cliente simples que invoca o serviço. 

- Inicie o serviço backend
   1. Baixe o arquivo JAR do serviço de backend [aqui](https://github.com/wso2-docs/WSO2_EI/blob/master/Back-End-Service/Hospital-Service-JDK11-2.0.0.jar).
   2. Abra o terminal, navegue até o local onde seu serviço de backend está salvo.
   3. Execute o seguinte comando para iniciar o serviço:
   
          java -jar Hospital-Service-JDK11-2.0.0.jar 

- Envie a requisição do cliente

  Vamos enviar a requisição para o recurso da API fazer o agendamento. Você pode usar um **HTTP Client** do WSO2 Integration Studio como segue:
  1. Abra o **HTTP Client** do WSO2 Integration Studio.
  
      **Dica**: Se você não vê falha no **HTTP Client**, vá até **Window → Show View - Other** e selecione o **HTTP Client** para disponibilizar a falha de cliente. 
  2. Adicione as informações requeridas como dadas abaixo e clique no ícone de **Send**.
  
  Method|POST
  :-:|:-:
  Headers|Content-Type=application/json
  URL|http://localhost:8290/healthcare/categories/surgery/reserve . O Formato da URI-Template que é usado nessa URL foi definida durante a criação do recurso da API: http://:/categories/{category}/reserve. 
  Body|{ "patient": { "name": "John Doe", "dob": "1940-03-19", "ssn": "234-23-525", "address": "California", "phone": "8770586755", "email": "johndoe@gmail.com", "cardNo": "7844481124110331" }, "doctor": "thomas collins", "hospital_id": "grandoaks", "hospital": "grand oak community hospital", "appointment_date": "2025-04-02" } . Esse payload JSON contém detalhes do agendamento da consulta, o que inclui detalhes do paciente, médico, hospital e data da consulta.

  Se você quiser enviar a requisição do cliente de seu terminal:
  1. Instale e configure [cUrl](https://curl.haxx.se) como seu cliente REST.
  2. Crie um arquivo JSON chamado *request.json* com o seguinte payload de requisição. 
   
          {
            "patient": {
            "name": "John Doe",
            "dob": "1940-03-19",
            "ssn": "234-23-525",
            "address": "California",
            "phone": "8770586755",
            "email": "johndoe@gmail.com"
            },
            "doctor": "thomas collins",
            "hospital_id": "grandoaks",
            "hospital": "grand oak community hospital",
            "appointment_date": "2025-04-02"
          }
  3. Abra um terminal e navegue até o diretório onde você salvou o arquivo *request.json* .
  4. Execute o seguinte comando.
  
          curl -v -X POST --data @request.json http://localhost:8290/healthcare/categories/surgery/reserve --header "Content-Type:application/json" 

- Analise a resposta

  Você verá a seguinte resposta recebida em seu **HTTP Client**: 

      {
      "patient":"John Doe",
      "actualFee":7000.0,
      "discount":20,
      "discounted":5600.0,
      "paymentID":"480fead2-e592-4791-941a-690ad1363802",
      "status":"Settled"
      }

  Agora cheque a aba **Console** do WSO2 Integration Studio e você verá a seguinte mensagem:

      INFO - LogMediator message = Routing to grand oak community hospital
  
Você acabou de descobrir como o Micro Integrator pode fazer o encadeamento de serviço usando o mediador Call e transformar payloads de mensagens de um formato para outro utilizando o mediador **PayloadFactory**.

- [Índice](#documentação-api-manager-410)

### Guardar e Encaminhar Mensagens para Entrega Garantida
#### Contexto
Mensageria armazenada e encaminhada é utilizada para servir ao tráfego de serviços de backend que só podem aceitar mensagens de requisição até um certo ponto. Isso também é usado para assegurar entrega garantida de mensagens. Mensagens nunca serão perdidas desde que elas sejam armazenadas no armazenamento de mensagens e estejam disponíveis para referência futura.

Nesse tutorial, invés de enviar a requisição diretamente ao serviço de backend, você armazenará a mensagem de requisição no RabbitMQ broker. Você então usará um **Message Processor** para recuperar a mensagem do armazenamento antes de entregá-la ao serviço de backend.

#### Passo 1: Configurar o Workspace
Download o [WSO2 Integration Studio](https://wso2.com/api-management/tooling/) relevante baseado em seu sistema operacional.

#### Passo 2: Desenvolva os Artefatos de Integração
Siga as instruções dadas nessa seção para criar e configurar os artefatos necessários.

- Criando um projeto de integração
  Um projeto de integração é um projeto especializado multimodular, o que conterá todos os módulos necessários para uma solução de integração.

  1. Abra o **WSO2 Integration Studio**.
  2. Clique em **New Integration Project** na aba **Getting Started** como mostrado abaixo. ![ti5-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/create-integration-project.jpg) Isso abrirá a caixa de diálogo **New Integration Project**. ![ti5-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/create-simple-message-project.jpg)
  3. Insira *SampleServices* como o nome do projeto e marque as seguintes caixas de seleção para criar os módulos necessários.
     - **Create ESB Configs**
     - **Create Composite Exporter**
  4. Clique em **Finish**.

  Agora você verá os projetos listados no **Project Explorer**.

- Criando uma REST API
  1. No **Project Explorer**, clique com o botão direito em **SampleServicesConfigs** e vá para **New → REST API**.
  2. Assegure-se que **Create a New API Artifact** está selecionado e clique em **Next**.
  3. Insira os detalhes dados abaixo para criar uma nova REST API.

      Property|Value|Descrição
      :-:|:-:|:-:|
      Name|HealthcareAPI|O nome da REST API.
      Context|/healthcare|Aqui você está ancorando a API no contexto /healthcare. Isso se tornará parte do nome da URL gerada usada pelo cliente ao enviar a requisição para o serviço de saúde. Por exemplo, configurando o contexto como /healthcare significa que a API vai apenas lidar com requisições HTTP onde o caminho da URL começa com *http://host:port/healthcare* .
      Save location|SampleServicesConfigs|Esse é o módulo **ESB Config** onde o artefato será salvo.

  4. Clique no API Resource padrão e acesse a aba **Properties** e insira as seguintes informações.

      Property|Value|Descrição
      :-:|:-:|:-:|
      Url Style|URI_TEMPLATE|Você pode agora especificar variáveis dinâmicas para extrair valores da URL de request.
      URI-Template|Insira */categories/{category}/reserve* .|A URL de request deve ser compatível com esse template. A variável {category} vai ser trocada pelo valor enviado no request. 
      Methods|POST|O recurso da API aceitará requisições POST.

      ![ti5-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/119132164.png)

- Criando o **Message Store**
  1. Clique com o botão direito em **SampleServices** no explorador do projeto e navegue até **New → Message Store**.
  2. Selecione **Create a new message-store artifact** e especifique os seguintes detalhes:
    
      Property|Value|Descrição
      :-:|:-:|:-:|
      Message Store Name| HospitalServiceMessageStore| O nome do armazenamento de mensagem.
      Message Store Type|RabbitMQ Message Store|Uma instância do servidor RabbitMQ será usada como broker.
      RabbitMQ Server Host Name|localhost|O endereço do RabbitMQ broker.
      RabbitMQ Server Port|5672|O número da porta do RabbitMQ message broker.
      RabbitMQ Queue Name|HospitalServiceMessageStoreQueue|A fila a qual a subscrição é criada.
      RabbitMQ Exchange Name|exchange|O nome do RabbitMQ exchange ao qual a fila está vinculada.
      Routing Key|key|O valor do exchange e da fila vinculadas.
      User Name| user name| O nome de usuário para conectar ao broker.
      Password|password|A senha para conectar ao broker.

  3. Clique em **Finish**. 

- Criando um Novo Endpoint
  
  Vamos criar um endpoint para representar o serviço backend do Hospital.

  1. Clique com o botão direito em **SampleServiceConfigs** no **Project Explorer** e clique em **New → Endpoint**.
  2. Assegure-se que **Create a New Endpoint** está selecionado e clique em **Next**.
  3. Vamos criar o endpoint do serviço do hospital (**HospitalServicesEP**) utilizando os seguintes valores.

  Property|Value|Descrição
  :-:|:-:|:-:
  Endpoint Name| HospitalServicesEP|Esse é apenas um endpoint configurado para encaminhar requisições para o hospital relevante ao ler os hospitais especificados no payload da requisição
  Endpoint Type|HTTP Endpoint|Indica que o serviço de backend é HTTP.
  URI Template|http://localhost:9090/{uri.var.hospital}/categories/{uri.var.category}/reserve|O template para a URL de request esperado pelo serviço de backend. As seguintes duas variáveis serão trocadas pelos valores correspondentes na mensagem de requisição 1. {uri.var.hospital} 2. {uri.var.category}
  Method|POST|O método REST do HTTP do endpoint.
  Save Endpoint in|SampleServicesConfigs|Esse é o módulo ESB Config que nós criamos na última seção.

  4. Clique em **Finish**.

- Criando uma Sequência
  
  Vamos criar uma Sequência que usa a mensagem no armazenamento de mensagem para enviar a requisição para o endpoint do serviço do hospital.
   
   1. Clique com o botão direito no projeto **SampleServices** no Project Explorer e clique em **New → Sequence**.
   2. Selecione **Create New Sequence** e dê **HospitalServiceSequence** como nome.
   3. Clique em **Finish**.
   4. Na sequência que você acabou de criar (no passo anterior), arraste e solte o mediador Call da paleta **Mediators** e adicione HospitalServicesEP da paleta **Defined Endpoints** para a caixa vazia adjunta ao mediador Call.
   5. Arraste e solte um mediador Log da paleta **Mediators** para logar a resposta do HospitalServicesEP. Acesse a aba **Property** e especifique os detalhes seguintes:
   
      Field|Value
      :-:|:-:|
      Log Category|INFO
      Log Level|FULL
   6. Adicione um mediador Drop da paleta **Mediators**.
   7. Salve a configuração atualizada da sequência.

- Criando o Message Processor
  
  Vamos criar um **Message Sampling Processor** para despachar as mensagens de requisição do **Message Store** para o **HospitalServiceSequence**.

  **Info**: Você também pode usar o **Schedule Message Forwarding Processor** aqui e definir o endpoint de dentro do processador. O **Message Sampling Processor** é usando porque você precisar performar mediação na mensagem de requisição no próximo tutorial.

  1. Clique com o botão direito no projeto **SampleServices** no projec explorer e clique em **New → Message Processor**. Selecione **Create a new message-processor artifact** e especifique os detalhes mostrados abaixo:
  
    Property|Value|Descrição
    :-:|:-:|:-:|
    Message Processor Type|Message Sampling Processor|Esse processador leva a mensagem do armazenamento e a coloca dentro de uma sequência.
    Message Processor Name|HospitalServiceMessageProcessor|O nome do processador de encaminhamento de mensagem agendada.
    Message Store|HospitalServiceMessageStore|O armazenamento de mensagem do qual a mensagem processador de encaminhamento de mensagem agendada consumirá as mensagens.
    Processor State|Activate|Se o processador precisa ser ativado ou desativado.
    Sequence|Siga os passos abaixo: 1. Clique em **Browse**. 2. Clique no link **workspace**. 3. Clique em **Carbon Application Sequences → Sample Services**. 4. Selecione **HospitalServiceSequence** e clique em **OK**.|O nome da sequência a qual a mensagem do armazenamento precisará ser enviada.
  2. Clique em **Finish**.

- Atualize o Mediation Flow

  Vamos atualizar a REST API para que a requisição do cliente seja encaminhada para o armazenamento de mensagem que nós criamos acima.
 
  1. Arraste o mediador **Property** da paleta **Mediators** para a In Sequence do recurso da API e nomeie-o **Get Hospital**. 
  
      **Info**: Isso é usado para extrair o nome do hospital que é enviado no payload da requisição.
  
  2. Com o mediador **Property** selecionado, acesse a aba **Properties** e insira os detalhes seguintes:

      Property|Value|Descrição
      :-:|:-:|:-:|
      Property Name|New Property...|Especifica que a nova propriedade foi criada.
      New Property Name|uri.var.hospital.|O nome que será usado para se referir aos valores da propriedade.
      Property Action|set|A ação da propriedade.
      Property Scope|default|O escopo da propriedade.
      Value|json-eval($hospital_id)| Siga os passos abaixo para especificar o valor da expressão: ![ti5-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/expression-value.png) 1. Clique no botão **Ex** antes do campo **Value**. Isso especificará o tipo de valor como *expression*. 2. Agora clique o botão **f** para abrir a caixa de diálogo do **Expression Selector**. 3. Insira *json-eval($.hospital_id)* como o valor da expressão. **Observação**: Essa é a expressão JSONPath que vai extrair o hospital do payload da requisição.
  
  3. Arraste e adicione o mediador **Store** da paleta de mediadores após o mediador Property.
  4. Com o mediador Store selecionado, acesse a aba **Property** e especifique os seguintes detalhes:
  
      Field|Descrição
      :-:|:-:|
      Avaiable Message Store|Selecione **HospitalServiceMessageStore
      Message Store|Clique duas vezes para popular o valor **HospitalServiceMessageStore**
      Description|Hospital Service Store
  5. Arraste um mediador **Respond** para retornar a resposta do backend do serviço de saúde para o cliente.
 
  Nós agora terminamos de criar todos os artefatos necessários.

#### Passo 3: Empacotar os Artefatos

  Empacote os artefatos em seu módulo **composite application** (SampleServicesCompositeExporter) para estar apto a implantar os artefatos no servidor.

  1. Abra o arquivo *pom.xml* no **composite application project** editor POM.
  2. Assegure-se que os artefatos seguintes estão selecionados no arquivo POM.
  - SampleServicesCompositeExporter 
     - HealthcareAPI
     - HospitalServicesEP
     - HospitalServiceMessageStore
     - HospitalServiceMessageProcessorEP
     - HospitalServiceSequence
  3. Salve o projeto.

#### Passo 4: Inicie o RabbitMQ Broker

  Certifique-se de ter instalado e inicie uma instância de servidor RabbitMQ antes de iniciar o Micro Integrator.

  Veja a [documentação da RabbitMQ](https://www.rabbitmq.com/download.html) para mais informações em como instalar e rodar o produto.

#### Passo 5: Construa e Rode os Artefatos
Para testar os artefatos, implante o artefatos empacotados acima embutidos no Micro Integrator:
1. Clique com o botão direito no módulo **composite exporter** e clique em **Export Project Artifacts and Run**.
2. Na caixa de diálogo que abrirá, confirme que os artefatos requeridos do módulo **composite exporter** estão selecionados.
3. Clique em **Finish**.

Os artefatos serão implantados no Micro Integrator embutido e o servidor será iniciado.
- Veja o log de inicialização na aba **Console**.
- Veja as URLs dos serviços implantados e as APIs na aba **Runtime Services**.

#### Passo 6: Teste o Estudo de Caso

  Vamos testar o estudo de caso enviando uma requisição de cliente simples que invoca o serviço. 

  - Inicie o serviço backend
    1. Baixe o arquivo JAR do serviço de backend [aqui](https://github.com/wso2-docs/WSO2_EI/blob/master/Back-End-Service/Hospital-Service-JDK11-2.0.0.jar).
    2. Abra o terminal, navegue até o local onde seu serviço de backend está salvo.
    3. Execute o seguinte comando para iniciar o serviço:
          
            java -jar Hospital-Service-JDK11-2.0.0.jar 

- Envie a requisição do cliente

  Vamos enviar a requisição para o recurso da API. Você pode usar um **HTTP Client** embutido do WSO2 Integration Studio como segue:
  1. Abra a aplicação Postman. Se você não tiver a aplicação, baixe-a [aqui](https://www.postman.com/downloads/).
  2. Adicione a informação requerida como dada abaixo e clique no botão **Send**.

      Method|POST
      :-:|:-:
      Headers|Content-Type=application/json
      URL|http://localhost:8290/healthcare/categories/surgery/reserve . O Formato da URI-Template que é usado nessa URL foi definida durante a criação do recurso da API QueryDoctorAPI: *http://:/categories/{category}/reserve* . 
      Body| { "patient": { "name": "John Doe", "dob": "1940-03-19", "ssn": "234-23-525", "address": "California", "phone": "8770586755", "email": "johndoe@gmail.com" }, "doctor": "thomas collins", "hospital_id": "grandoaks", "hospital": "grand oak community hospital", "appointment_date": "2025-04-02" } . Esse payload JSON contém detalhes do agendamento da consulta, o que inclui detalhes do paciente, médico, hospital e data da consulta.

  Se você quiser enviar a requisição do cliente de seu terminal:
     1. Instale e configure [cUrl](https://curl.haxx.se) como seu cliente REST.
     2. Crie um arquivo JSON chamado *request.json* com o seguinte payload de requisição. 
        
            {
              "patient": {
              "name": "John Doe",
              "dob": "1940-03-19",
              "ssn": "234-23-525",
              "address": "California",
              "phone": "8770586755",
              "email": "johndoe@gmail.com"
              },
              "doctor": "thomas collins",
              "hospital_id": "grandoaks",
              "hospital": "grand oak community hospital",
              "appointment_date": "2025-04-02"
            }
     3. Abra uma linha de comando do terminal e execute o seguinte comando do local onde o arquivo *request.json* foi criado.

            curl -v -X POST --data @request.json http://localhost:8290/healthcare/categories/surgery/reserve --header "Content-Type:application/json"

- Analise a resposta

  Você verá a seguinte resposta recebida em seu **HTTP Client**: 

      {"appointmentNumber":1,
       "doctor":
          {"name":"thomas collins",
           "hospital":"grand oak community hospital",
           "category":"surgery","availability":"9.00 a.m - 11.00 a.m",
           "fee":7000.0},
       "patient":
          {"name":"John Doe",
           "dob":"1990-03-19",
           "ssn":"234-23-525",
           "address":"California",
           "phone":"8770586755",
           "email":"johndoe@gmail.com"},
         "fee":7000.0,
       "confirmed":false,
       "appointmentDate":"2025-04-02"}

  Agora cheque a aba **Console** do WSO2 Integration Studio e você verá a seguinte mensagem:
    
      INFO - LogMediator message = Routing to grand oak community hospital.

      [2017-04-30 14:33:48,578] [EI-Core]  INFO - LogMediator message = Routing to grand oak community hospital

      [2017-04-30 14:33:48,598] [EI-Core]  INFO - TimeoutHandler This engine will expire all callbacks after GLOBAL_TIMEOUT: 120 seconds, irrespective of the timeout action, after the specified or optional timeout

      2017-04-30 14:33:53,464] [EI-Core]  INFO - LogMediator To: http://www.w3.org/2005/08/addressing/anonymous, WSAction: , SOAPAction: , MessageID: urn:uuid:a2cf1fd2-7a89-44b6-9571-990bbdfbd289, Direction: request, Payload: {"appointmentNo":1,"doctorName":"thomas collins","patient":"John Doe","actualFee":7000.0,"discount":20,"discounted":5600.0,"paymentID":"a77038e9-3e42-46f7-ac97-11e1b3a50018","status":"Settled"}

Você acabou de descobrir como o Micro Integrator pode ser usado para implementar armazenamento e encaminhamento de mensagem usando o **Message Store**, **Message Processor** e o **Store Mediator**.

- [Índice](#documentação-api-manager-410)
 
### Expondo Datasources como um Serviço
#### Contexto
Um **data service** oferece uma interface de serviço web para acessar dados que estão armazenados em várias fontes de dados. As seções seguintes descrevem como você pode usar o WSO2 Integration Studio para trabalhar com artefatos de data service.

**Dica**: Observe que essa feature é atualmente suportada no WSO2 Integration Studio para datasources relacionais e arquivos CSV.

#### Passo 1: Configurar o Workspace

- Download o [WSO2 Integration Studio](https://wso2.com/api-management/tooling/) relevante baseado em seu sistema operacional. O path para a extração/instalação é referido como *MI_TOOLING_HOME* através desse tutorial.

- Para demonstrar como data services funcionam, nós vamos usar um database MySQL como datasource. Siga os passos abaixo para configurar um database MySQL:
  1. Instale o servidor MySQL.
  2. Baixe o driver JDBC para MSQL [daqui](https://dev.mysql.com/downloads/connector/j/). Você vai precisar disso quando for configurar o servidor MySQL com o Micro Integrator.
  3. Crie um database chamado *Employees*.
  
          CREATE DATABASE Employees;
  4. Crie um usuário e garanta ao usuário acesso à Database.
  
          CREATE USER 'user'@'localhost' IDENTIFIED BY 'password'; GRANT ALL PRIVILEGES ON Employees.* TO 'user'@'localhost'; 
  5. Crie a tabela Employee dentro da database Employees.
  USE Employees;

          CREATE TABLE Employees (EmployeeNumber int(11) NOT NULL, FirstName varchar(255) NOT NULL, LastName varchar(255) DEFAULT NULL, Email varchar(255) DEFAULT NULL, Salary varchar(255));
          INSERT INTO Employees (EmployeeNumber, FirstName, LastName, Email, Salary) values (3, "Edgar", "Code", "edgar@rdbms.com", 100000);

#### Passo 2: Criando um Data Service
Siga os passos abaixo para criar um novo data service.

- Criando um Projeto Especializado Multimodular

  Todo os artefatos do data service que você criar deve estar armazenado no Módulo Data Service. Siga os passos abaixo para criar um módulo. 
  
  1. Abra o **WSO2 Integration Studio** e clique em **New Maven Multi Module Project** na aba **Getting Started** como mostrado abaixo. ![ti6-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/create_project/create_mmm_project.png)

  2. Na caixa de diálogo **Maven Modules Creation** que abrirá, dê um nome (artifactId) para o projeto.
  3. Se necessário, mude a informação Maven sobre o projeto.
  4. Clique em **Finish**. O novo projeto será listado no project explorer.

- Criando um Módulo de Data Service
  
  Todo os artefatos do data service que você criar deve estar armazenado no Módulo Data Service. Siga os passos abaixo para criar um módulo.

  1. Clique com o botão direito no **Maven Multi Module Project** criado e vá para **New → Data Service Configs**.
  2. Na caixa de diálogo **New Data Service Configs** que abrirá, dê o nome para o módulo config e clique em **Next**.
  3. Se necessário, mude a informação Maven sobre o module config.
  4. Clique em **Finish**. O novo módulo será listado no project explorer.

- Criando o Data Service

  Siga os passos abaixo para criar o arquivo data service.

  1. Selecione o já criado módulo **Data Service Config** no project explorer, clique com o botão direito e vá para **New → Data Service**. A janela **New Data Service** abrirá como mostrado abaixo. ![ti6-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/119130577/119130578.png)
  2. Para começar a criar um data service do zero, selecione **Create New Data Service** e clique em **Next** para ir à próxima página.
  3. Insira um nome para o data service e clique em **Finish**. ![ti6-3](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/new_dataservice.png)

      Property|Descrição
      :-:|:-:|
      Data Service Name|RDBMSDataService

      Um arquivo data service (arquivo DBS) será criado em seu módulo data service como mostrado abaixo. ![ti6-4](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/dataservice_view.png)

- Criando uma Conexão Datasource
  1. Clique em **Data Sources** para expandir a seção. ![ti6-5](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/data_source_expanded.png)
  2. Clique em **Add New** para abrir a página **Create Datasource**. ![ti6-6](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/add_data_source.png)
  3. Insira os detalhes da conexão datasource como dado abaixo.
  
      Property|Descrição
      :-:|:-:|
      Datasource ID|Datasource
      Datasource Type|RDBMS
      Datasource Type (Default/External)|Deixe **Default** selecionado.
      Database Engine|MySQL
      Driver Class|com.mysql.jdbc.Driver
      URL|jdbc:mysql://localhost:3306/Employees
      Username|user
      Password|password 
  4. Clique em **Test Connection** para expandir a seção. ![ti6-7](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/test_connection.png)
  5. Clique no botão **Test Connection** para verificar a conectividade entre o MySQL datasource e o data service.
  6. Salve o data service.

- Criado uma Query
  
  Vamos escrever uma query SQL para GET data do datasource MySQL que você configurou no passo anterior:
  
  1. Clique em **Queries** para expandir a seção. ![ti6-8](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/query_expanded.png)
  2. Clique em **Add New** para abrir a página **Add Query**. ![ti6-9](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/add_query.png)
  3. Insira os detalhes seguintes sobre a query:
  
      Parameter|Descrição
      :-:|:-:
      Query ID| GetEmployeeDetails
      Datasource|Datasource
      SQL Query| select EmployeeNumber, FirstName, LastName, Email from Employees where EmployeeNumber=:EmployeeNumber     
  4. Clique em **Input Mappings** para expandir a seção. ![ti6-10](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/input_mapping_expanded.png) 
  5. Clique em **Generate** para gerar input mappings automaticamente.
  
      **Dica**: Alternativamente, você pode manualmente adicionar os mappings. 
      
      1. Clique em **Add New** para abrir a página **Add Input Mapping**. 
       
      2. Insira os seguintes detalhes de elementos de input.

      Property|Descrição
      :-:|:-:
      Mapping Name|EmployeeNumber
      Parameter Type|SCALAR
      SQL Type|SCALAR 

  6. Salve o input mapping. ![ti6-11](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/input_mappings.png)
   
  7. Clique em **Result (Output Mappings)** para expandir a seção. ![ti6-12](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/out_mapping_expanded.png)
   
  8. Insira os seguintes valores para agrupar o output mapping:
  
      Property|Descrição
      :-:|:-:
      Grouped by Element|Employees

  9.  Clique em **Generate** para gerar os output mappings automaticamente.
      
      **Dica**: Alternativamente, você pode manualmente adicionar os mappings. 
      
      1. Clique em **Add New** para abrir a página **Add Output Mapping**. 
      
      2.  Insira os seguintes detalhes de elementos de input.

          Property|Descrição
          :-:|:-:
          Datasource Type|column
          Output Field Name|EmployeeNumber
          Datasource Column Name|EmployeeNumber
          Schema Type|String

      3. Salve o elemento.
      4. Siga os mesmos passos para criar os seguintes elementos output:
      
              | Datasource Type | Output Field Name | Datasource Column Name | Schema Type |
              |-----------------|-------------------|------------------------|-------------|
              | column          | FirstName         | FirstName              | string      |
              | column          | LastName          | LastName               | string      |
              | column          | Email             | Email                  | string      | 
  10. Clique em Salvar para salvar a query. ![ti6-13](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/output_mapings.png)

- Criando um Recurso para Invocar a Query
  
  Agora vamos criar um recurso REST que pode ser usado para invocar a query.

  1. Clique em **Resources** para expandir a seção. ![ti6-14](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/resource_expanded.png)
  2. Clique em **Add New** para abrir a página **Create Resource**. ![ti6-15](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/create_resource.png) 
  3. Insira os seguintes detalhes do recurso.
  
      Property|Descrição
      :-:|:-:|
      Resource Path| Employee/{EmployeeNumber}
      Resource Method|GET
      Query ID|GetEmployeeDetails

  4. Salve o recurso.
  
      **Dica**: Alternativamente, você pode gerar um data service de um datasource. Para mais informações, veja [Gerar Data Services](https://apim.docs.wso2.com/en/latest/integrate/develop/creating-artifacts/data-services/creating-data-services/#generate-data-service-from-a-datasource)

#### Passo 3: Empacotar os Artefatos

  Crie um novo módulo composite exporter.

  1. Clique com o botão direito em **Maven Multi Module Project** e vá para **New → Composite Exporter**.
  2. Na caixa de diálogo que abrirá, selecione o arquivo data service e clique em **Finish**. ![ti6-16](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/data_services/composite_app.png) Empacote os artefatos em seu composite exporter para estar apto a implementar os artefatos no servidor.
     
     1. Abra o arquivo *pom.xml* no composite application.
     2. Assegure-se que seu arquivo data service está selecionado no arquivo POM.
     3. Salve o arquivo. 

#### Passo 4: Configurando o Servidor Micro Integrator

  Nós vamos usar o embutido Micro Integrator do WSO2 Integration Studio para rodar essa solução.

  Para adicionar o driver do database MySQL ao servidor:

  1. Clique em **Embedded Micro Integrator Configuration**, cujo ícone ![ti6-17](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/server-config-64x64.png) fica na parte de cima do menu, para abrir a caixa de diálogo.
  2. Clique no ícone + para adicionar o driver JAR do MySQL para o diretório */lib* do embutido Micro Integrator.
  
  Se a classe do driver não existe no diretório relevante, você vai receber uma exceção como *Cannot load JDBC driver class com.mysql.jdbc.Driver* quando o Micro Integrator iniciar.

#### Passo 5: Construa e Rode os Artefatos
Para testar os artefatos, implante o artefatos empacotados acima embutidos no Micro Integrator:
1. Clique com o botão direito no módulo **composite exporter** e clique em **Export Project Artifacts and Run**.
2. Na caixa de diálogo que abrirá, confirme que os artefatos requeridos do módulo **composite exporter** estão selecionados.
3. Clique em **Finish**.

Os artefatos serão implantados no Micro Integrator embutido e o servidor será iniciado.
- Veja o log de inicialização na aba **Console**.
- Veja as URLs dos serviços implantados e as APIs na aba **Runtime Services**.

#### Passo 6: Testando o Data Service
Vamos testar o estudo de caso enviando uma requisição de cliente simples que invoca o serviço. 

- Envie a requisição do cliente

  Vamos enviar a requisição para o recurso da API fazer o agendamento. Você pode usar o **HTTP Client** embutido do WSO2 Integration Studio como segue:

  1. Abra a aplicação Postman. Se você não tiver a aplicação, baixe-a [aqui](https://www.postman.com/downloads/).
  
  2. Adicione a informação do requerida como dada abaixo e clique no botão **Send**.
    
      Method|GET
      :-:|:-:
      URL|http://localhost:8290/services/RDBMSDataService.HTTPEndpoint/Employee/3

      ![ti6-18](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/119132155/rdbms-employee.png)

  Se você quiser enviar a requisição do cliente de seu terminal:

    1. Instale e configure [cUrl](https://curl.haxx.se) como seu cliente REST.
    2. Execute o seguinte comando.
    
           curl -X GET http://localhost:8290/services/RDBMSDataService.HTTPEndpoint/Employee/3 

- Analise a Resposta
  
  Você receberá seguinte resposta recebida de seu **HTTP Client**:

      <Employees xmlns="http://ws.wso2.org/dataservice">
        <EmployeeNumber>3</EmployeeNumber>
        <FirstName>Edgar</FirstName>
        <LastName>Code</LastName>
        <Email>edgar@rdbms.com</Email>
      </Employees>

- [Índice](#documentação-api-manager-410)

### Processamento de Arquivo
#### Contexto
Esse exemplar demonstra como pegar um arquivo de uma pasta e processá-lo com o Micro Integrator. Nesse cenário, você pegará um arquivo de um diretório local, inserir os registros no arquivo para uma database, enviar um email com o conteúdo do arquivo, rastrear e escrever o log e finalmente mover o arquivo para outro diretório.

#### Passo 1: Configurar o Workspace
  
  Download o [WSO2 Integration Studio](https://wso2.com/api-management/tooling/) relevante baseado em seu sistema operacional.

  Vamos configurar uma database MySQL:

  1. Manualmente configure a database.
  2. Crie uma tabela chamada de *info* no seu esquema. Você pode rodar os seguintes comandos para fazer isso.
  
          delimiter $$

          CREATE TABLE `info` (
            `name` varchar(45) DEFAULT '',
            `surname` varchar(45) DEFAULT NULL,
            `phone` varchar(45) DEFAULT NULL
          ) ENGINE=InnoDB DEFAULT CHARSET=utf8$$ 
  3. Certifique-se que a tabela *info* foi criada e que ela contém as seguintes colunas:
      - name
      - surname
      - phone

#### Passo 2: Desenvolva os Artefatos de Integração

  Siga as instruções dadas nessa seção para criar e configurar os artefatos necessários.

- Criando um projeto de integração

  Crie um projeto de integração com os seguintes módulos: **ESB Configs** e **Composite Exporter**.
  
  1. Abra o **WSO2 Integration Studio**.
  2. Clique em **New Integration Project** na aba **Getting Started** como mostrado abaixo. ![ti7-1](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/common/create-integration-project.jpg)
  3. Insira *FileProcessingService* como o nome do projeto.
  4. Clique em **Finish**. O projeto criado foi salvo no **Project Explorer**.

- Crie as Sequências Main e Fault
  
  1. Crie a Sequência Main com a configuração seguinte. Veja as instruções em [Criando uma Sequência](https://apim.docs.wso2.com/en/latest/integrate/develop/creating-artifacts/creating-reusable-sequences/).

          <sequence name="main" xmlns="http://ws.apache.org/ns/synapse">
            <in>
              <log level="full"/>
              <filter regex="http://localhost:9000.*" source="get-property('To')">
                <then>
                  <send/>
                </then>
                <else/>
              </filter>
            </in>
            <out>
              <send/>
            </out>
          </sequence>
  2. Crie uma sequência Fault com a configuração seguinte. Veja as instruções em [Criando uma Sequência](https://apim.docs.wso2.com/en/latest/integrate/develop/creating-artifacts/creating-reusable-sequences/).
  
          <sequence name="fault" trace="disable" xmlns="http://ws.apache.org/ns/synapse">
            <log level="full">
              <property name="MESSAGE" value="Executing default 'fault' sequence"/>
              <property expression="get-property('ERROR_CODE')" name="ERROR_CODE"/>
              <property expression="get-property('ERROR_MESSAGE')" name="ERROR_MESSAGE"/>
            </log>
            <drop/>
          </sequence> 

- Crie o *FileProxy*
  
  1. Crie o serviço proxy chamdo *FileProxy* com a configuração seguinte. Veja as instruções em [Criando um Serviço Proxy](https://apim.docs.wso2.com/en/latest/integrate/develop/creating-artifacts/creating-a-proxy-service/)

          <proxy xmlns="http://ws.apache.org/ns/synapse" name="FileProxy" transports="vfs" startOnLoad="true" trace="disable">
            <target>
              <inSequence>
                <log level="full"/>
                <clone>
                  <target sequence="fileWriteSequence"/>
                  <target sequence="sendMailSequence"/>
                  <target sequence="databaseSequence"/>
                </clone>
              </inSequence>
            </target>
            <parameter name="transport.vfs.ActionAfterProcess">MOVE</parameter>
            <parameter name="transport.PollInterval">15</parameter>
            <parameter name="transport.vfs.MoveAfterProcess">file:///home/username/test/original</parameter>
            <parameter name="transport.vfs.FileURI">file:///home/username/test/in</parameter>
            <parameter name="transport.vfs.MoveAfterFailure">file:///home/username/test/failure</parameter>
            <parameter name="transport.vfs.FileNamePattern">.*.txt</parameter>
            <parameter name="transport.vfs.ContentType">text/plain</parameter>
            <parameter name="transport.vfs.ActionAfterFailure">MOVE</parameter>
          </proxy>
  
  2. Edite o serviço proxy e defina o diretório ao qual o arquivo original deverá ser movido após o processamento.
  
          <parameter name="transport.vfs.MoveAfterProcess">[file:///home/]<username>/test/original</parameter>  

  3. Edite o serviço proxy e defina onde o arquivo input deverá ser colocado.

          <parameter name="transport.vfs.FileURI">[file:///home/]<username>/test/in</parameter>
  
  4. Edite o serviço proxy e defina o diretório ao qual o arquivo deverá ser movido se um erro ocorrer.

          <parameter name="transport.vfs.MoveAfterFailure">[file:///home/]<username>/test/failure</parameter>

- Crie a *databaseSequence*

  Siga as instruções abaixo para criar uma sequência que pode ser usada para conectar à base de dados para inserir dados.

  1. Crie uma sequência chamada *databaseSequence* com a seguinte configuração. Veja as instruções em [Criando uma Sequência](https://apim.docs.wso2.com/en/latest/integrate/develop/creating-artifacts/creating-reusable-sequences/).

          <sequence xmlns="http://ws.apache.org/ns/synapse" name="databaseSequence">
            <log level="full">
              <property name="sequence" value="before-smooks"/>
            </log>
            <smooks config-key="smooks">
              <input type="text"/>
              <output type="xml"/>    
            </smooks>
            <log level="full">
              <property name="sequence" value="after-smooks"/>
            </log>
            <iterate expression="//csv-set/csv-record">
              <target>
              <sequence>
              <dbreport>
              <connection>
                <pool>
                  <password>db-password</password>
                  <user>db-username</user>
                  <url>jdbc:mysql://localhost:3306/test</url>
                  <driver>com.mysql.jdbc.Driver</driver>
                </pool>
              </connection>
                  <statement>
                    <sql><![CDATA[insert into INFO values (?, ?, ?)]]></sql>
                      <parameter expression="//csv-record/name/text()" type="VARCHAR"/>
                      <parameter expression="//csv-record/surname/text()" type="VARCHAR"/>
                      <parameter expression="//csv-record/phone/text()" type="VARCHAR"/>
                  </statement>
                 </dbreport>
               </sequence>
             </target>
           </iterate>
         </sequence>
  
  2. Especifique no database seu username,  password e URL na seção \<pool> da sequência.

- Crie o *fileWriteSequence*

  1. Crie a sequência chamada *fileWriteSequence* com a seguinte configuração. Veja as instruções em [Criando uma Sequência](https://apim.docs.wso2.com/en/latest/integrate/develop/creating-artifacts/creating-reusable-sequences/).

          <sequence xmlns="http://ws.apache.org/ns/synapse" name="fileWriteSequence">
            <log level="custom">
              <property name="sequence" value="fileWriteSequence"/>
            </log>
            <property xmlns:ns2="http://org.apache.synapse/xsd" name="transport.vfs.ReplyFileName" expression="fn:concat(fn:substring-after(get-property('MessageID'), 'urn:uuid:'), '.txt')" scope="transport"/>
            <property name="OUT_ONLY" value="true"/>
            <send>
              <endpoint name="FileEpr">
                <address uri="vfs:file:///home/username/test/out"/>
              </endpoint>
            </send>
          </sequence>
  
  2. Edite a sequência e defina o diretório ao qual o arquivo deve ser movido.

- Crie a *sendMailSequence*

  1. Crie uma sequência chamada *sendMailSequence* com a configuração seguinte. Veja as instruções em [Criando uma Sequência](https://apim.docs.wso2.com/en/latest/integrate/develop/creating-artifacts/creating-reusable-sequences/).

          <sequence xmlns="http://ws.apache.org/ns/synapse" name="sendMailSequence">
            <log level="custom">
              <property name="sequence" value="sendMailSequence"/>
            </log>
            <property name="messageType" value="text/html" scope="axis2"/>
            <property name="ContentType" value="text/html" scope="axis2"/>
            <property name="Subject" value="File Received" scope="transport"/>
            <property name="OUT_ONLY" value="true"/>
            <send>
              <endpoint name="FileEpr">
                <address uri="mailto:username@gmail.com"/>
              </endpoint>
            </send>
          </sequence>
  
  2. Edite a sequência e defina o endereço de email ao qual a notificação deverá ser enviada.

- Crie a Configuração Smooks

  Crie o arquivo de configuração smooks (por exemplo *smooks-config.xml*) como mostrado abaixo e salve em um local em seu computador.

      <smooks-resource-list xmlns="http://www.milyn.org/xsd/smooks-1.0.xsd">
        <!--Configure the CSVParser to parse the message into a stream of SAX events. -->
        <resource-config selector="org.xml.sax.driver">
          <resource>org.milyn.csv.CSVReader</resource>
          <param name="fields" type="string-list">name,surname,phone</param>
        </resource-config>
      </smooks-resource-list>

- Crie uma Local Registry Entry

  Configure uma entrada local como mostrado abaixo. Essa entrada local vai ser usada para referir-se à configuração smooks. Veja as instruções em [Criando uma Configuração de Registro Local](https://apim.docs.wso2.com/en/latest/integrate/develop/creating-artifacts/registry/creating-local-registry-entries/)

      <localEntry key="smooks" src="file:resources/smooks-config.xml"/>]

#### Passo 3: Empacotar os Artefatos

  Empacote os artefatos em seu módulo **composite application** para estar apto a implantar os artefatos no servidor.

1. Abra o arquivo *pom.xml* no módulo **composite exporter**.
2. Assegure-se que os artefatos relevantes estão selecionados no arquivo POM.
3. Salve as mudanças.

#### Passo 4: Configure o Servidor Micro Integrator

  1. Clique no ícone **Embedded Micro Integrator Configuration** na parte de cima do menu para abrir a caixa de diálogo. ![ti7-2](https://apim.docs.wso2.com/en/4.1.0/assets/img/integrate/tutorials/file-processing/embedded-server-configs.png)
  2. Adicione as configurações de servidor seguintes (ao arquivo *deployment.toml*) usando a seção de cima na caixa de diálogo.
      - O transporte **VFS** está habilitado no Micro Integrator por padrão. Ative o [transporte MailTo](https://apim.docs.wso2.com/en/latest/install-and-setup/setup/mi-setup/transport_configurations/configuring-transports/#configuring-the-mailto-transport) para enviar a mensagem de email como mostrado abaixo e atualize os valores:

            [[transport.mail.sender]]
            name = "mailto"
            parameter.hostname = "smtp.gmail.com"
            parameter.port = "587"
            parameter.enable_tls = true
            parameter.auth = true
            parameter.username = "demo_user"
            parameter.password = "mailpassword"
            parameter.from = "demo_user@wso2.com"
      **Observação**: Nesse exemplo, você não receberá emails de uma caixa de email. Portanto, você não precisará habilitar o mailto transport receiver.
      
      - Adicione o seguinte formatador de mensagem:
      
            text_xml = "org.apache.axis2.transport.http.ApplicationXMLFormatter"
  
  3. Clique no ícone + na seção de baixo e adicione os seguintes drivers e bibliotecas.
     - [MySQL database driver](https://github.com/wso2-docs/WSO2_EI/blob/master/Integration-Tutorial-Artifacts/Integration-Tutorial-Artifacts-EI7.1.0/EI7.1.0-file-processing-tutorial-JARS/mysql-connector-java-5.1.10-bin.jar)
     - [CSV smooks library](https://github.com/wso2-docs/WSO2_EI/blob/master/Integration-Tutorial-Artifacts/Integration-Tutorial-Artifacts-EI7.1.0/EI7.1.0-file-processing-tutorial-JARS/milyn-smooks-csv-1.2.4.jar)
  
  **Observação**: Essas foram copiadas da pasta */lib* do Micro Integrator embutido.

#### Passo 5: Construa e Rode os Artefatos

Para testar os artefatos, implante o artefatos empacotados acima embutidos no Micro Integrator:

1. Clique com o botão direito no módulo **composite exporter** e clique em **Export Project Artifacts and Run**.

2. Na caixa de diálogo que abrirá, confirme que os artefatos requeridos do módulo **composite exporter** estão selecionados.

3. Clique em **Finish**.

Os artefatos serão implantados no Micro Integrator embutido e o servidor será iniciado.
- Veja o log de inicialização na aba **Console**.
- Veja as URLs dos serviços implantados e as APIs na aba **Runtime Services**.

#### Passo 6: Teste o Estudo de Caso

- Crie o Arquivo Input
  
  Crie um arquivo de texto com o formato a seguir:

      name_1, surname_1, phone_1
      name_2, surname_2, phone_2
  
  Salve o arquivo no formato *.txt* no diretório *in* que você especificou.

- Analise o Resultado

  O Micro Integrator monitora o diretório local do arquivo no sistema. Quando um arquivo é jogado dentro do diretóri *in*, o Micro Integrator pega o arquivo.

  1. Certifique-se que o arquivo aparece no diretório *out*.
  2. O Micro Integrator insere as gravações de um arquivo de texto para o banco de dados. Certifique-se que os dados estão na tabela de informação.
  3. Certifique-se o arquivo original foi movido para o diretório */home/\<username>/test/original* .
  4. Certifique-se que a notificação de email é enviada para o endereço de email especificado. A mensagem deve conter os dados do arquivo. Se você receber a mensagem de erro *Username and Password not accepted* no log, você deve precisar habilitar *Allow less secure apps* na sua [conta Google](https://myaccount.google.com/intro/security).

- [Índice](#documentação-api-manager-410)

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
