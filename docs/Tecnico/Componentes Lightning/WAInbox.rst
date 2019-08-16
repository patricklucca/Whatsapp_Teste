############################
WAInbox
############################
Atributos
------------
+------------------------+-----------------------+-------------+
|  name                  | Tipo                  | Obrigatório |
+========================+=======================+=============+
| Status                 | String[]              | false       | 
+------------------------+-----------------------+-------------+
| chatStatus             | String[]              | false       | 
+------------------------+-----------------------+-------------+
| conversas              | ConversaWhatsapp__c[] | false       | 
+------------------------+-----------------------+-------------+
| idTabConversa          | String                | false       | 
+------------------------+-----------------------+-------------+
| acoes                  | AcaoWhatsapp__mdt[]   | false       | 
+------------------------+-----------------------+-------------+
| usuario                | User                  | false       | 
+------------------------+-----------------------+-------------+
| numerosAgente          | String                | false       | 
+------------------------+-----------------------+-------------+
| sessionId              | String                | false       | 
+------------------------+-----------------------+-------------+
| dataHoraDisponibilidade| DateTime              | false       | 
+------------------------+-----------------------+-------------+
| statusDisponibilidade  | String                | false       | 
+------------------------+-----------------------+-------------+
| timerId                | String                | false       | 
+------------------------+-----------------------+-------------+
| timer                  | String                | false       | 
+------------------------+-----------------------+-------------+
| temAgente              | Boolean               | false       | 
+------------------------+-----------------------+-------------+
| countNotificacao       | Integer               | false       | 
+------------------------+-----------------------+-------------+
| labelUtilityBar        | Integer               | false       | 
+------------------------+-----------------------+-------------+
| isHighlighted          | Boolean               | false       | 
+------------------------+-----------------------+-------------+

Function
----------
onChangeUserStatus
~~~~~~~~
Não está em uso

doInit
~~~~~~~~
Estabelece a conexão com o host

scriptsLoaded
~~~~~~~~
Inicia uma série de ações do helper, como carregar o usuário, mostrar as conversas vistas

onSelectWAAction
~~~~~~~~
executa o método doExecuteAction

onSelectConversa
~~~~~~~~
Retorna mensagens conversa e organiza-as

handleReceivedMessage
~~~~~~~~
Recebe um JSON com as mensagens enviadas para a conversa

handleClickConversa
~~~~~~~~
Atribui valores a variável listConversa e aciona outras functions "loadActions" e "setSeenSelectedConversa"
