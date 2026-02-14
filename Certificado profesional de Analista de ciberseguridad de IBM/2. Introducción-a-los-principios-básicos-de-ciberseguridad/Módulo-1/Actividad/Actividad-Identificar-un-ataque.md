# Actividad: Identificar un ataque

Esta actividad consiste en asociar síntomas comunes con el tipo de compromiso de seguridad correspondiente. Se incluye la respuesta esperada por el curso y el análisis técnico extendido.

## 1. Escenario: El sistema está extremadamente lento

1. Síntoma: La computadora rinde de forma inusual, con retrasos significativos en tareas simples.
2. Respuesta: **Computer system compromised**.
3. Lógica técnica: El malware (como mineros de criptomonedas o troyanos) consume ciclos de CPU y memoria RAM en segundo plano, restando potencia a las aplicaciones legítimas.

## 2. Escenario: El ratón se mueve solo o no hay control

1. Síntoma: El cursor del ratón realiza movimientos independientes o el teclado escribe solo.
2. Respuesta del curso: **Network compromised**.
3. Análisis crítico del consultor: Aunque el curso lo asocia a la red (por el uso de protocolos como RDP o VNC), técnicamente ya existe un compromiso de sistema (RAT - Remote Access Trojan). Si el atacante puede mover hardware, ya ha vulnerado las defensas del sistema operativo.
4. Defensa: Deshabilitar el escritorio remoto y aislar el equipo de la red inmediatamente.

## 3. Escenario: Mensajes extraños o solicitudes de amistad

1. Síntoma: Contactos reciben mensajes tuyos en plataformas sociales o recibes solicitudes de personas desconocidas.
2. Respuesta: **Social media compromised**.
3. Lógica técnica: Se basa en la semántica; el término "friends" y "messages" se asocian directamente a redes sociales. La cuenta ha sido secuestrada para propagar spam o phishing.

## 4. Escenario: Amigos reciben correos electrónicos (emails) extraños

1. Síntoma: Personas en tu lista de contactos de correo informan haber recibido enlaces sospechosos desde tu dirección.
2. Respuesta: **Email compromised**.
3. Lógica técnica: El atacante ha obtenido acceso a las credenciales del servidor de correo o ha secuestrado la sesión para enviar correos masivos (spamming) en nombre del usuario.

## Conclusión de la actividad

Identificar el síntoma clave (palabra disparadora) ayuda a categorizar el ataque rápidamente, aunque en la práctica real los vectores suelen estar interconectados. La mejor defensa universal es la autenticación de dos factores (MFA) y el monitoreo de procesos sospechosos.
