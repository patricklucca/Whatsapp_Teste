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

    ``SendWhatsappMessage.doAutenticarNumero('', '', '','');``
      
   
doAutenticarNumero
-----------------------
NÃO ESTÁ SENDO UTILIZADO// Registra o número que envia mensagens através do método doAutenticarNumero que é similar ao doEnviarMensagem na definição do content, recebendo como parâmetro quatro Strings DDI, número, operadora e método de envio.
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doAutenticarNumero('', '', '','');``
        
doRegistrarNumero
-----------------------
NÃO ESTÁ SENDO UTILIZADO// Registra o número que envia mensagens através do método doRegistrarNumero que é similar ao doEnviarMensagem na definição do content, recebendo como parâmetro quatro Strings DDI, número, operadora e método de envio.
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doAutenticarNumero('', '', '','');``
     

