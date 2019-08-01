.. testereadthedocs documentation master file, created by
   sphinx-quickstart on Tue Jul 30 11:35:45 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Whatsapp Core
========
.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Whatsapp Core
   
   TesteZap
   glossary

.. image:: WhatsApp-Messenger.png
    :width: 100px
    :alt: Solidity logo
    :align: center


Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse ullamcorper, nunc non porta blandit, nibh velit efficitur metus, ac dapibus augue tortor in libero. Pellentesque gravida et elit a pretium. Quisque vitae efficitur urna, et luctus dolor. Aenean nec purus a tellus posuere mollis et nec metus. Quisque ac ornare nisl. In hac habitasse platea dictumst. Morbi porta vel arcu vitae iaculis. Maecenas feugiat enim lobortis massa ultricies, vel ullamcorper est commodo. Duis turpis tortor, tincidunt quis malesuada eget, vehicula non mi.

    ``Ci vis pacem para Bellum``
    
    ``tail(X(i)) = enc(X(i))``
 et voluisse sat est
 
 ''Essas frases de cima são do meu latim, gastei dmsss''
 ``Essas frases de cima são do meu latim, gastei dmsss``

Teste teste teste

   .. code-block:: python

      from rubix.aws.cloudwatch import plot_metric
      Testando aaaaaaaaaaa
      # Load balancer P90 latency with deployment time markers
      plot_metric(namespace='AWS/ELB',
            metric_name='Latency',
            dimensions={'LoadBalancerName': 'prod-xyz-lb'},
            markers=deployment_times,
            statistics='p90')

      # Maximum CPU Utilization across EC2 for a specific time period
      plot_metric(namespace='AWS/EC2',
            metric_name='CPUUtilization',
            start_time=datetime.datetime(2018, 04, 25),
            end_time=datetime.datetime(2018, 04, 26)
            statistics='Maximum')
