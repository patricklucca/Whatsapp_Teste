#####################
WACoreExecutionBefore
#####################

onInicioConversa()
~~~~~~~~~~~~~~~~~~~~
  Implementação da WAActionInterface, não está sendo utilizado.
Assinatura
  public void onInicioConversa(List<ConversaWhatsapp__c> pListConversaWhatsapp)
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, Status__c FROM ConversaWhatsapp__c]);
      Map<Id, MensagemWhatsapp__c> mapResultMensagem = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name, Corpo__c, Destino__c, Direcao__c, NomeOrigem__c, Origem__c, Status__c FROM MensagemWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      List<MensagemWhatsapp__c> lstChangedMensagem = mapResultMensagem.values().deepClone(true, true, true);
      lstChangedMensagem[0].ConversaWhatsapp__c = null;
      lstChangedMensagem[0].Destino__c = '22222222';
      lstChangedMensagem[0].Origem__c = '22222222';
      new WACoreExecutionBefore().onInicioConversa(lstChanged);

onFimConversa()
~~~~~~~~~~~~~~~~~~~~
  Implementação da WAActionInterface, não está sendo utilizado.
Assinatura
  public void onFimConversa(List<ConversaWhatsapp__c> pListConversaWhatsapp)
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, Status__c FROM ConversaWhatsapp__c]);
      Map<Id, MensagemWhatsapp__c> mapResultMensagem = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name, Corpo__c, Destino__c, Direcao__c, NomeOrigem__c, Origem__c, Status__c FROM MensagemWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      List<MensagemWhatsapp__c> lstChangedMensagem = mapResultMensagem.values().deepClone(true, true, true);
      lstChangedMensagem[0].ConversaWhatsapp__c = null;
      lstChangedMensagem[0].Destino__c = '22222222';
      lstChangedMensagem[0].Origem__c = '22222222';
      new WACoreExecutionBefore().onFimConversa(lstChanged);
  
onEntradaMensagem()
~~~~~~~~~~~~~~~~~~~~
  Implementação da WAActionInterface, executa outros métodos privados da classe.
Assinatura
  public void onEntradaMensagem(List<MensagemWhatsapp__c> pListMensagemWhatsapp)
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: apex

      Map<Id, ConversaWhatsapp__c> mapResult = new Map<Id, ConversaWhatsapp__c>([SELECT Id, Name, ContatoWhatsapp__r.Name, ContatoWhatsapp__r.Numero__c, Status__c FROM ConversaWhatsapp__c]);
      Map<Id, MensagemWhatsapp__c> mapResultMensagem = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name, Corpo__c, Destino__c, Direcao__c, NomeOrigem__c, Origem__c, Status__c FROM MensagemWhatsapp__c]);
      List<ConversaWhatsapp__c> lstChanged = mapResult.values().deepClone(true, true, true);
      List<MensagemWhatsapp__c> lstChangedMensagem = mapResultMensagem.values().deepClone(true, true, true);
      lstChangedMensagem[0].ConversaWhatsapp__c = null;
      lstChangedMensagem[0].Destino__c = '22222222';
      lstChangedMensagem[0].Origem__c = '22222222';
      new WACoreExecutionBefore().onEntradaMensagem(lstChangedMensagem);
   
