#################
WAActionTemplate
#################
Atributos:
~~~~~~~~~~~~

+------------------------+-----------------------+-------------+
|  name                  | Tipo                  | Obrigatório |
+========================+=======================+=============+
| Footer                 | Aura.Component[]      | false       | 
+------------------------+-----------------------+-------------+
| title                  | String                | false       | 
+------------------------+-----------------------+-------------+
| conversaWhatsapp       | conversaWhatsapp__c   | false       | 
+------------------------+-----------------------+-------------+

Function
~~~~~~~~~~
close()

Método utilizado para fechamento da modal.


Exemplo:
~~~~~~~~
   .. code-block:: apex

      <aura:component extends="whats:WAActionTemplate" >
         <!-- Header -->
         <aura:set attribute="title" value="Relacionar Lead/Contato " />
         <!-- Footer -->
         <aura:set attribute="footer">
             <lightning:button variant="Neutral" label="Cancelar" title="Cancelar" onclick="{! c.close }" />
         </aura:set>

         <!-- Content -->
         <lightning:layout>         
             <!-- LookupField -->
             <lightning:layoutItem flexibility="auto" size="6" >
                 <lightning:recordEditForm aura:id="recordViewForm"
                     onsubmit="{!c.close}"
                     recordId="{!v.conversaWhatsapp.whats__ContatoWhatsapp__c}"
                     objectApiName="whats__ContatoWhatsapp__c">
                     <lightning:inputField aura:id="lead"
                         fieldName="whats__Lead__c"/>
                 </lightning:recordEditForm>
             </lightning:layoutItem>
         </lightning:layout>
      </aura:component>


