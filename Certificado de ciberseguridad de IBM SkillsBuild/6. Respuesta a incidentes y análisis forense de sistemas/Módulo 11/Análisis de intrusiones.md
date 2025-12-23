# Análisis de intrusiones

Cuando un sistema alerta a un equipo de respuesta a incidentes sobre un ciberataque, es fácil entrar en pánico. El plan de respuesta a incidentes tiene muchas instrucciones, pero ¿cómo decide el equipo cuáles seguir?

En esta lección, aprenderás sobre el análisis de intrusiones y el proceso de recopilación e interpretación de información sobre un ataque para que el equipo de respuesta a incidentes pueda formular una respuesta eficaz.

## ¿Qué es el análisis de intrusiones?

Cuando las herramientas de monitoreo detectan un incidente de ciberseguridad, el equipo de respuesta a incidentes (IR) recopila cualquier información disponible de registros del sistema, usuarios u otras fuentes. Luego, el equipo realiza un análisis de intrusiones como uno de sus primeros pasos.

El análisis de intrusiones es el proceso de emplear información sobre un ataque para determinar el alcance del ataque, el método empleado por el atacante para obtener acceso y el alcance del daño al sistema o la red.

## Áreas clave del análisis de intrusiones

A grandes rasgos, el análisis de intrusiones incluye cuatro áreas clave. Los equipos de IR deben investigar cada uno de ellos para desarrollar una imagen completa del ataque. Los modelos de la industria difieren en la manera en que describen el proceso de análisis de intrusiones, pero generalmente se centran en responder preguntas sobre estas cuatro áreas.

- **Adversario** Los equipos de IR se plantean las siguientes preguntas sobre el adversario que está detrás del ataque:

  - ¿Quiénes son los atacantes?

  - ¿Tienen un patrocinador?

  - ¿Desde dónde atacaron?

  - ¿Por qué atacaron?

  - ¿Cómo planearon el ataque?

- **Infraestructura** Los equipos de IR se hacen las siguientes preguntas para determinar cómo los atacantes podrían obtener acceso:

  - ¿El sistema contiene equipos infectados, nombres de dominio comprometidos, servidores u otro acceso no autorizado a los sistemas o servicios de datos de la organización?

  - ¿Los inicios de sesión comprometidos u otras credenciales esenciales tienen acceso a los sistemas?

  - ¿Los atacantes violaron físicamente o invadieron las instalaciones de la organización?

- **Capacidad** Los equipos de IR se hacen las siguientes preguntas sobre las capacidades de los atacantes:

  - ¿Qué habilidades tienen los atacantes para lanzar ataques, explotar vulnerabilidades y desplegar malware por control remoto?

  - ¿Qué habilidades tienen para desarrollar sus herramientas?

  - ¿Pueden realizar el reconocimiento necesario de la organización?

  - ¿Pueden los atacantes recuperar el acceso a los recursos de la organización en este momento?

- **Objetivo** Los equipos de TI se hacen las siguientes preguntas para determinar lo que los atacantes podrían querer:

  - ¿Qué datos atacaron y por qué los consideran valiosos?

  - ¿Parece que el ataque está dirigido a alguna persona?

  - ¿El ataque parece tener como objetivo dañar a un sector industrial o a un competidor, o incluso a un país?

## Marcos de análisis de intrusiones

El análisis eficaz de intrusiones se deriva de aprender a "pensar como un atacante". Un marco de análisis de intrusiones es una herramienta de planeación esencial porque describe las tácticas, estrategias y objetivos típicos de los atacantes. La elección de un marco establecido proporciona al equipo de IR un punto de partida sólido para comprender lo que se pretende lograr con los ataques. Al comprender los métodos y objetivos de los atacantes, el equipo puede planear la mejor respuesta para bloquear los ataques.

Ningún marco único se adaptará a las necesidades de todas las organizaciones. El equipo que elabora un plan de respuesta a incidentes debe investigar y evaluar la estructura y los objetivos de seguridad de su organización, y adaptar el marco en consecuencia. Sin embargo, examinar algunos marcos de ejemplo ayuda a tomar una decisión que coincida con los requisitos.

Exploremos dos marcos populares y efectivos para el análisis de intrusiones:

- Marco MITRE ATT&CK

- Marco Cyber Kill Chain

### Marco MITRE ATT&CK

El marco MITRE ATT&CK es un valioso recurso en el análisis de intrusiones. Puede ayudar a los analistas a identificar cómo accedieron los atacantes a las redes, qué herramientas emplearon y qué pasos siguieron para ejecutar el ataque. Aunque ningún marco es perfecto, el marco ATT&CK de MITRE sigue siendo uno de los modelos más sólidos del sector.

Basado en observaciones del mundo real, el marco proporciona una plataforma de investigación que los profesionales de la seguridad emplean para evaluar la postura de seguridad de su organización frente a adversarios avanzados. Los equipos de IR también emplean esta plataforma de código abierto para compartir tácticas de defensa y mejores prácticas.

La matriz MITRE ATT&CK contiene un conjunto de tácticas que los adversarios emplean para lograr un objetivo específico. Los objetivos aparecen más o menos en el orden en que los realizan los atacantes, desde el primer paso de reconocimiento hasta el objetivo final de impacto. Sin embargo, reconoce que algunos pasos tácticos pueden darse en un orden diferente o no ocurrir en absoluto.

1. **Reconocimiento** Los atacantes recopilan información para planear futuras operaciones del adversario, como buscar información sobre la organización objetivo.

2. **Desarrollo de recursos** Los atacantes establecen recursos para respaldar las operaciones de ataque, como codificar herramientas de ataque y crear infraestructura de control.

3. **Acceso inicial** Los atacantes intentan entrar en su red, por ejemplo, explotando un error de software.

4. **Ejecución** Los atacantes ejecutan código malicioso, como el despliegue de un virus.

5. **Persistencia** Los atacantes intentan mantener un punto de apoyo, por ejemplo, cambiando configuraciones si el sistema de IR se defiende contra el ataque.

6. **Escalada de privilegios** Los atacantes intentan obtener permisos de nivel superior, como usar una vulnerabilidad para elevar el acceso a más datos.

7. **Evasión de defensa** Los atacantes intentan evitar la detección, como usar procesos confiables para ocultar el malware.

8. **Acceso a credenciales** Los atacantes roban nombres de cuentas y contraseñas para aumentar el acceso, como el uso de una herramienta de registro de pulsaciones de teclas.

9. **Descubrimiento** Los atacantes intentan descifrar el entorno, por ejemplo, explorando lo que pueden controlar y que antes no sabían.

10. **Movimiento lateral** Los atacantes se mueven por el entorno para encontrar más objetivos, como usar credenciales legítimas para pasar por múltiples sistemas.

11. **Recopilación** Los atacantes recopilan datos de interés para el objetivo, como el acceso a datos en la nube y el almacenamiento en el sitio.

12. **Mando y control** Los atacantes se comunican con sistemas comprometidos para controlarlos, como imitar el tráfico web normal para comunicarse con una red víctima.

13. **Exfiltración** Los atacantes completan el robo de datos, como la transferencia de datos a la cuenta en la nube de un atacante.

14. **Impacto** Los atacantes manipulan, interrumpen o destruyen sistemas y datos, como cifrar datos con ransomware.

### Marco Cyber Kill Chain

El marco Cyber Kill Chain es otra herramienta valiosa para el análisis de intrusiones. Al igual que el marco MITRE ATT&CK, el marco Cyber Kill Chain proporciona una estructura para identificar, comprender, aislar y responder al comportamiento malicioso.

Los dos marcos tienen un número diferente de pasos, aunque algunos son comparables. Sin embargo, una idea importante diferencia el marco Cyber Kill Chain del marco MITRE ATT&CK. El marco Cyber Kill Chain estipula que los objetivos son más importantes que las técnicas y que los atacantes deben seguir el orden establecido para tener éxito. En otras palabras, MITRE ATT&CK se centra en contrarrestar las técnicas que emplean los atacantes, mientras que Cyber Kill Chain se centra en sus objetivos, independientemente de cómo los consigan, y Cyber Kill Chain establece que los ataques no tendrán éxito si no siguen un orden concreto de pasos.

1. **Reconocimiento** En el reconocimiento, también llamado observación, los atacantes suelen evaluar la situación desde el exterior para identificar objetivos y tácticas para el ataque.

2. **Armamento y entrega** Según lo que los atacantes descubren a partir del reconocimiento, ingresan al sistema objetivo, a menudo mediante malware o vulnerabilidades de seguridad.

3. **Explotación** Los atacantes explotan las vulnerabilidades para ampliar el acceso y enviar código malicioso al sistema para obtener una mejor posición.

4. **Escalada de privilegios** Los atacantes a menudo necesitan más privilegios del sistema para obtener acceso a los datos de destino, por lo que emplean el acceso explotado para escalar sus privilegios.

5. **Movimiento lateral** Cuando están en el sistema, los atacantes pueden moverse lateralmente a otros sistemas y cuentas para obtener mayores permisos, más datos o un mayor acceso a los sistemas.

6. **Ofuscación y antiforense** Para organizar con éxito un ataque cibernético, los atacantes deben ocultar sus acciones y, en este paso, a menudo dejan rastros falsos, comprometen datos y borran registros para confundir y retrasar al equipo de IR.

7. **Denegación de servicio** Los atacantes interrumpen el acceso normal de los usuarios y sistemas si el ataque tenía este objetivo, y esta interrupción también impide el monitoreo, seguimiento o bloqueo del ataque.

8. **Exfiltración** Los atacantes eliminan los datos del sistema comprometido si el ataque tenía este objetivo.
