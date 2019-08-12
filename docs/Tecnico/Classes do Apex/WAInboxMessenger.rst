#################
WAInboxMessenger
#################

getRefreshValue()
---------------
Assinatura
    public static Decimal getRefreshValue() 
Retorno
    Retorna a variável decimal result, que é atribuida com 60000 segundos ou com os dados do metadado PeriodicidadeAtualizacoes__mdt

getConversaWhatsapp()
---------------
Assinatura
    public static List<ConversaWhatsapp__c> getConversaWhatsapp(String pSoqlFilter) 
Retorno
    Retorna uma query feita através do registro ConversaWhatsapp

setSeenConversa()
---------------
Assinatura
    public static void setSeenConversa(String pConversaWhatsappId) 
Retorno
    Atualiza o campo Status__c das mensagens para "lido"
