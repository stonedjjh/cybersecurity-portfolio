# Redes privadas virtuales (VPN)

Una VPN es un túnel cifrado establecido entre dos o más puntos que hace que el tráfico sea ilegible para cualquier atacante que intente interceptarlo. Es fundamental para mitigar ataques de intermediarios (MitM) y de espionaje.

## 1. Tipos de Conexión VPN

- **Sitio a sitio (Site-to-Site):** Conecta dos redes completas a través de Internet (ej. una sucursal con la sede central). El tráfico interno no está cifrado, pero al salir a Internet se cifra mediante dispositivos VPN dedicados.
- **Host a sitio (Host-to-Site):** Un usuario remoto se conecta de forma segura a una red corporativa. El usuario usa software VPN y la empresa usa un dispositivo o software receptor.
- **Host a host (Host-to-Host):** Conexión directa entre dos usuarios o dispositivos remotos. Ambos requieren software VPN.

## 2. Implementación: Hardware vs. Software

### Hardware de VPN

Dispositivos diseñados específicamente o equipos de red con funciones integradas:

- **Enrutadores y Firewalls:** Muchos ya incluyen capacidades VPN.
- **Concentradores de VPN:** Dispositivos especializados para gestionar cientos o miles de conexiones simultáneas.

### Software de VPN

- **Sistemas Operativos:** Incluido de forma nativa en Windows y macOS.
- **Navegadores:** Algunos como Opera o Microsoft Edge ofrecen funciones de VPN integradas.

## 3. Protocolo IPsec (Internet Protocol Security)

Es el conjunto de estándares que permite la criptografía en Internet. Se divide en dos protocolos principales:

- **Authentication Header (AH):** Autentica al remitente y las direcciones IP (garantiza quién envía el dato).
- **Encapsulating Security Payload (ESP):** Cifra el contenido de los datos y también autentica al remitente.

### Modos de IPsec

- **Modo Túnel:** Cifra todo el paquete de datos y le pone un encabezado nuevo. Es el estándar para VPN **sitio a sitio**.
- **Modo Transporte:** Solo cifra el contenido (payload) del paquete; el encabezado IP original queda visible. Es común en VPN **host a sitio**.

## 4. Beneficios Clave

- **Confidencialidad:** Cifrado de datos.
- **Integridad:** Autenticación de datos mediante IPsec.
- **Protección contra reproducción:** Evita que un atacante capture un paquete válido y lo vuelva a enviar para engañar al sistema.
