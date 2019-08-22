############################
WAInboxConversaEvent
############################
Atributos
----------
+------------------------+-----------------------+-------------+
|  name                  | Tipo                  | Obrigatório |
+========================+=======================+=============+
| conversa               | ConversaWhatsapp__c   | false       | 
+------------------------+-----------------------+-------------+
Trata-se de um event type component

Exemplo
--------

  .. code-block:: apex
     <aura:registerEvent name="onClick" type="c:WAInboxConversaEvent"/>
