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
Exemplo

   .. code-block:: python

      WAMessageListenner_ctl
      
getCurrentUser()
---------------
Assinatura
    public static User getCurrentUser()
Retorno
    Retorna a variável result, que é uma lista das informações do usuário
Exemplo

   .. code-block:: python

      WAMessageListenner_ctl
      
getWAActions()
---------------
Assinatura
    public static List<AcaoInbox> getWAActions(ConversaWhatsapp__c pConversaWhatsapp)
Retorno
    Retorna a variável result, que é uma lista com as informações de AcaoWhatsapp__mdt
Exemplo

   .. code-block:: python

      WAMessageListenner_ctl
      
AcaoInbox
---------------
Assinatura
    public class AcaoInbox
Expecificação
    Possui as variáveis AcaoWhatsapp__mdt e isDisabled e o método AcaoInbox
 Exemplo

   .. code-block:: python

      WAMessageListenner_ctl
      
AcaoWhatsapp__mdt
---------------
Assinatura
    public AcaoWhatsapp__mdt action;
Acao
    Cria uma variável tipo metadado AcaoWhatsapp__mdt
Exemplo

   .. code-block:: python

      WAMessageListenner_ctl
      
isDisabled
---------------
Assinatura
    public Boolean isDisabled;
Acao
    Cria uma variável tipo booleano isDisabled
Exemplo

   .. code-block:: python

      WAMessageListenner_ctl
      
AcaoInbox()
---------------
Assinatura
    public AcaoInbox(AcaoWhatsapp__mdt pAcaoWhatsapp, ConversaWhatsapp__c pConversaWhatsapp)
Acao
    Atribui valores a isDisabled e action
Exemplo

   .. code-block:: python

      WAMessageListenner_ctl
      
      
      
      
      
      
      
      
