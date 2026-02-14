# Cortafuegos (Firewalls)

Un firewall es un sistema diseñado para prevenir el acceso no autorizado hacia o desde una red privada. Actúa como un filtro que analiza cada dato (paquete) antes de permitirle el paso.

## 1. Tipos de Firewalls

- **Basados en Host (Software):** Se instalan directamente en el dispositivo (ej. Windows Defender Firewall). Controlan el tráfico de puertos y aplicaciones específicas de ese equipo.
- **Basados en Red (Hardware):** Dispositivos independientes situados entre la red interna e Internet (ej. el firewall integrado en un router o equipos empresariales dedicados).

## 2. Métodos de Filtrado

Los firewalls no solo bloquean; deciden basándose en diferentes niveles de inteligencia:

1. **Filtrado de Paquetes:** Revisa fragmentos de datos individuales y los descarta si coinciden con amenazas conocidas.
2. **Inspección de Estado (Stateful):** Supervisa el estado de las conexiones activas. Es más inteligente porque entiende el contexto de la comunicación.
3. **Proxy Firewall:** Actúa como intermediario. El tráfico nunca llega directamente al destino; el proxy lo recibe, lo analiza y luego lo reenvía.

## 3. Perfiles de Red en Windows

El firewall ajusta su rigidez según dónde estés conectado:

- **Dominio:** Para redes corporativas gestionadas centralmente.
- **Privada:** Para hogares o pequeñas oficinas (confianza alta, permite compartir archivos).
- **Pública:** Para aeropuertos o cafeterías. Es la configuración más restrictiva para evitar que otros dispositivos te vean.

## 4. Reglas de Entrada y Salida

- **Reglas de Entrada (Inbound):** Protegen de ataques externos que intentan entrar al sistema.
- **Reglas de Salida (Outbound):** Controlan qué datos envía tu computadora hacia afuera (evita que un malware envíe tu información a un servidor criminal).

> **Estrategia de Oro:** Es mejor aplicar una política de **"Denegar todo por defecto"** y solo abrir los accesos estrictamente necesarios. Es más fácil añadir un permiso que limpiar un desastre por reglas demasiado laxas.
