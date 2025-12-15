# Resumen: Direccionamiento IP, Enrutamiento y Conmutación

Enhorabuena Ha completado este módulo. A estas alturas del módulo, ya sabes:

- Una dirección IP es un número decimal punteado que involucra números binarios con base 2. Estos números binarios pueden convertirse a sistemas numéricos octal, decimal y hexadecimal con bases 8, 10 y 16.

- Para calcular las representaciones numéricas, eleve la base a la potencia del número de dígitos disponibles.

- Para convertir del sistema de base al decimal, dibuje una tabla en la que los encabezados de las columnas representen la base elevada a potencias crecientes.

- Desde su introducción en 1983, el Protocolo de Internet versión 4 (IPv4) ha sido el protocolo fundamental para identificar y localizar dispositivos en las redes.

- Utiliza un esquema de direccionamiento de 32 bits dividido en cuatro octetos, cada uno de los cuales representa un segmento de la dirección, crucial para la identificación de redes y hosts.

- Las redes de clase A, B, C, D y E clasifican las direcciones en función de su alcance y uso previsto, desde la comunicación unidifusión a la multidifusión y fines experimentales.

- A pesar de su adopción generalizada, IPv4 se enfrenta a retos como el agotamiento de las direcciones debido al rápido crecimiento de los dispositivos conectados a Internet, lo que ha impulsado el desarrollo de IPv6.

- El Protocolo de Internet (IP) y las direcciones IP enrutan los paquetes de datos dentro de las redes y a través de Internet para una comunicación fiable.

- Los protocolos enrutables, como IP, pueden enrutarse fuera de la red de origen; es crucial conocer las máscaras de subred y las pasarelas por defecto.

- El encabezado del protocolo IP incluye la versión (IPv4 o IPv6) y otros elementos necesarios para la inspección y el procesamiento de paquetes.

- Las direcciones IP de origen identifican al remitente, y las direcciones IP de destino indican dónde se envía el paquete.

- Las máscaras de red dividen una dirección IP en segmentos de red y de host; el prefijo indica el número de bits utilizados para la parte de red.

- Las pasarelas por defecto reenvían paquetes fuera de la red local, gestionando el tráfico entre sistemas internos y externos.

- Las direcciones IP de broadcast tienen activados todos los bits de la parte de host, lo que permite la comunicación con todos los dispositivos de un segmento de red.

- IPv6 amplía las direcciones IP de 32 a 128 bits, aumentando enormemente el número de direcciones posibles.

- Las direcciones IPv6 utilizan ocho conjuntos de cuatro dígitos hexadecimales, cada conjunto separado por dos puntos.

- En IPv6, los dos puntos dobles pueden sustituir a los ceros consecutivos en una dirección. Las cabeceras de IPv6 son más sencillas y eficaces que las de IPv4, lo que mejora la velocidad de procesamiento. IPv6 admite Unicast, Multicast y Anycast, sustituyendo el método broadcast de IPv4 por Anycast.

- Las interfaces de red pueden ser un único chip o una tarjeta de interfaz de red completa, comúnmente denominada NIC.

- La suplantación de identidad Mac elude el filtrado de direcciones MAC mediante la configuración de un cortafuegos para proteger los activos.

- Una dirección MAC tiene 48 bits de longitud, o una cadena de 48 1s y 0s dividida en 6 octetos o 6 grupos de 8 bits cada uno.

- Los dominios de difusión también pueden denominarse LAN virtuales (VLAN).

- El protocolo de resolución de direcciones (ARP) es fundamental en las redes. Traduce direcciones IP a direcciones MAC para una transmisión de datos eficaz entre dispositivos dentro del mismo dominio de difusión.

- La Tabla de ARP, accesible a través de comandos como arp -a, proporciona asignaciones cruciales de direcciones IP a direcciones MAC, ayudando en la solución de problemas y la gestión de redes a través de diferentes sistemas operativos.

- Las direcciones MAC son esenciales para transmitir datos dentro del mismo dominio de difusión o red local.

- Las tablas de enrutamiento son cruciales para dirigir y optimizar el tráfico de red dentro de las organizaciones, garantizando una comunicación fluida entre los diferentes departamentos y edificios.

- Las interfaces de red específicas (enp0s9, enp0s8, enp0s3) gestionan el tráfico dentro de sus respectivos dominios de difusión, mientras que los conmutadores utilizan tablas MAC para una entrega eficiente de paquetes basada en direcciones MAC.

- Las redes están interconectadas a través de routers que abarcan múltiples dominios de difusión.

- La entrega de paquetes a través de las redes se facilita mediante la configuración de rutas por defecto y el mantenimiento de Tablas de ARP.

- Las tablas de enrutamiento dentro de los routers son cruciales para determinar las rutas más eficientes para el reenvío de paquetes.

- Las Tablas de ARP juegan un papel crucial en los routers mapeando direcciones IP a direcciones MAC para dispositivos en la misma red.

- Los routers mejoran la comunicación entre departamentos facilitando la transferencia fiable de documentos a través de distintos segmentos de red.

- Las rutas por defecto sirven para reenviar paquetes a destinos que no figuran explícitamente en la tabla de enrutamiento, garantizando la conectividad incluso cuando se desconocen detalles específicos de la red.

- Las rutas de conexión directa indican las redes accesibles a través de las interfaces de un enrutador, lo que simplifica la comunicación dentro de segmentos de red inmediatos.

- Las rutas dinámicas, gestionadas mediante protocolos como OSPF y EIGRP, automatizan las actualizaciones de rutas en función de las condiciones de la red, mejorando la eficacia y la adaptabilidad en entornos de red complejos.

- Las redes determinan las rutas de reenvío de paquetes mediante tablas de enrutamiento, dirigiendo el tráfico en función de las direcciones IP de destino.
