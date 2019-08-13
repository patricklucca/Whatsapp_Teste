########################
ParametroWhatsappHandler
########################

executeTrigger()
  Atribui os parâmetro passados à variáveis da classe e executa outros métodos da mesma.
Assinatura
  public static void executeTrigger(Map<Id, MensagemWhatsapp__c> pMapOldRecord, List<MensagemWhatsapp__c> pListRecord, Boolean pBeforeInsert, Boolean pBeforeUpdate, Boolean pAfterInsert, Boolean pAfterUpdate) 
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: apex

      Map<Id, MensagemWhatsapp__c> mapResult = new Map<Id, ParametroWhatsapp__c>([SELECT Id, Name, whats__Ativo__c, whats__Celular__c, whats__Conectado__c, whats__RespostaIntegracao__c, whats__Status__c FROM ParametroWhatsapp__c]);
      List<MensagemWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      
      ``Antes da insercao``
      MensagemWhatsappHandler.executeTrigger(mapResult, lstChanged, true, true, false, false);
      
      ``Depois da insercao``
      MensagemWhatsappHandler.executeTrigger(mapResult, lstChanged, false, false, true, true);
