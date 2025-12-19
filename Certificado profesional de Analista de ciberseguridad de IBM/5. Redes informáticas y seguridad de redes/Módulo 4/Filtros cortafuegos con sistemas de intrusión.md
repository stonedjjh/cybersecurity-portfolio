# Filtros de Firewall y Sistemas de Intrusión (IDS/IPS)

- **Propósito de los Filtros de Firewall:** Actúan como guardianes aplicando políticas de seguridad para regular el tráfico de red entrante y saliente.

- **Tipos de Filtros de Firewall:**

  - **Firewalls Sin Estado (Stateless):** Examinan paquetes de datos individuales basándose solo en sus encabezados. Toman decisiones sin tener en cuenta el contexto de la conexión.
  - **Firewalls Con Estado (Stateful):** Supervisan el estado de las conexiones activas, lo que permite tomar decisiones de filtrado más matizadas y basadas en el contexto de la sesión.
  - **Firewalls a Nivel de Aplicación:** Funcionan en la capa de aplicación del modelo OSI. Inspeccionan las cargas útiles de los paquetes, permitiendo un control granular basado en los datos específicos de las aplicaciones.

- **Sistemas de Detección de Intrusos (IDS) - Monitores Vigilantes:**

  - **Función:** Analizan continuamente el tráfico y las actividades del sistema en busca de señales de comportamiento sospechoso o posibles violaciones de seguridad.
  - **Acción:** Detectan y **generan una alerta** (ej. detectan un ataque de fuerza bruta), pero **no realizan ninguna acción directa** para detener la amenaza.
  - **Tipos de IDS:**
    - **NIDS (Network-based IDS):** Monitorea patrones de tráfico en toda la red, señalando anomalías y amenazas.
    - **HIDS (Host-based IDS):** Monitorea _hosts_ o dispositivos individuales, examinando registros del sistema, modificaciones de archivos y actividades de procesos.
  - **Desventaja:** Pueden sufrir sobrecarga por el alto volumen de alertas y los falsos positivos.

- **Sistemas de Prevención de Intrusos (IPS) - Guardias de Seguridad Proactivos:**

  - **Función:** Van más allá de la detección al **impedir activamente** que las amenazas identificadas causen daño.
  - **Acción:** Bloquean o neutralizan instantáneamente las amenazas conocidas (ej. bloquean una consulta de inyección SQL) antes de que lleguen al destino.
  - **Tipos de IPS:**
    - **Network-based IPS:** Implementados en el perímetro de la red para examinar el tráfico entrante/saliente.
    - **Host-based IPS:** Instalados directamente en dispositivos individuales, supervisan y frustran preventivamente acciones malintencionadas.
  - **Desventaja:** Requieren una configuración meticulosa para evitar bloquear tráfico legítimo (falsos positivos).

- **Integración con Filtros de Firewall:**
  - **Firewall + IDS (Coexistencia):** El _firewall_ bloquea amenazas conocidas aplicando políticas estáticas, mientras que el IDS examina el tráfico _permitido_ en busca de anomalías y alerta a los administradores para su posterior investigación.
  - **Firewall + IPS (Integración):** El _firewall_ filtra el tráfico entrante, y el IPS inspecciona y **neutraliza activamente** las amenazas en tiempo real. Esto crea un mecanismo de defensa robusto al combinar las políticas estáticas del _firewall_ con la protección dinámica y proactiva del IPS.
