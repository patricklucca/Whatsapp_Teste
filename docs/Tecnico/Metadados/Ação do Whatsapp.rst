################
Ação do Whatsapp
################
A Ação do Whatsapp é o metadado utilizado para gerenciar as ações utilizadas na aplicação do Whatsapp.
Se o metadado utilizar uma Classe Apex, deve-se implementar a interface WAActionInterfaceV2, caso utilize um Componente Lightning, implementar o extends WAActionTemplate.

.. image:: metadados1.png
    :width: 500px
    :alt: Solidity logo
    :align: center
 
Relacionar Contato ou Lead
 
.. image:: metadados2.png
    :width: 500px
    :alt: Solidity logo
    :align: center
 
O metadado Relacionar Contato ou Lead é utilizado no componente WAMessenger para relacionar um Contato do Whatsapp à um Contato ou uma Lead do Salesforce. O corpo e suas funcionalidades estão no componente lightning WACoreActionRelacionamento.

WA Core Antes da Entrada Mensagem
 
.. image:: metadados3.png
    :width: 500px
    :alt: Solidity logo
    :align: center
    
O metadado WA Core Antes da Entrada Mensagem, quando utilizado, cria novas conversas caso a mensagem não tenha uma conversa relacionada e relacionando mensagens com suas conversas já existentes.

WA Core Depois da Entrada Mensagem
 
.. image:: metadados4.png
    :width: 500px
    :alt: Solidity logo
    :align: center
   
O metadado WA Core Depois da Entrada Mensagem é responsável por disparar as mensagens para o servidor, além de criar e publica uma lista de eventos com do tipo WhatsappChat__e.
 
