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

## 1. O que é?

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
***

## 4. Event-Driven Architecture (EDA)

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
***

## 6. Camada de Mensageria

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
***

## 7. Arquitetura Orientada a Serviço (SOA)

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
***

## 8. Simple Object Access Protocol (SOAP)

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
***

## 9. SoapUI

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
***
