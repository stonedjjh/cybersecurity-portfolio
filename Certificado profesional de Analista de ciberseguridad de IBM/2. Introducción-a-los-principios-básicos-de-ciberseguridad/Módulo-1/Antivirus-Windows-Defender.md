# Antivirus Windows Defender

Microsoft Defender Antivirus es la solución de seguridad integrada en Windows que proporciona protección en tiempo real contra virus, gusanos y spyware.

## 1. Tipos de Análisis

Windows Defender ofrece diferentes niveles de profundidad según la necesidad:

- **Análisis rápido:** Se enfoca en áreas críticas (memoria, procesos activos, registro y carpetas temporales). Es ideal para un chequeo diario veloz.
- **Análisis completo:** Revisa todos los archivos y programas del disco duro. Puede tardar horas pero es el más exhaustivo.
- **Análisis personalizado:** Permite al usuario elegir carpetas o archivos específicos.
- **Análisis sin conexión (Offline):** Se ejecuta antes de que cargue el Sistema Operativo. Es vital para eliminar malware persistente que se protege cuando Windows está activo.
- **Análisis programado:** Automatización de revisiones mediante el Programador de tareas.

## 2. Acciones tras la detección

Una vez que el antivirus identifica una amenaza, permite tres acciones:

1. **Cuarentena:** Aislar el archivo en un entorno seguro para que no dañe el sistema.
2. **Eliminar:** Borrar definitivamente la amenaza.
3. **Permitir:** Agregar a excepciones si el usuario confía plenamente en el archivo.

## 3. Funciones Avanzadas de Protección

- **Exclusiones:** Posibilidad de indicar qué archivos o procesos no deben ser analizados (útil para evitar falsos positivos en software de desarrollo).
- **Protección contra manipulaciones:** Evita que aplicaciones maliciosas desactiven funciones críticas como la protección en tiempo real o la protección en la nube.
- **Envío automático de muestras:** Envía archivos sospechosos a Microsoft para análisis profundo, mejorando la base de datos global de amenazas.
- **Actualizaciones periódicas:** Descarga constante de nuevas definiciones de virus e inteligencia de amenazas para reconocer ataques de día cero.
