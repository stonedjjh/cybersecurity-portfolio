# Introducción al análisis forense digital

El campo de la ciberseguridad gira en torno a los datos de las personas u organizaciones. La mayoría de los profesionales de la ciberseguridad trabajan para preservar la confidencialidad, integridad o disponibilidad de estos datos. Pero los investigadores forenses digitales emplean los datos como medio para un fin diferente: llevar a los delincuentes cibernéticos ante la justicia.

Te damos la bienvenida al módulo Ciencia forense de sistemas digitales. En este módulo, aprenderás sobre la ciencia forense digital. Descubrirás las fuentes y usos de los datos forenses digitales y las consideraciones legales para los investigadores, incluida la cadena de custodia. A continuación, conocerás las fases del proceso forense digital. Descubrirás las medidas que toman los expertos en cada fase para preservar la integridad de las pruebas y la investigación. Luego, aprenderás sobre las herramientas forenses digitales. Explorarás los fines que persiguen estas herramientas y descubrirás herramientas y técnicas específicas para trabajar con datos. Inclusive practicarás el uso de herramientas estándar para analizar evidencia forense digital.

## Introducción a la ciencia forense digital

La mayor parte del trabajo de ciberseguridad se centra en prevenir, detectar y mitigar incidentes cibernéticos o recuperarse de ellos. Pero los investigadores forenses digitales van a la ofensiva, empleando sus conocimientos y habilidades para llevar a los delincuentes cibernéticos ante la justicia.

En esta lección, aprenderás los conceptos básicos de ciencia forense digital, incluidas las fuentes y los usos de los datos forenses digitales. También explorarás las consideraciones legales para los investigadores forenses digitales.

## Fuentes de datos forenses digitales

Para realizar la ciencia forense digital, los investigadores necesitan datos. Pueden recuperar datos, incluso datos borrados o cifrados, de varias fuentes. Las fuentes de datos varían según el caso, pero la siguiente lista incluye algunas de las fuentes más comunes.

- Unidades de disco duro internas de computadoras portátiles, tabletas, computadoras de escritorio y servidores físicos

- Medios de almacenamiento de computadora extraíbles, como memorias USB y unidades de disco duro externas

- Medios de almacenamiento de teléfonos inteligentes y cámaras digitales, como tarjetas de memoria y tarjetas Secure Digital (SD)

- Registros de dispositivos de seguridad física, como grabaciones de cámaras de seguridad, registros de sistemas de control de acceso y alertas de alarmas y sensores

- Dispositivos de red, como enrutadores y firewalls

- Medios de almacenamiento óptico, como CD y DVD

Dispositivos periféricos informáticos, como impresoras

- Archivos de registro de red

Muchas de estas fuentes de datos, como los discos duros y otros medios de almacenamiento, almacenan los datos en memoria no volátil. Recuerda que la memoria no volátil (NVM) conserva los datos almacenados incluso cuando apagas el dispositivo.

Pero, ¿qué ocurre con los datos almacenados temporalmente en la memoria RAM de un dispositivo? Son datos volátiles, y recuperarlos puede ser un reto. Los datos volátiles son datos de una sesión en vivo que se pierden cuando finaliza la sesión. Por ejemplo, cuando apagas la computadora, el sistema operativo cierra todos los archivos abiertos. Podrías perder estos y otros archivos temporales de aplicaciones para siempre si no capturaste una imagen de copia de seguridad o una instantánea del sistema en ese estado. Perder esos datos será perjudicial para las investigaciones forenses digitales de todo tipo y en todos los campos.

## Usos de la ciencia forense digital

La ciencia forense digital, o ciencia forense de computadoras o redes, es cada vez más importante para las **autoridades**, las investigaciones **corporativas** y la **seguridad nacional**. Exploremos el uso de la ciencia forense digital en cada ámbito.

### Autoridades

Cuando se trata de la ciencia forense, probablemente pienses en investigaciones criminales. Las autoridades emplean la ciencia forense para investigar delitos que involucran datos digitales.

Ejemplo

Considera el papel fundamental que puede desempeñar la ciencia forense digital en un caso de acoso.

- Los correos electrónicos, mensajes de texto u otros mensajes enviados a la víctima pueden proporcionar pistas sobre la identidad y la ubicación del acosador.

- A partir de las comunicaciones en línea del acosador, los investigadores pueden incluso descubrir su dirección IP, lo que permite establecer aún más su ubicación.

- Los datos de GPS de los teléfonos inteligentes del acosador y de la víctima pueden demostrar que el sospechoso suele estar en los mismos lugares al mismo tiempo que la víctima. Los investigadores pueden emplear esa evidencia para demostrar que el acosador está siguiendo a la víctima.

Todos estos datos, junto con las marcas de tiempo de los mensajes y otros datos relacionados con el tiempo, pueden ayudar a los investigadores a desarrollar una descripción detallada de las actividades del acosador, incluida una cronología. Estos datos pueden proporcionar pruebas suficientes para identificar, arrestar y procesar al sospechoso.

### Corporaciones

En entornos corporativos, los investigadores forenses investigan incidentes, como filtraciones de datos, robo de propiedad intelectual y mala conducta de los empleados. Pueden recuperar datos para determinar quién accedió a ellos y cuándo.

Ejemplos

Los investigadores forenses digitales investigan el fraude en las instituciones financieras.

- Los correos electrónicos, mensajes de texto o de otro tipo pueden demostrar la conexión del sospechoso con el fraude.

- El análisis de los datos financieros puede revelar discrepancias en las cuentas, montos de transacciones inusuales, cuentas de proveedores falsas u otras actividades sospechosas.

- La estación de trabajo de un empleado puede contener evidencia de que el empleado alteró o eliminó archivos confidenciales o almacenó los archivos en un dispositivo de almacenamiento extraíble.

- La actividad del empleado en las redes sociales, incluidas las fotos publicadas, puede contener pistas adicionales.

Con pruebas suficientes, las autoridades pueden procesar a los individuos responsables y evitar que se produzcan incidentes similares en el futuro.

### Seguridad nacional

Las agencias gubernamentales también emplean la ciencia forense digital para investigar fugas de datos, terrorismo, espionaje y delincuencia cibernética. Por ejemplo, la evidencia de un atentado terrorista planeado puede llevar a los investigadores a interceptar las comunicaciones de los sospechosos y evitar que se produzca el atentado. O piensa en un sospechoso de un atentado con bomba. El historial de navegación del sospechoso podría mostrar horas dedicadas a investigar cómo crear bombas. Su historial de compras en Internet podría revelar que encargó todos los materiales necesarios para crear la bomba.

Ejemplo

Considera la importancia de la ciencia forense digital en la búsqueda y detención de una filtración gubernamental.

- Los metadatos de los archivos podrían revelar que el sospechoso accedió a un archivo confidencial sin autorización.

- Los correos electrónicos, textos y mensajes de chat podrían incluir evidencia de que el sospechoso compartió ese archivo.

- Los paquetes que el sospechoso envía a través de la red podrían indicar que envió el archivo a un usuario o dispositivo externo.

- Los registros del sistema y de almacenamiento podrían indicar que alguien almacenó archivos confidenciales en unidades de disco duro externas o compartió los archivos externamente.

Los investigadores pueden emplear estas pruebas para identificar y procesar al filtrador.

## Cadena de custodia

Ahora que conoces algunos de los casos de uso de la ciencia forense digital, aprenderás más sobre las consideraciones legales importantes para realizar este trabajo.

Los investigadores forenses digitales trabajan junto con las investigaciones criminales. Las leyes y regulaciones varían según los gobiernos locales, estatales y federales y entre países. Los investigadores forenses digitales deben conocer los requisitos pertinentes para garantizar que la evidencia que manejan siga siendo admisible en los procedimientos legales. No deben comprometer la integridad de la investigación.

Uno de los requisitos legales más importantes para los investigadores forenses de datos es observar la cadena de custodia.

**La cadena de custodia es un proceso en el que se documenta el ciclo de vida de la evidencia**.

La cadena de custodia es el rastro de auditoría de la evidencia. Indica a todos y todo lo que entró en contacto con evidencia y cuándo, dónde y por qué ocurrió ese contacto. Ya sea manejando evidencia digital o física, siempre necesitas una cadena de custodia confiable.

### Documentación

Cuando los investigadores obtienen su primera prueba, siguen la cadena de custodia y comienzan a completar un formulario de cadena de custodia. Deberían actualizar el formulario de cadena de custodia cada vez que alguien manipule la evidencia.

Observar la cadena de custodia significa registrar información, como los siguientes detalles:

- Fecha, hora y duración en que cada persona manipuló las pruebas

- Acciones que la persona realizó, como transferir, copiar y analizar evidencia, y verificar la integridad de la copia en comparación con el original

- Ubicación en la que se almacena la evidencia cuando no está en uso

El siguiente ejemplo de un documento de cadena de custodia incluye campos en los que proporcionarías dicha información.

### Propósito

¿Por qué seguir una cadena de custodia claramente definida? Demuestra que manipulaste la evidencia correctamente en todo momento. Si alguien rompe la cadena de custodia, la investigación puede ser objeto de acusaciones de manipulación de evidencia. La integridad del sistema y de los datos contenidos se convierte en sospechosa, y las pruebas podrían resultar inadmisibles ante un tribunal.

## Aspecto destacado de la gestión profesional: investigador forense digital

Los investigadores recuperan datos digitales de dispositivos virtuales y físicos, y analizan esos datos usando software forense. También preservan los datos y aseguran su integridad. Otras tareas incluyen colaborar con partes relevantes, como recursos humanos y aplicación de la ley, y compartir sus conclusiones en informes forenses y procedimientos legales.

Para tener éxito, los investigadores deben entender y ser competentes en computadoras, redes, almacenamiento de datos, sistemas operativos, cifrado y software forense. Necesitan un razonamiento sólido y atención a los detalles para ayudarlos a analizar datos y sacar conclusiones válidas y significativas. Deben conocer las leyes y regulaciones de privacidad de datos relevantes para garantizar que sus métodos, hallazgos y conclusiones sean compatibles con el escrutinio legal. Finalmente, deben documentar y comunicar su trabajo de manera clara y persuasiva para audiencias de varios niveles de experiencia, como ejecutivos, abogados y jurados.

## Fases de la investigación forense digital

El número de fases de una investigación forense digital depende del investigador al que se le pregunte. La mayoría de los modelos incluyen de cuatro a cinco fases, mientras que otros incluyen hasta nueve. Los pasos específicos y la terminología empleada para describir cada fase también varían.

En cualquier caso, la mayoría de los modelos forenses digitales incluyen las tareas básicas y el proceso general que se encuentran en el siguiente modelo del National Institute of Standards and Technology (NIST).

- **Recopilación** Identificar todas las posibles fuentes de datos y luego etiqueta, registra y adquiere datos de esas fuentes mientras preservas la integridad de los datos.

- **Examen** Procesar grandes cantidades de datos recopilados para evaluar y extraer los datos más relevantes.

- **Análisis** Analizar los resultados del examen con métodos y técnicas legalmente justificables.

- **Presentación de informes** Informar los resultados del análisis.

### Fase 1: Recopilación

En la primera fase del proceso forense digital, la recopilación, los investigadores identifican todas las posibles fuentes de datos y, a continuación, etiquetan, codifican y recopilan datos de todas las fuentes posibles, preservando la integridad de los datos.

Esta fase requiere conocimientos y habilidades especiales para recuperar datos de forma segura de computadoras, smartphones u otros medios digitales. La persona que recopila evidencia debe saber lo siguiente sobre la recopilación:

- Tipos de datos que puede recopilar

- Métodos para recopilar los datos sin comprometer su integridad

- Leyes y estándares éticos para recopilar, estudiar y usar evidencia forense digital

Cualquier paso en falso podría poner en peligro la credibilidad de la investigación y la relevancia legal en el caso.

La fase de recopilación consta de dos pasos:

1. Identificar las fuentes de datos digitales.

2. Recopilar o crear imágenes de datos de esas fuentes.

#### Paso 1: Identificar fuentes de datos digitales

¿Cómo saben los investigadores forenses por dónde empezar a buscar datos digitales? Su conocimiento y experiencia los guían. Por ejemplo, cuando los investigadores ingresan a la oficina en casa de un sospechoso, casi no deberían tener problemas para detectar fuentes de datos relevantes. Las fuentes potenciales incluyen, entre otras, unidades de disco duro, medios de almacenamiento extraíbles, registros de dispositivos de seguridad, datos volátiles, dispositivos de red y archivos de registro de red.

> [!NOTE]
> Recuerda que los datos volátiles son datos de una sesión en vivo que se pierden cuando finaliza la sesión. Por ejemplo, cuando apagas la computadora, el sistema operativo cierra todos los archivos abiertos. Es posible que pierdas estos y otros archivos temporales de la aplicación para siempre si no capturaste una imagen, o instantánea, de la copia de seguridad, del sistema en ese estado.

#### Paso 2: Recopilar datos de las fuentes

Luego de determinar las fuentes que se emplearán, los investigadores deben recopilar datos de ellas. Según el National Institute of Standards and Technology (NIST), la recopilación de datos implica tres pasos:

1. Elaborar un plan

2. Adquirir los datos

3. Verificar la integridad de los datos

##### Desarrollar un plan

A menudo, los investigadores primero deben desarrollar un plan para recopilar los datos. ¿Por qué necesitan un plan? Por lo general, los datos relevantes pueden residir en muchas fuentes, por lo que los investigadores deben priorizarlos. Para hacerlo, los investigadores consideran factores, como el valor esperado de los datos de una fuente, la volatilidad de los datos y el esfuerzo que implica recopilarlos.

##### Adquirir los datos

En el segundo paso, los investigadores adquieren los datos. Los adquieren con métodos, como el escaneo de discos duros, la extracción de datos de bases de datos y memorias de dispositivos, y la recuperación de archivos borrados. Cada fuente presenta desafíos únicos para la recopilación de datos. Por ejemplo, solo puedes recopilar datos volátiles si el sistema sigue funcionando o si creaste una imagen de copia de seguridad del sistema en ese estado.

Además de adquirir los datos, los investigadores deben hacerles copias de seguridad. Con copias de seguridad precisas, los investigadores pueden estudiarlas y manipularlas según sea necesario, sin poner en peligro la fuente de datos original. En este punto de la recopilación de datos, aseguran la fuente para garantizar que ninguna persona o cosa los manipule en modo alguno durante la investigación.

##### Verificar la integridad de los datos

En el tercer paso, los investigadores verifican la integridad de los datos. Lo hacen empleando valores hash. Un valor hash es una serie de números generados mediante un algoritmo matemático que identifica de forma única un dato. Piensa en un valor hash como en tu huella dactilar. Tu huella dactilar te identifica de forma única. La única persona con la misma huella dactilar que tú es tu clon, ¡y los clones humanos no existen! Del mismo modo, el único dato con el mismo valor hash que el dato de origen es su copia de seguridad idéntica.

¿Qué tienen que ver los valores hash con la integridad de los datos? El software especializado de los investigadores crea valores hash para la fuente de datos original. Cuando hacen una copia de seguridad de esos datos, el software también crea un valor hash para la copia de seguridad, y pueden comparar ese valor con el de la fuente. Si la copia de seguridad cambia lo más mínimo, también su valor hash, lo que demuestra que la copia de seguridad ya no es una copia auténtica del original.

> [!NOTE]
> A lo largo de esta lección, explorarás un escenario en el que una empresa llamada We Insure You maneja un incidente de ciberseguridad. Explorarás el escenario a través de cuatro actividades, una para cada fase del proceso de forense digital. Luego de conocer una fase, leerás cómo We Insure You manejó el incidente de ciberseguridad durante esa fase. Tres actividades contienen verificaciones de conocimientos que ponen a prueba tu comprensión de la fase correspondiente y cómo We Insure You la completó.

### Fase 2: Examen

En la segunda fase del proceso forense digital, el examen, los investigadores examinan los datos recopilados para determinar qué es relevante y extraerlos para su posterior análisis.

Esta fase requiere conocimientos y habilidades especiales para recuperar y examinar los datos con seguridad. El examinador debe tener conocimientos sobre los siguientes temas:

- Tipos de datos que puede extraer sin violar las leyes de privacidad

- Métodos para examinar los datos sin comprometer su integridad

- Estructuras de datos y tipos de archivos relevantes para una investigación

Los investigadores podrían examinar los registros de actividad de los usuarios, los registros de tráfico de red, los archivos de imagen y los metadatos. Por ejemplo, si un sospechoso borra un documento incriminatorio de su memoria USB, los investigadores podrían recuperar parte del contenido del documento a partir de los metadatos de la memoria. Deben documentar cada paso e incluir fotos o capturas de pantalla de las tareas realizadas y de la evidencia adicional encontrada.

#### Desafíos

El examen puede ser difícil. Aunque los obstáculos varían según el caso, los examinadores a menudo enfrentan al menos dos desafíos:

- **Eludir los controles**

Los investigadores deben eludir los controles. Por ejemplo, los sistemas operativos y las aplicaciones pueden tener características de compresión y cifrado de archivos que dificultan el acceso y el examen de los datos. Pero con el conocimiento, las habilidades y las herramientas suficientes, los investigadores pueden eludir estas barreras. Pueden usar herramientas de descifrado de contraseñas para desbloquear archivos cifrados. Incluso pueden extraer archivos de archivos comprimidos y cifrados.

- **Trabajar con una gran cantidad de datos**

Es posible que los investigadores tengan que examinar muchos datos recopilados. Un disco duro puede tener cientos de miles de archivos, no todos relevantes para el caso. Lo mismo ocurre con los registros e informes del sistema. Filtrar entre todas esas fuentes para encontrar los datos más relevantes puede llevar mucho tiempo. E incluso después de que los investigadores identifiquen los archivos de interés, esos archivos suelen contener muchos datos irrelevantes. De los millones de registros de un archivo de registro, solo siete o menos pueden ser relevantes.

Afortunadamente, los investigadores pueden emplear herramientas para agilizar el proceso de filtrado. Por ejemplo, pueden emplear aplicaciones de búsqueda de texto para buscar en una colección de archivos datos concretos, como cadenas de texto que contengan el nombre de una víctima. Algunas herramientas de análisis forense pueden ayudar a encontrar tipos de archivos específicos, nombres de usuario o correo electrónicos relevantes para la investigación. Otras herramientas pueden ayudar a descubrir datos ocultos o eliminados dentro de estos archivos.

### Fase 3: Análisis

En la tercera fase del proceso forense digital, el análisis, los investigadores analizan los datos relevantes de la fase de examen para sacar conclusiones significativas al respecto.

Los investigadores centran su análisis en abordar preguntas relevantes para el caso. Al igual que los científicos, los analistas forenses siguen una metodología estricta para llegar a conclusiones razonables que respalden sus datos. A veces, la única conclusión es que ninguna conclusión es posible sin más datos. Pero los analistas pretenden proporcionar información más útil, como qué o quién causó un incidente.

Los investigadores identifican detalles notables en los datos para sacar conclusiones y determinar su relación. Pueden identificar patrones, determinar causa y efecto o construir una línea de tiempo de eventos. Incluso podrían descubrir evidencia adicional, como pistas en los metadatos de un archivo.

Las herramientas ayudan a los analistas a analizar. Por ejemplo, el software de análisis de seguridad puede ayudar a descubrir evidencia oculta. Con el software de visualización de datos, los investigadores pueden convertir conjuntos de datos complejos en imágenes simples que revelan patrones difíciles de detectar de otro modo.

### Fase 4: Elaboración de informes

En la cuarta fase del proceso forense digital, la elaboración de informes, los investigadores crean y comparten un informe detallado que describe todos los hallazgos de la investigación.

Para resistir el escrutinio legal y persuadir a los lectores, el informe debe ser preciso y completo, y sus conclusiones deben ser lógicamente sólidas y estar basadas en evidencia.

El número y los títulos de las secciones del informe varían. Pero la mayoría de los informes incluyen variaciones de estas cuatro secciones:

1. Descripción general

2. Adquisición forense y preparación de exámenes

3. Resultados e informe

4. Conclusión

- **Descripción general**

En la descripción general o el resumen del caso, el investigador proporciona contexto para la investigación. Explica cómo se involucró en el caso, el estado del caso en ese momento y las funciones que otros desempeñaron en la investigación. Por lo general, los investigadores también detallan el alcance y los objetivos de la investigación.

- **Adquisición forense y preparación de exámenes**

En la sección de adquisición forense y preparación de exámenes, los investigadores explican los métodos empleados. Para empezar, explican dónde recopilaron las pruebas, cómo las procesaron y cómo preservaron su integridad, incluidos los detalles de la cadena de custodia que se siguió. Detallan los procedimientos de recopilación, examen y análisis, incluidas las herramientas empleadas en cada fase. Describen cada dispositivo examinado, incluidas las herramientas usadas para examinarlos y las condiciones en las que se realizó el examen.

- **Resultados e informe**

En la sección de resultados e informes, también conocida como análisis forense, los investigadores describen sus hallazgos en detalle, incluidas las vulnerabilidades u otros problemas descubiertos. Para cada hallazgo, proporcionan ejemplos de la evidencia empleada, como capturas de pantalla de archivos de texto, el resultado de herramientas de análisis y visualizaciones que muestran patrones.

- **Conclusión**

En la sección de conclusión, el investigador resume su análisis y hallazgos. El investigador debe ser conciso y técnicamente preciso en todos los puntos planteados a lo largo del informe. En esta sección también es donde el investigador enumera las recomendaciones para acciones adicionales, como la recopilación, el examen o el análisis de datos adicionales.

## Preservación de datos

La preservación de datos se refiere al proceso de proteger y salvaguardar datos electrónicos para mantener su integridad, autenticidad y usabilidad para fines de investigación.

Ahora que sabes lo que sucede en cada fase del proceso forense digital, aprenderás sobre la importancia de la preservación de los datos durante todo el proceso.

Las pruebas digitales pueden ser muy frágiles. El simple hecho de cambiar el formato de los archivos o abrir un archivo en un sistema operativo diferente puede provocar la pérdida de datos, lo que pone en peligro el alcance y la integridad de la investigación.

Para garantizar la preservación de los datos, los investigadores deben seguir algunas reglas generales.

- **Crear una imagen de los datos**

Los investigadores deben crear una imagen completa de los datos mediante herramientas forenses. Una imagen es una copia bit a bit de todos los datos de un dispositivo, incluidos el espacio libre y los archivos eliminados, que garantiza la integridad de la copia de seguridad. Una imagen es una instantánea de lo que había exactamente en el dispositivo en ese momento.

La imagen debe ser una réplica exacta de los datos originales sin modificaciones, ni siquiera en los registros de acceso al sistema y a los archivos. Para cerciorarse de que la imagen coincide exactamente con el original, los investigadores deben crear la imagen antes de abrir un solo archivo en la fuente de datos. Además, deben almacenar esta imagen en un dispositivo cifrado, en un lugar seguro donde ninguna persona o cosa pueda alterar la evidencia.

- **Verificar la integridad de los datos**

El equipo forense debe verificar la integridad de los datos durante la investigación. Puede hacerlo comparando los valores hash de los datos originales y la imagen. Los valores hash coincidentes confirman que la imagen sigue siendo una copia auténtica del original.

- **Seguir una cadena de custodia**

Los investigadores deben seguir una cadena de custodia detallada para las fuentes de datos y sus datos. La documentación debe indicar quién accedió a la evidencia, cuándo y qué hizo con ella. Los investigadores deben actualizar el formulario de cadena de custodia cada vez que alguien manipula la evidencia.
