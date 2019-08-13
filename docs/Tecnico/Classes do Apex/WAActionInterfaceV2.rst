###################
WAActionInterfaceV2
###################

onClick()
  Método para ser executado ao clicar em algum botão através da classe que a implementam.
Assinatura
  void onClick(ConversaWhatsapp__c pConversaWhatsapp)
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: apex

      public class Exemplo implements WAACtionInterfaceV2
      public void onClick(ConversaWhatsapp__c pConversaWhatsapp) {
        setAgenteResponsavel(pConversaWhatsapp);
      }

isDisabled()
  Método para desabilitar/habilidar um botão através da classe que a implementam.
Assinatura
  Boolean isDisabled(ConversaWhatsapp__c pConversaWhatsapp)
Valor retornado
  Tipo:	Boolean.
Exemplo

   .. code-block:: apex

      public class Exemplo implements WAACtionInterfaceV2
      public Boolean isDisabled(ConversaWhatsapp__c pConversaWhatsapp) {
        return !String.isEmpty(pConversaWhatsapp.AgenteResponsavel__c);
      }


