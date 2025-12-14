# Preguntas

## Según la respuesta a incidentes descrita en el video, ¿cuáles crees que son los elementos más críticos de un plan de respuesta a incidentes bien preparado?

1. Tener especificadas las tareas y responsables.
2. Que cada integrante revise sus responsailidades asignadas y confirme su aceptacion o realice los cambios pertinentes.
3. Luego de la mitigacion o recuperacion actualizar los sistemas como antivirus, ids, firewall etc. Para evitar futuros ataques con la misma vurnerabilidad.
4. Realizar un analisis forence para estudiar la tecnica y herramientas usadas y como prevenirlas en el futuro.

**Actividad**: Aplicar un marco de respuesta a incidentes adecuado (fase 1)

Lee los antecedentes sobre cómo HealthGuard Medical Services completó la fase de preparación de la respuesta a incidentes. Luego, aplica tu conocimiento de esta fase para responder a la pregunta que sigue.

**Antecedentes**

HealthGuard Medical Services es un proveedor líder de servicios médicos, incluidas consultas de telesalud y citas en línea. El equipo de TI de la empresa implementó protocolos de seguridad para evitar filtraciones de datos y otras amenazas de ciberseguridad. El equipo de TI estableció un programa regular de parches para todos los sistemas, aplicaciones y dispositivos para abordar las vulnerabilidades conocidas con prontitud. Además, implementaron la autenticación multifactor en todos los sistemas y aplicaciones para evitar el acceso no autorizado. El equipo de TI instaló un sistema de detección de intrusiones en la red para monitorear el tráfico y detectar posibles amenazas. El equipo de TI realizó de manera regular pruebas de simulación de phishing para capacitar a los empleados para identificar y evitar correo electrónicos de phishing.

HealthGuard Medical Services también cuenta con un equipo de respuesta a incidentes. El equipo de respuesta a incidentes implementó un plan de copia de seguridad de datos y recuperación ante desastres para garantizar que puedan restaurar datos críticos de forma rápida y segura durante un incidente de seguridad.

¿Qué opinas?

**Repuesta** Tienen un plan bastante solido, pero no establecieron los responsables en caso de un incidente, en caso de un incidente de ciberseguridad no están preparado para solucionarlo perderan tiempo estableciendo que hacer y quien hacerlo

**Actividad**: Aplicar un marco de respuesta a incidentes apropiado (fase 2)

Lee los siguientes antecedentes sobre cómo HealthGuard Medical Services completó la fase de detección y análisis de la respuesta a incidentes. A continuación, aplica tus conocimientos sobre esta fase para responder a la pregunta siguiente.

**Antecedentes**

El equipo de TI de HealthGuard Medical Services detectó actividad sospechosa en su red a través de herramientas de monitoreo de red, en su caso, sistemas de detección de intrusiones (IDS) y sistemas de prevención de intrusiones (IPS) que detectan anomalías y posibles violaciones de seguridad. El equipo de TI comenzó rápidamente a analizar el tráfico mediante su sistema de gestión de eventos e información de seguridad (SIEM) y descubrió que un atacante obtuvo acceso no autorizado a su sistema. El sistema SIEM detectó varios intentos fallidos de inicio de sesión desde una dirección IP desconocida, lo que activó una alerta. En ese momento, se puso en marcha el plan de respuesta a incidentes.

El equipo de respuesta a incidentes registró inmediatamente la información conocida sobre el ataque y notificó a la gerencia según el componente de comunicación del plan de respuesta a incidentes. Luego, el equipo comenzó a investigar la fuente y el alcance del ataque.

¿Qué opinas?

¿Qué pasos de detección y análisis tomó el equipo de TI?

**Respuesta** El equipo de IT recibieron indicadores de los sistemas de las herramientas de monitoreo, documentaron el incidente y notificaron a las partes que debian ser notificadas.

**Actividad**: Aplicar un marco de respuesta a incidentes adecuado (fase 3)

Lee la siguiente información de antecedentes sobre cómo HealthGuard Medical Services completó la fase de contención y erradicación de la respuesta a incidentes. Luego, aplica tu conocimiento de esta fase para responder a la pregunta que sigue.

**Antecedentes**

El equipo de respuesta a incidentes puso en marcha su plan de respuesta a incidentes y empezó a aislar los sistemas afectados para evitar que el ataque se propagara. En primer lugar, el equipo de respuesta a incidentes desconectó de la red los sistemas afectados. A continuación, se cercioró de que ningún otro sistema se comunicara con los sistemas afectados, lo que podría haberlo expuesto al ataque. El equipo investigó la amenaza y descubrió que existía un parche. A continuación, el equipo de respuesta a incidentes se dedicó a eliminar el código malicioso de los sistemas afectados, se cercioró de que actualizaron sus sistemas y agregó medidas de seguridad adicionales para evitar futuros ataques.

¿Qué opinas?

¿Cómo pudo el equipo contener y erradicar el sistema afectado?

**Respuesta** El equipo de IT aislo los sistemas afectado y comprobo con que otros equipo mantuvieron comunicacion para asegurar que no hubo un movimiento lateral, hicieron inteligencia de amenaza y descubrieron que hay un parche que ayuda prevenir el incidente en cuestión. Procedieron con la erradicacion del código malicioso y culmiraron con la actualizacion y toma de medidas preventivas para evitar futuros ataques

**Actividad**: Aplicar un marco de respuesta a incidentes adecuado (fase 4)

Lee los antecedentes sobre cómo HealthGuard Medical Services completó la fase de recuperación de la respuesta a incidentes. Luego, aplica tu conocimiento de esta fase para responder a la pregunta que sigue.

Antecedentes

En la fase de recuperación, el equipo de TI de HealthGuard Medical Services trabajó para restaurar los sistemas afectados y verificó que el parche se aplicara a todos los sistemas necesarios. Además, llevó a cabo un análisis del incidente para identificar cualquier otra vulnerabilidad potencial e implementó medidas de seguridad adicionales para prevenir futuros incidentes.

HealthGuard Medical Services comunicó el incidente a todos los pacientes afectados y les ofreció servicios de protección de identidad como medida de precaución. La empresa también revisó su plan de respuesta a incidentes e hizo mejoras para prepararse mejor para futuros incidentes de ciberseguridad.

¿Qué opinas?

¿Consideras que HealthGuard Medical Services completó todos los pasos de recuperación necesarios?

**Respuesta** Si, considero que completaron todos los pasos necesarios, restauraron los sistemas afectados, verificaron que el parche se aplicara a todos los sistemas necesarios, realizaron un analisis del incidente para identificar otras vulnerabilidades potenciales e implementaron medidas de seguridad adicionales para prevenir futuros incidentes. Ademas comunicaron el incidente a los pacientes afectados y revisaron su plan de respuesta a incidentes para mejorarlo.

**Antecedentes**

SilverHedge Financial, una empresa de servicios financieros, se preparó para una posible violación de seguridad implantando medidas de seguridad, como firewalls, sistemas de detección de intrusiones y controles de acceso. Su equipo de seguridad detectó una actividad inusual en la red, como varios intentos fallidos de inicio de sesión, un rendimiento lento del sistema, una actividad inusual de archivos y un tráfico de red sospechoso. El equipo activó inmediatamente el plan de respuesta a incidentes e inició una investigación para determinar el alcance y el impacto del incidente.

El equipo de respuesta a incidentes identificó el origen de la violación como un correo electrónico de phishing enviado a un empleado que, sin saberlo, descargó malware en su computadora. El malware se propagó por la red de la empresa, permitiendo al atacante acceder a datos confidenciales. El equipo de seguridad contuvo rápidamente la violación aislando y desconectando de la red las máquinas infectadas y erradicando el malware.

Una vez eliminado el malware y considerada segura la red, el equipo de respuesta a incidentes de SilverHedge Financial restableció el funcionamiento normal. Restauró los datos alterados de las copias de seguridad y verificó que se instalaran todas las actualizaciones y parches más recientes. Realizaron una revisión exhaustiva del incidente para identificar áreas de mejora. Se accedió a los datos de los clientes y se pusieron en peligro, por lo que la empresa tuvo que informar del incidente a los clientes y asociados afectados y asegurarles que se tomaron las medidas adecuadas para proteger sus datos.

**Actividad**: Identificar las cuatro fases de una respuesta a incidentes

Ahora, describe cómo SilverHedge Financial completó cada fase del proceso de respuesta a incidentes. En cada descripción, identifica los pasos que SilverHedge Financial debe tomar para completar esa fase.

### Fase 1: Preparación

SilverHedge Financial implemento firewall, ids, IAM, preparandose para un posible incidente.

### Fase 2: Detección y análisis

SilverHedge Financial detectaron una intrusion causada por un pishing, determinaron la maquina afectada, notaron un incrementos de trafico en la red, pudieron determinar el alcance de la intrusion hasta los archivos confidenciales de sus clientes. Tambien notaton actividades inusuales e intentos de inicio de sesión fallidos.

### Fase 3: Contención y erradicación

SilverHedge Financial contuvo la intrusion aislando y desconectando de la red las maquinas infectadas, erradicaron el malware.

### Fase 4: Recuperación

SilverHedge Financial restauro los archivos a su estado original a traves de copias de seguridad, verificaron que todos los sistemas estuvieran parcheados y actualizados, identificaron areas de mejoras y notificaron a sus clientes sobre el incidente y como tomar medidas para proteger sus datos
