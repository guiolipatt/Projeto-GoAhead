# Documentação API Manager 4.1.0
- [Documentação API Manager 4.1.0](#documentação-api-manager-410)
  - [Tutoriais - Visão Geral](#tutoriais---visão-geral)
  - [Tutoriais de Cenário](#tutoriais-de-cenário)
    - [Cenário 1: Criar uma REST API através de uma OpenAPI Definition](#cenário-1-criar-uma-rest-api-através-de-uma-openapi-definition)
    - [Cenário 2: Permitir Controle de Acesso para a API](#cenário-2-permitir-controle-de-acesso-para-a-api)
    - [Cenário 3: Implementando uma API](#cenário-3-implementando-uma-api)
    - [Cenário 4: Inscrevendo um Novo Usuário](#cenário-4-inscrevendo-um-novo-usuário)
    - [Cenário 5: Envolvendo a Comunidade de Desenvolvedores](#cenário-5-envolvendo-a-comunidade-de-desenvolvedores)
    - [Cenário 6: Integrando com Data Sources](#cenário-6-integrando-com-data-sources)
    - [Cenário 7: Analytics](#cenário-7-analytics)
    - [Cenário 8: Limitação de Taxa](#cenário-8-limitação-de-taxa)
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
#### História do Usuário
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
### Cenário 3: Implementando uma API
### Cenário 4: Inscrevendo um Novo Usuário
### Cenário 5: Envolvendo a Comunidade de Desenvolvedores
### Cenário 6: Integrando com Data Sources
### Cenário 7: Analytics
### Cenário 8: Limitação de Taxa
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
