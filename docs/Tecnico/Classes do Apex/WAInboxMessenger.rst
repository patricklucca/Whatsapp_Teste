#################
WAInboxMessenger
#################

getRefreshValue()
---------------
Assinatura
    public static Decimal getRefreshValue() 
Retorno
    Retorna a variável decimal result, que é atribuida com 60000 segundos ou com os dados do metadado PeriodicidadeAtualizacoes__mdt
Exemplo

   .. code-block:: apex

      WAInboxMessenger_ctl.getRefreshValue();

getConversaWhatsapp()
---------------
Assinatura
    public static List<ConversaWhatsapp__c> getConversaWhatsapp(String pSoqlFilter) 
Retorno
    Retorna uma query feita através do registro ConversaWhatsapp
Exemplo

   .. code-block:: apex

      WAInboxMessenger_ctl.getConversaWhatsapp('');

setSeenConversa()
---------------
Assinatura
    public static void setSeenConversa(String pConversaWhatsappId) 
Retorno
    Atualiza o campo Status__c das mensagens para "lido"
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, AgenteResponsavel__c, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, ParametroWhatsapp__r.Celular__c, ParametroWhatsapp__r.Name, Status__c FROM ConversaWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      WAInboxMessenger_ctl.setSeenConversa(lstChanged[0].Id);
      
      
