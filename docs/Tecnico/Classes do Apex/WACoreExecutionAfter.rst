#################
WACoreExecutionAfter
#################

onInicioConversa()
---------------
Assinatura
    public void onInicioConversa(List<ConversaWhatsapp__c> pListConversaWhatsapp) 
Retorno
    Implementa WAActionInterface
Exemplo

   .. code-block:: apex

        Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, Status__c FROM ConversaWhatsapp__c]);
        Map<Id, MensagemWhatsapp__c> mapResultMensagem = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name, ConversaWhatsapp__c, Corpo__c, Destino__c, Direcao__c, Origem__c, Status__c FROM MensagemWhatsapp__c]);
        List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
        List<MensagemWhatsapp__c> lstChangedMensagem = mapResultMensagem.values().deepClone(true, true, true);
        new WACoreExecutionAfter().onInicioConversa(lstChanged);      
      
      
onFimConversa()
---------------
Assinatura
    public void onFimConversa(List<ConversaWhatsapp__c> pListConversaWhatsapp)  
Retorno
    Implementa WAActionInterface
Exemplo

   .. code-block:: apex

        Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, Status__c FROM ConversaWhatsapp__c]);
        Map<Id, MensagemWhatsapp__c> mapResultMensagem = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name, ConversaWhatsapp__c, Corpo__c, Destino__c, Direcao__c, Origem__c, Status__c FROM MensagemWhatsapp__c]);
        List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
        List<MensagemWhatsapp__c> lstChangedMensagem = mapResultMensagem.values().deepClone(true, true, true);
        new WACoreExecutionAfter().onFimConversa(lstChanged);
        
onEntradaMensagem()
---------------
Assinatura
    public void onEntradaMensagem(List<MensagemWhatsapp__c> pListMensagemWhatsapp)  
Retorno
    Implementa WAActionInterface
Exemplo

   .. code-block:: apex

        Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, Status__c FROM ConversaWhatsapp__c]);
        Map<Id, MensagemWhatsapp__c> mapResultMensagem = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name, ConversaWhatsapp__c, Corpo__c, Destino__c, Direcao__c, Origem__c, Status__c FROM MensagemWhatsapp__c]);
        List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
        List<MensagemWhatsapp__c> lstChangedMensagem = mapResultMensagem.values().deepClone(true, true, true);
        new WACoreExecutionAfter().onEntradaMensagem(lstChanged);
      
