WAQrView_ctl

param

Get e Set da variável pública do tipo ParametroWahtsapp__c.

Assinatura

public ParametroWhatsapp__c param {get;set;}

Valor retornado

Tipo de retorno do get:		ParametroWhatsapp__c.
Tipo do retorno do set:		sem retorno.

keepPolling

Get e Set da variável pública do tipo Boolean.

Assinatura

public Boolean keepPolling {get;set;}

Valor retornado

Tipo de retorno do get:		Boolean.
Tipo do retorno do set:		sem retorno.

WAQrView_ctl(std)

Atribui um Parâmetro Whatsapp a variável local param.

Assinatura

public WAQrView_ctl(ApexPages.StandardController std)

Valor retornado

Sem retorno.

init()

Executa outros métodos privados da classe.

Assinatura

public void init()

Valor retornado

Sem retorno.

loadQr()

Carrega a imagem do QR Code do Parâmetro Whatsapp da variável local param.

Assinatura

public void loadQr()

Valor retornado

Sem retorno.

getCurrentQrId()

Retorna o Id da imagem do QR Code do Parâmetro Whatsapp da variável local param.

Assinatura

public Id getCurrentQrId()

Valor retornado

Tipo: 	Id.

getDisplayMessage()

Retorna a mensagem “Aguardando QR Code...” caso esteja aguardando o QR Code e retorna a mensagem “Nenhum código disponível” caso a organização não esteja ativada no servidor ou se o Parâmetro Whatsapp já esteja conectado.

Assinatura

public String getDisplayMessage()

Valor retornado

Tipo: 	String.

