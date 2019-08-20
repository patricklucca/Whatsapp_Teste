############################
WAMessenger
############################
Atributos
----------
+------------------------+-----------------------+-------------+
|  name                  | Tipo                  | Obrigatório |
+========================+=======================+=============+
| idConversaWhatsapp     | String                | true        | 
+------------------------+-----------------------+-------------+
| disabled               | Boolean               | false       | 
+------------------------+-----------------------+-------------+
| selfStream             | Boolean               | false       | 
+------------------------+-----------------------+-------------+
| chatContent            | Object                | false       | 
+------------------------+-----------------------+-------------+
| conversaWhatsapp       | ConversaWhatsapp__c   | false       | 
+------------------------+-----------------------+-------------+
| iconUrl                | String                | false       | 
+------------------------+-----------------------+-------------+
| lastVisibleDate        | Date                  | false       | 
+------------------------+-----------------------+-------------+
| acoes                  | AcaoWhatsapp__mdt[]   | false       | 
+------------------------+-----------------------+-------------+
| relacao                | String                | false       | 
+------------------------+-----------------------+-------------+
| relacaoNome            | String                | false       | 
+------------------------+-----------------------+-------------+

Functions
----------
doInit
~~~~~~~~~~
NADA

scriptsLoaded
~~~~~~~~~~
Retorna informações da conversa do whatsapp e é responsável por definir o intervalo de atualização das mensagens

doReload
~~~~~~~~~~
Checa a conexão com o server e recarrega o conteúdo do chat

doSendMessage
~~~~~~~~~~
Apresenta a mensagem no chat

handleReceivedMessage
~~~~~~~~~~
No recebimento de novas mensagens, carrega elas em tela

onChangeChatContent
~~~~~~~~~~
Na mudança de conteúdo do chat desce o scroll da conversa pra baixo

handleClickConversa
~~~~~~~~~~
NADA

onScrollChatContent
~~~~~~~~~~


checkBreakline
~~~~~~~~~~
Pula um parágrafo caso o shift esteja apertado ao enviar a mensagem

verifyToSend
~~~~~~~~~~
Verifica se o shift não está apertado para mandar a mensagem, chamando a function de enviar mensagens

checkInputData
~~~~~~~~~~
Retorna a data de envio da mensagem

onSelectWAAction
~~~~~~~~~~















