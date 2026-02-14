# Continuidad de Datos y Cifrado

El cifrado es una medida crítica para garantizar la confidencialidad e integridad, permitiendo que las operaciones comerciales continúen de forma segura incluso ante incidentes.

## 1. Importancia para la Continuidad

El cifrado asegura que si un dispositivo (laptop, móvil) es robado o perdido, la información sea inútil para el atacante. Esto evita brechas de datos que podrían detener la operación de una empresa o causar multas legales.

## 2. Datos en Reposo (At Rest)

Información almacenada en discos, bases de datos o nubes.

- **Cifrado a nivel de archivo:** Control granular sobre archivos específicos.
- **Cifrado a nivel de disco (Full Disk Encryption):** Protege todo el dispositivo (ej. BitLocker en Windows, FileVault en macOS).
- **Cifrado de bases de datos:** Protege tablas o campos específicos (como números de tarjetas de crédito).

## 3. Datos en Tránsito (In Transit)

Información que se mueve por la red (Internet, Wi-Fi, redes privadas).

- **HTTPS:** Protege el tráfico web mediante protocolos SSL/TLS.
- **VPN:** Crea túneles cifrados para navegar seguro en redes públicas.
- **Cifrado de correo:** Uso de protocolos como S/MIME o PGP para asegurar que solo el destinatario lea el mensaje.

## 4. Mejores Prácticas

- **Gestión de claves:** El cifrado es tan fuerte como la seguridad de su clave.
- **Actualización de protocolos:** Usar estándares modernos y evitar algoritmos obsoletos.
- **Cumplimiento (Compliance):** Seguir normativas como GDPR (Europa), HIPAA (Salud) o PCI DSS (Finanzas).
