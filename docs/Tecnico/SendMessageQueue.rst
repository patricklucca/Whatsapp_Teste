###################
SendMessageQueue
###################

SendMessageQueue() 
-----------------------
Cria a fila de mensagens

Retorno
    Cria a variáevl setMensagemId e atribui o valor de pSetMensagemId
Assinatura
    public SendMessageQueue(Set<Id> pSetMensagemId)
Exemplo
    .. code-block:: apex
    Map<Id, MensagemWhatsapp__c> exemploresult = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name FROM MensagemWhatsapp__c]);
    SendWhatsappMessage.SendMessageQueue(exemploresult.keySet());
    
add() 
-----------------------
Método responsável pela inserção de mensagens a fila

Retorno
    Adiciona valores à variável setMensagemId
Assinatura
    public void add(Set<Id> pSetMensagemId) 
Exemplo
    .. code-block:: apex
    Map<Id, MensagemWhatsapp__c> exemploresult = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name FROM MensagemWhatsapp__c]);
    SendWhatsappMessage.add(exemploresult.keySet());
    
execute()  
-----------------------
Envia as mensagens enfileiradas
    
Retorno
    Setta o endpoint
Assinatura
    public void execute(QueueableContext context)
       
public class RemoteMessageEntity
-----------------------
Classe que define String id, String corpo, String origem, String destino e chama RemoteMessageEntity

Retorno
Assinatura
    public class RemoteMessageEntity
Exemplo
       .. code-block:: apex
       Map<Id, MensagemWhatsapp__c> exemploresult = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name FROM MensagemWhatsapp__c]);
       SendWhatsappMessage.doEnviarMensagens(exemploresult.keySet());
       
public RemoteMessageEntity() 
-----------------------
Define valores para String id, String corpo, String origem, String destino.

Retorno
    Variáveis String id, corpo, origem e destino
Assinatura
    public RemoteMessageEntity(MensagemWhatsapp__c pMensagemWa) 
Exemplo
       .. code-block:: apex
       Map<Id, MensagemWhatsapp__c> exemploresult = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name FROM MensagemWhatsapp__c]);
       SendWhatsappMessage.doEnviarMensagens(exemploresult.keySet());
             

 

