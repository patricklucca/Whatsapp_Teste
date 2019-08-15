O WAActionTemplate é o componente modelo que deve ser utilizado para a implementação dos componentes lightning que aparecerão no messenger. Ele funciona como uma modal, com o layout separado em três partes, cabeçalho, corpo e rodapé.
Nele temos os seguintes atributos:


.. image:: WAActionTemplate.png
    :width: 500px
    :alt: Solidity logo
    :align: center

Além dos atributos, tem um método para fechamento da modal close().

close()

Método utilizado para fechamento da modal.



Exemplo de utilização do componente como extends:

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

Referências:
Componente Lightning
WAMessenger
WACoreActionRelacionamento
Metadado
Ação do Whatsapp
Relacionar Contato ou Lead

