############################
WAStreamListenner
############################
Atributos
----------
+------------------------+-----------------------+-------------+
|  name                  | Tipo                  | Obrigatório |
+========================+=======================+=============+
| channels               | String[]              | false       | 
+------------------------+-----------------------+-------------+
| subscription           | Map                   | false       | 
+------------------------+-----------------------+-------------+
Exemplo
---------

.. code-block:: apex

   <c:WAStreamListenner channels="['/event/whats__WhatsappInbox__e']" />
                              
Functions
----------

doInit
~~~~~~~~~~
Se inscreve no canal do servidor para receber as mensagens 

onClear
~~~~~~~~~~
Limpa as notificações no console

onToggleMute
~~~~~~~~~~
Silencia as mensagens de desinscrição e reinscrição em canais
