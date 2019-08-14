#################
WAInboxUser
#################

doExecuteAction()
---------------
Assinatura
    public static void doExecuteAction(AcaoWhatsapp__mdt pAcaoWhatsapp, ConversaWhatsapp__c pConversaWhatsapp)
Retorno
    Executa o método doExecuteWaAction 
      WAActionHandler.doExecuteWaAction(pAcaoWhatsapp, pConversaWhatsapp);
Exemplo

   .. code-block:: apex

      WAInboxUser.doExecuteAction(doExecuteAction(new AcaoWhatsapp__mdt[]{
      new AcaoWhatsapp__mdt(TipoAcao__c = 'Entrada de Mensagem', ClasseApex__c = 'WACoreExecutionAfter', Assincrono__c = true)
      }, 'a021U000007pg2FQAQ');
      
getCurrentUser()
---------------
Assinatura
    public static User getCurrentUser()
Retorno
    Retorna a variável result, que é uma lista das informações do usuário
Exemplo

   .. code-block:: apex

      WAInboxUser_ctl.getCurrentUser();
      
getWAActions()
---------------
Assinatura
    public static List<AcaoInbox> getWAActions(ConversaWhatsapp__c pConversaWhatsapp)
Retorno
    Retorna a variável result, que é uma lista com as informações de AcaoWhatsapp__mdt
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, AgenteResponsavel__c, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, ParametroWhatsapp__r.Celular__c, ParametroWhatsapp__r.Name, Status__c FROM ConversaWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      WAInboxUser_ctl.getWAActions(lstChanged[0]);


      
      
      
      
      
      
      
      
