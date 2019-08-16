############################
WACoreActionRelacionamento
############################
Atributos
----------
+------------------------+------------+----------+-------------+
|  name                  | Tipo                  | Obrigatório |
+========================+============+==========+=============+
| Status                 | String[]              | false       | 
+------------------------+------------+----------+-------------+
| selItem                | object                | false       | 
+------------------------+------------+------------------------+
| tipoRelacao            | Map[]                 | false       | 
+------------------------+------------+------------------------+
| selecionado            | Map                   | false       | 
+------------------------+------------+------------------------+
| contatoWhatsapp        | ContatoWhatsapp__c    | false       | 
+------------------------+-----------------------+-------------+
| acaoMessenger          | String[]              | false       | 
+------------------------+------------+------------------------+
| relacionamento         | String[]              | false       | 
+------------------------+------------+------------------------+
| displayLead            | String[]              | false       | 
+------------------------+------------+------------------------+
| displayContact         | String[]              | false       | 
+------------------------+------------+------------------------+
| visibleActionIcon      | String[]              | false       | 
+------------------------+------------+------------------------+
| showSpinner     n      | Boolean               | false       | 
+------------------------+------------+------------------------+

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






