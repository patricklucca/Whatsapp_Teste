#################
WACoreExecuteAfter
#################

onInicioConversa()
---------------
Assinatura
    public void onInicioConversa(List<ConversaWhatsapp__c> pListConversaWhatsapp) 
Retorno
    Implementa WAActionInterface
   
onFimConversa()
---------------
Assinatura
    public void onFimConversa(List<ConversaWhatsapp__c> pListConversaWhatsapp)  
Retorno
    Implementa WAActionInterface
      
onEntradaMensagem()
---------------
Assinatura
    public void onEntradaMensagem(List<MensagemWhatsapp__c> pListMensagemWhatsapp)  
Retorno
    Implementa WAActionInterface
   
onEntradaMensagem()
---------------
Assinatura
    public void onFimConversa(List<ConversaWhatsapp__c> pListConversaWhatsapp)  
Retorno
    Implementa WAActionInterface;
    Executa os métodos doIntegrarMensagens passando seu parâmetro
    Executa doDispararEventos passando seu parâmetro
   
