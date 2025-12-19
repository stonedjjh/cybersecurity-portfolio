# Network Address Translation (NAT)

La traducción de direcciones de red (NAT) actúa como un intermediario entre una red privada local y la Internet pública para gestionar el tráfico de datos.

## Propósito y Beneficios de NAT

- **Seguridad**: Proporciona una capa adicional de protección al ocultar las direcciones IP internas de las amenazas externas; los dispositivos externos solo ven la dirección IP pública.
- **Conservación de direcciones**: Ayuda a gestionar la escasez de direcciones IPv4 al permitir que múltiples dispositivos internos compartan una o pocas direcciones IP públicas.
- **Administración simplificada**: Facilita el manejo de redes locales al permitir el uso de rangos de direcciones privadas internamente, gestionando solo las IP públicas en el borde de la red.
- **Funcionamiento**: Modifica el encabezado IP de los paquetes salientes para enmascarar la IP interna y traduce las IP públicas a privadas para los datos entrantes.

## Tipos de NAT

- **NAT Estática**: Asigna una dirección IP privada específica a una dirección IP pública fija. Es ideal para dispositivos que deben ser accesibles desde Internet, como servidores web.
- **NAT Dinámica**: Asigna una dirección IP privada a una dirección pública tomada de un grupo o "pool" de direcciones disponibles. Se utiliza cuando varios dispositivos necesitan acceso a Internet pero no requieren una IP fija.
- **PAT (Traducción de Direcciones de Puerto)**: También conocida como sobrecarga de NAT, permite que múltiples direcciones IP privadas compartan una única IP pública asignando un número de puerto diferente a cada sesión. Es el tipo más común en redes domésticas.

## Aplicaciones y Desafíos

- **Uso en redes**: Se aplica tanto en hogares para conectar tabletas y portátiles, como en pequeñas empresas para exponer servidores internos a usuarios externos.
- **Reenvío de puertos**: Una mala configuración puede hacer que servicios internos, como servidores de juegos, sean inaccesibles desde el exterior.
- **Conflictos de IP**: Pueden ocurrir problemas de enrutamiento si dos redes distintas utilizan el mismo rango de direcciones IP privadas.
- **Rendimiento y Protocolos**: NAT introduce un ligero retraso en el procesamiento de paquetes. Además, puede complicar protocolos que incluyen direcciones IP en su carga útil, como SIP utilizado en VoIP.
