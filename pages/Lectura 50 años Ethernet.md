- El documento habla sobre la historia y evolución de Ethernet, una tecnología de redes digitales locales. Comienza con su creación en el Centro de Investigación de Palo Alto de Xerox hace unos 50 años. Se menciona cómo Ethernet ha resistido el paso del tiempo, con mejoras que permitieron tasas de transferencia de datos de 100Mbps, 1Gbps y luego 100Gbps. También se discute la especificación de Ethernet, que es asincrónica y opera con su propio reloj de datos autónomo. Además, se menciona la decisión de Digital, Xerox e Intel de crear un estándar abierto para la tecnología Ethernet de 10Mbps, lo que permitió a muchos fabricantes construir productos interoperables. Finalmente, se describe cómo se instaló y operó Ethernet, utilizando un cable coaxial de 75 ohmios que se desenrollaba alrededor del entorno de la oficina.
- ## Temas principales
- Creación de Ethernet en el Centro de Investigación de Palo Alto de Xerox hace 50 años.
- La resistencia y evolución de Ethernet a lo largo del tiempo, con mejoras en las tasas de transferencia de datos.
- La especificación de Ethernet, que es asincrónica y opera con su propio reloj de datos autónomo.
- La decisión de Digital, Xerox e Intel de crear un estándar abierto para la tecnología Ethernet de 10Mbps.
- La adopción de este estándar por parte del comité IEEE 802 y la liberación del estándar LAN Ethernet IEEE 802.3.
- La instalación y operación de Ethernet, utilizando un cable coaxial de 75 ohmios en un entorno de oficina.
- La forma en que Ethernet permitió a cualquier cliente enviar un paquete directamente a cualquier otro cliente adjunto.
- ## Concepción
- Creado hace 50 años en el Centro de Investigación de Palo Alto de Xerox
- X-Wire
	- Sistema de red de oficina de bus común de 3 Mbps
- ### Especificación inicial
- Transmisión a una velocidad de 2.94 Mbps.
- No hay acuso de recibo de los paquetes
- No hay avisos de fallos de red (como la segmentación)
- No hay un reloj para imponer un tiempo común
- No hay imposición de ((64f479c2-c83e-4aa8-be2b-291d5472595c))
	- Expectativa para cualquier medio común compartido
- No hay ningún nivel de predicción en el sistema
- Las transmisiones individuales deben esperar un periodo de tiempo determinado (aleatorio) antes de transmitir. Esto tiene como consecuencia el ((64f479c5-d9de-4454-87ce-a64fadfa103e))
- No existe un control de flujo o priorización de paquetes
- No existe Full duplex
- Aunque no había un controlador general dentro de la arquitectura Ethernet, el modelo de bus era efectivo en la gestión de la congestión y era posible mantener cargas sostenidas de más del 90% de la capacidad nominal de la red
- ## AlohaNET: El predecesor de Ethernet
- Red de radio creada en la Universidad de Hawaii
- Red de radio de bajo costo
- Conecta usuarios remotos a un mainframe
- Modelo Hub-And-Spoke
	- El hub hace broadcasts de paquetes por radio a todos los clientes en un canal outbound que todos los clientes escuchan
	- El Hub escucha a todos los clientes en un canal inbound
	- Para cada paquete recibido envía un paquete corto de confirmación en el canal de broadcast outbound común.
	- Si el cliente no recibe respuesta luego de un tiempo de espera determinado el paquete se retransmite.
		- Para evitar deadlocks la transmisión se realiza luego de un tiempo aleatorio
	- El sistema de confirmación fue utilizado para detectar y corregir colisiones cuando dos máquinas emiten un mensaje simultáneamente.
	- A cada cliente se le entrega una dirección única
	- Cada paquete incluye la dirección del destinatario
- ## Ethernet
- Ethernet toma el concepto básico de permitir que los dispositivos transmitan cuando estimen necesario y luego manejen las colisiones en caso de ocurrir.
- En lugar de utilizar señales de radio para transmitir datos, Ethernet utiliza un cable común (bus)
- Cada dispositivo en la red puede transmitir datos en el cable cuando quiera. Si dos dispositivos intentan transmitir al mismo tiempo, sus datos interferirán entre sí en el cable.
- ## Marco de colisión
- Describe una parte de la red donde los paquetes pueden colisionar entre sí al ser enviados simultáneamente por dos dispositivos diferentes.
-
- ## Especificación 10 Mbps
- Se introducen los hubs de conmutación, permitiendo un recorrido de par trenzado de 100m desde el punto del hub hasta la estación.
- ### Hub de conmutación (switch)
- Un hub de conmutación, también conocido como switch o conmutador, es un dispositivo de red que se utiliza para conectar múltiples dispositivos  en una red. Funciona recibiendo una señal de un dispositivo conectado y  transmitiéndola solo al dispositivo al que está destinada.
- A diferencia de un hub tradicional, que transmite la señal a todos los dispositivos conectados, un switch es más inteligente y puede dirigir la señal solo al dispositivo correcto. Esto mejora la eficiencia
  de la red y reduce el tráfico, ya que las señales no se envían innecesariamente a todos los dispositivos.
- Los switches son una parte esencial de muchas redes ya que permiten la comunicación entre dispositivos, como computadoras, impresoras, servidores, entre otros, dentro de una red local (LAN).
- En un switch de red, cada puerto tiene su propio dominio de colisión. Esto significa que cada dispositivo conectado al switch puede transmitir simultáneamente sin riesgo de colisiones, lo que mejora la eficiencia 
  de la red.
-
- ## Fair Sharing
  id:: 64f479c2-c83e-4aa8-be2b-291d5472595c
- Principio de diseño que asegura que todos los usuarios o dispositivos tengan un acceso equitativo a los recursos de la red. Esto puede ser especialmente relevante en situaciones donde los recursos son limitados y/o hay una gran demanda de ellos.
- Por ejemplo, en una red Ethernet, el algoritmo de retroceso utilizado después de una colisión es un ejemplo de "Fair Sharing". Cuando ocurre una colisión (es decir, dos dispositivos intentan enviar un paquete al 
  mismo tiempo), cada dispositivo "retrocede" y espera un período de tiempo aleatorio antes de intentar retransmitir el paquete. Este algoritmo asegura que todos los dispositivos en la red tengan una 
  oportunidad justa de transmitir sus paquetes, evitando que cualquier dispositivo monopolice la red.
- Es importante destacar que el "Fair Sharing" no necesariamente significa que todos los usuarios o dispositivos obtengan la misma cantidad de recursos de la red. En cambio, significa que todos tienen una oportunidad equitativa de acceder a esos recursos. En algunas redes, puede haber políticas de calidad de servicio (QoS) que asignen más recursos a ciertos tipos de tráfico o a ciertos usuarios. Sin embargo, incluso en estos casos, el principio de "Fair Sharing" todavía se aplica en el sentido de que estas políticas deben ser transparentes y 
  aplicarse de manera justa.
- ## Network Jitter
  id:: 64f479c5-d9de-4454-87ce-a64fadfa103e
- Variación en el tiempo de llegada de los paquetes de datos en una red. En otras palabras, es la inconsistencia en la latencia de la red. En una red perfecta, los paquetes de datos llegarían exactamente cuando 
  se espera que lo hagan. Sin embargo, en el mundo real, las cosas no siempre suceden de manera perfecta y los paquetes de datos pueden llegar antes o después de lo esperado. Esta variación en el tiempo de llegada 
  se conoce como jitter.
- El jitter puede ser causado por una variedad de factores, incluyendo la congestión de la red, la falta de ancho de banda y la mala calidad de la conexión. Puede tener un impacto significativo en la calidad de las 
  llamadas de voz y video, así como en la transmisión de datos en tiempo real.
- ## Ethernet Basic Framing
- Refiere a una estructura básica de un paquete de datos en una red Ethernet. Un marco Ethernet típico incluye los siguientes componentes
- **Preamble**: Secuencia de bits que indica el comienzo de un margo. Eso permite a los dispositivos en la red sincronizarse y prepararse para recibir el resto del marco
- **Direcciones de destino y origen**: Direcciones MAC del dispositivo de origen y destino del marco
- **Tipo**: Indica el protocolo de nivel superior al que se debe pasar los datos del marco. Por ejemplo podría indicar que los datos deben ser procesados por el protocolo IP
- **FCS (Frame Check Sequence)**: Código de detección de errores que se utiliza para verificar que el marco no se ha corrompido en la transmisión.
- ## Point-to-Point Basic Framing
- Refiere a la estructura básica de un paquete de datos en una conexión de línea serial punto a punto. En este tipo de conexión, los datos se transmiten de un 
  dispositivo a otro a través de una línea de comunicación directa.  Un marco básico en una línea serial punto a punto podría incluir los siguientes componentes:
- **Preamble**: Una secuencia de bits que indica el comienzo de un marco.
- **Control Code**: Este campo puede indicar el papel del paquete, como control, información o datos.
- **Length Field**: Este campo puede indicar la longitud del paquete.
- **Data**: Esta es la carga útil del marco, es decir, los datos reales que se están enviando.
- **Checksum**: Este es un código de detección de errores que se utiliza 
  para verificar que el marco no se ha corrompido durante la transmisión.
- **End of Frame Marker**: Este es un indicador que señala el final del marco.
- Es importante tener en cuenta que en una conexión de línea serial punto a punto, no hay necesidad de incluir direcciones en el marco, ya que solo hay un dispositivo posible al que se puede enviar el marco. Sin embargo, la estructura exacta del marco puede variar dependiendo del protocolo específico que se esté utilizando.
-