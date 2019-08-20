######################
WAMessageListenner
######################

pushTopicId
  Get e Set da variável pública do tipo String.
Assinatura
  public String pushTopicId {get;set;}
Valor retornado
  Tipo de retorno do get:		String.
  Tipo do retorno do set:		sem retorno.
Exemplo

   .. code-block:: apex

      WAMessageListenner_ctl mCtl = new WAMessageListenner_ctl();
      mCtl.pushTopicId = 'afjkafsjk';

canExecuteScript
  Get e Set da variável pública do tipo Boolean.
Assinatura
  public Boolean canExecuteScript {get;set;}
Valor retornado
  Tipo de retorno do get:		Boolean.
  Tipo do retorno do set:		sem retorno.


init()
  Atribui o valor booleano para a variável pública local canExecuteScript.
Assinatura
  public void init()
Valor retornado
  Sem retorno.
Exemplo

   .. code-block:: python

      WAMessageListenner_ctl mCtl = new WAMessageListenner_ctl();
      mCtl.init();
