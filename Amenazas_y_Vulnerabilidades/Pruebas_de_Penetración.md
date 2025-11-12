# Pruebas de penetración

Los escáneres de vulnerabilidades ayudan a identificar vulnerabilidades. Estos escaneos son rápidos y no invasivos, por lo que puedes realizarlos de manera regular para encontrar vulnerabilidades comunes.

Pero, ¿cómo se confirman los hallazgos del escaneo? ¿Cómo sabes que las vulnerabilidades identificadas son debilidades reales que los atacantes podrían explotar? ¿Cómo sabes que los atacantes no descubrirán otras vulnerabilidades que el escáner pasó por alto? La respuesta a estas preguntas son las pruebas de penetración.

**Las pruebas de penetración** son un tipo de pruebas de seguridad que simulan técnicas reales de hackeo para encontrar vulnerabilidades de aplicaciones, redes o sistemas que los atacantes pueden explotar.

## Fases

Esta fase suele implicar los siguientes pasos.

- **Planificación** ¿Cuáles son el alcance, los objetivos, los sistemas objetivo y las restricciones de la prueba?

- **Planificación** ¿Cuáles son el alcance, los objetivos, los sistemas objetivo y las restricciones de la prueba?

- **Recopilación de información** ¿Cómo podrás recopilar, crear y notificar la inteligencia de amenazas pertinente?

- **Pruebas** ¿Qué métodos de ataque usarás?

- **Presentación de informes** ¿Cómo compartirás tus hallazgos y recomendaciones con el cliente?

### Fase 1 Planeación

En la primera fase de las pruebas de penetración, la planeación, el evaluador de penetración y el cliente colaboran para planear la prueba.

**Propósitos**
  
Esta fase tiene dos objetivos:

1. Cerciorarse de que el evaluador realice la prueba de penetración de manera segura y controlada
2. Cerciorarse de que la prueba siga objetivos claros alineados con los objetivos de seguridad del cliente

**Pasos**

Esta fase suele implicar los siguientes pasos.

1. **Determinar el alcance** El evaluador y el cliente definen el alcance de la prueba, incluidos los sistemas, las aplicaciones y la infraestructura de red a evaluar. También identifican activos y sistemas críticos que requieren protección y señalan otros posibles puntos de vulnerabilidad.
2. **Determinar los objetivos** El evaluador y el cliente determinan los objetivos de la prueba. Estos objetivos pueden incluir la identificación de posibles vulnerabilidades o la evaluación de los controles de seguridad existentes.
3. **Recopilar información sobre los sistemas de destino** El evaluador recopila información sobre los sistemas de destino para comprender mejor el entorno del cliente e identificar posibles vulnerabilidades. Esta información puede incluir diagramas de red, direcciones IP y configuraciones del sistema.
4. **Desarrollar un plan de prueba** El evaluador desarrolla un plan de prueba. Este plan describe las pruebas específicas que se deben realizar, las herramientas y técnicas que se deben usar y los resultados que se esperan.
5. **Obtener autorizaciones** Antes de que comiencen las pruebas de penetración, el evaluador debe recibir la autorización del cliente para realizar pruebas y acceder a los sistemas y datos seguros del cliente.

#### Reglas de compromiso

Un acuerdo verbal sobre el plan y el alcance de las pruebas no es suficiente. Debido a la naturaleza disruptiva de las pruebas de penetración y a las posibles consecuencias, el evaluador y el cliente deben llegar a un acuerdo legal antes de que comiencen las pruebas. Por lo general, este acuerdo incluye un contrato de reglas de compromiso que el evaluador y el representante autorizado del cliente deben firmar.

Este documento describe el alcance de las pruebas de penetración y, por lo general, incluye la siguiente información.

  1. **Qué se evaluará** El documento describe qué objetivos probar. Por ejemplo, el evaluador podría atacar aplicaciones. Puede atacar toda una red o solo dispositivos en esa red, incluidos teléfonos inteligentes, computadoras de escritorio y enrutadores. Incluso podría simular ataques de ingeniería social, como el phishing, para determinar la probabilidad de que los empleados caigan en estos trucos y divulguen información confidencial.
  2. **Qué no se evaluará** El documento describe lo que no se debe evaluar. Por ejemplo, un cliente podría prohibir la modificación o eliminación de pistas de auditoría que muestren evidencia de las acciones del evaluador. O el cliente podría prohibir probar sistemas específicos.
  3. **Cuándo evaluar** El documento describe cuándo realizar la prueba. Por ejemplo, el cliente podría prohibir las pruebas de penetración durante el horario laboral. Las pruebas de penetración, al igual que los ciberataques reales, pueden interrumpir significativamente las operaciones.
  4. **Cómo compartir resultados** El documento describe las expectativas para informar resultados. Por ejemplo, el cliente podría solicitar actualizaciones periódicas o solo un informe final. Los requisitos de comunicación pueden variar según el nivel de riesgo. Por ejemplo, el cliente podría requerir que el evaluador informe las vulnerabilidades críticas inmediatamente después de encontrarlas.
  5. **Cómo demostrar que las pruebas fueron satisfactorias** El documento describe cómo el evaluador debe demostrar que completó las pruebas de manera satisfactoria. Por ejemplo, el evaluador puede proporcionar un archivo de texto generado por la herramienta de prueba de penetración o una captura de pantalla de los resultados.

### Fase 2: Recopilación de información

En la segunda fase, recopilación de información, el evaluador recopila y crea inteligencia de amenazas. Esta inteligencia va más allá de la información limitada que se encuentra en la fase de planeación. Con las reglas de interacción implementadas, el evaluador ahora puede investigar el objetivo tan a fondo como lo permita el alcance.

**Propósitos**

Esta fase tiene varios propósitos:

1. Evaluar la postura de seguridad actual de la organización

2. Determinar qué vulnerabilidades abordar

3. Proporcionar al cliente un resumen preciso de su postura de seguridad actual

**Pasos**

Esta fase suele incluir los siguientes pasos.

- **Footprinting o reconocimiento** En el footprinting o reconocimiento, el evaluador hace un perfil del sistema y sus usuarios. Por ejemplo, podría recopilar las direcciones IP y los nombres de dominio de la red y determinar su topología.

- **Enumeración** En la enumeración, el evaluador emplea herramientas para sondear el sistema en busca de datos sobre hosts y servicios activos en una red. Algunos ejemplos de estos datos incluyen sistemas operativos (SO), nombres de dispositivos, nombres de usuario y detalles del servidor web.

- **Escaneo de vulnerabilidades** El evaluador emplea un escáner de vulnerabilidades para identificar vulnerabilidades en los hosts y servicios activos descubiertos a través de la enumeración.

- **Análisis e informes** Cuando termina de escanear, el evaluador analiza los resultados y prioriza las vulnerabilidades por gravedad y explotabilidad. Por lo general, el evaluador informa sus hallazgos y conclusiones al cliente en este punto.

### Fase 3: Pruebas

En la tercera fase, pruebas, el evaluador realiza ataques simulados en la aplicación, el sistema o la red. Esta fase es el núcleo de las pruebas de penetración. El evaluador penetra en el sistema del cliente dentro del alcance acordado para acceder a datos confidenciales o funciones esenciales del sistema.

**Propósitos**

Esta fase tiene varios propósitos:

1. Explotar las vulnerabilidades identificadas en la fase anterior para confirmar su existencia

2. Encontrar y explotar otras vulnerabilidades

**Métodos**

Esta fase puede incluir varios ataques, incluidos los siguientes ejemplos.

- **Descifrado de contraseñas** El evaluador de pruebas de penetración podría intentar descubrir contraseñas mediante herramientas de descifrado de contraseñas.

- **Ingeniería social** El evaluador de pruebas de penetración podría usar técnicas de ingeniería social, como el phishing, para engañar al personal para que divulgue datos confidenciales u otorgue acceso directo a sus cuentas.

- **Ataques específicos de la red** El evaluador de pruebas de penetración podría atacar vulnerabilidades de red, como puertos abiertos y servicios no seguros.

- **Inyección SQL** La inyección SQL es un ataque que coloca código malicioso en una instrucción de lenguaje de consulta estructurado (SQL) a través de una aplicación o sitio web. Los atacantes suelen emplear una solicitud de entrada de usuario, como un nombre de usuario, para introducir la instrucción SQL, que se ejecuta en la base de datos del servidor.

- **Cross-site scripting (XSS)** Cross-site scripting (XSS) es un ataque que inserta código malicioso en un sitio web cliente. Cuando un usuario accede a la página, su navegador reconoce el código como procedente de un sitio de confianza, lo que permite que el código se ejecute.

- **Ataques específicos de la aplicación** El evaluador de pruebas de penetración ataca otras vulnerabilidades específicas de aplicaciones web, aplicaciones móviles u otro software.

### Fase 4: Elaboración de informes

En la cuarta fase, elaboración de informes, el evaluador de pruebas de penetración documenta sus hallazgos y los informa al cliente y a cualquier otra parte implicada. El cliente debe entender los riesgos de seguridad y poseer la información necesaria para mejorar la postura de seguridad de su organización.

**Propósito**

Esta fase tiene un propósito: proporcionar al cliente información y recomendaciones prácticas para mejorar su postura general de seguridad.

**Tipos de informes**

Esta fase incluye los siguientes tipos de informes.

- **Informe formal** El evaluador de pruebas de penetración documenta sus hallazgos en un informe formal. El informe suele detallar los métodos del evaluador, los resultados, la evidencia de respaldo y las recomendaciones para mejorar la seguridad.

- **Comunicación en persona** El evaluador de pruebas de penetración también comunica sus hallazgos en persona, por ejemplo, a través de una presentación. Con la comunicación en persona, el evaluador puede proporcionar contexto adicional para el informe y abordar preguntas sobre sus hallazgos y recomendaciones.

- **Soporte de corrección** El evaluador de pruebas de penetración ayuda al cliente a corregir las vulnerabilidades identificadas e implementar los controles necesarios. También podría ayudar a evaluar los riesgos asociados con las vulnerabilidades identificadas y priorizar los esfuerzos de corrección.

## Herramientas para la recopilación de información

- Los **mapeadores de red** encuentran y mapean todos los dispositivos en una red. También descubren datos sobre cada dispositivo, como su dirección IP. Algunos de los mapeadores de red más populares incluyen Angry IP Scanner y SolarWinds Network Topology Mapper.

- Los **escáneres de puertos** identifican los puertos abiertos o disponibles de una red. Un puerto es un punto de conexión de red que envía o recibe datos para un servicio específico, como el correo electrónico. Un puerto abierto es aquel que acepta una conexión. Los atacantes quieren encontrar y explotar los puertos abiertos, y los administradores de red quieren cerrarlos o bloquearlos garantizando al mismo tiempo que los usuarios legítimos sigan teniendo acceso.

Existen muchas herramientas de escaneo de puertos, como Netcat y SolarWinds Open Port Scanner, pero el escáner de puertos más conocido es Nmap. Nmap, abreviatura de Network Mapper, es un escáner de puertos y mapeador de red gratuito y de código abierto disponible para Windows, macOS, Linux y otros SO. La mayoría de las instalaciones de Nmap también incluyen Zenmap, la interfaz gráfica oficial de Nmap.

- Los **escáneres de vulnerabilidades** analizan un sistema en busca de vulnerabilidades conocidas, como software obsoleto, parches faltantes, configuraciones erróneas o contraseñas débiles. Algunos escáneres de vulnerabilidades populares incluyen Nessus, Burp Suite y OWASP ZAP.

- Los **analizadores de paquetes**, también conocidos como rastreadores de paquetes, analizadores de protocolos o analizadores de red, capturan e inspeccionan datos en tránsito a través de una red. Con un analizador de paquetes, puedes determinar la cantidad de tráfico, la frecuencia de transmisión y, posiblemente, incluso el contenido de los datos. Dos de los analizadores de paquetes más populares son tcpdump y Wireshark.

## Herramientas para atacar

Algunas de las herramientas de ataque más comunes son los marcos de explotación y las aplicaciones para descifrar contraseñas.

- **Marcos de explotación** Los marcos de explotación proporcionan repositorios de ataques y exploits prediseñados. Considera el proyecto Metasploit, una herramienta para encontrar exploits existentes o compartir los propios. Con la aplicación Metasploit, puedes automatizar una variedad de ataques según la arquitectura del objetivo. Por ejemplo, puedes buscar ataques adaptados a una versión específica de un sistema operativo al que deseas apuntar y luego dejar que Metasploit realice el ataque.

- **Herramientas para descifrar contraseñas** Las herramientas de descifrado de contraseñas hacen lo que esperas; te ayudan a descubrir contraseñas anulando el cifrado o realizando ataques de fuerza bruta. Un ataque de fuerza bruta es cuando el atacante emplea prueba y error, probando diferentes contraseñas hasta que encuentra una que funcione. Una de las herramientas más conocidas para descifrar contraseñas es John the Ripper.
