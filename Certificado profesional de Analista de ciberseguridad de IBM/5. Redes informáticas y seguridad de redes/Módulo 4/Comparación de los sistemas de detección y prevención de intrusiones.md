# Sistemas de Detección y Prevención de Intrusiones (IDS e IPS)

Este resumen detalla el propósito, las diferencias y el funcionamiento de las tecnologías IDS e IPS dentro de una estrategia de seguridad de red.

## Sistema de Detección de Intrusos (IDS)

- Es una tecnología diseñada para monitorear el tráfico de red en busca de actividades sospechosas y posibles amenazas.
- Detecta e identifica anomalías o infracciones de políticas comparando el tráfico con una base de datos de firmas de ataques conocidos.
- Notifica al personal de seguridad o administradores mediante alertas o registros sobre las amenazas detectadas.
- Se divide en IDS basado en red (monitorea segmentos específicos) e IDS basado en host (supervisa registros y archivos locales).
- Funciona de forma pasiva y fuera de banda, por lo que tiene un impacto mínimo en el rendimiento de la red.

## Sistema de Prevención de Intrusiones (IPS)

- Se basa en las capacidades del IDS pero toma medidas proactivas para bloquear o mitigar las amenazas detectadas.
- Puede eliminar paquetes maliciosos, bloquear direcciones IP infractoras y restablecer conexiones automáticamente.
- Tiene la capacidad de modificar reglas de firewall e iniciar otras medidas defensivas inmediatas.
- El IPS basado en red (NIPS) previene actividades en tiempo real, mientras que el basado en host protege el dispositivo final.
- Al trabajar en línea inspeccionando todo el tráfico, puede afectar el rendimiento de la red.

## Comparación y Defensa por Capas

- **Mecanismo de respuesta**: El IDS genera alertas que requieren acción manual del administrador, mientras que el IPS toma acciones automáticas sin intervención humana.
- **Impacto**: El IDS prioriza el análisis detallado con bajo impacto técnico; el IPS prioriza la interceptación inmediata pero requiere una configuración cuidadosa.
- **Limitaciones**: Ambos pueden generar falsos positivos, pero en un IPS esto puede bloquear tráfico legítimo accidentalmente.
- **Estrategia**: Las organizaciones utilizan ambos para una defensa por capas, aprovechando los datos forenses del IDS y la protección en tiempo real del IPS.
