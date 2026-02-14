# Gestión de Correo Electrónico y Spam

La seguridad del correo electrónico se divide en dos: la **gestión técnica** (filtros) y la **prevención humana** (reconocer estafas).

## 1. El Spam (Correo Basura)

Es comunicación digital no solicitada enviada de forma masiva.

- **Propósito:** Publicidad económica o distribución de malware.
- **Riesgo:** Los enlaces pueden conectar tu PC a una **Botnet** (red de robots) o robar datos personales.
- **Mitigación:** \* Usar cuentas de correo desechables para registros no importantes.
  - Bloqueo a nivel de servidor (filtros de dominios).
  - Configurar reglas de eliminación automática en clientes como Outlook.

## 2. Phishing (Suplantación de Identidad)

Es una técnica de ingeniería social donde el atacante finge ser una entidad confiable (banco, jefe, gobierno).

### Anatomía de un ataque de Phishing

Los atacantes juegan con las emociones para anular el pensamiento lógico:

1. **Urgencia:** "Tu cuenta será cerrada en 2 horas".
2. **Miedo:** "Se detectó un inicio de sesión sospechoso".
3. **Codicia:** "Has ganado un premio, reclama aquí".

## 3. Señales de Alerta y Reglas de Oro

- **Errores gramaticales:** Muchas estafas usan traductores automáticos o logotipos pixelados.
- **URLs engañosas:** El texto dice `www.mubanco.com` pero al pasar el mouse encima, el enlace real es `www.estafa-total.xyz`.
- **Archivos adjuntos:** Nunca abrir archivos `.zip`, `.exe` o incluso `.pdf` de remitentes desconocidos.

> **Regla de Oro:** Si recibes un correo sospechoso de tu banco, **cierra el correo**. Abre tu navegador, escribe la dirección del banco manualmente y entra desde ahí. Nunca uses el enlace del correo.
