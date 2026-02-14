# Control de Acceso, Autorización y Autenticación (AAA)

Para que un sistema sea seguro, no basta con una contraseña; se requiere un equilibrio entre quién puede entrar, qué puede hacer y cómo rastreamos sus acciones.

## 1. El Triángulo de Acceso

- **Control de Acceso:** Establece los límites. Define qué áreas son accesibles y cuáles no.
- **Autorización:** Otorga el permiso específico. Se basa en el **Principio del Menor Privilegio** (dar solo lo necesario para trabajar).
- **Autenticación:** Es la prueba de identidad. Confirma que eres quien dices ser mediante los factores conocidos (Saber, Tener, Ser).

### RBAC (Control de Acceso Basado en Roles)

En lugar de dar permisos usuario por usuario, se crean **grupos** según el organigrama (ej. Grupo "Contabilidad", Grupo "IT"). El acceso se asigna al grupo, y al añadir un usuario al grupo, este hereda automáticamente sus permisos.

## 2. Contabilidad Digital (Auditoría)

Es el registro de lo que sucede en el sistema. Es vital para la informática forense y resolución de fallos:

- **Registros (Logs):** Muestran quién hizo qué, cuándo y cómo se comportó el sistema.
- **Seguimiento y Cookies:** Rastrean detalles técnicos (OS, navegador) y guardan sesiones de navegación.
- **Historial de navegación:** Lista de sitios visitados, usada por empresas para control y por atacantes para suplantación.

## 3. No Repudio

Es la capacidad de garantizar que una persona **no pueda negar** haber realizado una acción o haber estado en un lugar.
Se logra mediante cuatro métodos:

1. **Video:** Grabaciones nítidas de presencia física.
2. **Biometría:** Pruebas físicas de acceso a dispositivos o áreas (huella, iris).
3. **Firmas Digitales:** Combinación de firma con token de hardware que autentica legalmente al firmante.
4. **Recibo:** Comprobante digital de que un mensaje o dato fue enviado y recibido.

> **Reflexión técnica:** La seguridad falla si el equilibrio se rompe. De nada sirve tener MFA (Autenticación fuerte) si todos los usuarios están en el grupo de "Administradores" (Control de acceso débil).
