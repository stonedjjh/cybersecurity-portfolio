# Validación y Uso Seguro de Dispositivos

La seguridad no solo depende de las herramientas (Firewalls, Antivirus), sino de la integridad de las fuentes de software y el comportamiento del usuario.

## 1. Fuentes Confiables de Software y Firmware

Instalar software de sitios dudosos es la forma más rápida de comprometer un sistema. Las fuentes legítimas son:

- **Tiendas oficiales:** Windows Store, Google Play, Apple App Store.
- **OEM (Original Equipment Manufacturer):** Sitios oficiales de Dell, HP, Samsung, NVidia, etc.
- **Distribuidores autorizados:** Amazon (directo), Microsoft Store, Adobe.

### Verificación de Seguridad

- **Certificados SSL:** La URL debe empezar con `HTTPS`. El icono del candado permite verificar que el certificado sea vigente y pertenezca al dueño real del sitio.
- **Firmas Digitales:** Los controladores (drivers) deben estar firmados digitalmente. Esto garantiza que el código no ha sido alterado desde que el fabricante lo lanzó.

## 2. Lo que se debe evitar (Don'ts)

- **Software pirata (Torrents):** Casi siempre contienen troyanos o ransomware.
- **Jailbreak o Rooting:** Eliminar las restricciones del fabricante abre la puerta a malware que el sistema operativo normalmente bloquearía.
- **Bloatware:** Desinstalar aplicaciones pre-cargadas que no se usan, ya que al quedar obsoletas se convierten en puertas traseras.
- **Dispositivos desconocidos:** Nunca conectar un USB encontrado en la calle (técnica de "USB Drop").

## 3. Mejores Prácticas de Higiene Digital

- **Principio de Privilegio Mínimo:** Reducir el uso de cuentas con privilegios de Administrador para tareas diarias.
- **Herramientas de Limpieza:** Si un antivirus falla, usar herramientas de eliminación de malware gratuitas de empresas reputadas (McAfee, Norton, Microsoft).
- **Navegación Segura:** No confiar en correos ni siquiera si el remitente es conocido (su cuenta pudo ser comprometida).

> **Diferencia Clave:** Windows Defender protege contra malware y tiene Firewall, pero **NO incluye VPN**. Para cifrar el tráfico en redes públicas, se requiere un servicio de VPN independiente.
