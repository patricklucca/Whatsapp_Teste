############################
WAInboxUser
############################
Atributos
----------
+------------------------+-----------------------+-------------+
|  name                  | Tipo                  | Obrigatório |
+========================+=======================+=============+
| usuario                | User                  | false       | 
+------------------------+-----------------------+-------------+


Exemplo
~~~~~~~~
  .. code-block:: apex

      <lightning:tile label="{!v.usuario.Name}" href="{!'/'+v.usuario.Id}">

Functions
----------
doInit
~~~~~~~~~~
Retorna o usuário atual
