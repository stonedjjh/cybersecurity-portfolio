# Endurecimiento de Dispositivos (Hardening)

El endurecimiento es el proceso de asegurar un sistema eliminando tantas vulnerabilidades como sea posible. Se basa en el principio de: **"Si no lo necesitas, desactívalo o bórralo"**.

## 1. Capas de Seguridad Física y Lógica

Para proteger el hardware desde el arranque:

- **Contraseñas de BIOS/UEFI:** Evitan que alguien inicie el sistema desde un USB externo para robar datos.
- **Secure Boot (UEFI):** Verifica la firma digital del Sistema Operativo. Si el SO fue modificado por malware, no arranca.
- **TPM (Trusted Platform Module):** Chip físico que guarda claves de cifrado. Si detecta manipulación del hardware, bloquea el acceso.
- **Cifrado de Unidad (Drive Encryption):** Hace que los datos sean ilegibles si el disco duro es extraído o robado.

## 2. Gestión de Puertos y Funciones

Los hackers buscan "puertos" abiertos para entrar. Se deben cerrar todos los que no sean esenciales:

- **Puerto 80:** Tráfico web estándar (HTTP - No seguro).
- **Puerto 443:** Tráfico web seguro (HTTPS - Cifrado).
- **Puerto 22:** Conexiones de servidor seguras (SSH).
- **Funciones de riesgo:** Desactivar **Autorun** (evita virus por USB), **Bluetooth** y **NFC** si no están en uso.

## 3. Parches y Ataques de Día Cero (Zero-Day)

- **Parches:** Actualizaciones que corrigen debilidades ya conocidas. Son reactivos.
- **Ataque de Día Cero:** Una vulnerabilidad nueva que nadie conoce aún. No hay parche disponible.
- **Protección:** Para defenderse de lo desconocido, se usan **VPNs, IDS/IPS** (Sistemas de detección/prevención de intrusos) e higiene de seguridad general.

## 4. Peligros de las Redes y Configuración Inicial

- **Wi-Fi Público:** No tiene cifrado. Cualquiera en la misma red puede "oler" (sniffing) tu tráfico.
  - _Solución:_ Usar VPN, HTTPS o el hotspot del celular (que sí está cifrado).
- **Credenciales Predeterminadas:** Los equipos vienen con usuarios como `admin/admin`. Es lo primero que prueba un hacker.
  - _Acción:_ Cambiar contraseñas de fábrica inmediatamente y deshabilitar cuentas integradas innecesarias.
