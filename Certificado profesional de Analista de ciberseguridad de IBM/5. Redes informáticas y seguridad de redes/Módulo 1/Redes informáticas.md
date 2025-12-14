# Dispositivos de hardware de red

El texto describe los **dispositivos de hardware** que permiten la comunicación y la interacción en una red informática, incluyendo equipos (servidores, clientes, nodos) y dispositivos de conexión/enrutamiento.

- **Servidor:** Una computadora potente que almacena archivos y aplicaciones. Actúa como un punto central de recursos.
- **Cliente:** Dispositivo (computadora, móvil, etc.) que accede a la red a través de un servidor.
- **Nodo:** Cualquier dispositivo conectado a la red capaz de enviar o recibir información. Los clientes son un tipo de nodo.
- **Redes Cliente-Servidor:** Comunes en empresas, centralizan los archivos y el control de acceso.
- **Redes Punto a Punto (P2P):** Comunes en hogares e Internet, permiten compartir recursos e información directamente entre usuarios.

| Dispositivo                              | Función Principal                                                        | Notas Clave                                                                                                                                       |
| :--------------------------------------- | :----------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Hub (Concentrador)**                   | Conecta varios dispositivos.                                             | Envía los datos a **todos** los dispositivos conectados (menos el emisor), menos eficiente.                                                       |
| **Switch (Conmutador)**                  | Conecta varios dispositivos.                                             | Más eficiente que un hub; utiliza tablas de **direcciones MAC** para enviar datos solo al destinatario previsto.                                  |
| **Router (Enrutador)**                   | **Interconecta diferentes redes** o subredes.                            | Administra el tráfico mediante **direcciones IP** y tablas de enrutamiento; permite que múltiples dispositivos usen la misma conexión a Internet. |
| **Módem**                                | **Modula/demodula** los datos.                                           | Convierte los datos digitales para su transmisión (y viceversa) a través de la red (ej. cable, DSL).                                              |
| **Bridge (Puente)**                      | Une dos redes separadas.                                                 | Permite que las dos redes funcionen como una sola, puede ser cableado o inalámbrico.                                                              |
| **Gateway (Puerta de Enlace)**           | Permite que el flujo de datos entre redes con **diferentes protocolos**. | Conecta una red local a una red externa, como Internet.                                                                                           |
| **Repeater (Repetidor)**                 | Recibe una señal y la retransmite.                                       | Utilizado para extender el alcance de una señal (ej. Wi-Fi) y superar obstrucciones.                                                              |
| **Punto de Acceso Inalámbrico (WAP/AP)** | Permite que los dispositivos Wi-Fi se conecten a una red cableada.       | Actúa como un punto de conexión inalámbrica central.                                                                                              |

- **Tarjeta de Interfaz de Red (NIC):** Hardware que conecta un dispositivo individual (cableado o inalámbrico) a la red.
- **Firewall:** Monitorea y controla el tráfico de red (entrante/saliente) según reglas de seguridad predefinidas, creando una barrera entre redes confiables y no confiables (como Internet).
- **Servidor Proxy:** Actúa como intermediario entre una LAN e Internet. Evalúa las solicitudes, minimiza riesgos, oculta la dirección IP y ahorra ancho de banda (almacenando en caché archivos/actualizaciones).
- **Sistema de Detección de Intrusos (IDS):** Monitorea el tráfico de red e **informa** sobre actividades maliciosas.
- **Sistema de Prevención de Intrusiones (IPS):** Inspecciona el tráfico y **actúa** para eliminar, detener o redirigir elementos malintencionados.

## Modelos, Estándares, Protocolos y Puertos de Red

El documento describe la arquitectura, las reglas y los componentes utilizados para la comunicación entre sistemas en una red.

### 1. Modelos de Red

Los modelos de red describen la arquitectura y el diseño para establecer la comunicación. Los paquetes de datos siguen sus protocolos.

| Modelo                                                                 | Tipo                   | Descripción                                                                             |
| :--------------------------------------------------------------------- | :--------------------- | :-------------------------------------------------------------------------------------- |
| **OSI** (Interconexión de Sistemas Abiertos)                           | Marco conceptual       | Modelo de 7 capas utilizado para describir las funciones de un sistema de red.          |
| **TCP/IP** (Protocolo de Control de Transmisión/Protocolo de Internet) | Conjunto de estándares | Modelo de menos capas basado en OSI; permite a las computadoras comunicarse en una red. |

#### Capas del Modelo OSI (7 capas)

1. **Aplicación:** Interfaz para que los usuarios y las aplicaciones interactúen con el software.
2. **Presentación:** Garantiza que los datos estén en un formato utilizable; se produce el cifrado de datos.
3. **Sesión:** Controla el flujo de información entre equipos, incluyendo la autenticación y reconexiones.
4. **Transporte:** Gestiona la entrega y la comprobación de errores de los paquetes (a menudo usando TCP).
5. **Red:** Responsable de interpretar direcciones y dirigir la ruta que tomarán los datos.
6. **Enlace de Datos:** Define el formato de los datos y corrige errores de la capa física.
7. **Física:** Transmite datos sin procesar de forma física, eléctrica u óptica a través de un medio.

### 2. Estándares de Red

Los estándares definen las reglas de comunicación para asegurar la interoperabilidad. Son protocolos ampliamente aceptados.

| Tipo de Estándar     | Característica                                                                                                                        | Ejemplo                            |
| :------------------- | :------------------------------------------------------------------------------------------------------------------------------------ | :--------------------------------- |
| **Formal (De Jure)** | Desarrollados por organismos oficiales (gobierno/industria); pasan por procesos formales y tienen documentación pública.              | HTTP, HTML, IP, Ethernet 802.3d.   |
| **De Facto**         | Resultado de la dominación o la práctica del mercado; aceptados en la práctica, pero sin proceso formal ni documentación obligatoria. | Microsoft Windows, teclado QWERTY. |

#### Organizaciones Clave que Establecen Estándares

- **ISO:** Creó el modelo de referencia OSI.
- **UIT:** Estandarizó las telecomunicaciones internacionales y el uso de radiofrecuencia.
- **DARPA:** Estableció el conjunto de protocolos TCP/IP.
- **IEEE:** Estableció los estándares IEEE 802 (ej. para Ethernet y Wi-Fi).
- **IETF:** Mantiene los conjuntos de protocolos TCP/IP y desarrolló el estándar RFC.

### 3. Protocolos de Red

Un protocolo es un conjunto establecido de reglas que determina cómo se transmiten los datos entre dispositivos. Se basan en estándares y tienen tres acciones principales: seguridad, comunicación y administración.

| Protocolo                                     | Característica                                                                             | Uso Típico                                           |
| :-------------------------------------------- | :----------------------------------------------------------------------------------------- | :--------------------------------------------------- |
| **TCP** (Protocolo de Control de Transmisión) | Garantiza que los datos lleguen al destino previsto. Es más lento y requiere más recursos. | FTP, Navegación web (HTTP), Correo electrónico.      |
| **UDP** (Protocolo de Datagramas de Usuario)  | No garantiza la llegada de paquetes, pero es rápido y ligero.                              | Transmisión en vivo, Juegos en línea, llamadas VoIP. |

- **Suite TCP/IP:** Es una colección de protocolos que proporcionan una solución de red completa.
- **Protocolos IoT:** Conjunto de diversos protocolos para la recopilación, empaquetado, transferencia y control de datos en el Internet de las Cosas.

### 4. Puertos y Sockets

- **Puerto:** Es un punto final de comunicación para la información que se envía. Siempre tiene un protocolo y una aplicación asociados. Un dispositivo puede tener hasta 65.536 puertos numerados que no cambian.
- **Socket:** Es un canal de comunicación bidireccional que se utiliza cada vez que se envían datos (navegación, correo, video).

Cada socket se compone de: **Dirección IP de origen, Protocolo, Número de puerto, y Dirección IP de destino.**

## Redes y Estándares Inalámbricos

Este segmento describe los diferentes tipos de redes inalámbricas (que usan ondas de radio en lugar de cables) y los estándares IEEE que definen su funcionamiento.

### 1. Tipos de Redes Inalámbricas y Estándares

Las redes inalámbricas siguen los estándares **IEEE** (Instituto de Ingeniería Eléctrica y Electrónica).

| Tipo de Red               | Alcance / Área                          | Estándar IEEE   | Tecnologías                           | Ventajas Clave                                                                              | Desventajas Clave                                                                        |
| :------------------------ | :-------------------------------------- | :-------------- | :------------------------------------ | :------------------------------------------------------------------------------------------ | :--------------------------------------------------------------------------------------- |
| **WPAN** (Personal)       | ~10 metros (alcance personal).          | 802.15          | Bluetooth, Zigbee, Infrarrojos, UWB.  | Flexibilidad, fácil configuración, portátil.                                                | Alcance y velocidades de datos limitados, costo.                                         |
| **WLAN** (Local)          | Hogares, oficinas pequeñas, empresas.   | 802.11 (Wi-Fi)  | Wi-Fi (versiones como 802.11ax).      | Fiabilidad, altas velocidades de datos, versatilidad.                                       | Baja cobertura de red, velocidad afectada por la cantidad de dispositivos, menos segura. |
| **WMAN** (Metropolitana)  | Áreas geográficas, rangos > 100 metros. | 802.16 (WiMAX)  | WiMAX.                                | Cubre varias ubicaciones de la ciudad, fácil de extender, gestionada por ISP/entidad.       | Requiere permisos especiales, menos segura que cableada, más lenta que cableada.         |
| **WWAN** (Global/Extensa) | Regional, nacional y global.            | 802.20 / 802.22 | 4G, 5G, LTE, LoRaWAN, redes privadas. | Cobertura global, mayor seguridad que WLAN, infraestructura flexible y centralizada (Nube). | Costosa, difícil de mantener, cobertura reducida en áreas extensas.                      |
| **WANET** (Ad Hoc)        | Temporal, tamaño terrestre.             | 802.20 / 802.22 | Señales Wi-Fi/tecnología celular.     | Infraestructura flexible y no requerida, configuración instantánea en cualquier lugar.      | Calidad de ancho de banda limitada, no es robusta, riesgos de seguridad.                 |

### 2. Redes Celulares y Evolución

Las redes celulares proporcionan cobertura en malla regional, nacional y global para dispositivos móviles. Cada generación representa una evolución en velocidad y eficiencia:

- **2G:** Compatible con voz digital y datos simples (hasta 64 kbps).
- **3G:** Compatible con banda ancha móvil, permitiendo GPS y descargas multimedia (hasta 2 Mbps).
- **4G:** Aumenta velocidad y eficiencia (hasta 100 Mbps).
- **5G:** Logra hasta 1 Gbps, llevando las redes celulares a un nivel superior.

#### Estándares de Soporte de WWAN/Celulares:

- **IEEE 802.20:** Utiliza antenas inteligentes para optimizar el ancho de banda y la movilidad. Se usa para llenar la brecha entre redes celulares y otras redes inalámbricas.
- **IEEE 802.22:** Utiliza espacios vacíos en el espectro de TV para llevar banda ancha a zonas rurales o de difícil acceso con baja población.

Los casos de uso de estos estándares avanzados incluyen operaciones móviles de emergencia, Internet en aviones, redes ISP y monitoreo a gran escala (sísmico, inundaciones, exploración espacial).

## Protocolos y Puertos Comunes

Este segmento se centra en la definición de protocolos y puertos, la diferencia entre TCP y UDP, y la descripción de protocolos comunes y sus puertos predeterminados.

### 1. Protocolos y Puertos: La Relación

- **Protocolo de Red:** Conjunto establecido de reglas que determina cómo se transmiten los datos entre dispositivos. Los protocolos se basan en estándares de la industria y cumplen tres funciones principales: **Seguridad, Comunicación y Administración de red.**
- **Puerto:** Es un punto final de comunicación (la primera y la última parada de la información en una red). Siempre tiene un protocolo y una aplicación asociados.
- **Relación:** El protocolo es la ruta que lleva al puerto de la aplicación.
- **Puertos Disponibles:** Un dispositivo puede tener hasta **65,536** puertos. Los números de puerto predeterminados no cambian.

### 2. TCP vs. UDP

TCP y UDP son los dos protocolos principales de Internet que se utilizan para enviar y recibir datos a través de los puertos.

| Protocolo                                     | Característica                    | Garantía de Entrega                                     | Uso Típico (Aplicaciones)                                                     |
| :-------------------------------------------- | :-------------------------------- | :------------------------------------------------------ | :---------------------------------------------------------------------------- |
| **TCP** (Protocolo de Control de Transmisión) | Más lento, requiere más recursos. | **SÍ** (garantiza que los datos lleguen).               | Transferencia de archivos (FTP), Navegación web (HTTP/S), Correo electrónico. |
| **UDP** (Protocolo de Datagramas de Usuario)  | Rápido, requiere menos recursos.  | **NO** (no garantiza la llegada de todos los paquetes). | Transmisión en vivo, Juegos en línea, Llamadas por Internet.                  |

### 3. Protocolos Comunes y Sus Puertos

| Categoría                     | Protocolo                                   | Descripción                                                                                            | Puerto Predeterminado | Tipo (TCP/UDP) |
| :---------------------------- | :------------------------------------------ | :----------------------------------------------------------------------------------------------------- | :-------------------- | :------------- |
| **Páginas Web**               | **HTTP** (Transferencia de Hipertexto)      | Acceso estándar a Internet/páginas web.                                                                | 80                    | TCP            |
|                               | **HTTPS** (HTTP Seguro)                     | Acceso cifrado a Internet/páginas web (usado para datos confidenciales).                               | 443                   | TCP            |
| **Transferencia de Archivos** | **FTP** (Transferencia de Archivos)         | Transfiere archivos desde y hacia un servidor/cliente.                                                 | 21                    | TCP            |
|                               | **SFTP** (Transferencia Segura de Archivos) | Transferencia de archivos cifrados.                                                                    | 22                    | TCP            |
| **Acceso Remoto**             | **Telnet** (Red de Teletipos)               | Control remoto a través de consola/línea de comandos (¡No se recomienda por no tener cifrado!).        | 23                    | TCP            |
|                               | **SSH** (Secure Shell)                      | Control remoto seguro (cifrado) a través de consola/shell de comandos.                                 | 22                    | TCP            |
|                               | **RDP** (Escritorio Remoto)                 | Control remoto a través de una Interfaz Gráfica de Usuario (GUI).                                      | 3389                  | TCP/UDP        |
| **Correo Electrónico**        | **POP3** (Protocolo de Oficina Postal v3)   | Recibe correo electrónico (lo descarga del servidor a un dispositivo y luego lo elimina del servidor). | 110                   | TCP            |
|                               | **IMAP4** (Acceso a Mensajes v4)            | Recibe correo electrónico (lo almacena en el servidor y sincroniza con múltiples dispositivos).        | 143                   | TCP            |
|                               | **SMTP** (Transferencia Simple de Correo)   | Responsable del **envío** del correo electrónico.                                                      | 25                    | TCP            |
| **Administración de Red**     | **DHCP** (Configuración Dinámica de Host)   | Asigna automáticamente direcciones IP a los dispositivos.                                              | 67 y 68               | UDP            |
|                               | **DNS** (Sistema de Nombres de Dominio)     | Resuelve (traduce) nombres de dominio a direcciones IP.                                                | 53                    | UDP            |
|                               | **SMB** (Bloque de Mensajes del Servidor)   | Permite compartir archivos e impresoras en la red.                                                     | 137-139               | TCP/UDP        |
|                               | **SNMP** (Admin. Simple de Red)             | Monitorea la red.                                                                                      | 161                   | UDP            |
|                               | **LDAP** (Acceso a Directorios Ligero)      | Almacena y autentica contraseñas y cuentas para servicios de directorio.                               | 389                   | TCP/UDP        |
