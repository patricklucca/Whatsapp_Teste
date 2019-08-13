########################
MensagemWhatsappHandler
########################

executeTrigger(pMapOldRecord, pListRecord, pBeforeInsert, pBeforeUpdate, pAfterInsert, pAfterUpdate)

Executa uma determinada Ação do Wahtsapp do tipo Entrada de Mensagem, antes ou depois da inserção ou update de uma Mensagem do Whatsapp.

Assinatura
  public static void executeTrigger(Map<Id, MensagemWhatsapp__c> pMapOldRecord, List<MensagemWhatsapp__c> pListRecord, Boolean pBeforeInsert, Boolean pBeforeUpdate, Boolean pAfterInsert, Boolean pAfterUpdate) 
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: apex

      Map<Id, MensagemWhatsapp__c> mapResult = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name, Corpo__c, Direcao__c, Destino__c, Origem__c, Status__c FROM MensagemWhatsapp__c]);
      List<MensagemWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      
      ``Antes da insercao``
      MensagemWhatsappHandler.executeTrigger(mapResult, lstChanged, true, true, false, false);
      
      ``Depois da insercao``
      MensagemWhatsappHandler.executeTrigger(mapResult, lstChanged, false, false, true, true);
