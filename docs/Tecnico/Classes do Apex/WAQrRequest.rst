############
WAQrRequest
############

param
  Get e Set da variável pública do tipo ParametroWahtsapp__c.
Assinatura
  public ParametroWhatsapp__c param {get;set;}
Valor retornado
  Tipo de retorno do get:		ParametroWhatsapp__c.
  Tipo do retorno do set:		sem retorno.
  
  
response
  Get e Set da variável pública do tipo String.
Assinatura
  public String response {get;set;}
Valor retornado
  Tipo de retorno do get:		String.
  Tipo do retorno do set:		sem retorno.
  
  
WAQrRequest_ctl()
  Atribui um Parâmetro Whatsapp a variável local param.
Assinatura
  public WAQrRequest_ctl(ApexPages.StandardController std)
Valor retornado
  Sem retorno.
Exemplo
  ParametroWhatsapp__c pw = [SELECT Id, Celular__c FROM ParametroWhatsapp__c Where Celular__c = '13986751234' LIMIT 1];
  WAQrRequest_ctl ctlexemplo = new WAQrRequest_ctl(new ApexPages.StandardController(pw));
  ctlexemplo.init();
  ctlexemplo.getResponseMessage();
  
init()
  Executa outros métodos privados da classe.
Assinatura
  public void init()
Valor retornado
  Sem retorno.
Exemplo
  ParametroWhatsapp__c pw = [SELECT Id, Celular__c FROM ParametroWhatsapp__c Where Celular__c = '13986751234' LIMIT 1];
  WAQrRequest_ctl ctlexemplo = new WAQrRequest_ctl(new ApexPages.StandardController(pw));
  ctlexemplo.init();
  ctlexemplo.getResponseMessage();
  
getResponseMessage()
  Retorna a mensagem do json feito com o servidor ou Erro inesperado, caso a mensagem esteja vazia.
Assinatura
  public String getResponseMessage()
Valor retornado
  Tipo:	String.
Exemplo
  ParametroWhatsapp__c pw = [SELECT Id, Celular__c FROM ParametroWhatsapp__c Where Celular__c = '13986751234' LIMIT 1];
  WAQrRequest_ctl ctlexemplo = new WAQrRequest_ctl(new ApexPages.StandardController(pw));
  ctlexemplo.init();
  ctlexemplo.getResponseMessage();  
  
requestQr() 
  Faz o json de requisição de um QR Code para o ParametroWhatsapp__c da variável local param.
Assinatura
  public void requestQr()
Valor retornado
  Sem retorno.
Exemplo
   List<ParametroWhatsapp__c> lstRst = [
       SELECT
           Id
           ,Name
           ,Celular__c
       FROM
           ParametroWhatsapp__c
       WHERE
            Id = 'id_do_parametro'
   ];
   if (!lstRst.isEmpty()) {
        param = lstRst.get(0);
        requestQr(); 
   }
    
  
  
