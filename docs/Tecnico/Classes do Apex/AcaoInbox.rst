##########      
AcaoInbox
##########
Inner Class da classe WAInboxUser_ctl
Assinatura
    public class AcaoInbox
Expecificação
    Possui as variáveis AcaoWhatsapp__mdt e isDisabled e o método AcaoInbox
      
AcaoWhatsapp__mdt
---------------
Assinatura
    public AcaoWhatsapp__mdt action;
Acao
    Cria uma variável tipo metadado AcaoWhatsapp__mdt
      
isDisabled
---------------
Assinatura
    public Boolean isDisabled;
Acao
    Cria uma variável tipo booleano isDisabled
      
AcaoInbox()
---------------
Assinatura
    public AcaoInbox(AcaoWhatsapp__mdt pAcaoWhatsapp, ConversaWhatsapp__c pConversaWhatsapp)
Acao
    Atribui valores a isDisabled e action
Exemplo

   .. code-block:: apex

      AcaoInbox.AcaoInbox(new AcaoWhatsapp__mdt[]{
      new AcaoWhatsapp__mdt(TipoAcao__c = 'Entrada de Mensagem', ClasseApex__c = 'WACoreExecutionAfter', Assincrono__c = true)
      }, 'a021U000007pg2FQAQ');
