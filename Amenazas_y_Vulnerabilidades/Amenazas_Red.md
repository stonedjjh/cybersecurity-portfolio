# Amenazas en la red

## El mapeo de redes

El mapeo de redes es el proceso de comprender y visualizar las conexiones físicas y lógicas de una red.

Implica descubrir dispositivos de red, como enrutadores, conmutadores, firewalls y servidores, y comprender sus interacciones. Como administrador, puede seleccionar entre una variedad de herramientas para evaluar la topología de la red y reconocer los nodos, los servicios, los sistemas operativos y las rutas de datos. Una herramienta popular de mapeo de redes es Network Mapper o Nmap.

### Beneficios

- El mapeo de red ayuda a gestionar la complejidad de la red al representar claramente los componentes de la red y sus interconexiones. Con un mapa bien definido, puede identificar y solucionar problemas con facilidad, como puntos de falla o cuellos de botella, y planificar de manera eficiente las expansiones o configuraciones de la red.

- Un mapa de red actualizado es crucial para mantener la seguridad, ya que detecta rápidamente cualquier anomalía, como dispositivos no autorizados o cambios dentro de la red. El mapeo de redes apoya la gestión proactiva de la red y la planificación estratégica.

- Permite una documentación eficiente de la estructura de la red, lo que es útil tanto para planificar la expansión futura como para mantener la infraestructura existente.

### Uso por atacantes

- Al igual que un ladrón inspecciona una casa o un negocio antes de entrar, los atacantes utilizan herramientas de mapeo de red para descubrir información sobre la estructura de la red.

- Identifican los puntos de entrada no vigilados y los sistemas vulnerables y anotan los diferentes tipos de defensas existentes. Luego, los atacantes navegan por la red con un menor riesgo de detección.

- Pueden deducir la escala, la complejidad y la jerarquía de la red, lo que les ayuda a priorizar los segmentos a los que atacar primero.

- Los atacantes también pueden deducir la presencia de activos de alto valor, como bases de datos y sistemas administrativos, mediante el análisis de los patrones de tráfico o las ubicaciones de dispositivos específicos.

- Los atacantes pueden usar el mapeo de redes para crear campañas de suplantación de identidad o ataques de ingeniería social a medida. El atacante lleva a cabo la campaña al comprender el papel de los diferentes nodos, como las estaciones de trabajo utilizadas por los empleados con acceso a información confidencial.

## Sniffing de paquetes

La seguridad de Internet se enfrenta a un gran problema llamado detección de paquetes. Es como si alguien se colara en la información que se envía por Internet sin permiso.

Imagine un escenario en el que la red de una organización experimente ralentizaciones inusuales y, a pesar de los diagnósticos iniciales, se desconoce la causa principal. Aquí es donde entra en juego el concepto de rastreo de paquetes.

La detección de paquetes es una técnica que implica el uso de software para capturar y analizar paquetes de datos a medida que se mueven por una red. Cuando se implementa, este software recopila varios puntos de datos al interceptar el tráfico. En este escenario, la detección de paquetes podría revelar que el exceso de videoconferencias durante las horas punta
congestiona el ancho de banda.

Los rastreadores de paquetes funcionan colocando la tarjeta de interfaz de red ( NIC) del equipo analizador en modo promiscuo. Por lo general, una NIC solo presta atención a la dirección de tráfico hacia ella. Sin embargo, en el modo promiscuo, captura todo el tráfico de la red, independientemente del destino. Por ejemplo, cuando una NIC está en modo promiscuo, el rastreador de paquetes puede monitorear todo el tráfico en el segmento de red conectado. A continuación, el rastreador interpreta y decodifica el contenido del paquete, revelando los datos que contienen, siguiendo protocolos como IP, TCP, UDP y HTTP.

### Beneficios

Estas son algunas de las tareas que realizan los profesionales de TI con la ayuda del rastreo de paquetes.

- Emplean la detección de paquetes para el diagnóstico de la red. Pueden examinar los paquetes de datos para identificar actividades sospechosas o diagnosticar problemas de red.

- Son útiles para monitorear el rendimiento, ya que proporcionan datos críticos sobre el consumo de ancho de banda, lo que ayuda a identificar los acaparadores de recursos y los cuellos de botella de la red.

- Los administradores de red también pueden usar rastreadores de paquetes para monitorear la actividad web, incluido el seguimiento de los sitios web visitados y la naturaleza del contenido al que se accede, así como para supervisar los intercambios de comunicación, como los correos electrónicos.

> [!Warning]
Sin embargo, es importante recordar que la detección de paquetes solo es aceptable en las redes que están bajo el control de la organización. La detección de paquetes se convierte en ilegal cuando las personas capturan paquetes de datos sin autorización.

### Uso por atacantes

Ataque de rastreo, implica que los atacantes usen software para interceptar y examinar paquetes de datos no cifrados que contienen información confidencial. Estos datos comprometidos suelen incluir identificadores personales como nombres, direcciones físicas y números de teléfono, y datos financieros, incluidos los detalles de las cuentas bancarias y las credenciales de inicio de sesión de los usuarios.

La falta de medidas avanzadas de ciberseguridad deja a las redes vulnerables a una mayor explotación mediante técnicas como el protocolo de resolución de direcciones, **la manipulación de ARP(ARP Spoofing)**, el sistema de nombres de dominio, **el DNS Poisoning**, la falsificación o la introducción de código dañino en los flujos de datos mediante métodos como **la inyección de SQL**.

Existen principalmente dos tipos de tácticas de detección de paquetes, la detección pasiva y la detección activa.

- En la detección pasiva, un espía se conecta discretamente a una red en la que se comunican varios dispositivos, como redes de área local, LAN o redes WiFi, y monitorea silenciosamente el intercambio de datos. Esta táctica imita el espionaje subrepticio o las escuchas telefónicas, lo que dificulta la detección. Por ejemplo, un atacante en un punto de acceso WiFi público puede interceptar discretamente paquetes de datos entre usuarios sin su conocimiento.

- Por otro lado, los objetivos de rastreo activo cambiaron de red al introducir tráfico adicional para manipular el flujo de datos. Por ejemplo, en un entorno Ethernet corporativo, un atacante genera una actividad de red adicional, lo que hace que los conmutadores transmitan datos ampliamente y permite la interceptación de paquetes específicos.

## Medidas de Proteccion de la red

Para proteger su red contra la detección no autorizada de paquetes, implemente estas estrategias.

- Actualice periódicamente el software y los sistemas para cerrar las vulnerabilidades de seguridad que impiden las ciberintrusiones.

- Refuerce las medidas de inicio de sesión creando contraseñas seguras y empleando métodos de verificación adicionales, como la autenticación de dos o varios factores, para mejorar la seguridad.

- Esté atento a los correos electrónicos de fuentes desconocidas y evite los archivos adjuntos o enlaces sospechosos que podrían ser herramientas de suplantación de identidad que inicien ataques de rastreo de paquetes.

- Utilice una red privada virtual, VPN, para actividades cifradas en línea, especialmente en redes WiFi públicas susceptibles a las amenazas de rastreo de paquetes.

- Priorice los sitios web cifrados con HTTPS para una navegación más segura, prestando atención a las advertencias del navegador sobre los sitios HTTP no seguros.
