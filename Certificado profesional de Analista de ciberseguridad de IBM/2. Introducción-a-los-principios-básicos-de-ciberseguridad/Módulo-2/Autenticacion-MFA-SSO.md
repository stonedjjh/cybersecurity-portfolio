# Autenticación y SSO (Single Sign-On)

La autenticación es el proceso de verificar que un usuario es quien dice ser. Dependiendo de cuántas pruebas se exijan, el nivel de seguridad varía drásticamente.

## 1. Niveles de Autenticación

- **SFA (Single Factor):** Solo una credencial (usuario/contraseña). Es vulnerable a keyloggers (capturadores de teclas), phishing y filtraciones de bases de datos.
- **2FA (Two-Factor):** Requiere dos credenciales. Tradicionalmente basado en hardware (llaves USB/NFC tipo YubiKey). Es la mejor defensa contra el secuestro de cuentas.
- **MFA (Multi-Factor):** El estándar industrial actual. Utiliza una combinación de múltiples capas para reducir significativamente el riesgo.

## 2. Los Tres Factores de Identificación

Para que sea multifactor real, se deben combinar elementos de distintas categorías:

1. **Algo que sabes:** Contraseñas, PIN, preguntas de seguridad o códigos OTP (One-Time Password).
2. **Algo que tienes:** Teléfono móvil (para recibir SMS o usar apps de autenticador), correo electrónico o llaves físicas (tokens).
3. **Algo que eres (Biometría):** Huellas dactilares, reconocimiento facial, escaneo de retina o reconocimiento de voz.

## 3. SSO (Single Sign-On - Inicio de Sesión Único)

Es una propiedad de control de acceso que permite a un usuario iniciar sesión una sola vez y tener acceso a múltiples aplicaciones relacionadas (ej. Office 365, Salesforce).

- **Ventaja para el usuario:** No tiene que recordar ni gestionar decenas de contraseñas.
- **Ventaja para TI:** Centraliza el control y facilita la baja de un empleado de todos los sistemas con un solo clic.

> **Nota Crítica:** Aunque el MFA no es 100% infalible (existen ataques de fatiga de MFA o bypass), es la barrera más efectiva para detener ataques automatizados.
