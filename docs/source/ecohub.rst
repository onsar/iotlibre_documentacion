ecoHub
======
ecoHub implementa una serie de interfaces que pueden leer/suscribirse o enviar/publicar datos hacia y desde una multitud de servicios. 

.. image:: ./imagenes/raspberrypi.jpg

EcoHub se instala en una Raspberry Pi y esta basado en el software `rasppberry_shileds: <https://github.com/iotlibre/raspberry_shields/>`_ desarrollado para la medida y control de disponitivos de campo.

La principales funciones de ecoHub son las sibuientes:

* emoncms: Transmite la información a un servidor emoncms
* entradas: Lee el estado de las entradas físicas procedente de los pines GPIO
* salidas: Actua sobre las salidas físicas proporcionadas por los pines GPIO
* modbus_rtu: Recibe mensajes y envia órdenes a través del protocolo MODBUS RTU
* modbus_tcp: Recibe mensajes y envia órdenes a través del protocolo MODBUS TCP
* muestra_1wire: Lee las temperaturas de las sondas de temperatura que utilizan el protocolo oneWire
* python_serial: Lee la información proporcionada por otros equipos a través del bus serie

Características principales
---------------------------
* Bus de publicación y subscripción de MQTT
* Transmisión de datos al servidor Internet de la Energía
* Es posible implementar varios interfaces y ampliarlos de forma dinámica
* Depuración de errores y revisión del comportamiento mediante logs



