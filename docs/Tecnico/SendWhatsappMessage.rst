#################
SendWhatsappMessage
#################

doEnviarMensagem()
-----------------------
NÃO ESTÁ EM USO// As mensagens são montadas através do método doEnviarMensagem

Assinatura
    public static void doEnviarMensagem(String pOrigem, String pDestino, String pChave, String pMensagem, String pIdChat)
Valor retornado
    Não tem retorno
   
doEnviarMensagens()
-----------------------
Responsável pelo enfileiramento das mensagem com origem Empresa > Cliente 

Retorno
    O método manipula a variável singleQueue, criada dentro da classe
Assinatura
    public statis void doEnviarMensagens(Set<Id> pSetMensagem)

doEnviarContentMedia()
-----------------------
NÃO ESTÁ EM USO// As mensagens com imagens são montadas através deste método

Retorno
    Retorna o body da request
Assinatura
    public static void doEnviarContentMedia(String pOrigem, String pDestino, String pChave, String pContentMedia, String pContentSize)

public static void doRegistrarNumero(String pDdi, String pNumero, String pOperadora, String pMetodoEnvio)
-----------------------
egistra o número que envia mensagens
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doRegistrarNumero('', '', '','');``
      

public static void doAutenticarNumero(String pDdi, String pNumero, String pCodigo)
-----------------------
Autentifica o número que envia mensagens.
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doAutenticarNumero('', '', '');``
             
public static void doRegistrarNovoNumero(String oldNumero, String numero, String operadora, String callbackLogin, String callbackPassword, String msgIncompatibilidade, Boolean isAtivo)
-----------------------
Método responsável pela chamada do método ``registerNewNumber``
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doRegistrarNovoNumero('', '', '', '', '', '', true);``
                  
     
public static void doVerificaNovoNumero()
-----------------------
NÃO ESTÁ EM USO// Não recebe nenhum parâmetro e não é chamado por nenhum outro método em nenhuma outra classe, montando o content com informações constantes. 
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doRegistrarNovoNumero();``

public static void doRegitrarNovoGrupo()
-----------------------
NÃO ESTÁ EM USO// Registra uma nova conversa de grupo. Monta o content com informações constantes. 
A chamada pode ser realizada da seginte forma:

    ``SendWhatsappMessage.doRegistrarNovoNumero();``
             
public static String getQr(String pNumero)
-----------------------
Esta método é chamado pela método loadQr da classe `WAQrView`_ para montar a requisição ao servidor através da chamada:
    ``String response = SendWhatsappMessage.getQr(param.Celular__c);``



.. _WAQrView : 
             
public static String requestQr(String pNumero)
-----------------------
Esta método é chamado pelo método requestQr da classe `WAQrRequest`_ para montar a requisição ao servidor através da chamada:
    ``String response = SendWhatsappMessage.getQr(param.Celular__c);``



.. _WAQrRequest : 
             
             
public class SendMessageQueue implements Queueable, Database.AllowsCallouts
-----------------------
Método responsável por implementar Queable e chamada de método subsequentes
    
public SendMessageQueue(Set<Id> pSetMensagemId) 
-----------------------
Preenche a variável pSetMensagemId
    
public void add(Set<Id> pSetMensagemId) 
-----------------------
Método responsável pela chamada de método subsequentes
    
public void execute(QueueableContext context)  
-----------------------
Envia as mensagens enfileiradas
    
public class RemoteMessageEntity
-----------------------
Define String id, String corpo, String origem, String destino e chama RemoteMessageEntity
    
public RemoteMessageEntity(MensagemWhatsapp__c pMensagemWa) 
-----------------------
Define valores para String id, String corpo, String origem, String destino.

             

 

