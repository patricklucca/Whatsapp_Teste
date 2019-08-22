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
 Define se o scroll aparecerá ou não e carrega os dados da conversa

doReload
~~~~~~~~~~
 Recarrega o conteúdo do chat

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
 NADA

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
 Executa uma ação correspondente ao metadado selecionado ou abre o modal caso utilize um componente







