# Visión General del Proyecto Final: Acceso Seguro

## Visión general

En este curso, aprendiste las habilidades cruciales para enfrentar las amenazas y desafíos digitales modernos y en evolución. Desde la detección de amenazas hasta las estrategias de prevención, aprendiste a proteger tus organizaciones y sistemas contra violaciones de datos. En este proyecto, explorarás un escenario inspirado en el mundo real, identificarás posibles vulnerabilidades de seguridad y proporcionarás recomendaciones para fortalecer la postura de seguridad general de la organización.

Este proyecto final consta de tres tareas:

1. Evaluar la infraestructura de seguridad existente de la organización
2. Crear un plan de autenticación multifactor (MFA)
3. Evaluar las medidas de seguridad física existentes de la organización

## Instrucciones generales

El proyecto final consiste en tres tareas, cada una con dos preguntas, lo que contribuye a un total de 15 puntos. Lee cuidadosamente los escenarios y las tareas que los acompañan. Luego, analiza críticamente cada pregunta y proporciona respuestas bien consideradas para demostrar tu comprensión y competencia.

Para completar este proyecto, debes responder todas las preguntas y enviar la tarea como prueba de que has cumplido con los requisitos del proyecto final. Puedes pausar y reanudar el proceso de envío según tu horario, dándote la flexibilidad de completar este proyecto a tu propio ritmo. Tu envío será calificado automáticamente utilizando una herramienta de IA.

## Escenario para la Tarea 1 y la Tarea 2

Eres un Analista de Seguridad Informática en TechSolutions Inc. La empresa ha experimentado recientemente una violación de datos debido a credenciales comprometidas.

TechSolutions Inc. actualmente emplea la siguiente infraestructura de seguridad:

- Los métodos tradicionales de control de acceso incluyen:

  - Inicio de sesión con nombre de usuario y contraseña para cada sistema y aplicación.
  - Claves SSH para acceder a servidores remotos.
  - Tarjetas inteligentes para un acceso físico y digital seguro en múltiples ubicaciones de la empresa y la VPN corporativa.

- Los recursos a los que los empleados requieren acceso:

  - Sistema de correo electrónico corporativo: Esencial para la comunicación diaria, tanto interna como con partes interesadas externas.
  - Bases de datos internas: Contiene información sensible como detalles de clientes, datos de proyectos y registros financieros.
  - Servicios de almacenamiento en la nube: Utilizados para almacenar y compartir documentos y trabajo colaborativo.
  - Sistemas de recursos humanos: Incorpora información personal de los empleados, administración de beneficios y datos de reclutamiento.
  - Software de gestión de relaciones con clientes (CRM): Crítico para las operaciones de ventas, marketing y servicio al cliente.
  - Herramientas de gestión de proyectos: Utilizadas para rastrear el progreso, asignar tareas y optimizar el flujo de trabajo.
  - Entornos de desarrollo: Requeridos para el desarrollo de software, pruebas de aplicaciones y gestión de repositorios de código.
  - Intranet de la empresa y bases de conocimiento: Proporciona acceso a políticas de la empresa, materiales de capacitación y plataformas de comunicación interna.

## Instrucciones de la Tarea 1

Esta tarea consta de dos preguntas y tiene un total de 6 puntos. Revise detenidamente el escenario anterior y responda las preguntas.

Revise la infraestructura de seguridad actualmente implementada en TechSolutions Inc. Esta tarea requerirá que utilice su comprensión de los principios de ciberseguridad y aplique el pensamiento crítico para evaluar y mejorar la infraestructura de seguridad de TechSolutions Inc.

**Observaciones**

Entre los puntos a mejorar en los sistemas de control de acceso actuales tenemos:

- Revisar las políticas de las contraseñas de usuarios examinar que tengan políticas fuertes y rotación de claves periódicas y como medida adicional establecer MFA para mejorar la seguridad de autorización.
- Establecer filtro antispam y antiphishing en el servidor de correo electrónico.
- Asegurar que la base de datos encripte los datos de identificación personal para este en concordancia con el cumplimiento de PI y PII.
- Revisar las políticas IAM estableciendo los permisos necesarios mínimos para el cumplimiento de las tareas de los usuarios. Y asignando a los usuarios el rol correspondiente para la creación, visualización y modificación de los mismos según sus privilegios.
- Asegurar que los sistemas de recursos humanos cumplan con las políticas de trato de los datos de PI y PII.
- Para el CRM si es un software de tercero debemos asegurar su disponibilidad esto puede ser a través de redundancia si es un software de desarrollo propio a parte de lo ya descrito hay que revisar el cumplimiento de las políticas de trato de los datos de PI y PII.
- El desarrollo de software va bien encaminado solo hay que analizar si se está incluyendo la seguridad en todas las fases del desarrollo.

Como medidas adicionales se recomienda.

- Hacer un escaneo de puertos y ver que no haya una exposición indebida.
- Hacer un inventario de red
- Instalación de antivirus en todas las estaciones de trabajo.
- Establecer políticas de actualización de software.
- Establecer un cronograma de capacitación a los usuarios sobre ingeniería social y la importancia de no compartir sus accesos al sistema.

## Instrucciones de la tarea 2

Esta tarea incluye dos preguntas con un valor total de 3 puntos.

Considera los diversos métodos de autenticación que aprendiste en este curso. Tu tarea es renovar el sistema de control de acceso en TechSolutions Inc. incorporando la autenticación multifactor (MFA) para protegerse contra futuros accesos no autorizados.

**Observaciones**

Para renovar el sistema de control de acceso implementaría 2 medidas.

- Un factor híbrido entre token que puede ser generado por aplicaciones como Authy o Google Authenticator entre otros. Son app livianas que puedes instalar en dispositivos como teléfonos inteligentes y otro por FIDO que es el enfoque más seguro actualmente pero no todos los dispositivos permiten la implementación del mismo y no es tan adoptado aún por los usuarios. Pero previendo que el futuro apunta hacia allí es mejor ir adoptandolo en la solución. Ejemplo el personal de IT puede comenzar con plan piloto de uso de FIDO en el ambiente de Desarrollo y en Base de Datos y luego ser impulsores de este en las distintas áreas de la organización.

- En áreas sensibles como servidores y aunque esto entra más en un control físico implementaria algun control biometrico, ya sea escaner de huellas con presencia de calor o lector de venas, o reconocimiento facial.

## Escenario para la Tarea 3

TechSolutions Inc. actualmente emplea las siguientes medidas de seguridad física:

- Recepción y vestíbulo: La entrada cuenta con un mostrador de recepción que siempre está atendido. El recepcionista toma los nombres de cada visitante y emite credenciales temporales para visitantes.

- Espacios de trabajo de empleados: Los espacios de trabajo de planta abierta para empleados son accesibles desde dos direcciones. Una entrada, ubicada cerca del mostrador del recepcionista, conduce a la parte frontal del área de trabajo, mientras que otra puerta en la parte trasera se abre al estacionamiento de empleados. Ambas entradas están claramente marcadas con letreros que dicen “Solo Personal Autorizado”. El recepcionista cierra con llave la puerta frontal, y la última persona que se va por el día cierra con llave la puerta trasera.

- Salas de reuniones y salones de conferencias: Los espacios de reunión más grandes están adyacentes al espacio de trabajo compartido. Cada uno de estos espacios tiene puertas que se pueden cerrar con llave. Las reservas para estos espacios se pueden hacer a través de un sistema central de calendario.

- Centros de datos y salas de servidores: Estas áreas críticas están equipadas con puertas con cerradura, con acceso restringido al personal de TI y de limpieza. Además, estas habitaciones están equipadas con un termostato y un sensor de humedad para fines de monitoreo.

- Almacenamiento de archivos: Los gabinetes de archivos con mecanismos de bloqueo están ubicados estratégicamente en toda la oficina para asegurar que los documentos sensibles estén seguros y sean accesibles solo por personal autorizado.

- Estacionamiento: El estacionamiento de empleados está cerrado por una cerca con un solo punto de entrada. Se requieren calcomanías de estacionamiento para acceder a este estacionamiento.

- Áreas comunes y instalaciones: Las salas de descanso y los baños están adyacentes al área de trabajo común. Las puertas que conducen a estas áreas no tienen cerraduras.

## Instrucciones de la Tarea 3

Esta tarea consiste en dos preguntas que suman 6 puntos. Revisa detenidamente el escenario y responde las preguntas.

Revisa las medidas de seguridad física actualmente desplegadas en TechSolutions Inc. Esta tarea requerirá que aproveches tu comprensión de los principios de ciberseguridad y apliques el pensamiento crítico para evaluar y mejorar las medidas de seguridad física en TechSolutions Inc.

**Observaciones**

A continuación se listan una serie de mejoras que se pueden adoptar para aumentar los controles físicos.

Una cámara de monitoreo en el estacionamiento para filmar quien entra por ese acceso, además colocar las señales correspondientes como el cartel de que está siendo grabado como medida persuasoria.
Una cámara en la recepción del vestíbulo para grabar el acceso de personas a las instalaciones, esto sirve para constatar la información recolectada por el personal de recepción.
Las puertas de entrada desde la recepción y el estacionamiento además de la cerradura deben tener un panel de control de acceso activado por tarjetas de acceso.
En las salas de reuniones el control de acceso parece idóneo pero se debe asegurar que los activos estén fijos ya sea por cables de protección para las laptops e impresoras o la fijación de video beam entre otros equipos. Además de si se cuentan con gabinetes con recursos como borradores, marcadores deben estar resguardado con llave que se le entregará al responsable de la sala en uso, si se cuenta con dispositivos de visualización como un televisor o una pantalla de ser posible se le debe adaptar un filtro de visión que limite el ángulo de observación .
Centro de datos y salas de servidores deben estar resguardado con cerraduras biometricas además de contar con protectores de voltaje y suministro de energía en caso de fallos como ups o una planta de poder, estas áreas sensibles deben tener aires acondicionados de precisión y deshumidificadores además de protección contra estáticas, los rack deben estar asegurados y bloqueados, igual que los puertos de acceso como usb. Contar con sistema de extintores adecuados para la sala no basado en agua sino de agentes limpios como CO~2~.
