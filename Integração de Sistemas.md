# Introdução à Integração de Sistemas
***
- [Introdução à Integração de Sistemas](#introdução-à-integração-de-sistemas)
  - [1. O que é?](#1-o-que-é)
  - [2. Tipos de Integração de Sistemas](#2-tipos-de-integração-de-sistemas)
    - [2.1  Integração via transferência de arquivos - (*File Transfer*)](#21--integração-via-transferência-de-arquivos---file-transfer)
    - [2.2 Integração via banco de dados compartilhados - (*Shared Database*)](#22-integração-via-banco-de-dados-compartilhados---shared-database)
    - [2.3 Integração por meio de Chamada de Procedimento Remoto - (*Remote Procedure Call*)](#23-integração-por-meio-de-chamada-de-procedimento-remoto---remote-procedure-call)
    - [2.4 Mensageria - (*Messaging*)](#24-mensageria---messaging)
  - [3. Catálogo de Padrões de Integração de Sistemas - EIP (*Enterprise Integration Patterns*)](#3-catálogo-de-padrões-de-integração-de-sistemas---eip-enterprise-integration-patterns)
    - [3.1 Mensagem](#31-mensagem)
    - [3.2. Canais](#32-canais)
    - [3.3. Mensageria](#33-mensageria)
    - [3.4. Roteamento](#34-roteamento)
    - [3.5. Transformação](#35-transformação)
    - [3.6. Endpoint](#36-endpoint)
    - [3.7. Gerenciamento](#37-gerenciamento)
  - [4. Event-Driven Architecture (EDA)](#4-event-driven-architecture-eda)
  - [5. Componentes Comuns de EDA](#5-componentes-comuns-de-eda)
    - [5.1. Business Process Server (BPS)](#51-business-process-server-bps)
    - [5.2. Complex Event Processor (CEP)](#52-complex-event-processor-cep)
    - [5.3. Enterprise Service Bus (ESB)](#53-enterprise-service-bus-esb)
    - [5.4. Business Activity Monitor (BAM)](#54-business-activity-monitor-bam)
    - [5.5. Data Service Server (DSS)](#55-data-service-server-dss)
    - [5.6. Authentication, Authorization Server (IM)](#56-authentication-authorization-server-im)
    - [5.7. Governance Registry (G-Reg)](#57-governance-registry-g-reg)
    - [5.8. Rules Engine](#58-rules-engine)
    - [5.9. Message Broker (MB)](#59-message-broker-mb)
  - [6. Camada de Mensageria](#6-camada-de-mensageria)
  - [7. Arquitetura Orientada a Serviço (SOA)](#7-arquitetura-orientada-a-serviço-soa)
  - [8. Simple Object Access Protocol (SOAP)](#8-simple-object-access-protocol-soap)
    - [8.1. Segurança de serviços web (WS-Security)](#81-segurança-de-serviços-web-ws-security)
    - [8.2. WS-ReliableMessaging](#82-ws-reliablemessaging)
    - [8.3. Endereçamento de serviços web (WS-Adressing)](#83-endereçamento-de-serviços-web-ws-adressing)
    - [8.4. Linguagem de descrição de serviços web (WSDL)](#84-linguagem-de-descrição-de-serviços-web-wsdl)
  - [9. SoapUI](#9-soapui)
  - [10. O que é uma API?](#10-o-que-é-uma-api)
    - [10.1. Como APIs funcionam?](#101-como-apis-funcionam)
      - [10.1.1 APIs SOAP](#1011-apis-soap)
      - [10.1.2 APIs RPC](#1012-apis-rpc)
      - [10.1.3 APIs WebSocket](#1013-apis-websocket)
      - [10.1.4. APIs REST](#1014-apis-rest)
    - [10.2. Diferentes tipos de APIs](#102-diferentes-tipos-de-apis)
      - [10.2.1. APIs privadas](#1021-apis-privadas)
      - [10.2.2. APIs públicas](#1022-apis-públicas)
      - [10.2.3. APIs de parceiros](#1023-apis-de-parceiros)
      - [10.2.4. APIs compostas](#1024-apis-compostas)
  - [11. O que é Swagger?](#11-o-que-é-swagger)
    - [11.1. Como funciona?](#111-como-funciona)
  - [12. Microsserviços](#12-microsserviços)
    - [12.1. Características dos microsserviços](#121-características-dos-microsserviços)
    - [12.2. Benefícios dos microsserviços](#122-benefícios-dos-microsserviços)
  - [13. Protocolo HTTP](#13-protocolo-http)
    - [13.1. Status HTTP](#131-status-http)
  - [14. Protocolo REST](#14-protocolo-rest)
    - [14.1. Client-Server](#141-client-server)
    - [14.2. Stateless](#142-stateless)
    - [14.3. Cacheable](#143-cacheable)
    - [14.4. Uniform interface](#144-uniform-interface)
    - [14.5. Layered system](#145-layered-system)
  - [15. cUrl](#15-curl)
  - [16. Postman](#16-postman)
    - [16.1. Benefícios](#161-benefícios)
    - [16.2. Funcionamento](#162-funcionamento)
    - [16.2. Requisição GET](#162-requisição-get)
    - [16.3. Requisição POST](#163-requisição-post)
    - [16.4. Parâmetros de dados](#164-parâmetros-de-dados)
    - [16.5. Postman Tests](#165-postman-tests)
  - [17. Containers](#17-containers)
  - [18. Docker](#18-docker)
  - [19. Docker Compose](#19-docker-compose)
  - [20. Continuous Integration (CI)](#20-continuous-integration-ci)
  - [21. Continuous Delivery (CD)](#21-continuous-delivery-cd)
- [REFERÊNCIAS](#referências)
 
## 1. O que é?

![api integration](https://user-images.githubusercontent.com/110742899/187648087-95dcb3c6-620e-4b84-97c3-5bfff14a6775.svg)

   A **Integração de Sistemas** é uma solução tecnológica para automatizar uma série de procedimentos operacionais proporcionando ganho de produtividade com a otimização do fluxo de trabalho.

   Diversas empresas possuem diferentes sistemas de gestão, cada um com seu conjunto de dados. Por exemplo, um sistema contábil, outro de gestão financeira e até mesmo de estoque. A ausência da integração reflete na forma precária em que os conjuntos de dados se comunicam. Os processos funcionam de maneira mais harmoniosa, sem intervalos ociosos ou lacunas, quando há uma compactação dos sistemas utilizados aperfeiçoando a ligação entre os processos.

   Através do compartilhamento de dados há aumento e melhora da produtividade, diminuição dos erros amparados por sistemas automatizados e integrados, redução de custos eliminando informações conflitantes ou duplicadas, otimização dos processos e, por consequência, a ampliação do diferencial competitivo no mercado.

   Uma integração bem alinhada ocorre mediante o mapeamento visando identificar as falhas inerentes de cada processo mantido pela empresa, dessa forma providenciando os ajustes para a melhoria do fluxo operacional com a preparação da equipe de colaboradores para a adoção do modelo de integração em contínuo controle na avaliação de resultados.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
***

## 2. Tipos de Integração de Sistemas
 ### 2.1  Integração via transferência de arquivos - (*File Transfer*)

   Consiste em exportar os dados para um arquivo, gravar o arquivo, transferir o arquivo para outro lugar onde a segunda aplicação pode ler o arquivo e importar seus dados.

  ### 2.2 Integração via banco de dados compartilhados - (*Shared Database*)

   Integra aplicações fazendo com que guardem seus dados em um único Banco de Dados Compartilhado (Shared Database), assim definindo o esquema do banco de dados para lidar com todas as necessidades das diferentes aplicações.

  ### 2.3 Integração por meio de Chamada de Procedimento Remoto - (*Remote Procedure Call*)

   Desenvolvendo cada aplicação como um objeto de larga escala ou componente com dados encapsulados, fornece uma interface para permitir que outras aplicações interajam com a aplicação que está sendo executada.

   ### 2.4 Mensageria - (*Messaging*)
   
   O serviço de mensageria é proporcionado por um servidor que coordena a mediação da comunicação por mensagens. Esse servidor é às vezes chamado de Message Queue (MQ) ou Message-Oriented
   Middleware, ou MOM. Um MOM fornece a infraestrutura básica para a mensageria (conexões e canais), e age como mediador na comunicação entre aplicações.


- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#integração-de-sistemas)
***

## 3. Catálogo de Padrões de Integração de Sistemas - EIP (*Enterprise Integration Patterns*)

  ### 3.1 Mensagem

   Ícone | Nome | Descrição
   :---: |  :---: |  :---:    
   ![Command Message](https://docs.wso2.com/download/attachments/12421407/CommandMessage.png?version=1&modificationDate=1345664065000&api=v2) | Command Message | Chama um procedimento em outra aplicação de forma confiável.
   ![Document Message](https://docs.wso2.com/download/attachments/12421407/DocumentMessage.png?version=1&modificationDate=1345664107000&api=v2) | Document Message | Transfere uma estrutura de dados entre aplicações de forma confiável.
   ![Event Message](https://docs.wso2.com/download/attachments/12421407/EventMessage.png?version=1&modificationDate=1345664142000&api=v2) | Event Message | Usado para notificar ou transferir eventos de forma assíncrona e confiável entre aplicações.
   ![Request-Reply](https://docs.wso2.com/download/attachments/12421407/RequestReply.png?version=1&modificationDate=1345664354000&api=v2) | Request-Reply | Envia um par de mensagens Request-Reply, cada uma no seu próprio canal.
   ![Return Address](https://docs.wso2.com/download/attachments/12421407/ReturnAddress.png?version=1&modificationDate=1345664376000&api=v2) | Return Address | A mensagem de requisição deve contar com um Endereço de Resposta que indica para onde a resposta deve ser enviada.
   ![Correlation Identifier](https://docs.wso2.com/download/attachments/12421407/CorrelationIdentifier.png?version=1&modificationDate=1345664396000&api=v2) | Correlation Identifier | Cada mensagem de resposta deve conter um Identificador de Correlação - um identificador unívoco que indica para qual mensagem de requisição corresponde esta resposta
   ![Message Sequence](https://docs.wso2.com/download/attachments/12421407/MessageSequence.png?version=1&modificationDate=1345664431000&api=v2) | Message Sequence | Sempre que um grande conjunto de dados precisar ser partido em pedaços do tamanho das mensagens disponíveis, envie os dados como uma Message Sequence e marque cada mensagem com campos de identificação da sequência.
   ![Message Expiration](https://docs.wso2.com/download/attachments/12421407/MessageExpiration.png?version=1&modificationDate=1345664478000&api=v2) | Message Expiration | Indica quando uma mensagem deve ser considerada obsoleta, não devendo mais ser processada.
   *| Format Indicator | Indica qual o formato de dados a mensagem está usando, permitindo mudanças futuras.

   ### 3.2. Canais
   
   Ícone | Nome | Descrição
   :---: |  :---: |  :---:
   ![Point-to-Point Channel](https://docs.wso2.com/download/attachments/12421407/PointToPoint.png?version=1&modificationDate=1345663460000&api=v2) | Point-to-Point Channel | Garante que apenas um destinatário irá receber a mensagem.
   ![Publish-Subscribe Channel](https://docs.wso2.com/download/attachments/12421407/PublishSubscribe.png?version=1&modificationDate=1345663504000&api=v2) | Publish-Subscribe Channel | Entrega uma cópia do evento a cada destinatário.
   ![Datatype Channel](https://docs.wso2.com/download/attachments/12421407/DatatypeChanne.png?version=1&modificationDate=1345663551000&api=v2) | Datatype Channel | Simplifica a aplicação ao agrupar mensagens de mesmo tipo em um único canal.
   ![Invalid Message Channel](https://docs.wso2.com/download/attachments/12421407/InvalidMessageChannel.png?version=1&modificationDate=1345663659000&api=v2) | Invalid Message Channel | Um canal especial para mensagens que não puderam ser processadas por seus receptores.
   ![Dead Letter Channel](https://docs.wso2.com/download/attachments/12421407/DeadLetterChannel.png?version=1&modificationDate=1345663711000&api=v2) | Dead Letter Channel | Quando o sistema determina que não pode ou não deve entregar uma mensagem, poderá decidir mover a mensagem para um Canal de Mensagens Não-Entregadas.
   ![Guaranteed Delivery](https://docs.wso2.com/download/attachments/12421407/GuaranteedMessaging.png?version=1&modificationDate=1345663759000&api=v2) | Guaranteed Delivery | Garante a entrega de uma mensagem, mesmo que o sistema de mensageria falhe ou esteja fora de ar.
   ![Channel Adapter](https://docs.wso2.com/download/attachments/12421407/ChannelAdapter.png?version=1&modificationDate=1345663817000&api=v2) | Channel Adapter | Conecta uma aplicação ao sistema de mensageria para que ela possa enviar e receber mensagens.
   ![Messaging Bridge](https://docs.wso2.com/download/attachments/12421407/MessagingBridge.png?version=1&modificationDate=1345663925000&api=v2) | Messaging Bridge | Utilizado para realizar a integração entre dois sistemas de mensageria de fabricantes diferentes.
   ![Message Bus](https://docs.wso2.com/download/attachments/12421407/MessageBus.png?version=1&modificationDate=1345663937000&api=v2) | Message Bus | Permite que aplicações se conectem usando mensageria, um formato comum de comandos e dados, permitindo que compartilhem recursos e serviços disponibilizados no barramento.

   ### 3.3. Mensageria

   Ícone | Nome | Descrição
   :---: |  :---: |  :---:
   ![Message Channels](https://docs.wso2.com/download/attachments/12421407/Channels.png?version=1&modificationDate=1345659503000&api=v2) | Message Channels | Conecta as aplicações usando um Canal de Mensagens, onde uma aplicação grava informação no canal e a outra lê informação do canal.
   ![Message](https://docs.wso2.com/download/attachments/12421407/Message.png?version=1&modificationDate=1345659518000&api=v2) | Message | Empacota a informação dentro de um registro de dados que o sistema de mensageria pode transmitir através de um canal de mensagens.
   ![Pipes and Filters](https://docs.wso2.com/download/attachments/12421407/PipesAndFiltersIcon.gif?version=1&modificationDate=1345659576000&api=v2) | Pipes and Filters | Divide uma tarefa de processamento maior em uma sequência de passos menores e independentes que são conectados por canais.
   ![Message Router](https://docs.wso2.com/download/attachments/12421407/ContentBasedRouterIcon.gif?version=1&modificationDate=1345660358000&api=v2) | Message Router | Desacopla passos individuais de processamento de forma que mensagens possam ser passadas para diferentes filtros dependendo de uma série de condições.
   ![Message Translator](https://docs.wso2.com/download/attachments/12421407/MessageTranslatorIcon.gif?version=1&modificationDate=1345660483000&api=v2) | Message Translator | Usado como filtro especial para traduzir de um formato de dados para outro.
   ![Message Endpoint](https://docs.wso2.com/download/attachments/12421407/MessageEndpoint.png?version=1&modificationDate=1345660568000&api=v2) | Message Endpoint | Conecta uma aplicação a um canal de mensageria através de um cliente do sistema de mensageria que a aplicação pode usar para enviar ou receber mensagens.

   ### 3.4. Roteamento

   Ícone | Nome | Descrição
   :---: |  :---: |  :---:
   ![Content-Based Router](https://docs.wso2.com/download/attachments/12421407/ContentBasedRouter.png?version=1&modificationDate=1345665188000&api=v2) | Content-Based Router | Usado para rotear cada mensagem para o receptor correto baseado no conteúdo da mensagem.
   ![Message Filter](https://docs.wso2.com/download/attachments/12421407/MessageFilter.png?version=1&modificationDate=1345665231000&api=v2) | Message Filter | Elimina mensagens indesejadas de um canal com base em um conjunto de critérios.
   ![Dynamic Router](https://docs.wso2.com/download/attachments/12421407/DynamicRouter.png?version=1&modificationDate=1345665267000&api=v2) | Dynamic Router | É capaz de se autoconfigurar com base em mensagens de configuração enviadas pelos destinos participantes.
   ![Recipient List](https://docs.wso2.com/download/attachments/12421407/RecipientList.png?version=1&modificationDate=1345665338000&api=v2) | Recipient List | Rotea uma mensagem para uma lista de receptores especificados dinamicamente.
   ![Splitter](https://docs.wso2.com/download/attachments/12421407/Splitter.png?version=1&modificationDate=1345665389000&api=v2) | Splitter | Usado para partir a mensagem composta em uma série de mensagens individuais, cada uma contendo dados relacionados a um item.
   ![Aggregator](https://docs.wso2.com/download/attachments/12421407/Aggregator.png?version=1&modificationDate=1345665422000&api=v2) | Aggregator | Combina os resultados de mensagens individuais, mas relacionadas, para que possam ser processadas como uma só.
   ![Composed Message Processor](https://docs.wso2.com/download/attachments/12421407/DistributionAggregate.png?version=1&modificationDate=1345665573000&api=v2) | Composed Message Processor | Processa uma mensagem composta dividindo a mensagem e redirecionando as submensagens para os destinos apropriados, reagregando as respostas de volta em uma única mensagem.
   *| Scatter-Gather | Difunde uma mensagem para múltiplos receptores e reagrega as respostas de volta em uma única mensagem.
   ![Routing Slip](https://docs.wso2.com/download/attachments/12421407/RoutingTable.png?version=1&modificationDate=1345665694000&api=v2) | Routing Slip | Rotea uma mensagem consecutivamente através de uma série de etapas de processamento, quando a sequência de passos não é conhecida em tempo de design, e pode variar para cada mensagem.
   ![Process Manager](https://docs.wso2.com/download/attachments/12421407/ProcessManager.png?version=1&modificationDate=1345665819000&api=v2) | Process Manager | Usando uma unidade central de processamento para manter o estado da sequência e determinar o próximo passo de processamento com base em resultados intermediários.
   ![Message Broker](https://docs.wso2.com/download/attachments/12421407/MessageBroker.png?version=1&modificationDate=1345665873000&api=v2) | Message Broker | Desacopla o destino de uma mensagem do seu remetente e mantem um controle central sobre o fluxo das mensagens.
   ![Resequencer](https://docs.wso2.com/download/attachments/12421407/Resequencer.png?version=2&modificationDate=1511414659000&api=v2) | Resequencer | Coleta e reordena mensagens para que elas possam ser publicadas no canal de saída em uma ordem especificada.
  
   ### 3.5. Transformação

   Ícone | Nome | Descrição
   :---: |  :---: |  :---:
   ![Envelope Wrapper](https://docs.wso2.com/download/attachments/12421407/EnvelopeWrapper.png?version=1&modificationDate=1345698155000&api=v2) | Envelope Wrapper | Embrulha os dados da aplicação dentro de um envelope que seja compatível com a infraestrutura de mensageria usada desembrulhando quando a mensagem chega no seu destino.
   ![Content Enricher](https://docs.wso2.com/download/attachments/12421407/DataEnricher.png?version=1&modificationDate=1345698221000&api=v2) | Content Enricher | Acessa uma fonte de dados externa de maneira a adicionar à mensagem informação que lhe falta.
   ![Content Filter](https://docs.wso2.com/download/attachments/12421407/ContentFilter.png?version=1&modificationDate=1345698275000&api=v2) | Content Filter | Remove partes de uma mensagem que não são necessárias, deixando apenas os itens importantes.
   ![Claim Check](https://docs.wso2.com/download/attachments/12421407/StoreInLibrary.png?version=1&modificationDate=1345698324000&api=v2) |  Claim Check | Reduz o volume de dados de uma mensagem enviada através do sistema sem sacrificar o conteúdo da informação.
   ![Normalizer](https://docs.wso2.com/download/attachments/12421407/Normalizer.png?version=1&modificationDate=1345698367000&api=v2) | Normalizer | Processa mensagens que são semanticamente equivalentes mas que chegam em um formato diferente.
   *| Canonical Data Model | Minimiza dependências ao integrar aplicações que usam diferentes formatos de dados aplicando um formato em comum.
  
   ### 3.6. Endpoint

   Ícone | Nome | Descrição
   :---: |  :---: |  :---:
   ![Messaging Gateway](https://docs.wso2.com/download/attachments/12421407/MessagingGateway.png?version=1&modificationDate=1345698470000&api=v2) | Messaging Gateway | Encapsula chamadas específicas ao sistema de mensageria e expõe uma interface com métodos específicos ao domínio da aplicação.
   *| Messaging Mapper | Pode ser usado para incluir serviços de mensageria em uma aplicação sem alterar a sua lógica de negócios.
   ![Transactional Client](https://docs.wso2.com/download/attachments/12421407/TransactionalClient.png?version=1&modificationDate=1345698517000&api=v2) | Transactional Client | Faz com que a sessão do cliente com o sistema de mensageria seja transacional, para que o cliente possa especificar onde começa e onde termina uma transação.
   ![Polling Consumer](https://docs.wso2.com/download/attachments/12421407/PollingConsumer.png?version=1&modificationDate=1345698618000&api=v2) | Polling Consumer | Faz uma chamada explícita quando deseja receber uma mensagem.
   ![Event-Driven Consumer](https://docs.wso2.com/download/attachments/12421407/EventDrivenConsumer.png?version=1&modificationDate=1345698666000&api=v2) | Event-Driven Consumer | Ideal quando a produção de mensagens é irregular ou pouco frequente e as mensagens devem ser consumidas assim que forem entregues.
   ![Competing Consumers](https://docs.wso2.com/download/attachments/12421407/CompetingConsumers.png?version=1&modificationDate=1345698717000&api=v2) | Competing Consumers | Implementa uma solução escalável distribuindo o trabalho de consumir mensagens de uma fila por vários consumidores operando em paralelo.
   ![Message Dispatcher](https://docs.wso2.com/download/attachments/12421407/MessageDispatcher.png?version=1&modificationDate=1345698765000&api=v2) | Message Dispatcher | Permite distribuir o consumo de mensagens a vários componentes que irão processá-las em paralelo, controlando qual componente irá receber cada mensagem recebida. 
   ![Selective Consumer](https://docs.wso2.com/download/attachments/12421407/MessageSelector.png?version=1&modificationDate=1345698808000&api=v2) | Selective Consumer | Deve ser usado quando for necessário selecionar, dentre as mensagens recebidas, as que aderem a determinado critério baseado em suas propriedades, e descartar as demais.
   ![Durable Subscriber](https://docs.wso2.com/download/attachments/12421407/DurableSubscription.png?version=1&modificationDate=1345698853000&api=v2) | Durable Subscriber | Faz com que o sistema de mensageria guarde mensagens publicadas quando o assinante estiver desconectado.
   *| Idempotent Receiver | Lida com os efeitos colaterais da duplicação de mensagens.
   ![Service Activator](https://docs.wso2.com/download/attachments/12421407/MessagingAdapter.png?version=1&modificationDate=1345698920000&api=v2) | Service Activator | Permite que um serviço síncrono possa ser utilizado de forma assíncrona em um sistema de mensageria.

   ### 3.7. Gerenciamento

   Ícone | Nome | Descrição
   :---: |  :---: |  :---:
   ![Channel Purger](https://docs.wso2.com/download/thumbnails/12421407/ChannelPurgerIcon.gif?version=1&modificationDate=1364846389000&api=v2) | Channel Purger | Remove mensagens indesejadas de um canal.
   ![Control Bus](https://docs.wso2.com/download/attachments/12421407/ControlBusIcon.gif?version=2&modificationDate=1364846435000&api=v2) | Control Bus | Emprega canais separados para transmitir dados que são relevantes para o gerenciamento de componentes envolvidos no fluxo de mensagens.
   ![Detour](https://docs.wso2.com/download/thumbnails/12421407/DetourIcon.gif?version=1&modificationDate=1364846502000&api=v2) | Detour | Deve ser usado quando for necessário ter um caminho alternativo para testar mensagens em desenvolvimento, sem afetar a performance da aplicação em ambiente de produção.
   *| Message History | É uma lista de todas as aplicações pelas quais a mensagem passou desde que foi criada.
   ![Message Store](https://docs.wso2.com/download/thumbnails/12421407/MessageStoreIcon.gif?version=1&modificationDate=1364846556000&api=v2) | Message Store | Captura informação sobre cada mensagem em um ponto central.
   ![Smart Proxy](https://docs.wso2.com/download/thumbnails/12421407/SmartProxyIcon.gif?version=1&modificationDate=1364846586000&api=v2) | Smart Proxy | É usado para rastrear as mensagens de resposta.
   ![Test Message](https://docs.wso2.com/download/thumbnails/12421407/TestMessageIcon.gif?version=1&modificationDate=1364846619000&api=v2) | Test Message | Assegura a saúde dos compomentes de processamento de mensagens.
   ![Wire Tap](https://docs.wso2.com/download/thumbnails/12421407/WireTapIcon.gif?version=1&modificationDate=1364846659000&api=v2) | Wire Tap | Pode ser implantada para monitorar todas as mensagens que passam por um canal, sem interferir no fluxo normal da aplicação.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#arquitetura-de-microsserviços-dirigos-a-api)
***

## 4. Event-Driven Architecture (EDA)

![eda](https://user-images.githubusercontent.com/110742899/187648589-246f2519-cd88-42ed-9d87-f1807fce378d.png)

Praticamente todas as aplicações ou serviços atuais assumem que você pode fazer o que quiser imediatament recebendo retorno instantâneo sobre o status de sua requisição e interagindo em tempo real com a requisição ou qualquer um envolvido no processo. Seja lá se seu pedido for um produto ou uma viagem por aplicativo, manufatura, processo financeiro, chat ou mensageiro, hoje em dia tudo é orientado a eventos. 

A arquitetura orientada a Eventos (EDA) é fundamental para a resolução de problemas complexos, sendo acessível para todos os negócios sem a necessidade de programadores reinventando as mesmas soluções para os mesmos problemas. Suas ferramentas foram criadas para lidar com larga capacidade, segurança, robustez e resiliência a falha. 

Às vezes podendo ser chamada por sistema de mensageria posto que uma mensagem é simplesmente um evento ou inversamente um evento se torna uma mensagem. O conceito de um sistema orientado é tornar possível ser notificado de tais eventos os quais se beneficiaria em saber sobre. Por isso os primeiros sistemas orientados a eventos surgiram com a noção de publish/subscribe.

**Publish/subscribe** é uma outra forma de descrever mensageria orientada a eventos. As características em comum entre os sistemas publish/subscribe são:

- **Anonimato**: um publisher não precisa saber tudo sobre os subscribers da informação a quem está enviando a não ser que são intitulados a receber a informação. De forma similar, o subscriber não precisa saber tudo sobre o publisher a não ser que estão autenticados como legítimos publishers.
- **As mensagens são idênticas a todos os subscribers**: o potencial do sustema de publish/subscribe vem parcialmente do fato de cada subscriber receber a mesma mensagem. Se uma mensagem precisa ser customizada para cada subscriber, levaria a uma pesada carga para o publisher e iria requerer mudanças quando novos subscribers surgissem.
- **Descoberta**: um sistema de publish/subscribe deve suportar um mecanismo para que publishers encontrem novos subscribers e subscribers possam ser capazes de encontrar os publishers da informação imediatamente após a disponibilidade.
- **Payloads auto-descritíveis** (JSON ou XML).
- **Entrega garantida**: como um subscriber, você necessita saber que é garantido, se desejado, o recebimento de todas as mesangens dos publishers na sequência que elas ocorreram.
- **Baixa latência/simultaneidade**: todos subscribers devem ser notificados dos eventos tão logo seja possível.
- **Assunto**: você deve ser capaz de se subescrever e filtrar a informação baseado na descrição mnemônica do conteúdo desejado (queue ou topics).
  
Após certo tempo, foram descobertos certos padrões de comportamento necessários para diversas aplicações em uma empresa. Isso veio a ser conhecido como **Padrões de Integração de Sistemas** (EIPs) e todos sistemas baseados em mensageria começaram a incorporar tecnologias de mediação para padronizar esses EIPs.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
***

## 5. Componentes Comuns de EDA
![Componentes Comuns de EDA](https://b.content.wso2.com/sites/all/white-paper-landing/images/event-driven-architecture-figure-1.png)

  ### 5.1. Business Process Server (BPS)
  
  O componente de BPS provê um editor gráfico para desenvolvimento e teste de processos empresariais que incita um evento. Isso permite que pessoas não-programadoras desenvolvam processos empresarias e as implementem, permitindo alterações e rastreamentos mais rápidos. Outra funcionalidade é a de retorno a estados anteriores e mudanças operacionais enquanto transações estão em meio a um processo. O servidor BPS é capaz de lidar com milhares ou até mesmo milhões de processos de longa duração pendentes simultaneamente.
  
  ### 5.2. Complex Event Processor (CEP)

  Esse componente permite o reconhecimento de mensagens que podem sinalizar um evento interessante. Por exemplo, um certo tipo de sequência pode representar uma ameaçã a segurança, outro pode representar uma oportunidade de venda. A sequência de mensagens devem ocorrer dentro de um período de tempo específico. Isso permite acrescentar engenhosidade dentro de um sistema baseado no comportamento adotado nele.
  
  ### 5.3. Enterprise Service Bus (ESB)
  
  Proporciona a especifícação de EIPs bem conhecidas. Isso inclui o envio de mensagens para múltiplos receptores, acrescentamento de informações adicionais de outros serviços a uma mensagem e detectação de condições excepcionais que requerem um processamento diferente. Um ESB deve estar apto a lidar com eventos de dados de fontes diversas incluindo banco de dados, diretórios do sistema e protocolos de comunicação de legado, ou seja, ESB é um componente crítico na integração.

  ### 5.4. Business Activity Monitor (BAM)

  Desenvolvido para lidar com alto fluxo de mensagens oriundas de diferentes fontes incluindo arquivos de log ou fontes que possam ser não orientadas a mensagens. O servidor BAM pode computar operações chave ou métricas operacionais baseadas em todos os fluxos de mensagem. É também capaz de computar os critérios de **Service Level Agreement** (SLA), médias e totais, podendo também gerar eventos baseados em valores que essas métricas alcançam. Essa funcionalidade pode ser usada para o propósito de operações ou para métricas empresariais. Geralmente os fluxos são afunilados em um armazenamento de big data para futuro processamento ou análise.

  ### 5.5. Data Service Server (DSS)

  Utilizado para criar serviços acerca de banco de dados ou outros persistente (data at rest) mecanismo de armazenamento de datos como bancos de dados no-SQL ou até mesmo diversos tipos de arquivos de sistemas. Em uma arquitetura de múltiplas camadas, aplicações não conversam diretamente com as tabelas de bancos de dados. Na verdade, é definida um alto nível de abstração da tabela ou tabelas que tenham direta relevância ao empreendimento. DSS pode ofertar isolamento das mudanças na fonte de dados ou a arquitetura dos mecanimos de armazenamento de dados subjacentes.

  ### 5.6. Authentication, Authorization Server (IM)
  
  Fornece a habilidade de padronizar e tornar eficiente a manutenção da autenticação de protocolos e processos, como também a provisão de **entitlement services** bem detalhados. Isso permite a definição e implemento de políticas de segurança empresarial. Na arquitetura moderna, IM exerce uma função crítica como gatekeeper e apontador de aplicação de política, devendo ser altamente escalável.

  ### 5.7. Governance Registry (G-Reg)

  Em qualquer empreendimento ou arquitetura, há informações sobre a configuração do sistema que não são codificadas dentro do próprio sistema, mas são proporcionadas após a inicialização da aplicação. As informações referidas podem ser endereços físicos de IP de serviços que podem mudar com o tempo, parâmetros de operação e até mesmo regras de negócios para a companhia. Outros usos podem incluir a criptação de certificados.

  Em um cenário de recuperação após desastre, o G-Reg deve ser replicado. Diversas companhias com filiais espalhadas pelo mundo precisarão de múltiplas cópias de G-Reg. Ele é simplesmente uma forma de banco de dados que possui informações específicas que aplicações utilizam ao inicializar ou em operação.

  ### 5.8. Rules Engine

  É uma ferramenta que pode processar conjuntos de hierarquia de regras sobrepostas para computar a resposta correta em uma questão operacional. É especialmente útil para especificar esquemas complexos de atribuição de preço ou complexas regras de escalonamento **PaaS**, e decisões de intitulamento que são baseadas em complexas situações de critério onde o contexto pode diferir das escolhas previamente feitas.

  Ela necessita de uma interface de usuário simples e intuitiva para que possam ser construídas as regras de forma transparente antes delas serem implementadas para que a combinação de regras não produza resultados inesperados.

  ### 5.9. Message Broker (MB)
![Message Broker](https://b.content.wso2.com/sites/all/white-paper-landing/images/event-driven-architecture-figure-2.png)

  É um componente que provê comunicação pub/sub e semânticas transacionais. A maioria dos componentes descrita não precisa suportar verdadeiras semânticas transacionais graças ao uso de MB que oferta essa funcionalidade. Em uma arquitetura comum, mensagens julgadas críticas para o negócio são enviadas para um MB que armazena as mensagens e as distribui para os emissários de maneira garantida e confiável. Se um componente falha antes do processamento da mensagem, o MB vai recolocá-la na fila após o componente ser reinicializado ou passá-la para outro servidor similar que possa lidar com ela.

  MB lida com dois paradigmas de fluxo de mensagem: **topics** e **queues**. Topics devem ser entregues a vários subscribers quando expressam interesse em uma corrente de tópico, então é enviada uma corrente independente de mensagens in uma ordem apropriada. Queues são enviadas apenas para um de um número de determinadores que pode processar a transação. Uma mensagem não pode ser despachada até todos os subscribers em um protocolo baseado em tópico tenham recebido a mensagem. Ela também não pode ser despachada até que um dos determinadores reconheça o processamento da mensagem.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#event-driven-architecture-eda)
***

## 6. Camada de Mensageria

![messaging](https://user-images.githubusercontent.com/110742899/187649934-9206c688-ef9e-4772-9b9f-ff5bd6c8cce3.png)

Camada de mensageria é um médoto de comunicação onde o sistema põe uma mensagem em uma fila de mensagens e não requer uma resposta imediata para um processamento contínuo. 

Isso resolve o problema de conectividade intermitente. O receptor da mensagem não precisa estar online para receber a messagem pois as mensagem está armazenada em uma camada de intermediária. Isso permite que o receptor recupere a mensagem assim que estiver online.

Já os consumidores da mensagem não precisam saber sobre os publicadores da mensagem, de forma que ambos possam operar independentemente.

As vantagens da camada de mensageria incluem:
- Encarrega o request para algum sistema externo para processamento;
- Assegura a entrega da mensagem para um sistema externo;
- Regula a taxa de mensagens entre dois sistemas;
- Rearranja o processamento de mensagens.

Dentro das desvantagens podemos destacar:
- É necessário um componente adicional de **message broker** ou **transfer agent** para assegurar que a mensagem foi recebida, o que pode afetar tanto a performance quanto a confiabilidade.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#camada-de-mensageria)
***

## 7. Arquitetura Orientada a Serviço (SOA)

![soa](https://user-images.githubusercontent.com/110742899/187650494-3d9d0de0-b897-4beb-a08d-d0edae4d9d71.png)

A Arquitetura Orientada a Serviço (SOA) é um tipo de design de software que torna os componentes reutilizáveis usando interfaces de serviços com uma linguagem de comunicação comum em uma rede.

Um serviço é uma unidade ou conjunto de funcionalidades de software independente, que foi desenvolvido para concluir uma tarefa específica. Ele contém as integrações de dados e o código necessários para executar uma função de negócios completa e discreta. Esses serviços podem ser acessados remotamente e é possível interagir e atualizá-los de maneira independente.

Em comparação com as arquiteturas que a precederam, a SOA oferece benefíios significativos tais quais:

- A eficiência de montar aplicativos a partir de interfaces de serviço reutilizáveis, em vez de reescrever e reintegrar a cada novo projeto de desenvolvimento, possibilita que sejam desenvolvidos aplicativos muito mais rapidamente em resposta às novas oportunidades de negócio.

- Quando bem elaborada a SOA possibilita que os desenvolvedores facilmente escalem ou ampliem o uso de uma funcionalidade para plataformas ou ambientes novos.

- Como todos os serviços são autossuficientes e independentes, é possível modificá-los e atualizá-los conforme a necessidade, sem afetar os outros serviços.

- A SOA permite executar serviços usando várias plataformas, linguagens de programação e até mesmo serviços diferentes. ALém disso, a SOA usa um protocolo de comunicação padronizado, o que permite às empresas reduzir a interação entre clientes e serviços, tornando possível escalar aplicações com menos urgência e aborrecimentos.

- Por ser mais fácil fazer o debug de serviços menores do que um grande código, é possível criar aplicações ou a utilizar recursos que estão disponíveis para todos.

Na Arquitetura orientada a serviços (SOA), a comunicação entre os serviços é realizada por um sistema de "baixo acoplamento". Essa é uma maneira de interconectar componentes, também chamados de "elementos", em um sistema ou rede para que transmitam informações ou coordenem processos empresariais e reduzam as dependências entre eles, criando uma nova aplicação.

Pode se dizer que sua base é consituída de três funções:

1. Provedor de serviços:

    Cria serviços web e os oferece para um registro de serviços. Ele é responsável pelos termos de uso desse serviço.

2. Broker ou registro de serviços:

    É responsável por oferecer informações solicitadas sobre o serviço. O broker pode ser público ou privado.

3. Solicitante ou cliente de serviços:

    Encontra um serviço no broker ou no registro de serviços. Então, conecta-se ao provedor de serviços para recebê-lo.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#arquitetura-orientada-a-serviços---soa)
***

## 8. Simple Object Access Protocol (SOAP)

![soap](https://user-images.githubusercontent.com/110742899/187650978-56b8873a-601f-4d91-9fd0-f140fdc035f4.png)

SOAP é um protocolo padrão projetado originalmente para possibilitar a comunicação entre aplicações desenvolvidas em diferentes linguagens e plataformas. Como se trata de um protocolo, ele impõe regras integradas que aumentam sua complexidade e sobrecarga, desacelerando o tempo de carregamento das páginas. No entanto, esses padrões também proporcionam conformidade integrada, fazendo com que SOAP seja uma opção recomendada para casos empresariais.

Quando uma solicitação de dados é enviada a uma API SOAP, ela pode ser processada por meio de qualquer protocolo de camada da aplicação. No entanto, depois que a solicitação é recebida, as mensagens SOAP precisam ser retornadas como documentos **XML**. Um navegador não pode armazenar em cache uma solicitação concluída a uma API SOAP. Por isso, não é possível acessá-la depois sem fazer o reenvio à API. 

As especificações de serviço web comuns são:

### 8.1. Segurança de serviços web (WS-Security)

Padroniza como as mensagens são protegidas e transferidas por meio de identificadores exclusivos chamados de tokens.

### 8.2. WS-ReliableMessaging
  
Padroniza o processamento de erros entre as mensagens transferidas por uma infraestrutura de TI não confiável.

### 8.3. Endereçamento de serviços web (WS-Adressing)

Empacota informações de roteamento como metadados em cabeçalhos SOAP, em vez de armazená-las em camadas mais a fundo na rede.

### 8.4. Linguagem de descrição de serviços web (WSDL)

Descreve a atividade de um serviço web e onde é iniciado e finalizado.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#simple-object-access-protocol)
***

## 9. SoapUI

![soapui](https://user-images.githubusercontent.com/110742899/187651341-013ea80e-1dc6-4c94-bb2e-268b76233989.png)

É uma ferramenta open source escrita em Java cuja principal função é consumir e testar Web Services. 

Web service é uma tecnologia baseada em **XML** e **HTTP** que disponibiliza serviços interativos na WEB que podem ser acessados (ou consumidos) por qualquer outra aplicação indenpendente da linguagem ou plataforma em que a aplicação foi construída. Neste contexto, o SoapUI facilita todo o processo de criação e depuração dos testes por meio de uma interface gráfica visual e intuitiva.

Dentre suas principais características se destacam:

- Importação e geração automática das requisições descritas no **Web Service Description Language (WSDL)**.
- Capacidade de gerenciar um número ilimitado de requisições para cada operação.
- Gerenciamento de múltiplos endpoints para cada Web Service.
- Validação das requisições e respostas contra as suas definições no **WSDL**.
- Testes funcionais, carga e stress.
- Execução de diversos testes em paralelo.
- Editores com *syntax highlight* e formatação automática.
- Suporte a expressões **XPATH** e de criação de testes complexos utilizando scripts **Groovy**.
  
- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#soap-ui)
***

## 10. O que é uma API?

![API imagem](https://user-images.githubusercontent.com/110742899/187646608-6837952e-8cfd-43be-a749-8d1077e97653.jpeg)

API significa Application Programming Interface. No contexto de APIs, a palavra Aplicação refere-se a qualquer software com uma função distinta. A interface pode ser pensada como um contrato de serviço entre duas aplicações. Esse contrato define como as duas se comunicam usando solicitações e respostas. A documentação de suas respectivas APIs contém informações sobre como os desenvolvedores devem estruturar essas solicitações e respostas.

APIs são mecanismos que permitem que dois componentes de software se comuniquem usando um conjunto de definições e protocolos. A arquitetura da API geralmente é explicada em termos de **cliente e servidor**. A aplicação que envia a solicitação é chamada de cliente e a aplicação que envia a resposta é chamada de servidor.


### 10.1. Como APIs funcionam?

Existem quatro maneiras diferentes pelas quais as APIs podem funcionar, dependendo de quando e por que elas foram criadas:

#### 10.1.1 APIs SOAP

  Essas APIs usam o **Simple Object Access Protocol**. Cliente e servidor trocam mensagens usando **XML**. Esta é uma API menos flexível que era mais popular no passado.

#### 10.1.2 APIs RPC

  Essas APIs são conhecidas como **Remote Procedure Calls**. O cliente conclui uma função (ou um procedimento) no servidor e o servidor envia a saída de volta ao cliente.

#### 10.1.3 APIs WebSocket
  
  API Websocket é outro desenvolvimento de API da Web moderno que usa objetos **JSON** para passar dados. Uma API WebSocket oferece suporte à comunicação bidirecional entre aplicativos cliente e o servidor. O servidor pode enviar mensagens de retorno de chamada a clientes conectados, tornando-o mais eficiente que a API REST.

#### 10.1.4. APIs REST
  
  Essas são as APIs mais populares e flexíveis encontradas na Web atualmente. O cliente envia solicitações ao servidor como dados. O servidor usa essa entrada do cliente para iniciar funções internas e retorna os dados de saída ao cliente.

### 10.2. Diferentes tipos de APIs

As APIs são classificadas de acordo com sua arquitetura e escopo de uso, podendo ser elas:

#### 10.2.1. APIs privadas
  
  Elas são internas a uma empresa e são usadas apenas para conectar sistemas e dados dentro da empresa.

#### 10.2.2. APIs públicas
  
  Estas são abertas ao público e podem ser usadas por qualquer pessoa. Pode ou não haver alguma autorização e custo associado a esses tipos de APIs.

#### 10.2.3. APIs de parceiros
  
  Estas são acessíveias apenas por desenvolvedores externos autorizados para auxiliar parcerias entre empresas.

#### 10.2.4. APIs compostas
  
  Estas combinam duas ou mais APIs distintas para atender a requuisitos ou comportamentos complexos do sistema.


- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#apis)
***

## 11. O que é Swagger?

![swagger-7](https://user-images.githubusercontent.com/110742899/187651608-033e4416-3dc1-4819-b15c-4344ec1c19a7.png)

Trata-se de uma aplicação open source que auxilia desenvolvedores nos processos de definir, criar, documentar e consumir APIs REST. EM suma, o **Swagger** visa padronizar este tipo de integração, descrevendo os recursos que uma API deve possuir, como *endpoints*, dados recebidos, dados retornados, códigos HTTP e métodos de autenticação, entre outros.

Ele simplifica o processo de escrever APIs, especificando os padrões e fornecendo as ferramentas necessárias para escrever APIs seguras, com alto desempenho e escaláveis.

A principal contribuição do Swagger é garantir a padronização das interfaces de integração. Com isso, sempre que preciso, qualquer desenvolvedor pode ter acesso aos parâmetros necessários para a correta integração com seu sistema.

Os benefícios da utilização do Swagger são:

- **É compreensível para desenvolvedores e não desenvolvedores** 
  
  Gerentes de produto, parceiros e até clientes em potencial podem contribuir com o design de uma API, pois podem vê-la claramente mapeada nesta interface amigável.

- **É legível por humanos e por máquinas** 
  
  Isso significa que não apenas a documentação pode ser compartilhada com uma equipe internamente, mas também usada para automatizar processos dependentes de API.

- **É facilmente ajustável** 
  
  O que o torna perfeito para testar e depurar problemas relacionados às APIs.

### 11.1. Como funciona?

Quando o desenvolvedor trabalha com uma API existente, ele precisa conhecer as funcionalidades disponíveis e detalhes de como invocá-las: recursos, métodos, content-types e outras informações.

Para criar uma nova API REST, os profissionais da área de desenvolvimento se deparam com outras duas preocupações comuns: como modelar e documentar?

O Swagger é a melhor resposta. Ele simplifica algumas tarefas como:

- Modelagem da integração;
- Geração de documentação (legível);
- Geração de códigos do cliente e do servidor, com suporte a várias linguagens de programação.

Além disso, o Swagger traz um ecossistema formado por várias ferramentas para criação e manipulação de especificação de APIs. Veja, no quadro a seguir, algumas delas.
Nome | Descrição
:---: |  :---:
Swagger Codegen | Ferramenta em linha de comando usada para o desenho de “esqueletos” de Servidores em mais de 10 tecnologias e Clientes em mais de 25 tecnologias diferentes.
Swagger UI | Interface gráfica para explorar as definições de APIs baseadas em Swagger. É aplicado na publicação da documentação.
Swagger Editor | Editor usado para a criação do contrato com definições YAML ou JSON.
Swagger JS | Conjunto de bibliotecas javascript usado para o consumo de APIs especificadas com o Swagger, que podem ser utilizadas com aplicações clientes e node.js.
Swagger Node | Módulo Swagger para Node.js.
Swagger Socket | Expõe e invoca definições de APIs feitas com Swagger em WebSockets.
Swagger Parser | Biblioteca independente para parsing de Java.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#swagger)
***

## 12. Microsserviços

![microsserviços](https://user-images.githubusercontent.com/110742899/187651885-3bd0f7d5-9e00-401a-8e99-d48821bbf1a3.png)

Com as arquiteturas monolíticas, todos os processos são altamente acoplados e executam como um único serviço. Isso significa que se um processo do aplicativo apresentar um pico de demanda, toda a arquitetura deverá ser escalada. A complexidade da adição ou do aprimoramento de recursos de aplicativos monolíticos aumenta com o crescimento da base de código. Essa complexidade limita a experimentação e dificulta a implementação de novas ideias. As arquiteturas monolíticas aumentam o risco de disponibilidade de aplicativos, pois muitos processos dependentes e altamente acoplados aumentam o impacto da falha de um único processo.

Com uma arquitetura de microsserviços, um aplicativo é criado como componentes independentes que executam cada processo do aplicativo como um serviço. Esses serviços se comunicam por meio de uma interface bem definida usando APIs leves. Os serviços são criados para recursos empresariais e cada serviço realiza uma única função. Como são executados de forma independente, cada serviço pode ser atualizado, implantado e escalado para atender a demanda de funções específicas de um aplicativo.

Portanto, microsserviços são uma abordagem arquitetônica e organizacional do desenvolvimento de software na qual o software consiste em pequenos serviços independentes que se comunicam usando APIs bem definidas. Esses serviços pertencem a pequenas equipes autossuficientes.

As arquiteturas de microsserviços facilitam a escalabilidade e agilizam o desenvolvimento de aplicativos, habilitando a inovação e acelerando o tempo de introdução de novos recursos no mercado.

### 12.1. Características dos microsserviços

- **Autônomos**
  
  Cada serviço do componente de uma arquitetura de microsserviços pode ser desenvolvido, implantado, operado e escalado sem afetar o funcionamento de outros serviços. Os serviços não precisam compartilhar nenhum código ou implementação com os outros serviços. Todas as comunicações entre componentes individuais ocorrem por meio de APIs bem definidas.

- **Especializados**
  
  Cada serviço é projetado para ter um conjunto de recursos e é dedicado à solução de um problema específico. Se os desenvolvedores acrescentarem mais código a um serviço ao longo do tempo, aumentando sua complexidade, ele poderá ser dividido em serviços menores.

### 12.2. Benefícios dos microsserviços

- **Agilidade**
  Os microsserviços promovem uma organização de equipes pequenas e independentes que são proprietárias de seus serviços. As equipes atuam dentro de um contexto pequeno e claramente compreendido e têm autonomia para trabalhar de forma mais independente e rápida. O resultado é a aceleração dos ciclos de desenvolvimento. Você obtém benefícios significativos do throughput agregado da organização.

- **Escalabilidade flexível**
  
  Os microsserviços permitem que cada serviço seja escalado de forma independente para atender à demanda do recurso de aplicativo oferecido por esse serviço. Isso permite que as equipes dimensionem corretamente as necessidades de infraestrutura, meçam com precisão o custo de um recurso e mantenham a disponibilidade quando um serviço experimenta um pico de demanda.

- **Fácil implantação**
 
  Os microsserviços permitem a integração e a entrega contínuas, o que facilita o teste de novas ideias e sua reversão caso algo não funcione corretamente. O baixo custo de falha permite a experimentação, facilita a atualização do código e acelera o tempo de introdução de novos recursos no mercado.

- **Liberdade tecnológica**

  As arquiteturas de microsserviços não seguem uma abordagem generalista. As equipes são livres para escolher a melhor ferramenta para resolver problemas específicos. O resultado é que as equipes que criam microsserviços podem optar pela melhor ferramenta para cada tarefa.

- **Código reutilizável**
  
  A divisão do software em módulos pequenos e bem definidos permite que as equipes usem funções para várias finalidades. Um serviço criado para uma determinada função pode ser usado como componente básico para outro recurso. Isso permite que os aplicativos sejam reutilizados, pois os desenvolvedores podem criar recursos sem precisar escrever código.

- **Resiliência**

  A independência do serviço aumenta a resistência a falhas do aplicativo. Em uma arquitetura monolítica, a falha de um único componente poderá causar a falha de todo o aplicativo. Com os microsserviços, os aplicativos lidam com a falha total do serviço degradando a funcionalidade, sem interromper todo o aplicativo.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referêcias](#microsserviços)
***

## 13. Protocolo HTTP
![99427853_123396039361472_8630412506986184704_n](https://user-images.githubusercontent.com/110742899/187653928-7d2d0fd9-599d-43f5-b38d-1ab8ed3f4173.jpg)

HTTP - *Hypertext Transfer Protocol* - é um protocolo de transferência que possibilita que as pessoas que inserem a URL do seu site na Web possam ver os conteúdos e dados que nele existem. Esse sistema é a base da comunicação que existe em toda a Internet em que os sites e conteúdos que tragam hiperlinks possam ser encontrados mais facilmente pelo público por meio de um clique do mouse ou um toque na tela.

Qualquer servidor escolhido para hospedar o site de uma empresa tem um programa projetado para receber solicitações HTTP. Portanto, o navegador é um cliente HTTP que envia solicitações constantemente ao servidor. Assim, quando um usuário acessa ou digita a URL de um site, o navegador cria uma solicitação HTTP na web e a envia ao endereço de IP indicado pela URL. Dessa forma, o servidor recebe essa solicitação e envia os arquivos associados que, nada mais são, do que os sites acessados na Internet.

HTTP é um protocolo baseado em texto sem conexão. Isso significa que as pessoas que acessam o site da uma empresa enviam solicitações a servidores que as exibem na forma do site em formato de texto, imagens, e outros tipos de mídia. Depois que a solicitação é atendida por um servidor, a conexão entre o usuário e o servidor é desconectada. Uma nova conexão deve ser feita para cada solicitação, isto é, cada vez que alguém acessa um site. 

Em suma, quando alguém digita uma URL de site em um navegador, é isto que acontece:

1. Se a URL pertencer a um domínio próprio, o navegador primeiro se conecta a um servidor e recuperará o endereço IP correspondente ao servidor;

2. O navegador se conecta ao servidor e envia uma solicitação HTTP para a página da web desejada;;

3. O servidor recebe a solicitação e verifica a página desejada. Se a página existir, o servidor a mostrará. Se o servidor não conseguir encontrar a página solicitada, ele enviará uma mensagem de erro HTTP 404, ou seja, página não encontrada;

4. O navegador, então, recebe a página de volta e a conexão é fechada;

5. Caso a página exista, o navegador a analisa e procura outros elementos necessários para concluir a sua exibição, o que inclui seus textos, imagens e afins;

6. Para cada um desses elementos, o navegador faz conexões adicionais e solicitações HTTP para o servidor para cada elemento;

7. Quando o navegador terminar de carregar todos os elementos, a página será carregada na janela do navegador.
  
### 13.1. Status HTTP

Os códigos de status das respostas HTTP indicam se uma requisição HTTP foi corretamente concluída. As respostas são agrupadas em cinco classes:

1. Respostas de informação (100-199),
2. Respostas de sucesso (200-299),
3. Redirecionamentos (300-399)
4. Erros do cliente (400-499)
5. Erros do servidor (500-599)

Error HTTP são os códigos HTTP que referem-se a erros de cliente e servidor, respectivamente, e impedem o carregamento de um site. Os códigos HTTP Error são sempre começados pelos números 4 ou 5, que são respectivamente falhas do cliente (navegador) ou do servidor.

Quando um site é visitado, o navegador faz uma solicitação ao servidor, e o servidor responde o navegador com um código, os códigos HTTP. São esses códigos que informam o que o servidor e navegador estão conversando entre si. Os códigos podem ser divididos entre:

Os principais códigos de status HTTP são:

- **200 OK**

  Esta requisição foi bem sucedida. O significado do sucesso varia de acordo com o método HTTP.

- **201 Created**

  A requisição foi bem sucedida e um novo recurso foi criado como resultado. Esta é uma tipica resposta enviada após uma requisição POST.

- **204 No Content**]
  
  Não há conteúdo para enviar para esta solicitação, mas os cabeçalhos podem ser úteis. O user-agent pode atualizar seus cabeçalhos em cache para este recurso com os novos.

- **Error 403**

  O Erro 403 – Forbidden significa que o servidor entendeu a solicitação do navegador mas se recusa a fazê-lo, pois o navegador não possui autorização para isso.

  Ao enviar este erro, o servidor comunica “You don’t have permission to access on this server”, isso quer dizer que o acesso foi negado.

- **Error 404**

  Quando uma URL é digitada e emite a mensagem ERROR 404 – PAGE NOT FOUND quer dizer que esta URL não leva a lugar nenhum. Os motivos podem ser significar que a página não existe mais, a URL deste site mudou ou foi digitada a URL errada.

- **Error 500**

  Erro 500 significa que algum script ou solicitação não foi compreendida – o que nem sempre indica um problema com o servidor. Os motivos podem ser arquivos **.htaccess** corrompidos, permissões de arquivo incorreto, tempo limite de script, versão do PHP incompatível, etc.

- **Error 503**

  O status ERRO 503 significa serviço temporariamente indisponível. Há pelo menos cinco possíveis causas:

  1. Plugins e temas bugados;
  2. Um mau comportamento de um script PHP customizado;
  3. Servidores com recursos insuficientes;
  4. Problemas de servidor;
  5. Ataques maliciosos, como o infame Ataque Distribuído por Negação de Serviço (DDoS).

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#protocolo-http)
***

## 14. Protocolo REST

![rest](https://user-images.githubusercontent.com/110742899/187654278-ff18e8f4-22ae-46f1-aea1-ddae411c5967.jpg)

REST, ou *Representational State Transfer*, é um estilo arquitetônico aplicado para fornecer padrões entre sistemas de computador na web, facilitando a comunicação entre eles. Os sistemas em conformidade com REST, muitas vezes conhecidos como sistemas RESTful, são reconhecidos pelo jeito como separam as preocupações do cliente e do servidor. A utilização do estilo de arquitetura REST é fundamental para o estabelecimento de um ambiente favorável à realização das ações necessárias para manter um website em bom funcionamento.

No estilo REST, a implementação do cliente e do servidor pode ser feita de forma independente, sem que cada um conheça o outro. Isso significa que o código do lado do cliente pode ser alterado a qualquer momento, sem afetar a operação do servidor, e o contrário também é válido.

Ao utilizar uma interface REST, clientes diferentes atingem os mesmos pontos finais REST, executam ações iguais e recebem as mesmas respostas. Como os sistemas REST interagem por meio de operações padrão sobre recursos, eles não dependem da implementação de interfaces.

Essas restrições ajudam as aplicações RESTful a alcançar maior nível de confiabilidade, além de possibilitar um desempenho rápido e escalável. Todos os componentes podem ser gerenciados, atualizados e reutilizados sem afetar o sistema como um todo, mesmo durante a operação.

Um benefício principal do uso desse estilo, tanto do ponto de vista do cliente quanto do servidor, é que as interações baseadas em REST acontecem usando estruturas que são familiares a qualquer um que esteja acostumado a usar o HTTP da Internet. Um exemplo desse arranjo são as interações baseadas em REST — todas comunicam seu status usando códigos de status HTTP padrão.

Detalhes como a criptografia e a integridade do transporte de dados são resolvidos não adicionando novas estruturas ou tecnologias, mas confiando nos conhecidos sistemas de criptografia **Secure Sockets Layer** (SSL) e **Transport Layer Security** (TLS). Assim, toda a arquitetura REST é construída sobre conceitos com os quais a maioria dos desenvolvedores já está familiarizada.

REST é, também, um estilo arquitetônico independente do idioma. Aplicações baseadas nesse estilo podem ser escritas usando qualquer linguagem, seja Java, seja Kotlin, .NET, AngularJS ou JavaScript. Desde que uma linguagem de programação possa fazer solicitações baseadas na web usando HTTP, é possível que essa linguagem seja usada para ativar uma API ou serviço web RESTful.


### 14.1. Client-Server

  A separação das preocupações é o princípio por trás das restrições relacionadas à relação cliente-servidor. Desde que cada parte saiba o formato das mensagens a serem enviadas à outra, elas podem ser mantidas modulares e separadas.

  Separando as preocupações da interface do usuário daquelas do armazenamento de dados, é possível otimizar a flexibilidade da interface em todas as plataformas e melhorar a escalabilidade, tornando mais simples os elementos do servidor. Além disso, a separação permite a cada elemento a capacidade de evoluir de forma independente.

### 14.2. Stateless
  
  Os sistemas que seguem o paradigma REST são stateless, o que pode ser traduzido livremente como “sem estado”. Isso significa que o servidor não precisa saber nada sobre o estado em que o cliente se encontra e vice-versa.

  Dessa forma, tanto o servidor quanto o cliente podem compreender qualquer mensagem recebida, mesmo sem ver as anteriores. Isso acontece porque o sistema não utiliza comandos, mas os substantivos da Web, que descrevem qualquer arquivo que você precise armazenar ou utilizar.

### 14.3. Cacheable

  As restrições de cache requerem que as informações contidas em uma resposta a uma solicitação sejam, diretamente ou não, definidas como cacheáveis ou não cacheáveis. Caso uma resposta seja armazenável em cache, então, é dado ao cliente o direito de utilizar novamente esses dados para atividades similares no futuro.

  A vantagem de acrescentar restrições de cache é que elas têm o potencial de eliminar parcial ou completamente algumas interações, melhorando a eficiência, a escalabilidade e o desempenho percebido pelo usuário. Isso torna a experiência muito mais fluida e eficiente. 

### 14.4. Uniform interface

  O principal elemento que distingue o REST de outras opções com base na rede é o seu foco em uma interface uniforme entre os componentes. O princípio de generalidade, característica da engenharia de software, quando aplicado à interface de componentes, simplifica a arquitetura do sistema e torna as interações mais visíveis.

  A fim de obter uniformidade na interface, são necessárias múltiplas restrições para orientar o comportamento dos componentes. REST é definido por quatro fatores:

  1. Identificação de recursos;
  2. Gerenciamento de recursos por meio de representações;
  3. Mensagens auto-descritivas;
  4. Hipermídia.

### 14.5. Layered system

  Para melhorar ainda mais o desempenho para as atuais e crescentes exigências da Internet, é possível acrescentar restrições de sistema por camadas. Assim, a arquitetura é constituída por camadas que seguem uma ordem hierárquica. Isso restringe o comportamento dos elementos, de modo que cada um deles só possa “enxergar” a camada com que estão interagindo no momento.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#protocolo-rest)
***

## 15. cUrl

![curl-logo](https://user-images.githubusercontent.com/110742899/187654521-b5f605a0-72ed-43d4-a5a3-3c565faa2fce.jpg)

O cURL, ou "URL do cliente" é uma ferramenta de linha de comando que possibilita que desenvolvedores e usuários de serviços de hospedagem façam solicitações HTTP a partir do shell e protocolos como HTTPS, FTP, FTPS, IMAP, IMAPS, POP3, POP3S, SMTP e SMTP. Como é um projeto de código aberto, pode ser incrementado por uma comunidade de desenvolvedores, o que contribui constantemente para novas características e funcionalidades.

Algumas de suas funcionalidades são:

- **Testar uma API**
  
  Para testar o funcionamento de uma API, é preciso enviar argumentos por meio do método POST ou JSON com alguns parâmetros específicos. A simulação do comportamento de um formulário HTML por meio do comando cURL pode ser feito a partir de argumentos como:

      curl --data "name=joao&surname=emanuel" https://www.seudominio.com

  Nesse caso, a ramificação --data tem a mesma funcionalidade do-d. Com ele, o método mudará para POST automaticamente. No entanto, o usuário pode usar um -X e adicionar a requisição para especificar o método que deve ser chamado entre aspas antes do -d, como mostrado a seguir:

      curl -X "POST" -d "name=joao&surname=emanuel" https://www.seudominio.com

- **Fazer o download de um documento**
  
  Para fazer o download de um documento,você pode usar o cURL com:

  - -O: salva o arquivo no diretório de trabalho atual com o mesmo nome do local remoto;
  - -o: permite que você especifique um nome de arquivo e um local diferente do de origem. Veja os exemplos de comandos abaixo:
  
        $ curl -O https://seudominio.com/seuarquivo.tar.gz # Save as seuarquivo.tar.gz

        $ curl -o novonome.tar.gz https://seudominio.com/seuarquivo.tar.gz # Save as novonome.tar.gz

- **Reiniciar um download interrompido**

  Se um download for interrompido por alguma razão (Ctrl + c, por exemplo), você pode reiniciá-lo por meio do -C. Essa ramificação dentro do comando cURL orienta o reinício do download a partir do momento em que ele parou.

      $ curl -C - -O https://seudominio.com/seuarquivo.tar.gz
  ![cUrl 1](https://www.tecmint.com/wp-content/uploads/2018/08/Download-File-Using-Curl-Command.png)

- **Fazer o download de múltiplos arquivos**

  Com o comando cURL e a ramificação -O, o usuário também pode executar o download de mais arquivos simultaneamente.

      $ curl -O https://seudominio.com/info.html -O https://outrodominio.com/about.html 

- **Baixar URLs de um arquivo**

  Se o usuário combina o comando cURL com xargs, consegue fazer o download de todas as URLs presentes em um arquivo de uma vez. Esse processo pode ser bem útil na análise e visualização de dados.

      $ xargs -n 1 curl -O < listurls.txt

  ![cUrl2](https://www.tecmint.com/wp-content/uploads/2018/08/Download-Multiple-Files-with-Curl.png)

- **Usar um proxy com ou sem autenticação**

  Para encontrar um servidor proxy na porta 8080, o usuário pode usar o seguinte comando:

      $ curl -x proxy.seudominio.com:8080 -U usuario:senha -O https://seudominio.com/seuarquivo.tar.gz
  
  Caso o proxy não exija autenticação, basta eliminar o “usuário:senha” do código.

- **Consultar cabeçalhos HTTP**

  Os cabeçalhos HTTP permitem ao servidor enviar informações adicionais sobre o site, como detalhes sobre a execução da solicitação, que podem ser interessantes para o usuário.

  Apesar de essas informações ficarem disponíveis nas ferramentas de desenvolvedor dos navegadores, por meio do cURL o acesso também é rápido: basta escrever junto ao comando cURL a ramificação -I e o endereço do site pelo qual você deseja visualizar os dados:

      $ curl -I www.seudominio.com

- **Download ou upload de arquivos de um servidor FTP com ou sem autenticação**

  O download dos arquivos em um servidor FTP remoto também pode ser realizado por meio do cURL. Digite a ramificação -u para informar o usuário e a senha de acesso ao servidor (caso eles sejam exigidos), a ramificação -vsc nnnO e o diretório onde o arquivo foi armazenado no banco de dados (MySQL, por exemplo). Esse comando fará o download do arquivo requisitado no diretório de trabalho atual.

      $ curl -u usuario:senha -O ftp://seuservidorftp/seuarquivo.tar.gz 

  Já o upload pode ser executado a partir da ramificação -T, seguido pelo nome do arquivo e diretório FTP do servidor:

      $ curl -u usuario:senha -T seuarquivolocal.tar.gz ftp://seuservidorftp

- **Descobrir os cookies armazenados durante um acesso**

  Caso o usuário queira visualizar quais cookies foram armazenados em seu equipamento durante um acesso a um site, o cURL também consegue exibir essas informações. Suponha que você tenha navegado pelo site <https://www.cnn.com> para ler algumas notícias:

  A ramificação --cookie-jar seguida do nome como o arquivo será salvo em .txt, da URL do site que você deseja analisar e da ramificação -O salva as informações em seu diretório:

      $ curl --cookie-jar cnncookies.txt https://www.cnn.com/index.html -O

  Já a ramificação ~]$ cat seguida do nome em que o arquivo foi salvo em .txt retorna os dados requisitados:

  ![cUrl3](https://www.tecmint.com/wp-content/uploads/2018/08/Curl-Store-Cookies.png)

  Para enviar os cookies recuperados em solicitações subsequentes para o mesmo site de origem, basta usar a ramificação --cookie:

      $ curl --cookie cnncookies.txt https://www.cnn.com

  Alguns comandos, como--location-trusted, semelhante ao -L, permitem o envio de usuário e senha para todos os hosts para os quais o site redireciona. Isso poderá criar uma vulnerabilidade relacionada à segurança e, por isso, é importante usar certificados de segurança como o SSL e o TLS no seu site.

  Desenvolvedores podem solicitar o cURL a partir de qualquer terminal, uma vez que conseguem fazer o download por meio do apt-get no Linux. Apesar disso, a ferramenta já vem pré-instalada em sistemas operacionais baseados em Linux.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#curl)
***

## 16. Postman

![postman](https://user-images.githubusercontent.com/110742899/187654862-d0da9b9f-581a-48ed-ab4d-8c65361be2aa.jpg)

O Postman é uma ferramenta que dá suporte à documentação das requisições feitas pela API. Ele possui ambiente para a documentação, execução de testes de APIs e requisições em geral.

Ao utilizá-lo, você passará a trabalhar com APIs de modo mais eficiente, construindo solicitações rapidamente e, ainda, poderá guardá-las para uso posterior, além de conseguir analisar as respostas enviadas pela API.

Um bom motivo para usar essa ferramenta é que, por meio dela, é possível reduzir drasticamente o tempo necessário para testar e desenvolver APIs.

Em um exemplo prático, imagine que você queira fazer uma solicitação GET para procurar certas informações no nome da empresa.

Se fosse o caso de testar uma solicitação GET sem usar o Postman, você precisaria escrever todo um código para executar a requisição, além de uma interface visual para interagir com essa rotina.

Se fosse concedido, provavelmente você precisaria escrever tudo isso para criar um aplicativo funcional usando essa API, mas todo esse trabalho seria simplesmente para testar a sua funcionalidade, o que de fato, nesse formato, é tedioso e demorado.

Já com o Postman, esse teste é muito mais otimizado. Tudo o que precisa ser feito é:

1. Obter a conexão da rota à barra de endereços;
2. Selecionar o método de resposta GET na caixa suspensa à esquerda;
3. Digitar a chave da API na seção "Headers";
4. Especificar o formato da resposta, que poderia ser em JSON, por exemplo, e;
5. Clicar em enviar.

Em seguida, será obtido os dados de resposta em **JSON** (simples e fácil de ler) acompanhado do código de status 200, que confirma que a solicitação GET foi bem-sucedida.

### 16.1. Benefícios

Além de ser um aplicativo gratuito e fácil de aprender, com pouco tempo você já estará enviando seus primeiros requests (solicitações/requisições). No mais, trata-se de uma ferramenta com um amplo suporte para todas as APIs e Schemas.

Entre as principais vantagens em se usar o Postman, podemos destacar:

- **Possibilita qualquer tipo de chamada de API —  REST, SOAP ou HTTP;**

- **Oferece suporte para formatos de dados populares, como OpenAPI GraphQL e RAML;**

- **Fácil acessibilidade**: 
  
  Para usar o Postman, basta fazer login em sua conta, facilitando o acesso a arquivos a qualquer momento, em qualquer lugar, desde que um aplicativo Postman esteja instalado no computador;

- **Uso de Coleções**: 
  
  O Postman permite que os usuários criem coleções para suas chamadas de API. Cada coleção pode criar subpastas e várias solicitações. Isso ajuda a organizar suas suítes de teste;

- **Colaboração (Collaboration)**: 
  
  Coleções e ambientes podem ser importados ou exportados, facilitando o compartilhamento de arquivos. Um link direto também pode ser usado para compartilhar coleções;

- **Criar ambientes**: 
  
  Ter vários ambientes ajuda a ter menos repetições de testes, pois é possível usar a mesma coleção, mas em um ambiente diferente;

- **Elaborar testes**: 
  
  Pontos de verificação de teste, como a verificação do status de resposta HTTP bem-sucedido, podem ser adicionados a cada chamada de API, o que ajuda a garantir a cobertura do teste;

- **Teste de automação**: 
  
  Com o uso do **Collection Runner** ou **Newman**, os testes podem ser executados em várias iterações, economizando tempo para testes repetitivos;

- **Depuração**: 
  
  O console do Postman ajuda a verificar quais dados foram recuperados, facilitando a depuração de testes;

- **Integração Contínua**: 
  
  A partir da sua capacidade de oferecer suporte à integração contínua, são mantidas práticas de desenvolvimento.

### 16.2. Funcionamento

Já na página principal do aplicativos, temos muitas informações e, para esclarecer o modus operandi da  ferramenta, precisaremos dar uma passada rápida nas opções disponíveis na interface.

![postman1](https://enotas.com.br/blog/wp-content/uploads/2020/06/interface-1024x388.png)

- **New**: 
  
  É aqui que você criará uma nova solicitação, coleção ou ambiente.

- **Import**: 
  
  É usado para importar uma coleção ou ambiente. Existem opções como importar arquivo, pasta, vincular ou colar texto não processado.

- **Runner**: 
  
  Os testes de automação podem ser executados através do Collection Runner. Isso será discutido mais adiante.

- **Open New**: 
  
  Permite abrir uma nova guia, Postman Window ou Runner Window.

- **My Workspace**: 
  
  Você pode criar um novo espaço de trabalho individualmente ou em equipe.

- **Invite**: 

  Permite convidar membros da equipe.

- **History**: 
  
  As solicitações anteriores que você enviou serão exibidas no Histórico. Isso facilita o rastreamento das ações realizadas.

- **Collections**: 
  
  Permite criar coleções. Cada coleção pode ter subpastas e várias solicitações. Uma solicitação ou pasta também pode ser duplicada.

- **Request tab**: 
  
  Exibe o título da solicitação em que você está trabalhando.

- **HTTP Request**: 
  
  Clicar nesse botão exibirá uma lista suspensa de solicitações diferentes, como GET, POST, COPY, DELETE etc. Nos testes, as solicitações mais usadas são GET e POST.

- **Request URL**: 
  
  Também conhecido como “endpoint”, é aqui que você identificará o link para o qual a API se comunicará.

- **Save**: 
  
  Serve para salvar novas alterações.

- **Params**: 
  
  É aqui que você escreverá os parâmetros necessários para uma solicitação, como valores-chave.

- **Authorization**: 
  
  Para acessar APIs, é necessária uma autorização adequada. Pode ser na forma de nome de usuário e senha, token de portador, entre outros.

- **Headers**: 
  
  Você poderá definir cabeçalhos, como o tipo de conteúdo JSON, por exemplo.

- **Body**: 
  
  Este botão possibilita personalizar detalhes em uma solicitação comumente usada na solicitação POST.

- **Pre-request Script**: 
  
  São scripts que serão executados antes da solicitação. Geralmente, os scripts de pré-solicitação para o ambiente de configuração são usados ​​para garantir que os testes sejam executados no ambiente correto.

- **Tests**: 
  
  São scripts executados durante a solicitação. É importante ter testes, pois configura pontos de verificação para analisar se o status da resposta está de acordo, ou se os dados recuperados estão conforme o esperado, por exemplo.

### 16.2. Requisição GET

As requisições GET são usadas para recuperar informações da URL fornecida e não realizam alterações feitas nos endpoints.

Para realizar uma requisição GET é muito simples. Na área de trabalho do aplicativo, faça o seguinte:

1. Defina sua solicitação HTTP como GET.
2. No campo URL da solicitação, coloque o link de entrada.
3. Clique em Enviar.
4. Você verá na aba “Status” a mensagem “200 OK”.
![postamn3](https://enotas.com.br/blog/wp-content/uploads/2020/06/10.png)

Pode haver casos em que a requisição GET não tenha êxito. Isto pode acontecer devido a uma URL de solicitação ser inválida ou porque a autenticação é necessária.

### 16.3. Requisição POST

Pode-se dizer que a grande diferença entre um GET e um POST é que, no caso de um POST, existe a manipulação de dados, com o usuário adicionando informações ao endpoint. 

Para demonstrar isso na prática — usando os mesmos dados do exemplo anterior —, agora vamos adicionar nosso próprio usuário.

Para efetuar um Post Request você deverá seguir os 5 seguintes passos:

1. Clique em uma nova guia para criar uma nova solicitação.
2. Na nova guia, siga os seguintes caminhos:

   - Defina sua solicitação HTTP para POST.
   - Insira o mesmo link no URL da solicitação
   - Selecione a aba “Body”
![postman4](https://enotas.com.br/blog/wp-content/uploads/2020/06/2.png)

3. Agora, na aba “Body”, clique em “raw” e selecione JSON.

    ![postman5](https://enotas.com.br/blog/wp-content/uploads/2020/06/3.png)

4. O Post Request deve ter o formato correto para garantir que os dados solicitados serão criados. É uma boa prática usar o GET primeiro para verificar o formato JSON da solicitação. Copie e cole apenas o resultado de um usuário do GET, como segue exemplo abaixo.
   
   ![postman6](https://enotas.com.br/blog/wp-content/uploads/2020/06/5.png)

A partir daí, verifique se o código foi copiado corretamente com chaves e colchetes emparelhados. E então, altere os campos “id” para 11 e o “name” para qualquer nome desejado. Você também pode alterar outros detalhes, como o endereço, por exemplo.

5. Por fim, clique em Enviar (Send).
   
   ![postman7](https://enotas.com.br/blog/wp-content/uploads/2020/06/4.png)

### 16.4. Parâmetros de dados

A parametrização de dados é um dos recursos mais úteis do Postman. Em vez de criar as mesmas solicitações com dados diferentes, você pode usar variáveis ​​com parâmetros. 

Essas informações podem ser de um arquivo de dados ou de uma variável de ambiente. Vale lembrar que a parametrização ajuda a evitar a repetição dos mesmos testes e iterações podem ser usadas para testes de automação.

Esses parâmetros são criados por meio do uso de colchetes duplos: {{sample}}.

![postman7](https://enotas.com.br/blog/wp-content/uploads/2020/06/7.png)

- **Criando uma Parâmetro GET**
  
1. Defina sua solicitação HTTP como **GET**.
2. Insira o link da URL. Substitua a primeira parte do link por um parâmetro como {{url}}. A URL de solicitação agora deve ser “{{url}}/users”.
3. Clique em enviar (Send).
4. Você deverá receber uma mensagem dizendo que não houve resposta (“could not get any response”), isso pois ainda não definimos a fonte do nosso parâmetro.
   
   ![postman8](https://enotas.com.br/blog/wp-content/uploads/2020/06/any-response.png)

5. Para usar o parâmetro, você precisa definir o ambiente.
6. Clique no ícone com o desenho de um “olho”, localizado no canto superior direito.
7. Clique em “edit” para definir a variável para um ambiente global que pode ser usado em todas as coleções.
   
    ![postman9](https://enotas.com.br/blog/wp-content/uploads/2020/06/eye-icon.png)

8. Na aba “Variable”, defina o nome para o URL desejado.
9. Clique em "Save" (Salvar).
   
   ![postman10](https://enotas.com.br/blog/wp-content/uploads/2020/06/vari%C3%A1vel.png)

10. Se após isso surgir uma janela, como abaixo, basta fechá-la.
   
    ![postman11](https://enotas.com.br/blog/wp-content/uploads/2020/06/screen.png)

11. Volte para ao seu GET e clique em Enviar (Send). A partir de agora já deve haver resultados para sua solicitação.

Uma boa prática nesse quesito é sempre verificar se seus parâmetros possuem uma fonte, como uma variável de ambiente ou arquivo de dados, para evitar erros.

### 16.5. Postman Tests

Os Postman Tests são códigos JavaScript adicionados às solicitações, que ajudam a verificar resultados como status bem-sucedido ou com falha, além de poder fazer a comparação de resultados esperados, entre outras funcionalidades.

De regra, você verá que esse comando começará com "pm.tes". Abaixo, alguns testes básicos para as solicitações parametrizadas do tópico anterior:

1. Acesse seu GET de usuário.

2. Alterne para a guia “Tests”. No lado direito, aparecerá uma seção de códigos snippets.
   
3. Nesta seção, clique em "Status Code: code is 200".
   
4. O painel será preenchido automaticamente.
   
   ![postman12](https://enotas.com.br/blog/wp-content/uploads/2020/06/11.png)

5. Clique em Enviar (Send). O resultado do teste deve ser exibido.
   
   ![postman13](https://enotas.com.br/blog/wp-content/uploads/2020/06/9.png)

6. Volte para a guia “Tests” e vamos adicionar outro teste. Desta vez, será comparado o resultado esperado com o resultado real.

7. Na seção de snippets, clique em "Response body:JSON value check". Verificaremos aqui se “Rafael” possui o ID do usuário 1.

    ![postman14](https://enotas.com.br/blog/wp-content/uploads/2020/06/8.png)

8. Substitua "Your Test Name" do código por "Check if user with id1 is Rafael" para que o nome do teste especifique exatamente o que queremos testar.

9. Substitua jsonData.value por jsonData [0].name. Para obter o caminho, verifique também o “Body” no GET anterior. 

10. Se você deseja obter um segundo resultado, use jsonData [1] e assim por diante para obter resultados futuros.

11. No eql, insira "Rafael".
  
    ![postman15](https://enotas.com.br/blog/wp-content/uploads/2020/06/12.png)

12. Clique em Enviar (Send). A partir de agora deve haver dois resultados de teste aprovados para sua solicitação.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#postman)
***

## 17. Containers

Um container é um ambiente isolado utilizado para empacotar aplicações. Containers têm o objetivo de segregar e facilitar a portabilidade de aplicações em diferentes ambientes.

Um container contém um conjunto de processos que são executados a partir de uma imagem, imagem esta que fornece todos os arquivos necessários. Os containers compartilham o mesmo **kernel** e isolam os processos da aplicação do restante do sistema operacional.

A ideia é que cada container assuma apenas uma responsabilidade. Nos containers, você divide a responsabilidade isolando os processos de cada aplicação, garantindo assim que nenhum processo possa influenciar no funcionamento dos demais processos.

Um agrupamento de containers também é conhecido como **cluster**. Um cluster consegue compartilhar recursos como armazenamento, tornando possível a execução de dezenas e até centenas de containers de maneira simultânea a partir do mesmo ambiente.

Os containers são muito práticos em ambiente de desenvolvimento. Sua aplicabilidade serve como base para o modelo DevOps e auxilia as áreas de Operações e Desenvolvimento. Na área de desenvolvimento, os containers empacotam aplicações com todas as suas dependências, a fim de serem acessíveis e compartilhadas, ao mesmo tempo em que ficam agnósticas a características do ambiente, como sistema operacional. Já em operações, são processos de aplicações rodando em um kernel compartilhado, mais simples que máquinas virtuais.

Embora seja algo parecido, um container não é uma **máquina virtual**. A diferença entre um container e uma máquina virtual é que os containers conseguem compartilhar o mesmo kernel do sistema operacional.

As **Máquinas Virtuais** (VMs) têm muitos benefícios. Entre eles, a capacidade de executar diferentes sistemas operacionais no mesmo servidor, o uso mais eficiente e econômico de recursos físicos e provisionamento de servidor mais rápido. Por outro lado, cada VM contém uma imagem de SO, bibliotecas, aplicativos e muito mais. Portanto, podem ser bem grandes.

![vms](https://azurecomcdn.azureedge.net/cvt-0747fe673b2e8ca5993409bc08d252e543aa7f50e5fa3d6409c621fbdd48b5c7/images/page/resources/cloud-computing-dictionary/what-is-a-container/valprop1.svg)

O contêiner virtualiza o SO subjacente e faz com que o aplicativo em contêiner detecte que o SO (incluindo CPU, memória, armazenamento de arquivos e conexões de rede) está totalmente à sua disposição. Como as diferenças no SO subjacente e na infraestrutura são abstraídas, enquanto a imagem base for consistente, o contêiner poderá ser implantado e executado em qualquer local. Para os desenvolvedores, isso é muito atrativo.

Como os contêineres compartilham o SO hospedado, não precisam inicializar um SO ou carregar bibliotecas. Por isso, os contêineres são muito mais eficientes e leves. Os aplicativos em contêineres podem ser inicializados em questão de segundos e muito mais instâncias do aplicativo podem se ajustar à máquina em comparação com um cenário de VM. A abordagem de SO compartilhado tem o benefício adicional de reduzir a sobrecarga no que diz respeito à manutenção, como a aplicação de patches e as atualizações.

![container](https://azurecomcdn.azureedge.net/cvt-0747fe673b2e8ca5993409bc08d252e543aa7f50e5fa3d6409c621fbdd48b5c7/images/page/resources/cloud-computing-dictionary/what-is-a-container/valprop2.svg)

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#containers)
***

## 18. Docker

O Docker é uma plataforma open source que facilita a criação e administração de ambientes isolados. Ele possibilita o empacotamento de uma aplicação ou ambiente dentro de um container, se tornando portátil para qualquer outro host que contenha o Docker instalado. Então, você consegue criar, implantar, copiar e migrar de um ambiente para outro com maior flexibilidade. A ideia do Docker é subir apenas uma máquina, ao invés de várias. E, nessa única máquina, você pode rodar várias aplicações sem que haja conflitos entre elas.

O Docker é algo parecido com uma máquina virtual extremamente leve, mas não se trata de fato de uma máquina virtual. O Docker utiliza containers que possuem uma arquitetura diferente, permitindo maior portabilidade e eficiência. O container exclui a virtualização e muda o processo para o Docker. Então, não podemos dizer que o Docker é uma máquina virtual.

![docker1](https://dkrn4sk0rn31v.cloudfront.net/2018/09/28135438/virtualization-vs-containers.jpg)

Na virtualização, há um maior consumo de recursos, uma vez que para cada aplicação é preciso carregar um sistema operacional. Já no Docker, não existe essa necessidade de múltiplos sistemas operacionais convidados.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#docker)
***

## 19. Docker Compose
![dockercompose1](https://static.imasters.com.br/wp-content/uploads/2017/12/CSD.jpg)

Docker Compose é o orquestrador de containers da Docker. Ele rege através do arquivo chamado docker-compose, semelhante ao Dockerfile, escrito em **YAML** (acrônimo recursivo para YAML Ain’t Markup Language) que é um formato de codificação de dados legíveis por humanos, o que torna fácil de ler e entender o que um Compose faz.

Um exemplo prático de como funciona o Docker Compose é: imagine que temos uma aplicação Java ou PHP e que essa aplicação depende de um banco de dados MySQL e, para disponibilizar essa aplicação na internet, queremos utilizar um proxy na frente. O cenário é bem típico e um cara de infraestrutura configura esse ambiente fácil em menos de um dia.

Agora imagina que para cada cliente, precisamos realizar esse setup pelo menos umas três vezes: um para Desenvolvimento, Homologação e outro para Produção.

Outro detalhe, se esses ambientes estão em cloud e existe uma Instância/VM para cada aplicação, isso pode gerar muito custo, recurso desperdiçado e tempo desnecessário gasto, sem contar o trabalho que dá para montar essa infra toda vez que surge um projeto novo. E no mundo de hoje, precisamos ser ágeis para entregar valor ao cliente.

Outra grande desvantagem desse processo é que ele é altamente manual, logo existe uma possibilidade de acontecer um erro humano.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#docker-compose)
***

## 20. Continuous Integration (CI)

Integração contínua (CI) é uma prática de automatizar a integração de alterações de código de vários contribuidores em um único projeto de software. É uma prática primária de DevOps, permitindo que os desenvolvedores mesclem com frequência as alterações de código em um repositório central onde builds e testes são executados. Ferramentas automatizadas são usadas para afirmar a correção do novo código antes da integração.

Um sistema de controle de versão de código-fonte é o ponto crucial do processo de integração contínua. O sistema de controle de versão também é complementado com outras verificações, como testes de qualidade de código automatizados, ferramentas de análise do estilo da sintaxe e muito mais.

A CI ajuda a dimensionar a contagem de pessoas e a entrega de resultado das equipes de engenharia. A introdução da IC no cenário mencionado acima permite que os desenvolvedores de software trabalhem com autonomia nos recursos em paralelo. Quando estão prontos para mesclar esses recursos em um produto final, podem fazer isso com rapidez e autonomia. A IC é uma prática valiosa e bem estabelecida em organizações modernas de engenharia de software de alto desempenho.

Um dos principais benefícios de adotar a CI é que ela economiza tempo durante seu ciclo de desenvolvimento, identificando e abordando conflitos com antecedência. Também é uma ótima maneira de reduzir o tempo gasto na atualização de segurança e regressão dando mais ênfase a ter um bom conjunto de testes. Por fim, ajuda a compartilhar um melhor entendimento da base de código e dos recursos que você está desenvolvendo para seus clientes.

- **Testes unitários** 
  
  Têm um escopo restrito e no geral verificam o comportamento de métodos ou funções individuais.

- **Testes de integração**
 
  Garantem que vários componentes se comportem bem juntos. Isso pode envolver diversas classes, bem como teste da integração com outros serviços.

- **Testes de aceitação**
 
  São semelhantes aos testes de integração, mas se concentram nos casos de negócios em vez dos próprios componentes.

- **Testes de interface do usuário**

  Garantem que o aplicativo funcione bem desde a perspectiva do usuário.

  ![CI1](https://wac-cdn.atlassian.com/dam/jcr:af3ed106-66b2-4f9e-a58c-c3370c9fb5aa/TestingTriangle.png?cdnVersion=495)

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#ci---continuous-integration)
***

## 21. Continuous Delivery (CD)

Entrega contínua é uma prática de desenvolvimento de software que utiliza a automação para acelerar o lançamento de novo código.

Ela estabelece um processo pelo qual as alterações feitas por um desenvolvedor em uma aplicação possam ser enviadas para um repositório de código ou um registro de aplicações em container por meio da automação.

A entrega contínua é parte da CI/CD, um método de entrega de software usado com frequência ao automatizar algumas das fases de desenvolvimento de aplicações. 

"CI" refere-se à integração contínua. Com a integração contínua, novas alterações no código de uma aplicação são criadas, testadas e mescladas em um repositório compartilhado. É a solução ideal para evitar conflitos entre ramificações quando muitas aplicações são desenvolvidas ao mesmo tempo.

“CD” pode se referir à implantação contínua ou à entrega contínua, que descrevem formas de automatizar as fases posteriores do pipeline.

![CD1](https://www.redhat.com/cms/managed-files/styles/wysiwyg_full_width/s3/ci-cd-flow-desktop_edited.png?itok=k5bkXL-F)

Um pipeline de CI/CD consiste em uma série de etapas a serem realizadas para a disponibilização de uma nova versão de software. Assim que você implantar o CI/CD, terá estabelecido um pipeline correspondente.

O pipeline de CI/CD inclui monitoramento e automação para melhorar o fluxo de trabalho de desenvolvimento de aplicações, principalmente nos estágios de integração e teste, mas também na entrega e na implantação. 

É possível executar manualmente cada etapa do pipeline de CI/CD, mas o real valor dele está na automação do ciclo de vida da aplicação.

O CI/CD depende da automação para acelerar os processos de desenvolvimento, implementação e testes. A automação ajuda a manter a qualidade e reduz os erros humanos. Ela também aprimora a segurança como parte de uma estratégia DevSecOps.

- [Tabela de Conteúdos](#introdução-à-integração-de-sistemas)
- [Referências](#cd---continuous-delivery)
***

# REFERÊNCIAS

## Integração de Sistemas
- [WSO2]\: https://docs.wso2.com/display/IntegrationPatterns/Enterprise+Integration+Patterns+with+WSO2+ESB
- [Helder Rocha]\: https://www.academia.edu/11784011/Padr%C3%B5es_de_Integra%C3%A7%C3%A3o_de_Sistemas_com_aplica%C3%A7%C3%B5es_em_Java_

## Arquitetura de Microsserviços dirigos a API
- [Github]\: https://github.com/wso2/reference-architecture/blob/master/api-driven-microservice-architecture.md

## Event Driven Architecture (EDA)
- [WSO2]\: https://wso2.com/whitepapers/event-driven-architecture-the-path-to-increased-agility-and-high-expandability/#:~:text=WSO2%20offers%20a%20full%20suite,EDA%20and%20web%20services%20architectures
- [Medium]\: https://medium.com/@marcelomg21/event-driven-architecture-eda-em-uma-arquitetura-de-micro-servi%C3%A7os-1981614cdd45
- [Netreo]\: https://www.netreo.com/blog/sla-metrics-examples/
- [Youtube]\: https://youtu.be/qaSS4Pci8vM
- [Youtube]\: https://youtu.be/rsKUm6WA9TE

## Camada de Mensageria
- [WSO2]\: https://ei.docs.wso2.com/en/7.2.0/micro-integrator/use-cases/integration-use-case/asynchronous-message-overview/
- [Science Direct]\: https://www.sciencedirect.com/topics/computer-science/messaging-layer

## Arquitetura Orientada a Serviços - SOA
- [WSO2]\: https://wso2.com/library/webinars/2015/09/service-oriented-architecture/
- [Red Hat]\: https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-service-oriented-architecture#:~:text=Arquitetura%20orientada%20a%20servi%C3%A7os%20(SOA)%20%C3%A9%20um%20tipo%20de%20design,comunica%C3%A7%C3%A3o%20comum%20em%20uma%20rede
- [IBM]\: https://www.ibm.com/br-pt/cloud/learn/soa

## Simple Object Access Protocol
- [Red Hat]\: https://www.redhat.com/pt-br/topics/integration/whats-the-difference-between-soap-rest

## SOAP Ui
- [Programar]\: https://www.revista-programar.info/artigos/soapui-ferramenta-util-desenvolve-web-services/
- [DevMedia]\: https://www.devmedia.com.br/soapui-testes-de-web-services-rapido-e-descomplicado/37461

## APIs
- [AWS AMAZON]\: https://aws.amazon.com/pt/what-is/api/

## Swagger
- [GR1D]\: https://gr1d.io/2022/04/15/swagger/

## Microsserviços
- [AWS AMAZON]\: https://aws.amazon.com/pt/microservices/
- [WSO2]\: https://wso2.com/whitepapers/microservices-in-practice-key-architectural-concepts-of-an-msa/#02

## Protocolo HTTP
- [Rockcontent]\: https://rockcontent.com/br/blog/http/
- [Hostinger]\: https://www.hostinger.com.br/tutoriais/o-que-e-http-error-e-principais-codigos-http#O_que_e_HTTP_Error
- [Mozzila]\: https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Status

## Protocolo REST
- [Red Hat]\: https://www.redhat.com/pt-br/topics/api/what-is-a-rest-api#:~:text=REST%20n%C3%A3o%20%C3%A9%20um%20protocolo,recurso%20ao%20solicitante%20ou%20endpoint.
- [Rockcontent]\: https://rockcontent.com/br/blog/rest/

## cUrl
- [Rockcontent]\; https://rockcontent.com/br/blog/curl/

## Postman
- [eNotas]\: https://enotas.com.br/blog/postman/
- [Guru99]\: https://www.guru99.com/postman-tutorial.html

## Containers
- [ESR]\: https://esr.rnp.br/administracao-de-sistemas/containers-docker-como-utilizar/
- [Treinaweb]\: https://www.treinaweb.com.br/blog/afinal-o-que-e-um-container

## Docker
- [Treinaweb]\: https://www.treinaweb.com.br/blog/no-final-das-contas-o-que-e-o-docker-e-como-ele-funciona
- [AWS]\: https://aws.amazon.com/pt/docker/

## Docker Compose
- [4Linux]\: https://blog.4linux.com.br/docker-compose-explicado/
- [Imasters]\: https://imasters.com.br/banco-de-dados/docker-compose-o-que-e-para-que-serve-o-que-come
- [Mundo Docker]\: https://www.mundodocker.com.br/docker-compose/
- [Alura]\: https://www.alura.com.br/artigos/compondo-uma-aplicacao-com-o-docker-compose
- [Macoratti]\: https://www.macoratti.net/19/01/intro_docker13.htm

## CI - Continuous Integration
- [Atlassian]\: https://www.atlassian.com/br/continuous-delivery/continuous-integration

## CD - Continuous Delivery
- [Red Hat]\: https://www.redhat.com/pt-br/topics/devops/what-is-continuous-delivery
