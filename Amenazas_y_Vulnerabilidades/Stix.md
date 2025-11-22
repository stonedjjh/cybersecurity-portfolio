# STIX

Una de las mejores herramientas para organizar la inteligencia sobre amenazas es Structured Threat Information Expression (STIX). STIX es un lenguaje de programación de código abierto que proporciona un formato estandarizado para compartir inteligencia sobre amenazas.

El lenguaje trata cada información como un bloque de código llamado objeto.

Cada objeto tiene una propiedad llamada tipo que indica el concepto de inteligencia sobre amenazas relevante para el objeto, como "patrón de ataque", "actor de la amenaza" o "ubicación".

Otras propiedades representan características como el nombre y la descripción del objeto. Por ejemplo, el tipo de un objeto puede ser "patrón de ataque", y su nombre puede ser "spear phishing".

## Tipos de objetos STIX comunes

Exploremos algunos de los tipos de objetos STIX más empleados.

- **Patrón de ataque** “Un tipo de TTP [tácticas, técnicas y procedimientos] que describe las formas en que los adversarios intentan comprometer sus objetivos”

- **Campaña** "Un grupo de comportamientos adversarios que describe un conjunto de actividades maliciosas o ataques (a veces llamados oleadas) que ocurren durante un periodo de tiempo contra un conjunto específico de objetivos"

- **Curso de acción** “Una recomendación de un productor de inteligencia a un consumidor sobre las acciones que podría tomar en respuesta a esa inteligencia”

- **Identidad** Individuos, organizaciones o grupos específicos que fueron atacados, como el sector financiero.

- **Indicador** “Contiene un patrón que se puede usar para detectar ciberactividad sospechosa o maliciosa”

- **Ubicación** “Representa una ubicación geográfica”

- **Malware** Un tipo de TTP que representa código malicioso.

- **Actor de amenazas** “Individuos, grupos u organizaciones reales que se cree que operan con intenciones maliciosas”

- **Herramienta** “Software que pueden emplear los actores de amenazas para realizar ataques”

- **Vulnerabilidad** “Un error en el software que puede ser empleado directamente por un hacker para obtener acceso a un sistema o red”

- **Relación** Une dos objetos para describir cómo están relacionados.
