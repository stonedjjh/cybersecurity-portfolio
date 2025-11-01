# Seguridad de la red

La seguridad de la red es una medida de protección que protege la infraestructura de red contra el acceso no autorizado, la explotación o el robo. Implica establecer una infraestructura sólida que garantice un entorno operativo seguro para los dispositivos, los programas, los usuarios y las aplicaciones.

## Defensa en profundidad

Los mecanismos de seguridad de la red son similares a una serie de barreras alrededor de un castillo, cada una diseñada para proporcionar una capa adicional de protección contra posibles infracciones. Quizás haya un foso lleno de cocodrilos para disuadir a los posibles atacantes. Luego, una pared rodea el castillo con una puerta con una sola cerradura y guardias en cada esquina.

Por último, hay guardias adicionales estratégicamente estacionados dentro de los muros del castillo si los atacantes rompen el foso, las puertas cerradas con llave y los guardias externos. Este enfoque de seguridad de varios niveles se denomina defensa en profundidad.

## Objetivos de la seguridad en la red

La seguridad de la red tiene tres objetivos principales:

- Impedir que entidades no autorizadas accedan a los activos de la red.

- Identificar y detener las ciberamenazas e infracciones en curso.

- Garantizar que los usuarios legítimos puedan acceder a los activos de la red de forma segura cuando sea necesario.

## Mecanismos de seguridad Externos e Internos

Los mecanismos de seguridad de la red funcionan en dos frentes: el límite externo y la estructura interna de la red.

Las medidas de seguridad se implementan en el borde de la red para evitar que las amenazas traspasen el perímetro de la red. Sin embargo, a pesar de la seguridad externa, existe la posibilidad de intrusiones. Por lo tanto, se colocan protecciones adicionales internamente, que protegen los componentes críticos, como las computadoras y las bases de datos.

Si los atacantes atraviesan las defensas exteriores, se enfrentan a una mayor resistencia. Los profesionales de ciberseguridad combinan varias herramientas y métodos para proporcionar una red segura. Veamos cada una de estas herramientas y técnicas en detalle.

### Firewalls

Los firewalls actúan como una barrera de hardware o software para filtrar el tráfico de datos no autorizado o malintencionado que entra o sale de una red. Están ubicados estratégicamente en los puntos de entrada a la red, lo que garantiza que solo puedan pasar las comunicaciones autorizadas. Los firewalls varían en cuanto a sofisticación

| Firewall Basicos                                                                                                                        | Proxima Generación                                                                                                                                                                                                                                                                        |
| --------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Examinan el tráfico mediante el filtrado de paquetes, lo que implica examinar cada paquete para verificar su origen y destino aprobados | - Incorporan sistemas de prevención de intrusiones.</br>- Aprovechan las tecnologías de inteligencia artificial y aprendizaje automático.</br>- Pueden comprender y supervisar las aplicaciones.</br>- Utilizar la inteligencia de amenazas para ofrecer una línea de defensa más sólida. |

### Control de Acceso a la Red(Network Access Control)

El control de acceso a la red, NAC, actúa como guardián de la seguridad de la red.

- Gestiona la autenticación y la autorización de los usuarios para controlar la entrada y las actividades de la red. El proceso de autenticación garantiza que los usuarios coincidan con su identidad reclamada. Tras la autenticación, a estas personas se les conceden permisos específicos para acceder a determinadas áreas de red.

- Establecer la identidad del usuario, los sistemas NAC específicos evalúan los riesgos de los dispositivos antes de conceder el acceso a la red.

Este enfoque ayuda a mitigar los riesgos que representan los dispositivos vulnerables o que no cumplen las normas al restringir el acceso a los dispositivos con una protección antimalware anticuada o una configuración inadecuada.

### Sistema de Detección y Prevención de intrusos IDPS

- Un IDPS está situado justo detrás del firewall.
- Analiza el tráfico de red entrante.
- Identifica y gestiona posibles amenazas de seguridad.

Los IDPS evolucionaron a partir de los sistemas tradicionales de detección de intrusos los IDS, que detectan y señalan actividades inusuales para su análisis. Sin embargo, los IDPS modernos tienen funcionalidades mejoradas, lo que les permite reaccionar de forma proactiva ante las amenazas percibidas.

| IDS tradiccionales                                    | IDPS Modernos                                                                                                                                                                                                                                                               |
| ----------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Solo detectan y alertan sobre actividades sospechosas | - Detectan, alertan y responden a las amenazas en tiempo real.</br>- Pueden bloquear automáticamente el tráfico malicioso o terminar las conexiones sospechosas.</br>- Integran capacidades avanzadas de análisis de comportamiento para identificar amenazas desconocidas. |

### Red Privada Virtual (VPN)

Una red privada virtual, o VPN, es beneficiosa para:

- Ocultar su identidad en línea.

- Cifra su tráfico de Internet.

- Oculta sus direcciones IP

- Oculta su ubicación geográfica.

Puedes usar una VPN para redirigir tu conexión a Internet a través de un servidor seguro, que luego interactúa con Internet en general en tu nombre.

Esta funcionalidad se vuelve extremadamente importante para los empleados remotos que necesitan conectarse de forma segura a los sistemas empresariales, especialmente cuando utilizan redes Wi-Fi públicas vulnerables en cafeterías o aeropuertos.

### Segmentación de la Red

Es una táctica que divide una red en varios segmentos o subredes más pequeños. Este proceso refuerza la seguridad al limitar el movimiento lateral de los posibles atacantes dentro de la red. Aquí, cada segmento opera bajo políticas y controles de acceso únicos, lo que compartimenta de manera efectiva la red para aislar la información confidencial y los sistemas críticos.

Por ejemplo, puede separar un segmento que maneja datos financieros confidenciales del resto de la red, reduciendo así los puntos de exposición y reduciendo el riesgo de acceso no autorizado a esta información crítica.

La segmentación también permite a las organizaciones contener y controlar la propagación de las brechas de seguridad. Al limitar las amenazas a segmentos aislados, puede minimizar su impacto y tomar medidas correctivas sin comprometer toda la red.

### Seguridad de los terminales(Endpoints Security)

Los puntos finales incluyen dispositivos como **ordenadores** , **dispositivos móviles** y **servidores** que se conectan a la red. La seguridad de los puntos finales incluye enfoques y tecnologías que protegen estos puntos finales para proteger la red. Desempeña un papel fundamental en la seguridad de la organización, ya que los puntos finales sirven como posibles puntos de entrada para los atacantes.

Las soluciones integrales de seguridad para terminales utilizan:

- Software antivirus

- Antimalware

- Firewalls personales, entre otras herramientas para detectar , prevenir y responder a las amenazas de forma proactiva.

Estas medidas de seguridad ayudan a administrar y monitorear el acceso, garantizando que todos los puntos finales cumplan con las políticas de seguridad antes de conectarse a la red.

Además de proteger los dispositivos individuales, la seguridad de los terminales mantiene la integridad de la red al garantizar que todos los intercambios de datos de los dispositivos cumplan con los estándares de seguridad.

Los perímetros seguros se han extendido más allá de los límites tradicionales de las oficinas con el aumento del trabajo remoto y la adopción de políticas BYOD o traiga su propio dispositivo. Por lo tanto, garantizar que sus dispositivos de punto final estén libres de influencias malintencionadas ayuda a las redes a mantener la resiliencia frente a las amenazas externas e internas.

### Sistemas de Gestión de Información y Eventos de Seguridad SIEM(Security Information and Event Management)

La administración de eventos e información de seguridad, o SIEM, es otra medida de protección integral para mejorar la seguridad de la red. Agrega y analiza los datos de registro y eventos de servidores , puntos finales y dispositivos de red.

Al centralizar la recopilación de datos, los sistemas SIEM permiten la visibilidad en tiempo real de la postura de seguridad de una organización, identificando la actividad anormal indicativa de un incidente de seguridad.

Los SIEM avanzados también aprovechan el aprendizaje automático y la inteligencia artificial para automatizar la identificación de amenazas sofisticadas. Conectan puntos de datos dispares para identificar patrones de actividad maliciosa, lo que ayuda a detectar posibles infracciones de seguridad y responder rápidamente a ellas. Las alertas SIEM permiten a los analistas de seguridad abordar las amenazas antes de que se conviertan en incidentes importantes.

### Security Orchestration, Automation and Response SOAR

Orquestación , automatización y respuesta de seguridad. En colaboración con los sistemas SIEM, las plataformas SOAR agilizan las operaciones de seguridad en entornos de gran volumen. Estas soluciones integran varias herramientas y procesos de seguridad, automatizando los flujos de trabajo y las acciones de respuesta a incidentes.

Esta solución de automatización permite a los equipos de seguridad administrar las alertas de manera eficiente, lo que a menudo reduce el tiempo de respuesta a los incidentes. Las plataformas SOAR también ayudan a reducir el riesgo de fatiga ante las alertas, lo que permite a los profesionales de la ciberseguridad centrarse en amenazas más complejas.
