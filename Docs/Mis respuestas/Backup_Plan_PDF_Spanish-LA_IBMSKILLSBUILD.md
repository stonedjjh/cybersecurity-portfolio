# Elaborar un plan para las copias de seguridad

Imagina que trabajas en el departamento de TI de una gran franquicia minorista y hay un equipo de 20 expertos. Tu supervisor te asigna la tarea de desarrollar un plan para realizar copias de seguridad.

**Paso 1**
Identifica a la persona, equipo o dispositivo que completará las copias de seguridad. Para esta actividad tienes tres opciones:

* Encargado de la tienda
* Equipo de TI
* Sistema de copia de seguridad automatizado

Asegúrate de explicar tu elección.

Aunque la copia de seguridad la realice una herramienta para este fin o un script ejecutado por Cron debe haber un encargado de el equipo de IT que se asegure de que las copias se realicen según el cronograma planteado. 

**Paso 2**
Identifica los tipos de datos que deben respaldarse en la empresa mediante copias de seguridad. Tu respuesta debe incluir uno o más de los siguientes tipos:

* Registros de empleados
* Registros financieros
* Datos de los clientes
* Documentación empresarial
* Propiedad intelectual
* Datos del sistema

Enumera un ejemplo para cada tipo de datos que identifiques.

* Registros de empleados: Información personal y profesional de los empleados, como nombres, direcciones, números de identificación y detalles de empleo.

* Registros financieros: Transacciones de ventas, balances y estados financieros.

* Datos de los clientes: Información de contacto, historial de compras y preferencias de los clientes.

* Datos del sistema: Respaldo de la data ingresada y generada por el sistema que permita restaurar a un estado operativo en caso de un imprevisto.

**Paso 3**
Identifica el tipo de copia de seguridad diaria que se debe realizar en tu empresa:

* Completa
* Diferencial
* Incremental

Para elegir una opción, considera qué tipo de respaldo es el más adecuado para una franquicia de venta minorista importante. Explica la opción que elijas.

Para este caso aplicaría un respaldo Diferencial. Por el rubro de la empresa y el tamaño del equipo de IT se puede dedicar un equipo a implementar este tipo de copia y de ser necesario restaurar el sistemas sería más rápido. Al ser un minorista con varias franquicias la cantidad de data que debe mover es considerable, por lo cual hacer respaldos completos ocuparía mucho espacio e incremental tardaría mucho en hacer una restauración, lo que se puede traducir como pérdidas.

**Paso 4**
Usa la regla 3-2-1 para identificar dónde deben almacenarse las copias de seguridad en tu empresa.

¿Qué tipos de almacenamiento usarás y dónde se ubicarán las copias de seguridad?

Asegúrate de justificar las opciones elegidas utilizando la regla 3-2-1.

Para cumplir con esta regla almacenaria los backup en el nas o centro de datos de la empresa y en un CSP aprovechando los precios de almacenamiento en frio, es decir estos datos que no son accesado constantemente.

**Paso 5**
Determina cuándo deben realizarse copias de seguridad en tu empresa: diariamente,semanalmente o una combinación de ambos.

Justifica la opción que elijas.

Por el tipo de actividad de la empresa, recomendaría un respaldo Diario. Los registros de ventas son datos operativos críticos que se generan constantemente; por lo tanto, un respaldo diario garantiza la continuidad del negocio. Esto asegura que los clientes puedan hacer cambios o reclamos y evita que la empresa caiga en algún incumplimiento legal, como no declarar las ganancias de un día completo de operaciones.