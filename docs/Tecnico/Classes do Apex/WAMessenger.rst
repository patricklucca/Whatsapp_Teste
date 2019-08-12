WAMessenger_ctl

conversaWhatsappId

Get e Set da variável pública do tipo String.

Assinatura

public String conversaWhatsappId {get;set;}

Valor retornado

Tipo de retorno do get:		String.
Tipo do retorno do set:		sem retorno.

conversaWa

Get e Set da variável pública do tipo ConversaWhatsapp__c.

Assinatura

public ConversaWhatsapp__c conversaWa {get;set;}

Valor retornado

Tipo de retorno do get:		ConversaWhatsapp__c.
Tipo do retorno do set:		sem retorno.

msg

Get e Set da variável pública do tipo String.

Assinatura

public String msg {get;set;}

Valor retornado

Tipo de retorno do get:		String.
Tipo do retorno do set:		sem retorno.

refreshPeriod

Get e Set da variável pública do tipo Decimal.

Assinatura

public Decimal refreshPeriod {get;set;}

Valor retornado

Tipo de retorno do get:		Decimal.
Tipo do retorno do set:		sem retorno.

WAMessenger_ctl()

Atribui o valor para a váriavel pública refreshPeriod.

Assinatura

public WAMessenger_ctl()

Valor retornado

Sem retorno.

getIconId()

Retorna a URL do ícone do Contato do Whatsapp relacionado a Conversa do Whatsapp atribuída à variável pública conversaWA.

Assinatura

public String getIconId()

Valor retornado

Tipo:	String.

resetData()

Atribui null à variável local conversaWA.

Assinatura

public void resetData()

Valor retornado

Sem retorno.

getConversaWhatsapp()

Retorna a Conversa do Whatsapp do Id igual à variável pública local conversaWhatsappId.

Assinatura

public ConversaWhatsapp__c getConversaWhatsapp()

Valor retornado

Tipo:	ConversaWhatsapp__c.

saveMessage()

Insere uma nova mensagem no servidor, através das variáveis públicas locais msg e conversaWA.

Assinatura

public void saveMessage()

Valor retornado

Sem retorno.

@AuraEnabled
getConversaWa(pConversaWaId)

Retorna a Conversa do Whatsapp do Id igual à variável pública local conversaWhatsappId.

Assinatura

public static ConversaWhatsapp__c getConversaWa(String pConversaWaId)

Valor retornado

Tipo:	ConversaWhatsapp__c.

@RemoteAction
getMensagemWa(pConversaWaId)

Retorna as últimas 1000 Mensagem do Whatsapp relacionado ao Id do parâmetro passado  pConversaWaId.

Assinatura

global static List<MensagemWhatsapp__c> getMensagemWa(String pConversaWaId)

Valor retornado

Tipo:	List<MensagemWhatsapp__c>.


@AuraEnabled
getChatContent(pConversaWaId)

Retorna uma classe ChatContent, enviando as últimas 1000 mensagens da conversa com o Id igual à pConversaWaId como parâmetro.

Assinatura

public static ChatContent getChatContent(String pConversaWaId)

Valor retornado

Tipo:	ChatContent.


@AuraEnabled
doSaveMessage(pConversaWhatsapp, pCorpo)

Insere uma nova mensagem no servidor, com os parâmetros enviados pCorpo e pConversaWhatsapp.

Assinatura

public static void doSaveMessage(ConversaWhatsapp__c pConversaWhatsapp, String pCorpo)

Valor retornado

Sem retorno.

@AuraEnabled
getIconUrl(pContatoId)

Retorna a URL do icone do Contato do Whatsapp com o id pContatoId não tenha icone e retorna uma String vazia caso contrário.

Assinatura

public static String getIconUrl(String pContatoId)

Valor retornado

Tipo:	String.



getHostUrl()

Retorna a URL da organização.

Assinatura

public static String getHostUrl()

Valor retornado

Tipo:	String.

@AuraEnabled
getWAActions(pConversaWhatsapp)

Retorna uma lista AcaoMessenger com os tipos de metadados de Ação do Whatsapp do tipo Messenger com a pConversaWhatsapp.

Assinatura

public static List<AcaoMessenger> getWAActions(ConversaWhatsapp__c pConversaWhatsapp)

Valor retornado

Tipo:	List<AcaoMessenger>.

@AuraEnabled
doExecuteAction(pAcaoWhatsapp, pConversaWhatsapp)

Executa o método doExecuteWaAction da classe WAActionHandler.

Assinatura

public static void doExecuteAction(AcaoWhatsapp__mdt pAcaoWhatsapp, ConversaWhatsapp__c pConversaWhatsapp)

Valor retornado

Sem retorno.


