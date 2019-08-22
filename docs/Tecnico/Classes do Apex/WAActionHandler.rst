###############
WAActionHandler
###############

doExecuteWaAction()
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  Executa outros métodos privados da classe, os métodos executados depende do valor do atributo Assincrono__c do parâmetro pAcaowhatsapp.
Assinatura
  public static void doExecuteWaAction()
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: apex
   
      WAActionHandler.doExecuteWaAction(new AcaoWhatsapp__mdt(
          Assincrono__c = true,
          ClasseApex__c = 'WACoreExecutionAfter',
          TipoAcao__c = 'Entrada de Mensagem'
      ), lstChangedMensagem);      
      
getWaAction()
~~~~~~~~~~~~~~
  Retorna a instância de uma classe apex WAActionInterface.
Assinatura
  public static WAActionInterface getWaAction(AcaoWhatsapp__mdt pAcaoWhatsapp)
Valor retornado
  Tipo: 	WAActionInterface.
Exemplo

   .. code-block:: apex

      WAActionHandler.getWaAction(new AcaoWhatsapp__mdt(
            Assincrono__c = true,
            ClasseApex__c = 'WACoreExecutionAfter',
            TipoAcao__c = 'Entrada de Mensagem);
