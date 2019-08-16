############################
WACoreActionRelacionamento
############################
Atributos
----------
+------------------------+-----------------------+-------------+
|  name                  | Tipo                  | Obrigatório |
+========================+=======================+=============+
| Status                 | String[]              | false       | 
+------------------------+-----------------------+-------------+
| selItem                | object                | false       | 
+------------------------+-----------------------+-------------+
| tipoRelacao            | Map[]                 | false       | 
+------------------------+-----------------------+-------------+
| selecionado            | Map                   | false       | 
+------------------------+-----------------------+-------------+
| contatoWhatsapp        | ContatoWhatsapp__c    | false       | 
+------------------------+-----------------------+-------------+
| acaoMessenger          | String[]              | false       | 
+------------------------+-----------------------+-------------+
| relacionamento         | String[]              | false       | 
+------------------------+-----------------------+-------------+
| displayLead            | String[]              | false       | 
+------------------------+-----------------------+-------------+
| displayContact         | String[]              | false       | 
+------------------------+-----------------------+-------------+
| visibleActionIcon      | String[]              | false       | 
+------------------------+-----------------------+-------------+
| showSpinner            | Boolean               | false       | 
+------------------------+-----------------------+-------------+

Exemplo
~~~~~~~~
. . codeblock apex
    <aura:attribute name="exemplo" type="String" default = "texte1">
    <whats:WACoreActionRelacionamento
                                   status = {!v.exemplo}>

Functions
----------
doInit
~~~~~~~~~~
Atribui à contatoWhatsapp um contato do whatsapp relacionado a conversa

onSelectRelacao
~~~~~~~~~~
Verifica se um Contato ou Lead foi selecionado, atribuindo valores à displayLead ou displayContact

closeModal
~~~~~~~~~~
Fecha o modal de relação

onChangeRelacionamento
~~~~~~~~~~
Troca o relacionamento de Lead para Contato ou de Contato para Lead

handleSave
~~~~~~~~~~
Salva o contato ou lead no componente recordViewForm e recarrega a página.

handleLoad
~~~~~~~~~~
Mostra o contrato ou lead selecionado previamente

Exemplo
~~~~~~~~
        ´<lightning-button label="texte" onclick={doInit}/>´






