WAHostControl_ctl

getHost()

Retorna a URL da organização.

Assinatura

public String getHost()

Valor retornado

Tipo:	String

Exemplo

//Exemplo de link da home de uma organização
//https://exemplo-dev-ed.lightning.force.com/lightning/page/home
WAHostControl_ctl wahost = new WAHostControl_ctl();
String s = wahost.getHost();
system.assertEquals(s, 'exemplo-dev-ed.my.salesforce.com');
