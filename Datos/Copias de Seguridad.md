# Copias de seguridad

Uno de los tres objetivos de la tríada CIA es la **disponibilidad**: debes garantizar el acceso a los datos de la empresa y su uso de manera oportuna y confiable. Las copias de seguridad son un control técnico esencial para cumplir ese objetivo. Con ellas puedes recuperar los datos críticos perdidos debido a incidentes de seguridad, como filtraciones o fallos del sistema.

### Las empresas necesitan copias de seguridad por varias razones:

- Cumplimiento: Algunas leyes y regulaciones requieren que las organizaciones mantengan copias de seguridad de datos críticos, como registros de salud, información de clientes y registros financieros. Si una organización no mantiene copias de seguridad confiables, corre el riesgo de sufrir graves sanciones o acciones legales.

- Protección contra errores de empleados: Si un empleado borra datos importantes por accidente, la organización puede recuperar esos datos desde la copia de seguridad.

- Recuperación ante desastres: Las copias de seguridad garantizan que las organizaciones puedan restablecer datos y sistemas críticos si ocurren desastres naturales, fallas de hardware o ataques cibernéticos.

- Archivo: Las organizaciones pueden usar copias de seguridad para almacenar información a largo plazo y preservar registros históricos.

### **¿Quién, qué, dónde y cuándo?**

Al desarrollar un plan de copia de seguridad, debes responder cinco preguntas:

#### **¿Quién es el responsable de las copias de seguridad?**

Por lo general, los departamentos de TI o de datos se encargan de las copias de seguridad. Sin embargo, las responsabilidades específicas de las copias de seguridad pueden variar en función del tamaño de la organización. Incluso si una empresa automatiza las copias de seguridad, alguien debe monitorear la actividad y probar las copias de seguridad periódicamente.

#### **¿Qué datos se deben respaldar?**

Un plan de respaldo también debe enumerar los tipos de datos que se deben respaldar mediante copias de seguridad.

Deberías hacer una copia de seguridad de todos los datos críticos. Esa información incluye datos confidenciales sobre clientes, empleados y negocios de la empresa. También incluye la configuración del servidor y cualquier otro dato necesario para la funcionalidad del sistema.

- **Registros de empleados** Ejemplos de registros de empleados incluyen contratos laborales, información de contacto e información de la nómina.

- **Registros financieros** Ejemplos de registros financieros incluyen facturas, recibos, registros fiscales y registros contables.

- **Datos de los clientes** Algunos ejemplos de datos de clientes son la información de contacto, el historial de compras o servicios, los registros de soporte y los comentarios.

- **Documentación de la empresa** Algunos ejemplos de documentación de la empresa son los informes de ventas, los registros de producción y los registros de inventario.

- **Propiedad intelectual** Algunos ejemplos de propiedad intelectual son las patentes, los derechos de autor y las marcas registradas.

- **Datos del sistema** Algunos ejemplos de datos del sistema incluyen licencias de software, copias de seguridad de aplicaciones e imágenes y configuraciones del sistema.

#### **¿Qué tipo de copia de seguridad se necesita?**

Luego de decidir qué datos respaldar, debes determinar el tipo de copia de seguridad que vas a utilizar. Tienes tres opciones: **Completa**, **incremental** y **diferencial**.

- **Copia de seguridad completa:** Las copias de seguridad completas copian todo el contenido del sistema o dispositivo. Se respaldan todos los datos, incluso los datos más antiguos de los que ya se hizo una copia de seguridad. Por esta razón, las copias de seguridad completas son las que tardan más en completarse. Pero también son las copias de seguridad más rápidas al momento de la recuperación. Esto se debe a que, a diferencia de otros tipos de copias de seguridad, las copias completas copian todos los datos en el mismo archivo. Un archivo de almacenamiento es una colección de múltiples archivos y metadatos sobre ellos. Los otros tipos de copias de seguridad distribuyen los datos copiados en varios archivos.

- **Copia de seguridad incremental:** Las copias de seguridad incrementales capturan solo los cambios realizados desde la última copia de seguridad. En primer lugar, se realiza una copia de seguridad completa. Pero las copias de seguridad adicionales incluyen solo los cambios realizados desde la última copia de seguridad. Y cada copia de seguridad adicional coloca las copias en un nuevo archivo de respaldo.  

Las copias de seguridad incrementales son el tipo más pequeño, por lo tanto también son las más rápidas de realizar. Pero la recuperación es más lenta que con las copias de seguridad completas. Con las copias de seguridad incrementales, el proceso de recuperación debe extraer datos que están repartidos en varios archivos de almacenamiento, no en uno. Cuanto mayor sea el número de archivos de almacenamiento, más tiempo tardará la recuperación.

- **Copia de seguridad diferencial:** Las copias de seguridad diferenciales combinan los conceptos de copia de seguridad completa e incremental. Primero, se realiza una copia de seguridad completa. Después, cada copia de seguridad adicional incluirá solo los cambios realizados desde la última copia de seguridad completa.

Imagina que haces una copia de seguridad de los datos una vez al día. La copia de seguridad del día 1 es una copia de seguridad completa. La copia de seguridad del día 2 incluye solo los cambios realizados desde ese día 1. La copia de seguridad del día 3 también incluye todos los cambios realizados desde el día 1, incluidos los cambios de los que ya se hizo copia de seguridad el día 2. Por tanto, con las copias de seguridad diferenciales, tu archivo del día 3 es mayor que el que crearías con el método incremental.  

Las copias de seguridad diferenciales suelen ser más grandes que las incrementales y tardan más en completarse. Pero siguen siendo más rápidas que las copias de seguridad completas.

La recuperación con copias de seguridad diferenciales es más lenta que con las copias de seguridad completas, pero a menudo más rápida que con las copias de seguridad incrementales. La razón es sencilla. La recuperación solo extrae datos de dos archivos: el primer archivo completo y el archivo diferencial más reciente.

#### **¿Dónde se deben almacenar las copias de seguridad?**

Luego de averiguar qué tipo de copias de seguridad necesitas, debes determinar dónde guardarlas. ¿Qué tipos de almacenamiento usarás y dónde se ubicarán las copias de seguridad?

##### **Tipos de almacenamiento**

- **Nube** Las copias de seguridad en la nube son más fáciles de configurar y administrar que las que se hacen en las instalaciones. Puedes dejar que tu proveedor de la nube administre las copias de seguridad, así no tienes que lidiar con dispositivos de almacenamiento físico. Por lo general, las copias de seguridad en la nube también cuestan menos. Pero cuanto más tiempo uses el servicio y mayor sea la cantidad de datos que almacenes, mayor será el precio de la copia de seguridad en la nube.

- **Unidad de disco duro** Las copias de seguridad del disco duro son rápidas. Además, no se necesita una conexión a Internet para recuperar las copias de seguridad. Por lo tanto, estas copias de seguridad son excelentes si tu conexión de Internet es irregular o si se desconectan los sistemas durante un ataque. Lamentablemente, también son uno de los tipos de almacenamiento más caros. Y debido a que las unidades se guardan en una oficina, un desastre natural puede dañarlas o destruirlas.

- **Cinta** Las cintas solían ser el tipo de almacenamiento de respaldo de uso habitual. Hoy en día, las empresas rara vez utilizan cintas, excepto para archivar datos muy antiguos. Las cintas requieren más mantenimiento y gestión que otras opciones. Aun así, ofrecen algunas ventajas. Debido a que las cintas están fuera de línea, los atacantes cibernéticos no pueden acceder a ellas. Y las cintas pueden almacenar toneladas de datos de forma más económica que las unidades de disco duro.

##### **Ubicaciones de almacenamiento**

- **Fuera de las instalaciones** El almacenamiento externo tiene dos formas: físico y en la nube. Históricamente, el almacenamiento externo significaba llevar una unidad de disco duro, una unidad óptica o una cinta a un lugar externo para su custodia. Las empresas siguen empleando el almacenamiento físico externo, pero el espacio en la nube es mucho más común.

Ya sea físico o en la nube, el almacenamiento externo debe estar geográficamente separado de tus copias de seguridad en las instalaciones. De este modo, si se produce un desastre natural o algo similar, probablemente no afectará ni a tu almacenamiento en las instalaciones y ni al externo.

El almacenamiento externo tiene desventajas. La recuperación lleva más tiempo que con las opciones de almacenamiento en las instalaciones. Además, el espacio de guardado en la nube se encarece rápidamente.

- **En las instalaciones** El almacenamiento en las instalaciones suele implicar unidades de disco duro, unidades ópticas o cintas. Puedes mantener estas copias de seguridad externas, haciéndolas invulnerables a los ataques cibernéticos. Pero siguen siendo vulnerables a robos, daños físicos y daños ambientales.

##### **Regla 3-2-1**

Para determinar dónde almacenar las copias de seguridad, sigue la regla 3-2-1, una de las mejores prácticas de la industria:

- **3** Crea 3 copias de seguridad de todos los datos críticos: 1 copia de seguridad principal y 2 copias de seguridad más.

- **2** Almacena las copias de seguridad en 2 tipos diferentes de medios de almacenamiento, como unidades de disco duro y almacenamiento en la nube.

- **1** Mantén al menos 1 copia de seguridad fuera de las
instalaciones, ya sea en la nube o en un lugar físico externo.

#### **¿Cuándo se deben realizar las copias de seguridad?**

Tu plan de copias de seguridad también debe incluir una programación. ¿Con qué frecuencia debes hacer copias de seguridad? ¿Todos los días? ¿Cada semana? ¿Cada mes?

Para determinar la programación, considera primero la importancia de los datos para las operaciones diarias y la frecuencia con que cambian.

Podrías combinar copias de seguridad completas con copias incrementales o diferenciales. Por ejemplo, algunas empresas programan una copia de seguridad completa al día con copias incrementales cada 4-6 horas. Otras programan una copia de seguridad completa a la semana con copias incrementales todos los días intermedios.

Recuerda que cada copia de seguridad requiere tiempo y recursos. Si no necesitas una copia de seguridad incremental cada hora, prográmalas con menos frecuencia. Si realizas varias copias de seguridad a la semana, prográmalas de forma que se limiten las interrupciones del flujo de trabajo. Programa copias de seguridad completas solo durante los momentos más tranquilos de la semana.

Sea cual sea la programación que elijas, debe incluir copias de seguridad periódicas. Luego, puedes adaptar los detalles del programa a las necesidades y recursos de tu empresa.
