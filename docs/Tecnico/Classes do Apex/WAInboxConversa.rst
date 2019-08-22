###############
WAInboxConversa
###############
@AuraEnabled

getIconUrl()
~~~~~~~~~~~~~~~~~~~~
  Retorna a URL do ícone do Contato do Whatsapp caso o mesmo tenha um ícone, caso contrário retorna uma string vazia.
Assinatura
  public static String getIconUrl(String pContatoId)
Valor retornado
  Tipo:	String.
Exemplo

   .. code-block:: apex

      String result = ''
      if (!String.isEmpty(iconId))
      result = 'https://'+getHostUrl()+'/servlet/servlet.FileDownload?file='+iconId;
      return result; 

getHostUrl()
~~~~~~~~~~~~~~~~~~~~
  Retorna a URL da organização.
Assinatura
  public static String getHostUrl()
Valor retornado
  Tipo:	String.
Exemplo

   .. code-block:: apex

      String result = ''
      result = getHostUrl()
      return result;
