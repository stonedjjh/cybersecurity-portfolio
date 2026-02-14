# Gestión de Contraseñas y Credenciales

La gestión de contraseñas es un componente crítico de la ciberseguridad que busca proteger el acceso a las cuentas mediante la creación, almacenamiento y mantenimiento seguro de credenciales.

## 1. Características de una Contraseña Fuerte

- **Longitud:** Debe tener entre 12 y 16 caracteres. La longitud es más importante que la complejidad para resistir ataques de fuerza bruta.
- **Complejidad:** Combinar mayúsculas, minúsculas, números y caracteres especiales.
- **Impredecibilidad:** Evitar patrones de teclado (qwerty) o palabras comunes (Password123).

## 2. Riesgos y Políticas Actuales

- **Reutilización:** Nunca usar la misma contraseña en varios sitios. Un compromiso en un sitio pone en riesgo todos los demás.
- **Expiración:** La tendencia actual recomienda cambiar contraseñas solo si hay evidencia de compromiso, no de forma obligatoria y frecuente (esto evita contraseñas débiles y predecibles).
- **Credenciales Predeterminadas:** Es vital cambiar usuarios y contraseñas "de fábrica" en routers, dispositivos IoT y bases de datos inmediatamente tras la instalación.

## 3. Herramientas y Autenticación Avanzada

### Gestores de Contraseñas

Herramientas como Bitwarden o 1Password que:

- Generan contraseñas complejas automáticamente.
- Almacenan credenciales de forma cifrada bajo una única contraseña maestra.
- Sincronizan entre dispositivos y alertan sobre brechas de seguridad.

### Más allá de la contraseña (MFA y SSO)

- **Autenticación Multifactor (MFA):** Combina algo que sabes (contraseña), algo que tienes (token/celular) y algo que eres (biometría).
- **Inicio de Sesión Único (SSO):** Permite acceder a múltiples aplicaciones con una sola autenticación.

## 4. Gestión de Cuentas y Privilegios

Se basa en el **Principio de Menor Privilegio (PoLP)**:

| Tipo de Cuenta       | Permisos Recomendados                                                              |
| :------------------- | :--------------------------------------------------------------------------------- |
| **Administrador**    | Solo para tareas específicas (instalar software, gestionar usuarios).              |
| **Usuario Estándar** | Solo lo mínimo necesario para el trabajo diario (aplicaciones y archivos propios). |

## 5. Mejores Prácticas de Privacidad

- **Shoulder Surfing:** Cuidado con personas mirando tu pantalla en espacios públicos.
- **Restablecimiento Seguro:** Iniciar siempre el proceso desde el sitio oficial, nunca desde enlaces en correos no solicitados (riesgo de Phishing).
