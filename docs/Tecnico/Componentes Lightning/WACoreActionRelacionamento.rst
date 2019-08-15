############################
WACoreActionRelacionamento
############################
Atributos
----------
status
~~~~~~~~
Tipo: String[]
Obrigatório: false

selItem
~~~~~~~~
Tipo: object
Obrigatório: false

tipoRelacao
~~~~~~~~
Tipo: Map[]
Obrigatório: false

selecionado
~~~~~~~~
Tipo: Map
Obrigatório: false

contatoWhatsapp
~~~~~~~~
Tipo: ContatoWhatsapp__c
Obrigatório: false

acaoMessenger
~~~~~~~~
Tipo: String[]
Obrigatório: false

relacionamento
~~~~~~~~
Tipo: String
Obrigatório: false

displayLead
~~~~~~~~
Tipo: String
Obrigatório: false

displayContact
~~~~~~~~
Tipo: String
Obrigatório: false

visibleActionIcon
~~~~~~~~
Tipo: String
Obrigatório: false

showSpinner
~~~~~~~~
Tipo: Boolean
Obrigatório: false

Exemplo
~~~~~~~~
<aura:attribute name="exemplo" type="String" default = "texte1">
<whats:WACoreActionRelacionamento
                             status = {!v.exemplo}>

Functions
----------
doInit
~~~~~~~~~~
helper.setContatoWhatsapp(component, helper);

onSelectRelacao
~~~~~~~~~~
helper.setSelecionado(component, event, helper, tipo);

closeModal
~~~~~~~~~~
$A.enqueueAction(a);

onChangeRelacionamento
~~~~~~~~~~
component.set("v.relacionamento", event.getSource().get("v.value"));

handleSave
~~~~~~~~~~
helper.saveRelacao(component, event, helper);

handleLoad
~~~~~~~~~~
component.set('v.showSpinner', false);
component.set('v.visibleActionIcon', '');

Exemplo
~~~~~~~~
        <lightning-button label="texte" onclick={doInit}/>






