# File Integrity Monitoring (FIM)

El Monitoreo de la Integridad de los Archivos (FIM) es un proceso de ciberseguridad vital que verifica continuamente la integridad de los archivos del sistema operativo y del software de aplicaciones comparándolos con una línea base confiable.

## Importancia y Propósito de la FIM

- **Detección de cambios**: Identifica rápidamente modificaciones no autorizadas que pueden indicar infracciones de seguridad, infecciones de malware o amenazas internas.
- **Mantenimiento de la integridad operativa**: Garantiza que los archivos esenciales del sistema y de las aplicaciones no hayan sido manipulados para evitar vulnerabilidades significativas.
- **Cumplimiento regulatorio**: Es un requisito legal para estándares como PCI DSS, HIPAA y SOX, lo que ayuda a generar confianza con clientes y partes interesadas.
- **Defensa en capas**: Complementa otras medidas de seguridad, como firewalls y antivirus, para proporcionar una estrategia de defensa robusta.

## Componentes y Archivos Supervisados

- **Línea base (Baseline)**: Es el punto de referencia creado al capturar el estado de los archivos en un momento específico.
- **Archivos del sistema**: Archivos críticos del sistema operativo necesarios para la funcionalidad y seguridad.
- **Archivos de configuración**: Determinan el comportamiento del software; cambios no autorizados pueden causar errores de configuración o vulnerabilidades.
- **Archivos de aplicaciones**: Incluyen ejecutables y recursos necesarios para el funcionamiento seguro del software.
- **Archivos de datos de usuario**: Contienen información confidencial y su monitoreo asegura el cumplimiento de las normas de protección de datos.

## Proceso de Implementación y Respuesta

- **Definición del alcance y hashing**: Se establecen las líneas base utilizando algoritmos como MD5, SHA-1 o SHA-256 para crear identificadores únicos de cada archivo.
- **Métodos de supervisión**: Puede realizarse mediante escaneos programados (más eficientes en recursos) o monitoreo continuo en tiempo real (detección inmediata).
- **Gestión de alertas**: El sistema notifica a los administradores a través de canales como correo electrónico o SMS ante cualquier modificación, adición o eliminación detectada.
- **Respuesta ante incidentes**:
  - Investigar cambios no autorizados para comprender su causa e impacto.
  - Restaurar archivos afectados utilizando copias de seguridad confiables.
  - Mitigar brechas reparando vulnerabilidades y mejorando las medidas de seguridad actuales.
