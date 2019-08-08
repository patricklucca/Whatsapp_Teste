#################
SendWhatsappMessage
#################

doEnviarMensagem()
-----------------------
NÃO ESTÁ EM USO// As mensagens são montadas através do método doEnviarMensagem

Assinatura
    public static void doEnviarMensagem(String pOrigem, String pDestino, String pChave, String pMensagem, String pIdChat)
Retorno
    Retorna o body da request e setta o endpoint
   
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
    Retorna o body da request e setta o endpoint
Assinatura
    public static void doEnviarContentMedia(String pOrigem, String pDestino, String pChave, String pContentMedia, String pContentSize)

doRegistrarNumero()
-----------------------
Registra o número que envia mensagens

Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static void doRegistrarNumero(String pDdi, String pNumero, String pOperadora, String pMetodoEnvio)


doAutenticarNumero()
-----------------------
Autentifica o número que envia mensagens.
    
Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static void doAutenticarNumero(String pDdi, String pNumero, String pCodigo)
             
doRegistrarNovoNumero()
-----------------------
Método responsável pela chamada do método ``registerNewNumber``

Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static void doRegistrarNovoNumero(String oldNumero, String numero, String operadora, String callbackLogin, String callbackPassword, String msgIncompatibilidade, Boolean isAtivo)
     
doVerificaNovoNumero()
-----------------------
NÃO ESTÁ EM USO// Não recebe nenhum parâmetro e não é chamado por nenhum outro método em nenhuma outra classe, montando o content com informações constantes. 

Retorno
    Retorna o body da request e setta o endpoint    
Assinatura
    public static void doVerificaNovoNumero()


doRegitrarNovoGrupo()
-----------------------
NÃO ESTÁ EM USO// Registra uma nova conversa de grupo. Monta o content com informações constantes. 

Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static void doRegitrarNovoGrupo()

getQr()
-----------------------
Esta método é chamado pela método loadQr da classe `WAQrView`_ para montar a requisição ao servidor através da chamada:
    ``String response = SendWhatsappMessage.getQr(param.Celular__c);``

Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static String getQr(String pNumero)


.. _WAQrView : 
             
requestQr()
-----------------------
Esta método é chamado pelo método requestQr da classe `WAQrRequest`_ para montar a requisição ao servidor através da chamada:
    ``String response = SendWhatsappMessage.getQr(param.Celular__c);``

Retorno
    Retorna o body da request e setta o endpoint
Assinatura
    public static String requestQr(String pNumero)


.. _WAQrRequest : 
             
             
SendMessageQueue
-----------------------
Classe responsável por implementar Queable e chamada de método subsequentes

Retorno
Assinatura
    public class SendMessageQueue implements Queueable, Database.AllowsCallouts

SendMessageQueue() 
-----------------------
Cria a fila de mensagens

Retorno
    Cria a variáevl setMensagemId e atribui o valor de pSetMensagemId
Assinatura
    public SendMessageQueue(Set<Id> pSetMensagemId)
    
add() 
-----------------------
Método responsável pela inserção de mensagens a fila

Retorno
    Adiciona valores à variável setMensagemId
Assinatura
    public void add(Set<Id> pSetMensagemId) 
    
execute()  
-----------------------
Envia as mensagens enfileiradas
    
Retorno
    Setta o endpoint
Assinatura
    public void execute(QueueableContext context)

public class RemoteMessageEntity
-----------------------
Classe que define String id, String corpo, String origem, String destino e chama RemoteMessageEntity

Retorno
Assinatura
    public class RemoteMessageEntity
    
public RemoteMessageEntity() 
-----------------------
Define valores para String id, String corpo, String origem, String destino.

Retorno
    Variáveis String id, corpo, origem e destino
Assinatura
    public RemoteMessageEntity(MensagemWhatsapp__c pMensagemWa) 

             

 

