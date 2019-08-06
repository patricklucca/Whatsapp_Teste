#################
SendWhatsappMessenger
#################

A classe SendWhatsappMessage é responsável pelo envio das mensagens da conversa, registro de número, atualização do mesmo e sua autentificação. 

doEnviarMensagem
-----------------------
NÃO ESTÁ SENDO UTILIZADO// As mensagens são montadas através do método doEnviarMensagem, que recebem como parâmetro cinco String Origem, Destino, Chave, ContentMedia e ContentSize
Trata-se de um método público que não tem retorno onde através dele é instituido o content, Timeout, Endpoint, Header,Method e Body, este metodo também recebe o StatusCode do servidor.
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doEnviarMensagem('origem', 'destino', 'contentmedia', 'contentsize');``
   
doEnviarMensagem
-----------------------
Responsável pelo enfileiramento das mensagem a serem madadas com origem Empresa > Cliente *ver campo Direcao__c nos `Objetos`_
Recebe como parâmetro setIdToIntegrate que é estabelecido através do método doIntegrarMensagens da classe `WACoreExecutionAfter`_ e também é um método estático sem retorno.
O método manipula a variável singleQueue, criada dentro da classe, usando-o com um comparativo:

.. code-block:: apex

       if (singleQueue == null) {
       singleQueue = new SendMessageQueue(pSetMensagemId);
       singleQueueId = System.enqueueJob(singleQueue);
            
e limpando-o caso não seja null:

.. code-block:: apex

        else {
        System.abortJob(singleQueueId);
        singleQueue.add(pSetMensagemId);
        singleQueueId = System.enqueueJob(singleQueue);
        
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doEnviarMensagens(mapa_id_mensagem.keySet());``
   
.. _Objetos : https://whatsapp-teste.readthedocs.io/en/latest/Tecnico/Objetos.html?highlight=objeto
.. _WACoreExecutionAfter : 

doEnviarContentMedia
-----------------------
NÃO ESTÁ SENDO UTILIZADO// As mensagens com imagens seriam montadas através do  método doEnviarContentMedia que é similar ao doEnviarMensagem, recebendo como parâmetro também cinco String Origem, Destino, Chave, ContentMedia e ContentSize
Diferencia pela utilização da chave na criação do content e definição do endpoint.
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doEnviarContentMedia('origem', 'destino', 'chave', 'contentmedia', 'contentsize');``
   
doRegistrarNumero
-----------------------
NÃO ESTÁ SENDO UTILIZADO// Registra o número que envia mensagens através do método doRegistrarNumero que é similar ao doEnviarMensagem na definição do content, recebendo como parâmetro quatro Strings DDI, número, operadora e método de envio.
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doRegistrarNumero('', '', '','');``
      
   
doAutenticarNumero
-----------------------
NÃO ESTÁ SENDO UTILIZADO// Registra o número que envia mensagens através do método doAutenticarNumero que é similar ao doEnviarMensagem na definição do content, recebendo como parâmetro quatro Strings DDI, número, operadora e método de envio.
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doAutenticarNumero('', '', '');``
             
doRegistrarNovoNumero
-----------------------
Método responsável pela chamada do método subsequente, a ``registerNewNumber``, pois a doRegistrarNovoNumero é publica, enquanto a ewgisternewnumber é privada. Este método recebe seis Strings e um Boolean, sendo eles respoectivamente as Strings oldNumero, numero, operadora, callbackLogin, callbackPassword, msgIncompatibilidade e o Boolean isAtivo
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doRegistrarNovoNumero('', '', '', '', '', '', true);``
                  
registerNewNumber
-----------------------
Responsável pela criação de uma String nomeada content que possui as informações de número, novo número e todas as strings que ele recebe. Esta método recebe seis Strings e um Boolean, sendo eles respoectivamente as Strings oldNumero, numero, operadora, callbackLogin, callbackPassword, msgIncompatibilidade e o Boolean isAtivo
Por ser um método privado não pode ser chamado externamente.
Esta método é indiretamente chamado pela método syncParametro da classe `ParametroWhatsappHandler`_ através de uma verificação:
    ``if (afterInsert || (afterUpdate && hasChangedServerParam(mapOldRecord.get(param.Id), param)))``
Atualizando o número do ParametroWhatsapp__c

.. _ParametroWhatsappHandler : 
     
doVerificaNovoNumero
-----------------------
NÃO ESTÁ SENDO UTILIZADO// Trata-se de um método void que não recebe nenhum parâmetro e não é chamado por nenhum outro método em nenhuma outra classe, montando o content com informações constantes. 
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doRegistrarNovoNumero();``

doRegitrarNovoGrupo
-----------------------
NÃO ESTÁ SENDO UTILIZADO// Similar ao método doVerificarNovoNumero, trata-se de um método void que não recebe nenhum parâmetro e não é chamado por nenhum outro método em nenhuma outra classe, montando o content com informações constantes. 
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doRegistrarNovoNumero();``
             
getQr
-----------------------
Responsável pela criação de uma String nomeada content que possui as informações de número e clienteID. Esta método recebe apenas uma String com o número do cliente
Esta método é chamado pela método loadQr da classe `WAQrView`_ para montar a requisição ao servidor através da chamada:
    ``String response = SendWhatsappMessage.getQr(param.Celular__c);``



.. _WAQrView : 
             
requestQr
-----------------------
Responsável pela criação de uma String nomeada content que possui as informações de número e clienteID, montando a requisição ao servidor. Esta método recebe apenas uma String com o número do cliente
Esta método é chamado por um método homonimo (requestQr) da classe `WAQrRequest`_ para montar a requisição ao servidor através da chamada:
    ``String response = SendWhatsappMessage.getQr(param.Celular__c);``



.. _WAQrRequest : 
             
getMensagemWaJson
-----------------------
Responsável pela criação pela criação de um arquivo Json com a mensagem. Utilizado dentro da própria classe pelo método void execute recebendo como parâmetro 



.. _WAQrRequest : 
 

