# Laboratorio: Máscaras de Subred y Cálculo de Hosts (IPv4 e IPv6)

## Objetivo

Adquirir experiencia práctica con el enmascaramiento de subredes, el cálculo de subredes y el cálculo de hosts para direcciones IPv4 e IPv6.

## Tarea 1: Cálculo de la Máscara de Subred IPv4

### Instrucciones

Tienes una dirección IP con una máscara de subred específica. Tu tarea es determinar la máscara de subred en formato decimal.

Dado

- Dirección `IP: 192.168.1.0/24`

Solución

1. Determina la máscara de subred

- La notación /24 indica que los primeros 24 bits de la dirección IP son la porción de red de la dirección.

- Esto resulta en la máscara de subred 255.255.255.0 en formato decimal. Cada octeto de la máscara de subred representa ocho bits establecidos en 1 (255) o 0 (0), correspondiente al prefijo /24.

2. Verificando la respuesta a través de una calculadora de máscara de subred en línea

- En este laboratorio, verificarás el cálculo utilizando Visual Subnet Calculator https://www.davidc.net/sites/default/subnets/subnets.html. (Nota: Hay muchas calculadoras de IP y enmascaramiento de red disponibles en línea. Puedes usar cualquiera).

- Abre la Visual Subnet Calculator
- Ingresa la Dirección de Red 192.168.1.0 y el Bit de Máscara 24
- Selecciona la opción Netmask en Mostrar columnas:
- Haz clic en Actualizar y verifica que la máscara de subred que calculaste coincida con el resultado mostrado por la calculadora.

## Tarea 2: Cálculo de subredes IPv4

### Instrucciones

Debes dividir una red dada en subredes más pequeñas. Calcula la nueva máscara de subred y enumera las subredes resultantes con sus rangos de direcciones.

Dado

- Dirección de red: `10.0.0.0/24`
- Subredes requeridas: 4

Solución

1. Calcular la nueva máscara de subred:

- Para crear 4 subredes, necesitas tomar prestados 2 bits de la porción de host de la dirección IP.
- Esto cambia la notación CIDR a /26 (24 bits de red originales + 2 bits tomados prestados).
- La nueva máscara de subred es 255.255.255.192.

2. Listar subredes:

- Subred 1: 10.0.0.0/26 con el rango 10.0.0.0 - 10.0.0.63
- Subred 2: 10.0.0.64/26 con el rango 10.0.0.64 - 10.0.0.127
- Subred 3: 10.0.0.128/26 con el rango 10.0.0.128 - 10.0.0.191
- Subred 4: 10.0.0.192/26 con el rango 10.0.0.192 - 10.0.0.255

3. Verificar la respuesta a través de una calculadora de máscaras de subred en línea

#### Subred 1

- Abre la Calculadora de Subred Visual. (https://www.davidc.net/sites/default/subnets/subnets.html)
- Verifica la Subred 1.
- Ingresa la Dirección de Red 10.0.0.0 y el Bit de Máscara 26 como se muestra en el cálculo para la Subred 1.
- Asegúrate de que la dirección de Subred, la Máscara de Red y el Rango de direcciones estén seleccionados en Mostrar columnas.
- Haz clic en Actualizar y verifica la salida de la calculadora.
- Observa la dirección de Subred, la Máscara de Red, el Rango de direcciones y otra información mostrada en la calculadora en línea.

#### Subred 2

- De manera similar, verifiquemos el cálculo para la Subred 1.
- Ingresa la Dirección de Red 10.0.0.64 y el Bit de Máscara 26 como se muestra en el cálculo para la Subred 2.
- Asegúrate de que la opción de dirección de Subred, Máscara de Red y Rango de direcciones estén seleccionadas en Mostrar columnas.
- Haz clic en Actualizar y selecciona la salida de la calculadora.
- Observa la dirección de Subred, la Máscara de Red, el Rango de direcciones, IPs utilizables y otras opciones mostradas en la calculadora en línea.
- Puedes abordar el cálculo para la Subred 3 y la Subred 4, que puedes verificar de manera similar.

##### Nota Personal entiendo el ejercicio

###### Documentación del Razonamiento (Subneteo /26)

**Objetivo:** Dividir la red 10.0.0.0/24 en 4 subredes iguales.

###### 1. Análisis de la Dirección Original

- **Dirección Dada:** 10.0.0.0/24
- **Clase y Tipo:** Es de Clase A y está en el rango privado (RFC 1918).
- **Notación CIDR (/24):**
  - **Bits de Red (N):** 24 bits. (10.0.0.)
  - **Bits de Host (H):** 8 bits. (El cuarto octeto, 32 - 24 = 8).
  - **Conclusión:** Se deben tomar prestados bits de los 8 bits de Host disponibles en el cuarto octeto para crear las subredes.

### 2. Determinación de Bits de Subred Necesarios

- **Requisito:** 4 subredes.
- **Fórmula:** $2^n \geq$ Subredes Requeridas.
- **Cálculo:** Se deben tomar prestados **2 bits** ($n=2$) de la porción de host, ya que $2^2 = 4$.

### 3. Cálculo de la Nueva Máscara de Subred (CIDR y Decimal)

- **Nueva Notación CIDR:** 24 bits de Red originales + 2 bits prestados = **/26**.
- **Nueva Máscara Decimal:** La máscara se obtiene encendiendo (poniendo a 1) los 2 bits prestados en el cuarto octeto.
  - Cuarto octeto en binario: $11000000$.
  - Valor decimal: $128 + 64 = \mathbf{192}$.
- **Nueva Máscara Completa:** $255.255.255.192$

### 4. Cálculo de Hosts y Tamaño del Bloque

- **Bits de Host Restantes:** $8 \text{ bits originales} - 2 \text{ bits prestados} = \mathbf{6 \text{ bits de Host}}$.
- **Tamaño del Bloque (Número total de direcciones):** $2^6 = \mathbf{64}$ direcciones por subred.

_(Nota: Hosts útiles = $64 - 2 = 62$. El tamaño del bloque de 64 define el incremento de las subredes.)_

### 5. Listado de las Subredes

Dado que el tamaño del bloque es de 64, las direcciones de red para el cuarto octeto se incrementan de 64 en 64 (utilizando las 4 combinaciones posibles de los 2 bits de subred: 00, 01, 10, 11).

| Subred (2 bits) | Dirección de Red  | Rango de Hosts (1er IP - Última IP) | Dirección de Broadcast |
| :-------------- | :---------------- | :---------------------------------- | :--------------------- |
| **00**          | **10.0.0.0/26**   | 10.0.0.1 - 10.0.0.62                | 10.0.0.63              |
| **01**          | **10.0.0.64/26**  | 10.0.0.65 - 10.0.0.126              | 10.0.0.127             |
| **10**          | **10.0.0.128/26** | 10.0.0.129 - 10.0.0.190             | 10.0.0.191             |
| **11**          | **10.0.0.192/26** | 10.0.0.193 - 10.0.0.254             | 10.0.0.255             |

## Tarea 3: Cálculo de hosts IPv4

### Instrucciones

Dada una máscara de subred, calcula el número de hosts utilizables dentro de esa subred.

Dado

- Dirección de red: `10.10.0.0`
- Máscara de subred: 255.255.255.192

Solución

1. Calcular el número de hosts:

- La máscara de subred 255.255.255.192 corresponde a un prefijo /26, lo que significa que hay 6 bits disponibles para direcciones de hosts (32 bits totales menos 26 bits de red).
- El número de hosts utilizables se calcula como 2^6 - 2 = 62 (restando 2 se tienen en cuenta las direcciones de red y de broadcast).

2. Verificando la respuesta a través de una calculadora de máscara de subred en línea

Abre la Calculadora Visual de Subredes (https://www.davidc.net/sites/default/subnets/subnets.html)

- Ingresa la Dirección de Red 10.10.0.0 y el Bit de Máscara 26.
- Asegúrate de que las opciones Dirección de subred, Máscara de red, Rango de direcciones, IPs utilizables y Hosts estén seleccionadas en las columnas a mostrar.
- Haz clic en Actualizar y verifica la salida de la calculadora.
- Observa la Dirección de subred, Máscara de red, Rango de direcciones, IPs utilizables y Hosts mostrados en la calculadora en línea.

## Tarea 4: Subredes IPv6

### Instrucciones

Se te proporciona una dirección IPv6 y necesitas crear subredes. Calcula la nueva máscara de subred y enumera algunas de las subredes resultantes.

Dado

- Dirección IPv6: `2001:0db8:85a3::/48`
- Subredes requeridas: 16

Solución:

1. Calcular la nueva máscara de subred:

- Para crear 16 subredes, necesitas tomar prestados 4 bits de la porción de host de la dirección IPv6.
- Esto cambia la notación CIDR a /52 (48 bits de red originales + 4 bits tomados prestados).
- La nueva máscara de subred es ffff:ffff:ffff:ffff:ffff:ffff:ffff:0000.

2. Enumerar algunas subredes:

Subred 1: `2001:0db8:85a3:0000::/52`
Subred 2: `2001:0db8:85a3:0010::/52`
Subred 3: `2001:0db8:85a3:0020::/52`
Subred 4: `2001:0db8:85a3:0030::/52`

## Tarea 5: Cálculo de hosts IPv6

Instrucciones

Dada una dirección IPv6 y una máscara de subred, calcula los posibles hosts dentro de esa subred.

Dado

- Dirección IP: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`
  Máscara de subred: `ffff:ffff:ffff:ffff:0000:0000:0000:0000 (CIDR /64)`

Solución

1. Calcular el número de hosts:

- La máscara de subred ffff:ffff:ffff:ffff:0000:0000:0000:0000 corresponde a un prefijo /64, lo que significa que hay 64 bits disponibles para direcciones de host (128 bits en total menos 64 bits de red).
- El número de posibles hosts es 2^64, que equivale aproximadamente a 1.84 x 10^19 direcciones.

2. Verificando la respuesta a través de una calculadora de máscara de subred en línea

- Abre la Calculadora de Subred IPv6 (https://www.vultr.com/resources/subnet-calculator-ipv6/). (Nota: Hay muchas calculadoras de IPc6 y enmascaramiento de red disponibles en línea. Puedes usar cualquiera).
- Ingresa la Dirección IP 2001:0db8:85a3:0000:0000:8a2e:0370:7334 y el Bit de Máscara /64, es decir, 2001:0db8:85a3:0000:0000:8a2e:0370:7334/64
- Haz clic en Calcular Subred y verifica la salida de la calculadora.
- Observa las direcciones utilizables en la salida. (Nota: No todas las direcciones IP son utilizables, ya que algunas están reservadas.)
- Calculadora de Subred IPv6

## Ejercicios

### Ejercicios de IPv4

Ejercicio 1: Cálculo de la Máscara de Subred IPv4

Instrucciones

Dada una dirección IP y un prefijo CIDR, determina la máscara de subred en formato decimal.

Dado

- Dirección IP: `172.16.0.0/20`

Solución:

tenemos que la mascara seria `11111111.11111111.11110000.0000` que se traduce como 255.255.240.0.

Sugerencia:
La notación /20 significa que los primeros 20 bits son para la porción de red. Convierte esto a una máscara de subred decimal.

Ejercicio 2: Cálculo de Subredes IPv4

Instrucciones

Necesitas dividir una red dada en subredes más pequeñas. Calcula la nueva máscara de subred y enumera algunas subredes resultantes con sus rangos de dirección.

Dado

- Dirección de Red: `192.168.10.0/24`
- Subredes Requeridas: 8

Sugerencia

Para crear 8 subredes, necesitarás tomar prestados un cierto número de bits de la porción de host. Ajusta la notación CIDR en consecuencia y determina la nueva máscara de subred.

Solución:

$2^3$ = 8 por lo cual debemos pedir 3 prestados quedando nuestro
CIDR en `192.168.10.0/27`

quedando la mascara de subred en: `11111111.11111111.11111111.11100000` que se traduce como 255.255.255.224.

### Ejercicio de IPv6

Ejercicio 1: Subredes IPv6

Instrucciones

Se te proporciona una dirección IPv6 y necesitas crear subredes. Calcula la nueva máscara de subred y enumera algunas de las subredes resultantes.

Dado

- Dirección IPv6: `2001:abcd:1234::/48`
- Subredes requeridas: 4

Sugerencia

Para crear 4 subredes, necesitas tomar prestados 2 bits de la porción de host. Ajusta la notación CIDR y la máscara de subred en consecuencia.

Solución

$2^2$ = 4 por lo cual debemos pedir 2 prestados quedando nuestro
CIDR en `2001:abcd:1234::/50`

Conclusión

Has adquirido experiencia práctica en este laboratorio con el enmascaramiento de subredes y los cálculos de hosts para direcciones IPv4 e IPv6. Aprendiste a determinar la máscara de subred en formato decimal a partir de la notación CIDR, lo cual es fundamental para entender la segmentación de redes. Practicaste dividir una red en subredes más pequeñas, calcular nuevas máscaras de subred y enumerar las subredes resultantes con sus rangos de direcciones, lo que es crucial para un diseño de red eficiente. Además, exploraste el enrutamiento de IPv6 calculando nuevas máscaras de subred y enumerando subredes, enfatizando la importancia de gestionar grandes espacios de direcciones de manera efectiva. Estos ejercicios mejoran tus habilidades en la optimización del rendimiento de la red, mejorando la seguridad y gestionando las asignaciones de direcciones en escenarios del mundo real.
