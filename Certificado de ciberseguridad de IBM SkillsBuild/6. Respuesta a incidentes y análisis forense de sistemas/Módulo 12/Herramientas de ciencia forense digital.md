# Herramientas de ciencia forense digital

Las herramientas forenses digitales son hardware o software que recopilan, extraen, clasifican, preservan o recuperan evidencia digital.

## Elegir las herramientas forenses digitales adecuadas

La disciplina de la ciencia forense digital comenzó cuando los datos y dispositivos digitales, como las computadoras, se convirtieron en algo habitual. Al principio, analizar estos dispositivos era sencillo. Pero la tecnología evolucionó en las últimas décadas. Los teléfonos inteligentes, las plataformas de redes sociales, el almacenamiento en la nube y los dispositivos crean, transmiten y almacenan enormes cantidades de datos cada día. Y los conjuntos de datos ahora no solo incluyen texto y números, sino también imágenes, videos, grabaciones de audio y otros elementos multimedia.

A medida que aumentaba la cantidad y complejidad de los datos almacenados en dispositivos digitales, también aumentaba la necesidad de herramientas especializadas para trabajar con estos datos para investigaciones forenses. Los investigadores necesitan herramientas para recopilar, extraer, analizar y preservar datos cada vez más complejos sin comprometer su integridad. Los profesionales de ciberseguridad se refieren a estas herramientas como herramientas forenses digitales.

Para determinar qué herramientas usar, los investigadores deben considerar los siguientes criterios.

### Características

Los investigadores deben tener en cuenta las características de la herramienta. ¿Para qué usarán la herramienta, con qué tipo de datos trabajarán y en qué formato los almacenarán? Por ejemplo, es posible que necesiten una herramienta para extraer direcciones de correo electrónico de un archivo de imagen de disco y almacenar esos datos en un archivo de texto. Los investigadores también deben considerar cómo analizarán los datos. Con herramientas, como Autopsy, los investigadores pueden realizar búsquedas de palabras clave y análisis de líneas de tiempo.

### Confiabilidad y precisión

Los investigadores deben considerar la confiabilidad y precisión de la herramienta. ¿Ellos u otros expertos probaron y avalaron la herramienta? ¿La herramienta tiene un historial comprobado de eficacia en investigaciones similares? En resumen, ¿los investigadores confían en esta herramienta?

### Facilidad de uso

Los investigadores deben considerar la facilidad de uso. ¿Qué conocimientos técnicos y experiencia necesitan para emplear la herramienta de manera eficaz? Por ejemplo, algunos softwares forenses vienen con una interfaz gráfica de usuario (GUI) fácil de usar. Otros están disponibles solo como aplicaciones de línea de comandos y pueden ser difíciles de usar sin experiencia en esta área.

### Asequibilidad(Costo)

Los investigadores deben considerar la asequibilidad. ¿Cuánto cuesta la herramienta? ¿Está dentro de su presupuesto? Existen muchas herramientas gratis de código abierto para realizar tareas básicas de análisis forense digital. Pero algunas de las herramientas más complejas y poderosas pueden ser costosas.

## Objetivos de las herramientas forenses digitales

Los investigadores emplean herramientas forenses digital durante la mayor parte del proceso de análisis forense digital. Los tipos y la cantidad de herramientas necesarias dependen de los objetivos, las fuentes de datos y los datos de la investigación.

En general, los investigadores emplean herramientas con cuatro fines.

- **Adquisición y análisis**

Las herramientas de adquisición y análisis recopilan y analizan evidencia digital de fuentes de datos, como unidades de disco duro y tarjetas de memoria. Una herramienta estándar de la industria para esto es EnCase Forensic. Con esta herramienta, los investigadores pueden buscar palabras clave o cadenas de caracteres dentro de los bloques de datos y descubrir archivos ocultos y eliminados.

Otras herramientas que los investigadores suelen emplear para la adquisición y el análisis son Autopsy, FTK Imager y Volatility.

- **Clasificación**

Las herramientas de clasificación analizan rápidamente grandes cantidades de datos adquiridos en busca de archivos o palabras clave importantes. Por ejemplo, los investigadores pueden usar Belkasoft Evidence Center para examinar el espacio no asignado de un dispositivo o el volcado de memoria en busca de nombres de usuario, correo electrónicos y tipos de archivos específicos.

Algunas otras herramientas que los investigadores suelen emplear para la clasificación incluyen Bulk Extractor, Electronic Evidence Examiner, EnCase Portable y BlackLight.

- **Creación de imágenes**

Las herramientas de creación de imágenes crean una imagen digital, o copia, fiel al original, de una unidad de disco duro, una memoria USB u otro medio de almacenamiento. Por ejemplo, los investigadores pueden usar X-Ways Forensics para realizar diversas tareas forenses, pero la herramienta es especialmente útil para obtener imágenes rápidas de cualquier medio de almacenamiento.

Otras herramientas que los investigadores suelen emplear para la obtención de imágenes son Foremost y FTK Imager.

- **Recuperación**

Las herramientas de recuperación recuperan archivos eliminados o inaccesibles, proporcionando evidencia valiosa en algunos casos. Por ejemplo, los investigadores pueden emplear PhotoRec para recuperar datos de imágenes dañadas o corruptas.

Otras herramientas que los investigadores suelen emplear para la recuperación son TestDisk, R-Studio y Recuva.

## Creación de imágenes

Imagina que eres un trabajador de TI. Tu jefa sospecha que un empleado resentido borró archivos que contenían datos importantes del cliente; te asigna la tarea de encontrar y recuperar esos archivos. Si los archivos aún existen, están en la unidad de disco duro de la computadora del empleado. Puedes trabajar directamente en esa unidad para recuperar los datos. Pero la recuperación de archivos puede complicarse y, si accidentalmente sobrescribes o corrompes estos archivos, podrías perder los datos para siempre. Entonces, creas una imagen de la unidad y luego trabajas en esa imagen para recuperar los archivos.

Los investigadores forenses digitales crean imágenes de disco por razones similares. Recuerda que una imagen es una copia bit por bit de todos los datos de un dispositivo, incluyendo espacio libre y archivos eliminados, lo que garantiza la integridad de la copia de seguridad. Con una imagen, el investigador puede estudiar y manipular una copia precisa de los datos sin comprometer el original. Para confirmar que la imagen es una copia exacta, los investigadores comparan los valores hash del original y de la imagen. Los valores hash coincidentes confirman que la imagen sigue siendo una copia auténtica del original.

### Bloqueadores de escritura

Antes de crear una imagen de disco, un investigador suele conectar la fuente de datos, como una unidad de disco duro, a un bloqueador de escritura. Un bloqueador de escritura es un dispositivo que bloquea cualquier comando de escritura enviado a un dispositivo de almacenamiento. Con un bloqueador de escritura, los investigadores pueden cerciorarse de no alterar accidentalmente la fuente de datos. A su vez, pueden crear la imagen sin el riesgo de comprometer la integridad del original en el proceso.

### FTK Imager

Una de las herramientas de creación de imágenes más confiables es FTK Imager. FTK Imager es una herramienta de código abierto para crear imágenes de disco sin riesgo de realizar incluso cambios menores en la fuente de datos original.

Con FTK Imager, puedes realizar las siguientes tareas:

- Crear imágenes de discos duros, disquetes, CD, DVD, carpetas y archivos.

- Crear valores hash para la imagen y el original, y luego compararlos para confirmar la integridad de la imagen.

- Obtener una vista previa de los datos de la fuente sin el riesgo de dañar la fuente de datos. De esa manera, puedes decidir si los datos merecen un análisis adicional, posiblemente ahorrando tiempo y esfuerzo en la obtención de imágenes de datos inservibles.

- Montar una imagen para una vista previa de solo lectura, similar a montar un dispositivo de almacenamiento conectado a un bloqueador de escritura. Con esta vista previa, puedes examinar el contenido de la imagen tal como lo hizo el usuario con la fuente de datos original.

- FTK Imager está disponible en Microsoft Windows y Linux. La versión de Windows viene con una GUI, pero también puedes usar la línea de comandos. Sin embargo, la versión de Linux requiere usar la línea de comandos.

### Recuperación de datos

La recuperación de datos es un proceso para recuperar datos perdidos, eliminados, dañados o inaccesibles.

Piensa en la situación anterior, en la que eres un informático que intenta encontrar archivos borrados en el disco duro de un empleado. Tras crear una imagen de la unidad, la examinas para determinar si puedes recuperar los archivos borrados. Los profesionales de la ciberseguridad se refieren a este proceso de rescate como recuperación de datos.

La recuperación de datos ayuda a los investigadores a encontrar todos los datos forenses relevantes en un dispositivo. Hacerlo puede ser un reto si, por ejemplo, un sospechoso borra o cifra archivos incriminatorios. Pero con las herramientas de recuperación, los investigadores pueden descubrir esos archivos y cerrar el caso.

Para explicar cómo funciona la recuperación de datos, exploremos primero el proceso de recuperación de un archivo borrado.

## Otras herramientas forenses digitales clave

Aprendiste sobre las herramientas forenses digitales estándar e incluso practicaste su uso en una investigación forense digital. Exploremos varias herramientas forenses digitales más que cualquier profesional de ciberseguridad debería conocer.

- **Volatility**

Volatility es valiosa para identificar y analizar software malicioso, como un virus, en la memoria de un sistema. Muchas herramientas analizan datos en unidades de disco duro, memorias USB u otros dispositivos de almacenamiento estándar para memoria no volátil (NVM). Pero como su nombre lo indica, Volatility analiza datos volátiles, específicamente datos volátiles en RAM. Con esta herramienta, los investigadores pueden extraer datos del sistema operativo y los procesos que se ejecutan en la memoria.

Pensemos en un investigador que estudia una infección de malware. El malware a menudo oculta procesos en segundo plano o servicios asociados con él, lo que dificulta su detección mediante herramientas básicas del sistema. Pero con Volatility, el investigador puede analizar el contenido de la memoria del sistema para descubrir estos procesos. El investigador también puede identificar las conexiones de red o los archivos que abrió el malware.

- **Kali Linux**

Si quieres trabajar en ciberseguridad, deberías explorar Linux. Es una familia de sistemas operativos (SO) de código abierto que se ejecuta en la mayoría de los dispositivos de red, aplicaciones de seguridad y servidores basados en la nube. Necesitarás conocer Linux para reforzar la seguridad o recopilar los datos de seguridad de estos dispositivos, aplicaciones y servidores.

La familia Linux incluye cientos de sistemas operativos Linux diferentes, también conocidos como distribuciones. Kali Linux es una de las distribuciones más populares para pruebas de penetración, hacking ético y análisis forense digital. Viene con una serie de herramientas estándar de ciberseguridad para tareas, como el análisis de redes, la ingeniería inversa, el escaneo de vulnerabilidades y la explotación. Además, recibe actualizaciones periódicas con nuevas herramientas, exploits y funciones, lo que lo convierte en un recurso inestimable para los profesionales de la ciberseguridad. Además, es fácil de usar y puedes ejecutarlo desde Windows o macOS como máquina virtual.

> [!NOTE]
> Recuerda que una máquina virtual (VM) es una versión meramente basada en software de una computadora y un SO que se ejecuta dentro del sistema operativo real de un dispositivo. Las VM pueden ejecutar sus propias aplicaciones y otro software, al igual que las máquinas físicas.

Kali Linux viene con numerosas herramientas forenses digitales preinstaladas, como Autopsy, Bulk Extractor, Foremost, entre otras. También viene con otras herramientas estándar de ciberseguridad sobre las que aprendiste en este curso. Algunos ejemplos son Wireshark, tcpdump, Nmap y John the Ripper.
