# Análisis de Flujos y Redes

El análisis de flujos de red, ejemplificado por protocolos como NetFlow, proporciona datos y estadísticas esenciales sobre los paquetes que atraviesan las interfaces de los dispositivos de red.

---

## - Concepto y Fuente de Datos

- **Función del Flujo de Red:** Los flujos de red ofrecen **datos y estadísticas** detalladas sobre los paquetes que fluyen a través de las interfaces de los dispositivos.
- **Dispositivos de Recolección:** Los datos de flujo se recopilan tomando muestras de los flujos que atraviesan las interfaces de dispositivos clave como **enrutadores (routers) y conmutadores (switches)**.

---

## - Datos Proporcionados por el Análisis de Flujo

Al inspeccionar un registro de flujo de red, la herramienta de análisis (como un servidor NetFlow) muestra información detallada sobre la comunicación:

- **Estadísticas de Tráfico:**
  - Cantidad de **paquetes** utilizados en el flujo.
  - Cantidad de **bytes** enviados.
  - **Marcas de tiempo** (indicando cuándo se inició el flujo).
- **Información de Conexión:**
  - Direcciones **IP de origen y destino**.
  - **Puertos de origen y destino** (para protocolos como TCP y UDP).
- **Detalles del Flujo y la Calidad:**
  - **Identidad de la interfaz** de entrada y la interfaz de salida.
  - Información de **Calidad de Servicio (QoS)**, incluido el tipo de servicio.
  - **Protocolos en uso:** Permite identificar protocolos por su número (ej. ICMP es Protocolo 1, UDP es 17 y TCP es 6).

---

## - Visualización y Aplicación de los Datos

El panel de análisis de NetFlow permite clasificar y visualizar el tráfico para una mejor comprensión de la red:

- **Clasificación por Protocolo y Aplicación:**
  - Permite ver qué **protocolos** son los más utilizados en una interfaz (ej. más del 84% de tráfico es TCP/tráfico web).
  - El tráfico se puede categorizar fácilmente por **aplicación** (ej. HTTP es la aplicación número 1).
- **Dirección del Tráfico:**
  - Se puede determinar rápidamente la cantidad de **bytes de datos** que entran (ingresan) y salen (egresan) de la interfaz.
  - Se puede determinar la cantidad de **paquetes** enviados a través de la interfaz en cada dirección.

---
