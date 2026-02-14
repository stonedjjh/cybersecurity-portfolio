# Tipos de Amenazas: Espionaje, Inyección y Ataques de Red

## 1. Espionaje y Rastreo de Paquetes (Eavesdropping)

El espionaje busca interceptar datos en tránsito entre dispositivos. Se conoce comúnmente como rastreo de paquetes (packet sniffing) y afecta conexiones inalámbricas, cableadas y telefónicas.

1. Rastreadores de paquetes: Herramientas que interceptan todo el tráfico en una red. Si la red no está cifrada, el atacante puede ver, alterar o eliminar los datos.
2. Prevención: Evitar redes wifi públicas, utilizar VPN y asegurar el cifrado de extremo a extremo.

## 2. Ataques de Intermediario (MITM / On-Path)

El atacante se sitúa entre la víctima y el punto de recepción sin que ninguno lo detecte.

1. MITM Físico: El atacante está cerca de la víctima, generalmente en la misma red wifi, "olfateando" el tráfico no cifrado.
2. MITM Lógico: Uso de enlaces falsos en correos o mensajes para robar datos o instalar malware.
3. Ataques de Repetición (Replay Attacks): Intercepción de un token de acceso o clave de seguridad de una entidad confiable para suplantar la identidad del usuario y acceder a cuentas privadas.

## 3. Secuencias de Comandos entre Sitios (XSS)

Consiste en adjuntar código malicioso a sitios web de confianza que se ejecuta cuando el usuario carga la página.

1. XSS Reflejado: El código va incrustado al final de una URL legítima.
2. XSS Persistente: El código se inserta en foros o secciones de comentarios y se ejecuta para cada usuario que visite la página.
3. Prevención: Validar y desinfectar entradas de usuario, establecer reglas de cookies para bloquear JavaScript y configurar Firewalls de Aplicaciones Web (WAF).

## 4. Inyección de Código SQL

El atacante inserta comandos SQL maliciosos en campos de entrada (como el inicio de sesión) para manipular la base de datos del sitio.

1. Detección de vulnerabilidad: Uso de comillas en campos de texto para forzar errores de sintaxis.
2. Consecuencias: Eludir contraseñas, descargar bases de datos completas o eliminarlas.
3. Prevención: Parametrizar consultas, usar listas de permitidos (allowlists) y evitar que el sistema lea entradas de usuario como código ejecutable.

## 5. Botnets y Criptominería

Una botnet es una red masiva de ordenadores comprometidos (zombis) controlados remotamente por un atacante.

1. Uso de Botnets: Realización de ataques a gran escala o tareas de computación intensiva.
2. Criptojacking: Uso no autorizado de la CPU de otros ordenadores para minar criptomonedas, a menudo mediante código incrustado en sitios web.

## 6. Ataques de Denegación de Servicio (DoS y DDoS)

Buscan inundar una red con tanto tráfico que los servicios legítimos se bloquean.

1. Desbordamiento de búfer: Enviar más tráfico del que el sitio puede manejar.
2. Inundación ICMP: Saturar la red con pings de diagnóstico.
3. Inundación SYN: Enviar solicitudes de conexión incompletas para bloquear el servidor.
4. DDoS (Distribuido): Uso de una botnet para realizar el ataque. Es más devastador y difícil de rastrear debido a que el tráfico proviene de miles de fuentes distintas.
