#################
SendWhatsappMessage
#################

doEnviarMensagem()
---------------
NÃO ESTÁ EM USO// As mensagens são montadas através do método doEnviarMensagem

Assinatura
    public static void doEnviarMensagem(String pOrigem, String pDestino, String pChave, String pMensagem, String pIdChat)
Retorno
    Retorna o body da request e setta o endpoint
Exemplo

   .. code-block:: apex

      SendWhatsappMessage.doEnviarMensagem('551399999999', '5513997733761', '', 'teste', 'a011U00000Occ0WQAR');      
      
   
doEnviarMensagens()
-----------------------
Responsável pelo enfileiramento das mensagem com origem Empresa > Cliente 

Retorno
    O método manipula a variável singleQueue, criada dentro da classe
Assinatura
    public statis void doEnviarMensagens(Set<Id> pSetMensagem)
Exemplo
      
   .. code-block:: apex
  
      Map<Id, MensagemWhatsapp__c> exemploresult = new Map<Id, MensagemWhatsapp__c>([SELECT Id, Name FROM MensagemWhatsapp__c]);
      SendWhatsappMessage.doEnviarMensagens(exemploresult.keySet());
       
doEnviarContentMedia()
-----------------------
NÃO ESTÁ EM USO// As mensagens com imagens são montadas através deste método

Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static void doEnviarContentMedia(String pOrigem, String pDestino, String pChave, String pContentMedia, String pContentSize)
Exemplo

   .. code-block:: apex

      SendWhatsappMessage.doEnviarContentMedia('551399999999', '5513997733761', '', 'teste', '60000');
       
doRegistrarNumero()
-----------------------
Registra o número que envia mensagens

Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static void doRegistrarNumero(String pDdi, String pNumero, String pOperadora, String pMetodoEnvio)
Exemplo
       
   .. code-block:: apex

      SendWhatsappMessage.doRegistrarNumero('13', '999999999', 'operadora', '');

doAutenticarNumero()
-----------------------
Autentifica o número que envia mensagens.
    
Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static void doAutenticarNumero(String pDdi, String pNumero, String pCodigo)
Exemplo
       
   .. code-block:: apex
      
      SendWhatsappMessage.doAutenticarNumero('13', '55999999999', '');
             
doRegistrarNovoNumero()
-----------------------
Método responsável pela chamada do método ``registerNewNumber``

Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static void doRegistrarNovoNumero(String oldNumero, String numero, String operadora, String callbackLogin, String callbackPassword, String msgIncompatibilidade, Boolean isAtivo)
Exemplo
 

   .. code-block:: apex

      SendWhatsappMessage.doRegistrarNovoNumero('55999999999', '55988888888', 'operadora', 'xxxx_xx@xxxx.com', 'xxx51465xx', '', '1');
    
doVerificaNovoNumero()
-----------------------
NÃO ESTÁ EM USO// Não recebe nenhum parâmetro e não é chamado por nenhum outro método em nenhuma outra classe, montando o content com informações constantes. 

Retorno
    Retorna o body da request e setta o endpoint    
Assinatura
    public static void doVerificaNovoNumero()
Exemplo


   .. code-block:: apex

      SendWhatsappMessage.doVerificaNovoNumero();


doRegitrarNovoGrupo()
-----------------------
NÃO ESTÁ EM USO// Registra uma nova conversa de grupo. Monta o content com informações constantes. 

Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static void doRegitrarNovoGrupo()
Exemplo

   .. code-block:: apex

      SendWhatsappMessage.doRegitrarNovoGrupo();


getQr()
-----------------------
Esta método é chamado pela método loadQr da classe WAQrView para montar a requisição ao servidor através da chamada:
    ``String response = SendWhatsappMessage.getQr(param.Celular__c);``

Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static String getQr(String pNumero)
Exemplo
       
       .. code-block:: apex
       SendWhatsappMessage.getQr('55999999999');


.. _WAQrView : 
             
requestQr()
-----------------------
Esta método é chamado pelo método requestQr da classe WAQrRequest para montar a requisição ao servidor através da chamada:
    ``String response = SendWhatsappMessage.getQr(param.Celular__c);``

Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static String requestQr(String pNumero)
Exemplo
  

   .. code-block:: apex

      SendWhatsappMessage.requestQr('55999999999');


.. _WAQrRequest : 
             
             
SendMessageQueue
-----------------------
Classe responsável por implementar Queable e chamada de método subsequentes

Retorno
Assinatura
    public class SendMessageQueue implements Queueable, Database.AllowsCallouts
Exemplo


   .. code-block:: apex

      SendWhatsappMessage.SendMessageQueue('55999999999');
