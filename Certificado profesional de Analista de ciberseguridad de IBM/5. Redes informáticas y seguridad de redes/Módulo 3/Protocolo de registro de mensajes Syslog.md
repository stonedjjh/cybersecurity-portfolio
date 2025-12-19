# Protocolo de Registro de Mensajes Syslog

Syslog (abreviatura de registro de mensajes) es un protocolo estándar que **separa el software que genera los mensajes, el sistema que los almacena y el software que los analiza**. Proporciona un formato estructurado para los mensajes de registro y es vital para la administración de registros en entornos de red.

---

## - Funciones y Usos Principales

- **Separación de Funciones:** Facilita la gestión de registros al aislar la generación, el almacenamiento y el análisis.
- **Formato Estándar:** Cada mensaje se etiqueta con un **código de instalación** (indicando el software de origen) y un **nivel de gravedad**.
- **Usos Comunes:**
  - Administración del sistema.
  - Auditoría de seguridad.
  - Análisis de información general.
  - Mensajes de depuración y notificación de eventos.
  - Investigación forense.

---

### - Capas del Protocolo Syslog

Syslog opera a través de tres capas distintas:

- **Capa de Contenido:** Almacena los mensajes de Syslog reales.
- **Capa de Aplicación:** Gestiona la generación, la interpretación, el enrutamiento y el almacenamiento de los mensajes.
- **Capa de Transporte:** Administra el transporte de los mensajes de Syslog a través de la red (típicamente utilizando TCP o UDP).

---

### - Actores Clave de Syslog

El protocolo involucra cinco roles principales para el manejo de mensajes:

- **Originador:** El lugar donde se produce el evento (ej. una máquina local).
- **Recopilador:** El servidor Syslog central que almacena y recopila los mensajes.
- **Servidor de Retransmisión:** Reenvía mensajes del originador al recopilador.
- **Remitente del Transporte:** Prepara los mensajes para su transmisión a través de la red.
- **Receptor del Transporte:** Recibe los mensajes y los entrega al servidor Syslog.

---

### - Componentes y Proceso del Mensaje Syslog

El mensaje comienza en el remitente y se enriquece antes de ser enviado al servidor.

- **Componentes del Mensaje (Encabezado y Contenido):**
  - **Código de la Instalación:** Indica qué proceso de la máquina creó el mensaje (ej. si fue escrito originalmente para BSD UNIX, refleja nombres de procesos de UNIX; routers Cisco suelen usar local6 o local7).
  - **Nivel de Gravedad:** Un valor de 0 (Emergencia) a 7 (Depuración). Permite filtrar mensajes para evitar la sobrecarga del servidor.
  - **Identificador de Proceso Originador.**
  - **Marca de Tiempo.**
  - **Nombre de Host** o **Dirección IP** del dispositivo de notificación.
  - **Contenido del mensaje** (el mensaje de registro real).

- **Proceso del Mensaje:**
    1. El remitente crea el mensaje e incluye el código de instalación y el nivel de gravedad.
    2. El cliente Syslog agrega el identificador de proceso, la marca de tiempo y la dirección IP/nombre de host al encabezado.
    3. El mensaje se envía al servidor de retransmisión o directamente al recopilador.

---
