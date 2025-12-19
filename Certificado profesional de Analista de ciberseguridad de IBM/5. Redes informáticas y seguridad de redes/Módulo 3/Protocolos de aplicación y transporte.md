# Protocolos de Aplicación y Transporte (TCP vs. UDP)

---

## 1. Diferencias Clave entre TCP y UDP

| Característica           | Protocolo de Control de Transmisión (TCP)                                                                                  | Protocolo de Datagramas de Usuario (UDP)                                                            |
| :----------------------- | :------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------- |
| **Confianza**            | **Orientado a la conexión (Fiable)**. Requiere un "apretón de manos" (handshake).                                          | **Sin conexión (No fiable)**. No confirma la entrega.                                               |
| **Orden**                | Proporciona una lista ordenada de paquetes enviados y recibidos. Reensambla en orden correcto y reenvía paquetes perdidos. | El receptor reensambla en el orden en que llegan los paquetes (pueden estar desordenados o faltar). |
| **Velocidad/Sobrecarga** | Lento; alta sobrecarga debido a la verificación, orden y reenvío.                                                          | **Rápido**; baja sobrecarga (fast and cheap) al omitir la confirmación.                             |
| **Encabezado**           | Contiene información para verificar, ordenar, remitente y destinatario.                                                    | Contiene información esencial, incluyendo puertos de origen y destino.                              |
| **Analogía**             | Envío de carta con número de seguimiento y firma (garantía de recepción).                                                  | Envío masivo de correo (alta velocidad, sin confirmación de entrega).                               |

## 2. Estructura y Función de los Encabezados

- **Propósito del Encabezado:** Al igual que la parte frontal de un sobre, el encabezado del paquete (tanto TCP como UDP) identifica al remitente, al destinatario y otra información de control.
- **Puertos (TCP y UDP):** Los protocolos especifican los **puertos de origen y destino** para dirigir los paquetes de datos a la **aplicación correcta** en el dispositivo de destino, asegurando una comunicación adecuada.

## 3. Aplicaciones Reales que Prefieren UDP

UDP se elige para aplicaciones donde la **velocidad** es prioritaria y la pérdida o el desorden de algunos paquetes es **insignificante** o tolerable, ya que la sobrecarga de TCP ralentizaría demasiado la comunicación.

| Protocolo                                      | Puerto(s)       | Función Principal                                   | Razón para Usar UDP                                                                |
| :--------------------------------------------- | :-------------- | :-------------------------------------------------- | :--------------------------------------------------------------------------------- |
| **TFTP** (Trivial File Transfer Protocol)      | 69              | Transferencia de archivos muy pequeños.             | Evita la sobrecarga de conexión de TCP para transferencias rápidas.                |
| **DNS** (Domain Name System)                   | 53              | Consultas de nombres (traduce nombres a IP).        | Velocidad en la respuesta a consultas. (Puede usar TCP para tareas menos comunes). |
| **SNMP** (Simple Network Management Protocol)  | 161, 162        | Supervisión y gestión de dispositivos de red.       | Velocidad sobre la fiabilidad para el monitoreo. (Puede usar TCP).                 |
| **DHCP** (Dynamic Host Configuration Protocol) | 67              | Asigna y administra direcciones IP automáticamente. | Velocidad y eficiencia en la asignación de direcciones.                            |
| **VoIP** (Voz sobre IP)                        | 5060            | Envío de voz a través de Internet.                  | Prioriza la velocidad, ya que la pérdida de algún paquete de voz es tolerable.     |
| **IPTV** (Internet Protocol TV)                | 80, 5004, 12000 | Transmisión de señales de TV.                       | Prioriza la velocidad de transmisión.                                              |

## Protocolos de Aplicación y Transporte (TCP)

---

### 2. Mecanismo y Componentes de TCP (Control de Transmisión)

TCP es un protocolo **orientado a la conexión** que garantiza una entrega de datos **fiable** y **ordenada** entre aplicaciones.

- UDP es, en contraste, un protocolo **sin conexión** que envía paquetes sin establecer una conexión previa.

#### 2.1. El Protocolo de Enlace a Tres Bandas (Three-Way Handshake)

Las conexiones TCP deben establecerse formalmente mediante un proceso de tres pasos antes de que comience la transmisión de datos.

1. **SYN (Sincronización):** El remitente envía un paquete SYN al destinatario para solicitar el inicio de la conexión.
2. **SYN-ACK (Sincronización-Acuse de Recibo):** El destinatario responde con un paquete que incluye la bandera SYN (lista para recibir) y la bandera ACK (acuse de recibo de la solicitud original).
3. **ACK (Acuse de Recibo):** El remitente responde con un paquete ACK final para confirmar que la conexión está establecida.

Este proceso asegura que ambas partes estén listas y acuerden el número de secuencia inicial para la transmisión.

#### 2.2. Entrega Fiable y Ordenada

- **Transmisión en Serie:** TCP generalmente envía datos en una serie continua sin esperar un acuse de recibo para cada paquete individual.
- **Números de Secuencia y ACK:** TCP utiliza números de secuencia para identificar el orden de los paquetes.
  - Si el receptor detecta que falta un paquete en una serie (mediante el número de secuencia), avisa al remitente para que lo reenvíe.
  - El número **ACK** que envía el receptor es, en realidad, el número de secuencia del **siguiente segmento** que espera recibir, completando el ciclo de confirmación.

#### 2.3. Componentes del Encabezado TCP

El encabezado TCP (Capa 4) es crucial para gestionar la transmisión fiable. Los componentes clave incluyen:

- **Puerto de Origen:** El puerto local desde donde se origina la comunicación (e.g., puerto dinámico 58038).
- **Puerto de Destino:** El puerto de la aplicación remota a la que se intenta conectar (e.g., puerto 22 para SSH).
- **Indicadores (Flags):** Incluyen SYN y ACK, que se usan para establecer y gestionar la conexión.
- **Número de Secuencia:** Utilizado para ordenar los paquetes.
- **Número de Acuse de Recibo (ACK):** Utilizado para confirmar la recepción y solicitar el siguiente paquete.

#### 2.4. Aplicaciones Comunes que Utilizan TCP

TCP es preferido para aplicaciones donde la **fiabilidad y el orden** de los datos son críticos.

- **HTTP** (Protocolo de Transporte de Hipertexto): Utilizado para la navegación web y el ciclo de respuesta a solicitudes (cliente solicita, servidor responde).
  - **Nota de Seguridad:** HTTP no es seguro.
- **HTTPS** (HTTP Seguro): Versión de HTTP que utiliza certificados **SSL/TLS** para **cifrar los datos**, garantizando privacidad y seguridad.
- **SMTP** (Protocolo Simple de Transferencia de Correo): Utilizado para el envío de correos electrónicos.
- **FTP** (Protocolo de Transferencia de Archivos): Utilizado para la transferencia de archivos.

## DNS y DHCP

- **Propósito:** DNS y DHCP son servicios de red esenciales que permiten a los dispositivos conectarse a la red empresarial y navegar de forma segura.
- **DNS (Sistema de Nombres de Dominio):**
  - **Función:** Traduce nombres de dominio (URLs) a sus correspondientes direcciones IP.
  - **Servicio Principal:** Resolución de DNS. Cuando se consulta un dominio (ej. google.com), el servicio traduce ese nombre a la dirección IP real del servidor.
  - **Dependencia:** Requiere que los dispositivos tengan direcciones IP válidas asignadas por DHCP.
- **DHCP (Protocolo de Configuración Dinámica de Host):**
  - **Función:** Asigna automáticamente direcciones IP a los dispositivos que se conectan a la red desde un conjunto de direcciones disponibles, eliminando la necesidad de configuración manual.
  - **Proceso de Enlace (DORA - Discovery, Offer, Request, Acknowledgement):**
    1. **Descubrimiento (Discovery):** El cliente envía un mensaje de difusión (broadcast) para localizar un servidor DHCP.
    2. **Oferta (Offer):** El servidor DHCP responde con una dirección IP propuesta, la máscara de subred, la duración del arrendamiento y su propia dirección.
    3. **Solicitud (Request):** El cliente acepta la oferta seleccionada y lo comunica con un mensaje de solicitud (también por difusión) para informar a otros servidores.
    4. **Acuse de Recibo (ACK):** El servidor DHCP ganador envía la confirmación final del arrendamiento de la dirección IP.
  - **Puertos:** Utiliza UDP, con el cliente en el puerto 68 y el servidor en el puerto 67.
- **Diagnóstico:** Herramientas como Wireshark capturan los paquetes DHCP para visualizar la comunicación (Descubrimiento, Oferta, Solicitud, ACK) y ayudar a diagnosticar problemas de conexión.

## El Filtrado de DNS en la Ciberseguridad

El filtrado de DNS utiliza el Sistema de Nombres de Dominio (DNS), que convierte nombres legibles por humanos en direcciones IP, para **bloquear el acceso a sitios web o servicios específicos** basándose en criterios predefinidos como políticas empresariales o listas de sitios maliciosos.

---

### - Concepto y Funcionamiento

- **Definición de DNS:** El DNS evalúa los nombres de dominio (ej. google.com) para determinar las direcciones IP (ej. 192.0.2.1) que la computadora usa para la localización en la red o internet.
- **Mecanismo de Bloqueo:**
  - Cuando un usuario intenta visitar un sitio, el sistema de filtrado **intercepta la consulta de DNS**.
  - Compara el dominio solicitado con sus políticas de filtrado (listas de permitidos y bloqueados).
  - Si el dominio está bloqueado, **la solicitud se rechaza o se redirige**, impidiendo el acceso a contenido dañino o no deseado.

---

### - Importancia y Beneficios Clave

El filtrado de DNS es una **defensa de primera línea** que mejora la seguridad, el cumplimiento y la productividad:

- **Prevención de Ciberamenazas:**
  - **Bloquea sitios maliciosos** asociados con malware, suplantación de identidad (phishing) y servidores de comando y control.
  - Ayuda a **prevenir infecciones y filtraciones de datos** al detener las amenazas antes de que lleguen al dispositivo.
  - **Reduce los puntos de entrada** potenciales para los atacantes.
- **Control de Contenido y Cumplimiento:**
  - Permite a las organizaciones **aplicar políticas de uso de Internet** (ej. bloquear redes sociales en horario laboral o contenido para adultos).
    - Contribuye al **cumplimiento normativo** al garantizar un uso seguro y apropiado de Internet.
- **Mejora de la Productividad y Rendimiento:**
  - Mantiene la productividad de los empleados al **bloquear sitios distractores o no relacionados con el trabajo**.
  - **Reduce el uso del ancho de banda** al bloquear el tráfico no esencial o dañino, mejorando el flujo de tráfico legítimo.
- **Mejora de la Privacidad:**
  - Bloquea dominios que rastrean el comportamiento del usuario, publican anuncios o inyectan malware.

---

### - Tipos de Filtrado

- **Filtrado Basado en Seguridad:** Se enfoca en bloquear dominios conocidos por alojar ciberamenazas (malware, phishing).
- **Filtrado Basado en Contenido:** Clasifica los dominios por categorías (redes sociales, juegos, noticias) para aplicar políticas de uso aceptable.
- **Filtrado Personalizado:** Permite a las organizaciones crear sus propias listas de dominios permitidos y denegados para satisfacer necesidades específicas.

---

### - Implementación del Filtrado de DNS

La implementación de un sistema de filtrado de DNS implica una estrategia de varios pasos:

1. **Evaluación y Selección de la Solución:** Considere la facilidad de uso, opciones de personalización, capacidad de informes y costo.
2. **Implementación del Sistema:** Idealmente se utiliza un enfoque dual:
    - **Nivel de Red:** Usando firewalls, dispositivos dedicados o servicios basados en la nube para aplicar políticas a todos los dispositivos de la red.
    - **Nivel de Cliente:** Instalando agentes de software en dispositivos individuales para aplicar políticas sin importar la red a la que se conecten.
3. **Configuración de Ajustes:**
    - Definir políticas de filtrado (bloqueo por categoría, listas personalizadas de bloqueo y denegación).
    - Aplicar **políticas diferentes a distintos grupos de usuarios** según sus funciones o requisitos.
4. **Mantenimiento:**
    - Revisar regularmente los registros e informes para verificar la efectividad.
    - Ajustar las políticas según sea necesario para abordar amenazas emergentes o requisitos cambiantes.

---

