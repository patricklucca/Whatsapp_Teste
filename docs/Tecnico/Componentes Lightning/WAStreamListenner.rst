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
