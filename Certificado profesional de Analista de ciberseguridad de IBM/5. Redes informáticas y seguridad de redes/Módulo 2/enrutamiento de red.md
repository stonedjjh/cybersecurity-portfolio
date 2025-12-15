## Conceptos Básicos del Enrutamiento de Red

Este resumen se centra en las diferencias entre las capas de red, el papel de ARP, y la función de las tablas de enrutamiento.

---

### 1. Direccionamiento de Capa 2 vs. Capa 3

| Característica   | Capa 2 (Enlace de Datos)                                                          | Capa 3 (Red)                                                                          |
| :--------------- | :-------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------ |
| **Nombre Común** | **Dirección MAC**                                                                 | **Dirección IP**                                                                      |
| **Función**      | **Identificador Físico**. Comunicación **dentro del mismo segmento** (red local). | **Direccionamiento Lógico**. **Enrutamiento** de paquetes **entre diferentes redes**. |
| **Integración**  | Integrada en la tarjeta de interfaz de red (NIC).                                 | Asignada lógicamente (estática o dinámica).                                           |

### 2. Protocolo de Resolución de Direcciones (ARP)

El Protocolo de Resolución de Direcciones (ARP) conecta las Capas 2 y 3.

- **Función:** Mapea una **Dirección IP (Lógica)** a su correspondiente **Dirección MAC (Física)** dentro de una red local.
- **Propósito:** Asegura que los datos enviados a una IP lleguen al dispositivo físico correcto.

### 3. Función de las Tablas de Enrutamiento

- **Ubicación:** Se encuentran en todos los dispositivos de red (principalmente enrutadores).
- **Función Crucial:** Determinar la **mejor ruta** que debe seguir un paquete de datos para llegar a su destino final.
- **Tipos de Rutas:** Incluyen Rutas Predeterminadas y Rutas Directas.

---

**Conclusión:** El direccionamiento de Capa 3 (IP) permite la transmisión de datos entre redes, mientras que el direccionamiento de Capa 2 (MAC), asistido por ARP, facilita la entrega local. Las tablas de enrutamiento guían el tráfico a través de la red.

## Direccionamiento de Capa 2: Direcciones MAC

Este resumen detalla la función, estructura y vulnerabilidades de las Direcciones MAC (Capa 2) en el contexto de las interfaces de red.

---

### 1. La Interfaz de Red (NIC)

- **Definición:** Los sistemas se conectan a través de **Interfaces de Red** (como una tarjeta de interfaz de red, **NIC**).
- **Dirección Física:** La NIC contiene una dirección física grabada, conocida como **Dirección MAC**.
- **Permanencia:** La dirección MAC está codificada físicamente en la NIC y **no se puede cambiar**.

### 2. Estructura de la Dirección MAC

La dirección MAC es el identificador físico para la comunicación dentro de un dominio de transmisión:

- **Longitud:** **48 bits** (o 48 unos y ceros).
- **Formato de Presentación:** Se condensa usando **números hexadecimales** (base 16) para facilitar la lectura humana.
- **División:** Se divide en seis octetos:
  - **Primeros 3 octetos (OUI):** Identificador Único Organizacionalmente. Identifica al **fabricante** de la NIC.
  - **Últimos 3 octetos:** Identifican a la **tarjeta única** de ese fabricante.

### 3. Visualización y Suplantación

| Sistema Operativo | Comando para ver la MAC | Campo de Salida  |
| :---------------- | :---------------------- | :--------------- |
| **Linux**         | `ifconfig`              | N/A              |
| **Windows**       | `ipconfig /all`         | Dirección Física |

- **Suplantación de Direcciones MAC (MAC Spoofing):** Consiste en configurar una interfaz para que represente una dirección MAC diferente.
- **Uso:** Se utiliza para **eludir el filtrado de direcciones MAC** configurado en _firewalls_ para proteger los activos.

### 4. Flujo de Paquetes y Dominios de Transmisión

- **Entrega del Paquete:** El paquete se entrega inicialmente a la dirección MAC de Capa 2. El dispositivo receptor verifica que la MAC y la IP de Capa 3 en el encabezado coincidan con las suyas.
- **Dominios de Transmisión:** El segmento de la red donde un mensaje de _broadcast_ (transmisión general) es recibido por todos los dispositivos.
- **Conexiones:** Un dispositivo con múltiples interfaces (e.g., un router) está conectado a **múltiples dominios de transmisión diferentes**.
- **Equivalencia:** Los dominios de transmisión también se denominan **LAN Virtuales (VLAN)**.

---

## Protocolo de Resolución de Direcciones (ARP)

El Protocolo de Resolución de Direcciones (ARP) es un protocolo fundamental de red esencial para la comunicación fluida entre dispositivos, al **traducir direcciones IP lógicas en direcciones MAC físicas**.

---

### 1. Conceptos Fundamentales

| Concepto | Descripción | Rol en la Red |
| :--- | :--- | :--- |
| **Dirección IP** | Identificador lógico único asignado a cada dispositivo en una red. Permite la comunicación a nivel de red (Capa 3). | Identificación del dispositivo a nivel de red. |
| **Dirección MAC** | Dirección física única (Dirección de Control de Acceso a Medios) grabada en el hardware de red (NIC). Necesaria para la entrega final de datos a nivel de enlace de datos (Capa 2). | Entrega de datos dentro del mismo dominio de transmisión (red local). |
| **ARP** | **A**ddress **R**esolution **P**rotocol (Protocolo de Resolución de Direcciones). | Convierte una **Dirección IP** conocida en su **Dirección MAC** correspondiente. |

### 2. La Tabla ARP

La **Tabla ARP** es una caché que almacena las asignaciones (traducciones) de direcciones IP a direcciones MAC que un dispositivo ha aprendido recientemente.

- **Propósito:** Permite a los dispositivos localizar direcciones MAC de forma eficiente sin tener que realizar el proceso de solicitud ARP cada vez.
- **Visualización:** Se puede ver en sistemas operativos (Windows, Linux, macOS) utilizando el comando `arp -a` en la línea de comandos o terminal.
  - En un router Linux, se usa el comando `ip neighbor show`.
- **Uso en Solución de Problemas:** Es una herramienta crucial para diagnosticar problemas de red y verificar las asignaciones de direcciones.

### 3. Funcionamiento de ARP (Proceso de Solicitud/Respuesta)

Antes de que un dispositivo pueda enviar un paquete de datos a otro dispositivo dentro de la misma red local, necesita conocer la dirección MAC del destino. **Un paquete siempre se entrega a una dirección física (MAC), no a una IP.**

El proceso de operación de ARP ocurre en dos pasos clave:

1. **Solicitud ARP (ARP Request):**
  
- El dispositivo de origen (Ej.: 192.168.52.4) quiere hacer ping a un destino (Ej.: 192.168.52.100), pero no tiene su MAC.
  
- Envía un paquete de **difusión** (broadcast) a **todos** los dispositivos del dominio de transmisión.

- El mensaje es esencialmente: *"¿Quién tiene la IP 192.168.52.100? Por favor, envíame tu dirección MAC."*

2. **Respuesta ARP (ARP Reply):**

- El dispositivo con la IP solicitada (192.168.52.100) es el único que responde.

- Envía un paquete de **unicast** (directo) al remitente.

- El mensaje es: *"Yo tengo la IP 192.168.52.100, y mi dirección MAC es [la dirección física]."*.

- El remitente actualiza su Tabla ARP con esta nueva traducción IP-MAC.

Una vez que la tabla ARP se ha completado, la comunicación real (como el ping/ICMP) puede transmitirse con éxito.

### 4. Direcciones MAC y Enrutamiento

La necesidad de la dirección MAC depende de si la comunicación es local o remota:

- **Comunicación Local (Mismo Dominio de Transmisión):** Solo se necesita la **dirección MAC del dispositivo de destino** para entregar los datos.

- **Comunicación Remota (Diferente Dominio de Transmisión):** Se necesita la **dirección MAC de la Puerta de Enlace Predeterminada** (Generalmente el Router).
  - El dispositivo utiliza ARP para encontrar la MAC del *router*, y luego el router se encarga de dirigir el paquete hacia la red externa (utilizando su propia **Tabla de Enrutamiento**).

ARP es fundamental porque traduce el identificador lógico (IP) utilizado por las aplicaciones y la capa de red al identificador físico (MAC) requerido para la entrega de datos a nivel de hardware.

# ARP, Routers y Tablas de Enrutamiento

Este resumen integra la función del Protocolo de Resolución de Direcciones (ARP) con el rol de los Routers y las Tablas de Enrutamiento, destacando cómo las Capas 2 (MAC) y Capa 3 (IP) trabajan juntas para la comunicación de red.

---

## 1. Tablas de Enrutamiento (Capa 3: Red)

La Tabla de Enrutamiento es un componente esencial para dirigir el tráfico.

- **Ubicación:** Todos los dispositivos conectados a una red (routers, servidores, computadoras) mantienen su propia tabla.

- **Función:** Consultada por el dispositivo para determinar la **mejor ruta** (interfaz de salida o Puerta de Enlace) basándose en la **Dirección IP de destino**.

- **Contenido:** Cada entrada (o tupla) consta principalmente de:
  1. **Destino de Red:** La dirección o rango de red al que se quiere llegar.
  2. **Interfaz:** El puerto de salida o la Puerta de Enlace para el siguiente salto.

- **Actualización:** Las tablas se actualizan **dinámicamente** para adaptarse a los cambios en la red.

- **Comando de Visualización:** Se puede ver con comandos como `netstat -nr`.

## 2. La Lógica del Enrutamiento y la Puerta de Enlace

Cuando un dispositivo necesita enviar un paquete, aplica la siguiente lógica basada en su Tabla de Enrutamiento:

- **Destino Local (Mismo Dominio de Transmisión):**
  - Los datos se envían **directamente** al destino.
  - **Proceso ARP:** El dispositivo utiliza ARP para convertir la IP de destino en su MAC y entregar la trama.
- **Destino Remoto (Red Diferente):**
  - Si la IP de destino no está en la red local o en la tabla, el paquete se reenvía a la **Puerta de Enlace Predeterminada (Gateway)**.
  - **Proceso ARP:** El dispositivo usa ARP para encontrar la **MAC del Router/Gateway**, y luego entrega el paquete a ese router para que lo dirija más lejos.

## 3. Interfaces y Dominios de Transmisión

- Las **Interfaces de Red** (Ej: `enp0s9`) gestionan el tráfico dentro de sus respectivos **Dominios de Transmisión** (redes locales).

- En el contexto de un router, una interfaz puede ser un punto final (para una red local) y otra puede ser la Puerta de Enlace Predeterminada (conectada a otra red o Internet).

## 4. ARP (Capa 2: Enlace de Datos)

ARP es el puente entre las dos capas.

- **Función:** Traduce la **Dirección IP (Capa 3)** en la **Dirección MAC (Capa 2)**.

- **Necesidad:** Un paquete nunca se entrega a una IP, sino siempre a una dirección física (MAC).

- **Proceso:** El equipo de origen envía una **Solicitud ARP** (broadcast) preguntando por la MAC de una IP conocida. El destino responde con su MAC (**Respuesta ARP**).

- **Tabla ARP:** Almacena la tupla (par **IP, MAC**) aprendida para evitar futuras solicitudes.

## 5. Diferencia Clave: Routers (Capa 3) vs. Switches (Capa 2)

| Dispositivo | Capa Principal | Dirección Utilizada | Mecanismo de Reenvío |
| :--- | :--- | :--- | :--- |
| **Router** | Capa 3 (Red) | **Dirección IP** | Utiliza la **Tabla de Enrutamiento** para decidir el mejor camino entre redes. |
| **Switch** | Capa 2 (Enlace de Datos) | **Dirección MAC** | Utiliza la **Tabla MAC** para dirigir la trama a la interfaz correcta dentro de la red local. |

## Recorrido del Paquete y Múltiples Redes

Este segmento describe cómo los paquetes de datos viajan a través de múltiples routers y redes (dominios de transmisión) utilizando las rutas predeterminadas y las tablas de enrutamiento y ARP.

---

### 1. Componentes Clave de la Comunicación en Múltiples Redes

La comunicación eficiente y segura en las organizaciones depende de la interacción de varios componentes de red:

- **Dominio de Transmisión (Segmento de Red):** La red local o segmento donde todos los dispositivos se comunican directamente entre sí en la **Capa de Enlace de Datos (Capa 2)**.
- **Puerta de Enlace Predeterminada (Gateway):** El punto de salida que conecta una red local a otras redes externas o a Internet.
- **Router:** Un dispositivo de Capa 3 (o un firewall/conmutador de Capa 3) que conecta diferentes redes y utiliza tablas de enrutamiento para tomar decisiones de reenvío.
- **Tabla de Enrutamiento:** Almacenada en routers y computadoras, lista las rutas a destinos para determinar el camino más eficiente para reenviar paquetes.
- **Tabla ARP:** Utilizada por los routers para hacer coincidir las direcciones IP con las direcciones MAC de los dispositivos **dentro de la misma red local**.

### 2. El Viaje del Paquete a Través de Múltiples Redes

El proceso de envío de un paquete de una red a otra involucra una serie de decisiones de enrutamiento y saltos (hops).

#### Escenario: Envío de Paquete (Red 1 → Red 3)

Imaginemos que un dispositivo **1.8** de la **Red 1** quiere enviar un paquete al dispositivo **3.6** de la **Red 3**, conectados por el Router 1 y el Router 2. 

1. **Dispositivo de Origen (1.8):** Solo necesita tener configurada una **Ruta Predeterminada** que apunte a su Puerta de Enlace. En este caso, el Puerto 1 del Router 1.
2. **Router 1 (Decisión del Primer Salto):**

- Recibe el paquete.
- Comprueba la IP de destino (3.6).
- Si la Red 3 (donde está 3.6) **no está conectada directamente** al Router 1, este envía el paquete a su propia Puerta de Enlace Predeterminada. En este ejemplo, esa Puerta de Enlace es el Puerto 1 del Router 2.

3. **Router 2 (Entrega Final):**

- Recibe el paquete.
- Identifica que el dispositivo **3.6 está conectado directamente** a su Puerto 2.
  - **Utiliza su Tabla ARP** para encontrar la Dirección MAC (MAC Adress) de 3.6.
- Entrega el paquete final al dispositivo 3.6.

### 3. Comunicación Bidireccional (Rutas de Retorno)

Para que la comunicación sea exitosa (por ejemplo, para que un `ping` se aplique y el dispositivo 1.8 reciba la respuesta):

- Debe existir una **ruta de envío** (1.8 a 3.6).
- Debe existir una **ruta de retorno** (3.6 a 1.8) a través del Router 2 y el Router 1.

### 4. Conclusión del Proceso

Los enrutadores interconectan varios dominios de transmisión. La entrega de paquetes se facilita mediante:

- El mantenimiento de **Rutas Predeterminadas** en los dispositivos.
- El uso de **Tablas de Enrutamiento** en los routers para determinar la ruta más eficiente entre redes.
- El uso de **Tablas ARP** en los routers para mapear IP a MAC al entregar paquetes dentro de la red local conectada.

## Tipos de Rutas y Lógica de Reenvío

Este segmento finaliza la discusión sobre enrutamiento analizando los diferentes tipos de rutas que componen una tabla y reafirmando el papel de la Tabla ARP en el contexto de la Puerta de Enlace Predeterminada.

---

### 1. Tipos de Rutas

Las tablas de enrutamiento contienen diferentes tipos de rutas, cada una con un propósito específico para dirigir el tráfico (paquetes).

#### A. Ruta Predeterminada (Default Route)

- **Función:** Es la "ruta de último recurso". Se utiliza para enviar datos a destinos que **no figuran específicamente** en la tabla de enrutamiento.
- **Uso Práctico:** Si un dispositivo necesita enviar un paquete a una IP desconocida (Ej: 4.2.2.2), el paquete se envía a la Puerta de Enlace Predeterminada (Ej: 10.0.4.2), y esta se encarga de enrutarlo al siguiente salto.
- **Importancia:** Garantiza la conectividad incluso cuando los detalles de la red de destino son desconocidos.

#### B. Ruta Conectada Directamente (Directly Connected Route)

- **Función:** Indica una red que está conectada directamente a una interfaz física del router o servidor.
- **Uso:** Simplifica la comunicación y garantiza que los paquetes a redes vecinas inmediatas no tengan que pasar por saltos innecesarios.

#### C. Rutas Estáticas y Dinámicas

- **Rutas Estáticas:** Son establecidas **manualmente** por un administrador de red. No cambian automáticamente.
- **Rutas Dinámicas:** Se **actualizan automáticamente** mediante protocolos de enrutamiento dinámico (Ej: OSPF, RIPv1, RIPv2, EIGRP), adaptándose a los cambios y condiciones de la red para mejorar la eficiencia y la adaptabilidad.

### 2. La Lógica del Reenvío de Paquetes

Los dispositivos utilizan la Tabla de Enrutamiento para tomar una decisión sobre el siguiente salto.

- **Caso de Uso (Ping Exitoso a Red Remota):**
  - Si un dispositivo (Servidor 100) intenta hacer ping a una IP remota (Servidor 200, IP 172.16.52.100), y **no hay una ruta directa** en su tabla para `172.16.0.0`.
  - La tabla de enrutamiento dirige el paquete a la **Puerta de Enlace Predeterminada**.
  - La Puerta de Enlace garantiza la entrega del paquete a través de múltiples saltos hasta que el paquete llega a un dispositivo de Capa 3 que tiene el destino **conectado directamente**.
- **Comprobación:** El comando `traceroute` (o `tracert`) permite ver exactamente cómo se enruta el paquete desde el host local a través de la Puerta de Enlace.

### 3. El Papel Estricto de la Tabla ARP

El texto reitera la función limitada, pero crítica, de la Tabla ARP:

- **Restricción de ARP:** La Tabla ARP solo se llena con las direcciones IP y MAC de los dispositivos que están **conectados directamente** a las interfaces del router, es decir, solo los dispositivos dentro del **mismo dominio de transmisión local**.
- **Ejemplo:** Aunque el ping a la dirección remota `172.16.52.100` sea exitoso, esa dirección **no** se agregará a la Tabla ARP local.
- **Uso con el Gateway:** Al enviar datos a una dirección IP remota, el dispositivo necesita la **Dirección MAC de la Puerta de Enlace Predeterminada** (Ej: 192.168.52.4). La traducción de esa IP (la del Gateway) a su MAC (Ej: 08:00:27:84:64:a5) **sí** se busca y se almacena en la Tabla ARP, ya que el Gateway está en el segmento de red local.

**Conclusión:** La Tabla de Enrutamiento determina a dónde enviar un paquete (la IP del Gateway). La Tabla ARP determina la dirección MAC necesaria para enviar ese paquete físicamente al Gateway (el siguiente salto).
