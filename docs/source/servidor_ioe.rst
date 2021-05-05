El Servidor Internet de la Energía (IoE)
========================================
El servidor de IoE esta compuesto por **módulos de Software Libre** que han demostrado un alto rendimiento y estabilidad. Entre ellas esta Apache, php, MySQL, MQTT y Node-RED. El resultado es un servidor de software libre que puede competir con las mejores aplicaciones. Este servidor se ha orientado a la monitorización y transformación de magnitudes energéticas por lo que es un servidor muy especializado. De ahí su nombre **Internet de la Energía**

El procesado de los datos se hace en el serviodor IoE instalado en un **proveedor de servicios en la nube**.

El servidor de la nube estará **dedicado al cliente o puede ser compartido** con otras redes de sensores de tal manera que el administrador del servicio pueda ampliarlo, limitar su acceso o incluir nuevas funcionalidades. 

La dimensión del servidor se calcula para que sea suficiente para la gestión de todos los datos originados en el proyecto pero, en caso de ser necesario, por  un gran cantidad de nuevas instalaciones, la **ampliación de las capacidades** de IoE, , se puede hacer de forma sencilla, mediante configuración, sin necesidad de ampliar el hardware que soporta el servidor.

La transmisión de datos, desde los sensores al servidor, se hace de forma estándar y sencilla usando el **protocolo MQTT o mediante un API RESTful**. Los dispositivos se dan de **alta de forma automática** cuando se reciben los datos con las correspondientes credenciales.

Los datos se presentan en **gráficas** que pueden reflejar el consumo diario semanal o mensual de los recursos que se miden. Estas gráficas podrán combinar varias fuentes de datos para que puedan ser comparados y que permitan la creación de informes. Los datos también pueden ser exportados a una **hoja de cálculo**.
