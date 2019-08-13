#######################
ConversaWhatsappHandler
#######################

executeTrigger()
  Atribui os parâmetro passados à variáveis da classe e executa outros métodos da mesma.
Assinatura
  public static void executeTrigger(Map<Id, MensagemWhatsapp__c> pMapOldRecord, List<MensagemWhatsapp__c> pListRecord, Boolean pBeforeInsert, Boolean pBeforeUpdate, Boolean pAfterInsert, Boolean pAfterUpdate) 
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, Status__c FROM ConversaWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      lstChanged[0].Status__c = 'Fechado';
      ConversaWhatsappHandler.executeTrigger(mapResult, lstChanged, true, true, true, true); 

