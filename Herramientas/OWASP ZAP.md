# OWASP ZAP

OWASP ZAP es un escáner de vulnerabilidades gratuito y de código abierto y una herramienta de pruebas de penetración diseñada para probar la seguridad de una aplicación web. Con ZAP, puedes buscar posibles vulnerabilidades y explotarlas para confirmar su existencia.

## Cómo funciona ZAP

La forma más básica de usar ZAP es un escaneo automatizado.

- **Paso 1: Escaneo pasivo**
El primer paso del escaneo automatizado es un escaneo pasivo, en el que ZAP escanea una aplicación web objetivo mediante una araña. Una araña, o rastreador sitio web, es un programa que busca e indexa contenido web.

La araña de ZAP indexa el contenido de la aplicación, incluidos los hipervínculos, las etiquetas HTML y los metadatos. Agrega la URL de cada hiperenlace a una lista de URL a las que acceder. A continuación, la araña repite el proceso para cada una de esas URL. Accede a las URL, indexa el contenido de su página y agrega a la lista las URL recién descubiertas. A continuación, la araña repite este proceso con estas nuevas URL, y el ciclo continúa hasta que la araña no encuentra más URL.

Mediante los hallazgos del escaneo pasivo, ZAP mapea las páginas de una aplicación web y anota las vulnerabilidades.

- **Paso 2: Escaneo activo**
El siguiente paso en el análisis automatizado es un análisis activo. En este análisis, ZAP emplea ataques conocidos en las URL para explotar las vulnerabilidades identificadas y descubrir otras nuevas.

- **Paso 3: Informe**
Finalmente, ZAP informa los resultados de ambos escaneos. El informe incluye mucha información sobre cada vulnerabilidad identificada y clasifica las vulnerabilidades por nivel de riesgo. Puedes emplear este informe para identificar y priorizar vulnerabilidades para investigar más a fondo.
