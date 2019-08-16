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

Functions
----------
doInit
~~~~~~~~~~
Carrega o ícone com a imagem do contato

notifyParent
~~~~~~~~~~
Recebendo mensagens setta a variável conversa
