# Inspección Sin Estado (Stateless Inspection)

- **Definición:** Es un método de inspección de paquetes utilizado por _routers_ comunes y algunos _firewalls_. También se conoce como _filtrado sin estado_.
- **Concepto "Sin Estado" (Stateless):** Los dispositivos inspeccionan **cada paquete de datos individualmente** en los puertos de origen y destino sin recordar ni conocer información sobre los paquetes anteriores o sesiones en curso.
- **Registro:** No mantiene una base de datos o una tabla de sesiones de los paquetes inspeccionados, por lo que no hay registro de las inspecciones previas.

- **Proceso de Inspección de Paquetes:**
  1. Se examina la dirección IP y el puerto de origen. Se utiliza una ACL (Lista de Control de Acceso) o regla para determinar si la fuente está permitida en la red.
  2. Se examina la dirección IP y el puerto de destino para determinar si el servicio o la dirección están permitidos para ingresar a la red.
  3. Este proceso se repite para cada paquete, **sin memoria** de inspecciones anteriores.
- **Ejemplo (Tráfico Web TCP):**

  - Un empleado abre su navegador (creando tráfico TCP o UDP).
  - El encabezado del paquete contendrá la dirección IP de origen (cliente) y la IP de destino (servidor web).
  - Esta información se usa para el enrutamiento.
  - Se añade la información de la Capa 2 (direcciones MAC de origen, destino y de la puerta de enlace).
  - El _router_ evalúa el paquete: si la IP de origen, el tráfico (TCP/UDP) y el puerto de destino están permitidos, el paquete es enviado al servidor.

- **Casos de Uso (Por qué se utiliza):**

  - Proteger los recursos del motor de enrutamiento.
  - Controlar el tráfico que entra o sale de la organización (mediante ACLs).
  - Ayudar a solucionar problemas de red.
  - Administrar el enrutamiento del tráfico (especialmente en entornos de virtualización de _routers_).
  - Realizar tareas de **QoS (Calidad de Servicio)** y **CoS (Clase de Servicio)**, priorizando o marcando el tráfico.

- **Beneficios:**
  - Es más **rápido** que la inspección con estado (_stateful inspection_).
  - Proporciona cierto grado de control sobre lo que está permitido en la red.
  - Es ideal para la resolución de problemas al clasificar los paquetes.

## Inspección con Seguimiento de Estado (Stateful Inspection)

- **Definición:** Es una tecnología de _firewall_ también conocida como **filtrado dinámico de paquetes**. Es crucial para la seguridad de la red ya que monitorea el estado de las conexiones activas.
- **Concepto "Con Estado" (Stateful):** Implica inspeccionar cada paquete de datos **con conocimiento de todos los demás paquetes** que han sido enviados o recibidos en la **misma sesión**.
- **Sesión:** Consiste en todos los paquetes intercambiados entre dos partes.
- **Elementos de la Sesión (Base de Datos):** El _firewall_ mantiene una base de datos o tabla de sesiones que registra elementos clave:

  - Dirección IP de origen y destino.
  - Puerto de origen y destino.
  - Identificador de sesión (ID).
  - Interfaz entrante/saliente, VLAN.
  - Número de paquetes y bytes utilizados en la sesión.
  - Valor de tiempo de espera (timeout) configurable.

- **Flujo de Paquetes en el _Firewall_ (Prioridad de Inspección):**
  - La **inspección sin estado** se realiza _primero_, seguida de la **inspección con estado**.
- **Ruta de un Paquete:**

  - **Si coincide con una sesión existente:** La ruta a través del _firewall_ es más corta. El paquete se evalúa rápidamente, se le aplican los servicios requeridos (como AppTrack, AppDoS, etc.) y se permite o descarta automáticamente.
  - **Si NO coincide con una sesión existente:** La ruta es más larga, ya que debe evaluarse para crear una nueva sesión:
    1. Se aplican las "pantallas" (filtros de protección contra ataques DoS/flooding).
    2. Se aplica NAT estático (si está configurado).
    3. Se realiza el enrutamiento y la evaluación de políticas (zonas y políticas que permiten o descartan el tráfico).
    4. Se aplican los servicios avanzados.
    5. Finalmente, se construye la nueva sesión y se añade a la tabla de estado.

- **Ventaja Clave:** Al recordar los detalles de la sesión, el _firewall_ puede permitir o denegar automáticamente los paquetes subsiguientes de esa misma conexión de manera eficiente y segura.
