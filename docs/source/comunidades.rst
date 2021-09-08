Comunidades Energéticas
========================
Introducción
------------
Esta propuesta, construida con software libre, esta diseñada para la monitorización de los elementos que componen un autoconsumo compartido de una comunidad energética. Todos los elementos que componen esta solución se han probado y comparado con otras soluciones, también de software libre, de tal manera que lo que aquí se presenta el la mejor opción en cuanto a calidad y estabilidad. Además, este servicio esta pensado para que el coste sea reducido, intentando que pueda asumirse, sin grandes esfuerzos, como parte de la instalación.

El sistema es configurable y lo forman módulos, tanto de hardware como de software, de tal manera que se pueden sustituir por otros mas evolucionados, si se diera el caso.

Arquitectura
-----------
La siguiente figura muestra un esquema funcional de todos los elementos que componen la aplicación.

.. image:: ./imagenes/arquitectura_autoconsumo_compartido.png

**emoncms:** Desarrollado por la comunidad de "Open Energy Monitor" es una referencia en el area de de la energía y en este caso es el motor de la solución. El software se pude encontrar en `Github <https://github.com/emoncms/emoncms/>`_

`Python <http://www.python.org/>`_

**PhP:** Es el lenguaje de programación con el que se ha desarrollado emoncms. Este lenguaje tiene un rendimiento muy alto para aplicaciones web. Página oficial de `pHp: <https://www.php.net/>`_

**NodeRed:** Permite dar flexibilidad a la solución y que esta sea fácilmente configurable para evitar modificar el código fuente de la aplicación. Página oficial de `NodeRed: <https://nodered.org/>`_

**JavaScript:** Las aplicaciones para móvil y para tableta funcionan con JavaScript para darle una funcionalidad dinámica incluso en entornos donde el ancho de banda es limitado. Página de `JavaScript <https://developer.mozilla.org/es/docs/Web/JavaScript/>`_ en Mozilla

**Medidores de Energía(E):** Son analizadores de redes con transformadores de intensidad (pinzas). Todas las maracas comerciales que cumplan con el protocolo MQTT son válidas. También pueden instalarse equipos de Open Energy Monitor que pueden integrarse de forma nativa

**OpenVpn:** La conexión al inversor se hace de forma segura mediante una VPN. Esta VPN también cumple el propósito de habilitar el acceso a la Raspberry para tareas de mantenimiento remoto.Pagina oficial de `OpenVpn: <https://openvpn.net/>`_

**ecoHub:** Es el software para conectarse al inversor mediante MODBUS y enviar la información al servidor haciendo uso del API Rest del servidor. Desarrollado en Python, este software se instala en una Raspberry en la misma localización del inversor. Software de `ecoHub en Github: <https://github.com/iotlibre/eco_modbus_tcp/>`_

Tipos de instalación
--------------------
Además de la instalación del software de servidor que se debe hacer en un proveedor de servicios en Internet es necesario instalar equipos tanto en los edificios donde se mide el consumo de energía como en las ubicaciones donde se genera la energía:

Los valores de energía que genera el inversor se obtienen con el software ecoHub instalado en una Raspberry. La siguiente figura muestra un esquema simplificado de como se haría la conexión

.. image:: ./imagenes/medida_inversor.png

------------------

La energía consumida por el usuario se mide mediante un analizador de redes instalado en el cuadro del edificio. La siguiente figura muestra un esquema simplificado de como se haría la conexión

.. image:: ./imagenes/medida_tansformador.png


Cliente para móvil y tableta
---------------------------

Existen múltiples formas de ver la información de la instalación de autoconsumo. En esta imagen se puede ver la forma mas extendida de comparar la energía producida (en el porcentaje asignado al usuario) comparándola con la energía consumida:

.. image:: ./imagenes/cliente_potencia.png

La siguiente gráfica muestra un resumen de los que ha ocurrido cada día

.. image:: ./imagenes/cliente_historico.png
