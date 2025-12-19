# Análisis del Comportamiento del Usuario (UBA)

El Análisis del Comportamiento del Usuario (UBA) es el monitoreo sistemático y el análisis detallado de las acciones de los usuarios dentro de una red. Su objetivo principal es **identificar patrones y anomalías** que podrían indicar amenazas de seguridad, a menudo centrándose en amenazas internas o cuentas comprometidas, complementando las medidas de seguridad tradicionales.

---

## - Conceptos Fundamentales de la UBA

La UBA se basa en la diferenciación del comportamiento para detectar riesgos:

- **1. Base del Comportamiento Normal:**
  - Monitoreo de acciones rutinarias (tiempos de inicio de sesión, acceso a archivos) para **establecer un patrón de referencia** de lo que se considera normal para cada usuario.
  - **Ejemplo:** Un empleado que siempre inicia sesión entre las 8:00 a.m. y las 9:00 a.m.
- **2. Detección de Anomalías:**
  - Identificación de **desviaciones significativas** de la línea base, lo que puede indicar posibles amenazas de seguridad o violaciones de políticas.
  - *Ejemplo:* Descarga de grandes cantidades de datos confidenciales a altas horas de la noche por un empleado que normalmente no lo hace.
- **3. Conciencia Contextual:**
  - Análisis del **contexto de las acciones** (función del usuario, patrones típicos, políticas) para evaluar la sospecha.
  - *Ejemplo:* Acceso a archivos sensibles desde una dirección IP desconocida durante un periodo vacacional.

---

## - Técnicas y Herramientas Utilizadas

- **Algoritmos de Aprendizaje Automático (ML):**
  - Aprenden y actualizan automáticamente los patrones de comportamiento de los usuarios, **mejorando la precisión** en el reconocimiento de patrones sutiles y la predicción de amenazas.
- **Análisis Estadístico:**
  - Cuantifica las desviaciones del comportamiento normal utilizando técnicas como la **desviación estándar** y el análisis de correlación para evaluar la importancia de las anomalías.
- **Análisis de Registros:**
  - Analiza registros de diversas fuentes (acceso, aplicaciones, red) para ofrecer una **visión completa** de las actividades y correlacionar datos (ej. intentos de inicio de sesión desde múltiples ubicaciones geográficas, sugiriendo robo de credenciales).

---

## - Casos de Uso Comunes

- **Detección de Amenazas Internas:** Identificación de actividades maliciosas de personas con información privilegiada que se desvían de sus actividades diarias.
- **Cuentas Comprometidas:** Detección de patrones de inicio de sesión o acceso inusuales (ej. acceso desde un país extranjero).
- **Filtración de Datos (Exfiltración):** Supervisión de transferencias de datos no autorizadas (ej. grandes volúmenes de datos enviados a una dirección IP externa).

---

## - Implementación y Desafíos

- **Métodos de Implementación:**
  - **Recopilación Exhaustiva de Datos:** Tráfico de red, registros del sistema y actividad de los usuarios.
  - **Integración con SIEM:** Mejora las capacidades de detección y respuesta al correlacionar datos de la UBA con otros eventos de seguridad.
  - **Monitoreo Continuo:** Análisis constante para adaptarse a los cambios en los comportamientos y amenazas emergentes.
- **Desafíos Clave:**
  - **Privacidad de los Datos:** Garantizar la anonimización de datos y el cumplimiento normativo (ej. GDPR).
  - **Falsos Positivos:** Ajustar el sistema para diferenciar entre cambios legítimos y amenazas, evitando la fatiga de alertas.
  - **Escalabilidad:** Los sistemas deben gestionar grandes volúmenes de datos y usuarios sin reducir el rendimiento, a menudo utilizando soluciones escalables basadas en la nube.

---
