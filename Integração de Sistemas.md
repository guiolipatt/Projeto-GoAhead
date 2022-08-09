# Introdução à Integração de Sistemas #
***
## O que é? ##

A **Integração de Sistemas** é uma solução tecnológica para automatizar uma série de procedimentos operacionais proporcionando ganho de produtividade com a otimização do fluxo de trabalho.

Diversas empresas possuem diferentes sistemas de gestão, cada um com seu conjunto de dados. Por exemplo, um sistema contábil, outro de gestão financeira e até mesmo de estoque. A ausência da integração reflete na forma precária em que os conjuntos de dados se comunicam. Os processos funcionam de maneira mais harmoniosa, sem intervalos ociosos ou lacunas, quando há uma compactação dos sistemas utilizados aperfeiçoando a ligação entre os processos.

Através do compartilhamento de dados há aumento e melhora da produtividade, diminuição dos erros amparados por sistemas automatizados e integrados, redução de custos eliminando informações conflitantes ou duplicadas, otimização dos processos e, por consequência, a ampliação do diferencial competitivo no mercado.

Uma integração bem alinhada ocorre mediante o mapeamento visando identificar as falhas inerentes de cada processo mantido pela empresa, dessa forma providenciando os ajustes para a melhoria do fluxo operacional com a preparação da equipe de colaboradores para a adoção do modelo de integração em contínuo controle na avaliação de resultados.
***
## Tipos de Integração de Sistemas ##
- **Integração banco a banco**

    A partir de um banco de dados comum os sistemas são integrados por intermédio de um software apropriado de extração de dados.

- **Integração via compartilhamento de dados eletrônicos**

  Nesse caso os dados utilizados são exportados ou importados de um sistema para outro.

- **Integração por meio de API** (*Application Programming Interface*)

    Tende a ser a mais indicada com o trânsito em tempo real de conjunto de dados de um sistema ao outro garantindo maior velocidade de tráfego de dados, além de uma comunicação direta dispensando processos intermediários.
***
## Catálogo de Padrões de Integração de Sistemas - EIP (*Enterprise Integration Patterns*) ##
1. **Mensagem**
   
Ícone | Nome | Descrição
:---: |  :---: |  :---:    
![Command Message](https://docs.wso2.com/download/attachments/12421407/CommandMessage.png?version=1&modificationDate=1345664065000&api=v2) | Mensagem - Comando | Chama um procedimento em outra aplicação de forma confiável.
![Document Message](https://docs.wso2.com/download/attachments/12421407/DocumentMessage.png?version=1&modificationDate=1345664107000&api=v2) | Mensagem - Documento | Transferir uma estrutura de dados entre aplicações de forma confiável.
![Event Message](https://docs.wso2.com/download/attachments/12421407/EventMessage.png?version=1&modificationDate=1345664142000&api=v2) | Mensagem - Evento | Para notificação assíncrona e confiável entre aplicações.
![Request-Reply](https://docs.wso2.com/download/attachments/12421407/RequestReply.png?version=1&modificationDate=1345664354000&api=v2) | Requisição - Resposta | xxx
![Return Adress](https://docs.wso2.com/download/attachments/12421407/ReturnAddress.png?version=1&modificationDate=1345664376000&api=v2) | Endereço de Resposta | xxx
![Correlation Identifier](https://docs.wso2.com/download/attachments/12421407/CorrelationIdentifier.png?version=1&modificationDate=1345664396000&api=v2) | Identificador de Correlação | xxx
![Message Sequence](https://docs.wso2.com/download/attachments/12421407/MessageSequence.png?version=1&modificationDate=1345664431000&api=v2) | Sequência de Mensagens | xxx
![Message Expiration](https://docs.wso2.com/download/attachments/12421407/MessageExpiration.png?version=1&modificationDate=1345664478000&api=v2) | Prazo de Validade | xxx
*| Indicador de Formato | xxx

2. **Canais**
   
Ícone | Nome | Descrição
:---: |  :---: |  :---:
![Point-to-Point Channel](https://docs.wso2.com/download/attachments/12421407/PointToPoint.png?version=1&modificationDate=1345663460000&api=v2) | Canal Ponto-a-Ponto | xxx
![Publish-Subscribe Channel](https://docs.wso2.com/download/attachments/12421407/PublishSubscribe.png?version=1&modificationDate=1345663504000&api=v2) | Canal Publicar - Inscrever | xxx
![Datatype Channel](https://docs.wso2.com/download/attachments/12421407/DatatypeChanne.png?version=1&modificationDate=1345663551000&api=v2) | Canal de Tipo de Dados | xxx
![Invalid Message Channel](https://docs.wso2.com/download/attachments/12421407/InvalidMessageChannel.png?version=1&modificationDate=1345663659000&api=v2) | Canal de Mensagens Inválidas | xxx
![Dead Letter Channel](https://docs.wso2.com/download/attachments/12421407/DeadLetterChannel.png?version=1&modificationDate=1345663711000&api=v2) | Canal de Mensagens Não - Entregues | xxx
![Guaranteed Delivery](https://docs.wso2.com/download/attachments/12421407/GuaranteedMessaging.png?version=1&modificationDate=1345663759000&api=v2) | Entrega Garantida | xxx
![Channel Adapter](https://docs.wso2.com/download/attachments/12421407/ChannelAdapter.png?version=1&modificationDate=1345663817000&api=v2) | Adaptador de Canal | xxx
![Messaging Bridge](https://docs.wso2.com/download/attachments/12421407/MessagingBridge.png?version=1&modificationDate=1345663925000&api=v2) | Ponte de Mensageria | xxx
![Message Bus](https://docs.wso2.com/download/attachments/12421407/MessageBus.png?version=1&modificationDate=1345663937000&api=v2) | Barramento de Mensagem | xxx

3. **Mensageria**

Ícone | Nome | Descrição
:---: |  :---: |  :---:
![Message Channels](https://docs.wso2.com/download/attachments/12421407/Channels.png?version=1&modificationDate=1345659503000&api=v2) | Canal de Mensagens | xxx
![Message](https://docs.wso2.com/download/attachments/12421407/Message.png?version=1&modificationDate=1345659518000&api=v2) | Mensagem | xxx
![Pipes and Filters](https://docs.wso2.com/download/attachments/12421407/PipesAndFiltersIcon.gif?version=1&modificationDate=1345659576000&api=v2) | Dutos e Filtros | xxx
![Message Router](https://docs.wso2.com/download/attachments/12421407/ContentBasedRouterIcon.gif?version=1&modificationDate=1345660358000&api=v2) | Roteador de Mensagens | xxx
![Message Translator](https://docs.wso2.com/download/attachments/12421407/MessageTranslatorIcon.gif?version=1&modificationDate=1345660483000&api=v2) | Tradutor de Mensagens | xxx
![Message Endpoint](https://docs.wso2.com/download/attachments/12421407/MessageEndpoint.png?version=1&modificationDate=1345660568000&api=v2) | Endpoint de Mensageria | xxx

4. **Roteamento**

Ícone | Nome | Descrição
:---: |  :---: |  :---:
![Content-Based Router](https://docs.wso2.com/download/attachments/12421407/ContentBasedRouter.png?version=1&modificationDate=1345665188000&api=v2) | Roteador baseado em conteúdo | xxx
![Message Filter](https://docs.wso2.com/download/attachments/12421407/MessageFilter.png?version=1&modificationDate=1345665231000&api=v2) | Filtro de Mensagens | xxx
![Dynamic Router](https://docs.wso2.com/download/attachments/12421407/DynamicRouter.png?version=1&modificationDate=1345665267000&api=v2) | Roteador Dinâmico | xxx
![Recipient List](https://docs.wso2.com/download/attachments/12421407/RecipientList.png?version=1&modificationDate=1345665338000&api=v2) | Lista de Receptores | xxx
![Splitter](https://docs.wso2.com/download/attachments/12421407/Splitter.png?version=1&modificationDate=1345665389000&api=v2) | Divisor | xxx
![Aggregator](https://docs.wso2.com/download/attachments/12421407/Aggregator.png?version=1&modificationDate=1345665422000&api=v2) | Agregador | xxx
![Composed Message Processor](https://docs.wso2.com/download/attachments/12421407/DistributionAggregate.png?version=1&modificationDate=1345665573000&api=v2) | Processador de Mensagens Compostas | xxx
*| Espalha - Recorre | xxx
![Routing Slip](https://docs.wso2.com/download/attachments/12421407/RoutingTable.png?version=1&modificationDate=1345665694000&api=v2) | Lista de Circulação | xxx
![Process Manager](https://docs.wso2.com/download/attachments/12421407/ProcessManager.png?version=1&modificationDate=1345665819000&api=v2) | Gerente de Processos | xxx
![Message Broker](https://docs.wso2.com/download/attachments/12421407/MessageBroker.png?version=1&modificationDate=1345665873000&api=v2) | Corretor de Mensagens | xxx
![Resequencer](https://docs.wso2.com/download/attachments/12421407/Resequencer.png?version=2&modificationDate=1511414659000&api=v2) | Ressequenciador | xxx

5. **Transformação**

Ícone | Nome | Descrição
:---: |  :---: |  :---:
![Envelope Wrapper](https://docs.wso2.com/download/attachments/12421407/EnvelopeWrapper.png?version=1&modificationDate=1345698155000&api=v2) | Envelope | xxx
![Content Enricher](https://docs.wso2.com/download/attachments/12421407/DataEnricher.png?version=1&modificationDate=1345698221000&api=v2) | Enriquecedor de Conteúdo | xxx
![Content Filter](https://docs.wso2.com/download/attachments/12421407/ContentFilter.png?version=1&modificationDate=1345698275000&api=v2) | Filtro de Conteúdo | xxx
![Claim Check](https://docs.wso2.com/download/attachments/12421407/StoreInLibrary.png?version=1&modificationDate=1345698324000&api=v2) |  Recibo de Bagagem | xxx
![Normalizer](https://docs.wso2.com/download/attachments/12421407/Normalizer.png?version=1&modificationDate=1345698367000&api=v2) | Normalizador | xxx
*| Modelos de Dados Canônicos | xxx

6. **Endpoint**

Ícone | Nome | Descrição
:---: |  :---: |  :---:
![Messaging Gateway](https://docs.wso2.com/download/attachments/12421407/MessagingGateway.png?version=1&modificationDate=1345698470000&api=v2) | Gateway de Mensageria | xxx
*| Mapeador de Mensageria | xxx
![Transactional Client](https://docs.wso2.com/download/attachments/12421407/TransactionalClient.png?version=1&modificationDate=1345698517000&api=v2) | Cliente Transacional | xxx
![Polling Consumer](https://docs.wso2.com/download/attachments/12421407/PollingConsumer.png?version=1&modificationDate=1345698618000&api=v2) | Consumidor de Sondagem | xxx
![Event-Driven Consumer](https://docs.wso2.com/download/attachments/12421407/EventDrivenConsumer.png?version=1&modificationDate=1345698666000&api=v2) | Consumidor ativado por Eventos | xxx
![Competing Consumers](https://docs.wso2.com/download/attachments/12421407/CompetingConsumers.png?version=1&modificationDate=1345698717000&api=v2) | Consumidores Concorrentes | xxx
![Message Dispatcher](https://docs.wso2.com/download/attachments/12421407/MessageDispatcher.png?version=1&modificationDate=1345698765000&api=v2) | Despachante de Mensagens | xxx
![Selective Consumer](https://docs.wso2.com/download/attachments/12421407/MessageSelector.png?version=1&modificationDate=1345698808000&api=v2) | Consumidor Seletivo | xxx
![Durable Subscriber](https://docs.wso2.com/download/attachments/12421407/DurableSubscription.png?version=1&modificationDate=1345698853000&api=v2) | Assinante Durável | xxx
*| Receptor Idempotente | xxx
![Service Activator](https://docs.wso2.com/download/attachments/12421407/MessagingAdapter.png?version=1&modificationDate=1345698920000&api=v2) | Ativador de Serviço | xxx

7. **Gerenciamento**

Ícone | Nome | Descrição
:---: |  :---: |  :---:
![Channel Purger](https://docs.wso2.com/download/thumbnails/12421407/ChannelPurgerIcon.gif?version=1&modificationDate=1364846389000&api=v2) | Purificador de Canal | xxx
![Control Bus](https://docs.wso2.com/download/attachments/12421407/ControlBusIcon.gif?version=2&modificationDate=1364846435000&api=v2) | Barramento de Controle | xxx
![Detour](https://docs.wso2.com/download/thumbnails/12421407/DetourIcon.gif?version=1&modificationDate=1364846502000&api=v2) | Desvio | xxx
*| Histórico da Mensagem | xxx
![Message Store](https://docs.wso2.com/download/thumbnails/12421407/MessageStoreIcon.gif?version=1&modificationDate=1364846556000&api=v2) | Repositório de Mensagens | xxx
![Smart Proxy](https://docs.wso2.com/download/thumbnails/12421407/SmartProxyIcon.gif?version=1&modificationDate=1364846586000&api=v2) | Proxy Inteligente | xxx
![Test Message](https://docs.wso2.com/download/thumbnails/12421407/TestMessageIcon.gif?version=1&modificationDate=1364846619000&api=v2) | Mensagem de Teste | xxx
![Wire Tap](https://docs.wso2.com/download/thumbnails/12421407/WireTapIcon.gif?version=1&modificationDate=1364846659000&api=v2) | Escuta | xxx
