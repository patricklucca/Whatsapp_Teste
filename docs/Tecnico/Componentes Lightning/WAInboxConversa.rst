################
WAInboxConversa
################
Atributos
----------
+------------------------+-----------------------+-------------+
|  name                  | Tipo                  | Obrigatório |
+========================+=======================+=============+
| conversa               | ConversaWhatsapp__c   | false       | 
+------------------------+-----------------------+-------------+
| iconUrl                | String                | false       | 
+------------------------+-----------------------+-------------+
| alertChat              | Boolean               | false       | 
+------------------------+-----------------------+-------------+
Exemplo
---------
  
   .. code-block:: html

      <aura:component extends="whats:WAActionTemplate" >
         <!-- Events -->
         <aura:registerEvent name="onClick" type="c:WAInboxConversaEvent"/>      
         <!-- Header -->
         <aura:handler name="init" value="{!this}" action="{!c.doInit}"/>
         
         <div class="{!'chat-item ' + ((v.conversa.selecionado == true) ? ' selected ' : '') + ((v.alertChat == true) ? ' new-chat ' : '')}" onclick="{!c.onClickConversa}">
            <div class="default-user-icon">
                        <div class="slds-is-absolute position-alert-icon">
    				        <span class="alertIcon slds-theme_warning">!</span>
    				    </div>
    				    <img src="{!v.iconUrl}" draggable="false" class="avatar-image is-loaded"/>
        		 </div>
         </div>
       

Functions
----------
doInit
~~~~~~~~~~
Carrega o ícone com a imagem do contato

notifyParent
~~~~~~~~~~
Recebendo mensagens setta a variável conversa
