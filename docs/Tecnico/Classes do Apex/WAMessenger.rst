################
WAMessenger
################

conversaWhatsappId
  Get e Set da variável pública do tipo String.
Assinatura
  public String conversaWhatsappId {get;set;}
Valor retornado
  Tipo de retorno do get:		String.
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
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, ParametroWhatsapp__r.Celular__c, ParametroWhatsapp__r.Name, Status__c FROM ConversaWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      WAMessenger_ctl mCtl = new WAMessenger_ctl();
      mCtl.conversaWhatsappId = lstChanged[0].Id;
      mCtl.getIconId();

resetData()
  Atribui null à variável local conversaWA.
Assinatura
  public void resetData()
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, ParametroWhatsapp__r.Celular__c, ParametroWhatsapp__r.Name, Status__c FROM ConversaWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      WAMessenger_ctl mCtl = new WAMessenger_ctl();
      mCtl.conversaWhatsappId = lstChanged[0].Id;
      mCtl.getIconId();
      mCtl.resetData();
      
getConversaWhatsapp()
  Retorna a Conversa do Whatsapp do Id igual à variável pública local conversaWhatsappId.
Assinatura
  public ConversaWhatsapp__c getConversaWhatsapp()
Valor retornado
  Tipo:	ConversaWhatsapp__c.
Exemplo

   .. code-block:: apex

      ConversaWhatsapp__c conversaWa = getConversaWhatsapp(parametroWa.Id, contatoWa.Id);
      insert conversaWa>
      
      
saveMessage()
  Insere uma nova mensagem no servidor, através das variáveis públicas locais msg e conversaWA.
Assinatura
  public void saveMessage()
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, ParametroWhatsapp__r.Celular__c, ParametroWhatsapp__r.Name, Status__c FROM ConversaWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      WAMessenger_ctl mCtl = new WAMessenger_ctl();
      mCtl.conversaWhatsappId = lstChanged[0].Id;
      mCtl.getIconId();
      mCtl.msg = 'Exemplo';
      mCtl.saveMessage();
      
@AuraEnabled
getConversaWa()
  Retorna a Conversa do Whatsapp do Id igual à variável pública local conversaWhatsappId.
Assinatura
  public static ConversaWhatsapp__c getConversaWa(String pConversaWaId)
Valor retornado
  Tipo:	ConversaWhatsapp__c.
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, ParametroWhatsapp__r.Celular__c, ParametroWhatsapp__r.Name, Status__c FROM ConversaWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      WAMessenger_ctl mCtl = new WAMessenger_ctl();
      mCtl.conversaWhatsappId = lstChanged[0].Id;
      mCtl.getIconId();
      mCtl.msg = 'Exemplo';
      mCtl.saveMessage();
      WAMessenger_ctl.getConversaWa(lstChanged[0].Id);
      
@RemoteAction
getMensagemWa()
  Retorna as últimas 1000 Mensagem do Whatsapp relacionado ao Id do parâmetro passado  pConversaWaId.
Assinatura
  global static List<MensagemWhatsapp__c> getMensagemWa(String pConversaWaId)
Valor retornado
  Tipo:	List<MensagemWhatsapp__c>.
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, ParametroWhatsapp__r.Celular__c, ParametroWhatsapp__r.Name, Status__c FROM ConversaWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      WAMessenger_ctl mCtl = new WAMessenger_ctl();
      mCtl.conversaWhatsappId = lstChanged[0].Id;
      mCtl.getIconId();
      mCtl.msg = 'Exemplo';
      mCtl.saveMessage();
      WAMessenger_ctl.getMensagemWa(lstChanged[0].Id);
      

@AuraEnabled
getChatContent()
  Retorna uma classe ChatContent, enviando as últimas 1000 mensagens da conversa com o Id igual à pConversaWaId como parâmetro.
Assinatura
  public static ChatContent getChatContent(String pConversaWaId)
Valor retornado
  Tipo:	ChatContent.
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, ParametroWhatsapp__r.Celular__c, ParametroWhatsapp__r.Name, Status__c FROM ConversaWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      WAMessenger_ctl mCtl = new WAMessenger_ctl();
      mCtl.conversaWhatsappId = lstChanged[0].Id;
      mCtl.getIconId();
      mCtl.msg = 'Exemplo';
      mCtl.saveMessage();
      WAMessenger_ctl.getChatContent(lstChanged[0].Id);

@AuraEnabled
doSaveMessage()
  Insere uma nova mensagem no servidor, com os parâmetros enviados pCorpo e pConversaWhatsapp.
Assinatura
  public static void doSaveMessage(ConversaWhatsapp__c pConversaWhatsapp, String pCorpo)
Valor retornado
  Sem retorno.


@AuraEnabled
getIconUrl()
  Retorna a URL do icone do Contato do Whatsapp com o id pContatoId não tenha icone e retorna uma String vazia caso contrário.
Assinatura
  public static String getIconUrl(String pContatoId)
Valor retornado
  Tipo:	String.
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, ParametroWhatsapp__r.Celular__c, ParametroWhatsapp__r.Name, Status__c FROM ConversaWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      WAMessenger_ctl mCtl = new WAMessenger_ctl();
      mCtl.conversaWhatsappId = lstChanged[0].Id;
      mCtl.getIconId();
      mCtl.msg = 'Exemplo';
      mCtl.saveMessage();
      WAMessenger_ctl.getIconUrl(lstChanged[0].ContatoWhatsapp__c);


getHostUrl()
  Retorna a URL da organização.
Assinatura
  public static String getHostUrl()
Valor retornado
  Tipo:	String.
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, ParametroWhatsapp__r.Celular__c, ParametroWhatsapp__r.Name, Status__c FROM ConversaWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      WAMessenger_ctl mCtl = new WAMessenger_ctl();
      mCtl.conversaWhatsappId = lstChanged[0].Id;
      mCtl.getIconId();
      mCtl.msg = 'Exemplo';
      mCtl.saveMessage();
      WAMessenger_ctl.getHostUrl();

@AuraEnabled
getWAActions()
  Retorna uma lista AcaoMessenger com os tipos de metadados de Ação do Whatsapp do tipo Messenger com a pConversaWhatsapp.
Assinatura
  public static List<AcaoMessenger> getWAActions(ConversaWhatsapp__c pConversaWhatsapp)
Valor retornado
  Tipo:	List<AcaoMessenger>.
Exemplo

   .. code-block:: apex

      WAMessenger.getWAActions(a021U000007pg2FQAQ)
      
@AuraEnabled
doExecuteAction()
  Executa o método doExecuteWaAction da classe WAActionHandler.
Assinatura
  public static void doExecuteAction(AcaoWhatsapp__mdt pAcaoWhatsapp, ConversaWhatsapp__c pConversaWhatsapp)
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: apex

      WAMessenger.doExecuteAction(new AcaoWhatsapp__mdt[]{
      new AcaoWhatsapp__mdt(TipoAcao__c = 'Entrada de Mensagem', ClasseApex__c = 'WACoreExecutionAfter', Assincrono__c = true)
      }, 'a021U000007pg2FQAQ');
      
      
      
      
      

