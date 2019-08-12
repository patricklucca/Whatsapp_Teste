ChatContent

Essa classe contém a variável listSectionConversa e os métodos ChatContent, isSameSection e getLastMensagemWa.

Assinatura

public ChatContent(List<MensagemWhatsapp__c> pListMensagemWa)

Explecificações

@AuraEnabled
listSectionConversa

Cria a variável pública do tipo lista de SectionConversa.

Assinatura

public List<SectionConversa> listSectionConversa;

ChatContent(pListMensagemWa)

Atribui os valores da variável pública listSectionConversa através da lista de mensagens passada pelo parâmetro pListMensagemWa.

Assinatura

public ChatContent(List<MensagemWhatsapp__c> pListMensagemWa)

Valor retornado

Sem retorno.


isSameSection(pSectionConversa, pMensagemWa)

Verifica se a última mensagem da pSectionConversa é igual à mensagem enviada via parâmetro pMensagemWa, retornando true caso for verdade e false caso contrário.

Assinatura

public Boolean isSameSection(SectionConversa pSectionConversa, MensagemWhatsapp__c pMensagemWa)

Valor retornado

Tipo:	Boolean.

getLastMensagemWa(pSectionConversa)

Retorna a última mensagem do parâmetro enviado pSectionConversa.

Assinatura

public MensagemWhatsapp__c getLastMensagemWa(SectionConversa pSectionConversa)

Valor retornado

Tipo:	MensagemWhatsapp__c.
