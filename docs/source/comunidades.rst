Comunidades Energéticas
========================
Introducción
------------
Este documento presenta una propuesta construida con software libre para la monitorización de los elementos que componen un autoconsumo compartido por una comunidad energética.

Todos los elementos que componen esta solución se han probado y comparado con otras soluciones de software libre de tal manera que lo que aquí se presenta el la mejor opción en cuanto a calidad y estabilidad.

El sistema es configurable y lo forman módulos tanto hardware como software de tal manera que se pueden sustituir por otros mas evolucionados, si se diera el caso.

Arquiectura
-----------
A continuación se presenta la arquitectura sortware de las comuidades energéticas

.. image:: ./imagenes/arquitectura_autoconsumo_compartido.png

Los valores de energía que genera el inversor se hace con el software ecoHub instalado en una Raspberry.

.. image:: ./imagenes/medida_inversor.png

La energía consumida por el usuario se mide mediante un analizador de redes instalado en el cuadro del usuario.

.. image:: ./imagenes/medida_tansformador.png

**emoncms**

Desrrollado por la comunidad de "Open Energy Monitor" es una referencia y este caso es el motor de la solución

**NodeRed**

Permite dar flexibilidad a la solución y que esta sea facilmente configurable para evitar modificar el cófigo fuente de la aplicación.

**JavaScript**

Las aplicaciones para móvil y para tablet funcionan con JavaScript para darle una funcinalidad dinámica incluso en entornosdonde el ancho de banda es limitado.



