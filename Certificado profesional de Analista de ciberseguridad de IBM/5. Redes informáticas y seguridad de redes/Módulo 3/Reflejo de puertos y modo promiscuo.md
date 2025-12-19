# Duplicación de Puertos y Modo Promiscuo

La duplicación o **reflejo de puertos** es una técnica esencial utilizada por los administradores e ingenieros de red para **analizar y depurar** el tráfico, supervisar el rendimiento de la red y detectar errores o problemas.

---

## - Concepto de Duplicación de Puertos (Port Mirroring)

- **Definición:** Consiste en configurar un switch para crear una copia de **todo el tráfico** que atraviesa uno o más puertos de origen y enviar esos paquetes copiados a un único puerto de destino específico.
- **Nombres Específicos:**
  - En switches Cisco, se denomina **SPAN** (Switch Port Analyzer).
  - La variante **RSPAN** (Remote SPAN) permite que el puerto de destino se encuentre en un switch diferente al que realiza la copia.
  - Otros proveedores usan nombres distintos (ej. 3Com lo llama "wrap for roving analyst port"). 

---

## - Importancia y Riesgos de la Duplicación

- **Importancia:** Permite la **supervisión pasiva** de la red y ayuda a generar alertas cuando se detectan problemas.
- **Riesgo de Seguridad:** Si un atacante obtiene acceso y configura la duplicación de puertos, podría enviar una copia de todo el tráfico de la red a sus propios servidores para explotación sin ser detectado.

---

## - Rol del Sistema de Detección de Intrusiones (IDS)

Para analizar los datos reflejados y mitigar los riesgos, los paquetes copiados suelen enviarse a un IDS:

- **Análisis en Tiempo Real:** El IDS se conecta al puerto de destino y **monitoriza todo el tráfico** en tiempo real.
- **Detección de Anomalías:** Envía una **alerta** si detecta cualquier anomalía o comportamiento sospechoso.
- **Naturaleza Pasiva:**
  - Un IDS está **apartado** y trabaja solo con una copia del tráfico.
  - Esto significa que **no ralentiza la red**.
  - **No puede actuar directamente** sobre los paquetes (ej. bloquear la entrega); solo puede generar alertas.

---

## - El Modo Promiscuo

El dispositivo que recibe el tráfico reflejado (como un IDS o un servidor de análisis) debe operar en modo promiscuo:

- **Necesidad del Modo Promiscuo:** La **NIC** (Tarjeta de Interfaz de Red) del punto final receptor debe funcionar de forma **promiscua** para leer todas las tramas que recibe.
- **Motivo:** Las tramas copiadas tienen **direcciones MAC de destino** que apuntan a otros sistemas. Una NIC que no esté en modo promiscuo ignoraría estas tramas.
- **Herramientas:** Programas como **Wireshark** ayudan a poner la NIC en modo promiscuo para capturar todo el tráfico a través de su interfaz.

---
