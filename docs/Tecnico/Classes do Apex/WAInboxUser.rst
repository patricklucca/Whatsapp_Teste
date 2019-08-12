#################
WAInboxUser
#################

doExecuteAction()
---------------
Assinatura
    public static void doExecuteAction(AcaoWhatsapp__mdt pAcaoWhatsapp, ConversaWhatsapp__c pConversaWhatsapp)
Retorno
    Executa o método doExecuteWaAction 
      WAActionHandler.doExecuteWaAction(pAcaoWhatsapp, pConversaWhatsapp);

getCurrentUser()
---------------
Assinatura
    public static User getCurrentUser()
Retorno
    Retorna a variável result, que é uma lista das informações do usuário
    
getWAActions()
---------------
Assinatura
    public static List<AcaoInbox> getWAActions(ConversaWhatsapp__c pConversaWhatsapp)
Retorno
    Retorna a variável result, que é uma lista com as informações de AcaoWhatsapp__mdt
        
AcaoInbox
---------------
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
