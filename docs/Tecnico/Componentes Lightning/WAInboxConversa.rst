################
WAInboxConversa
################
Atributos
----------
+------------------------+-----------------------+-------------+
|  name                  | Tipo                  | Obrigatório |
+========================+=======================+=============+
| conversa               | ConversaWhatsapp__c   | false       | 
+------------------------+-----------------------+-------------+
| iconUrl                | String                | false       | 
+------------------------+-----------------------+-------------+
| alertChat              | Boolean               | false       | 
+------------------------+-----------------------+-------------+
Exemplo
---------

.. code-block:: apex

   <lightning:layoutItem class="flex">
       <ui:outputText value="{!v.conversa.whats__ContatoWhatsapp__r.Name}" class="conversa-title ellipsis"/>
   </lightning:layoutItem>

Functions
----------
doInit
~~~~~~~~~~
Carrega o ícone com a imagem do contato

notifyParent
~~~~~~~~~~
Recebendo mensagens setta a variável conversa
