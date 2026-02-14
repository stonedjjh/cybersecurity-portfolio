# Técnicas de Gestión de Contraseñas

La gestión de identidades es la primera línea de defensa. Más del 80% de las filtraciones de datos empresariales se deben a contraseñas débiles o robadas.

## 1. Métodos de Ataque

Los atacantes no "adivinan" manualmente, usan herramientas automatizadas:

- **Fuerza Bruta:** Probar todas las combinaciones posibles hasta dar con la correcta.
- **Ataque de Diccionario:** Uso de listas de palabras comunes, nombres, lugares o citas de libros/películas.
- **Rainbow Tables (Tablas Arcoíris):** Uso de bases de datos de **hashes** precalculados para revertir la codificación y obtener la contraseña original.

> **Concepto clave: Hash.** Es una "huella digital" de longitud fija generada por un algoritmo. Las empresas no deben guardar tu contraseña real, sino su hash.

## 2. Características de una Contraseña Segura

Para que una contraseña sea robusta frente a ataques que procesan billones de intentos por segundo, debe cumplir:

1. **Longitud mínima:** Al menos 12 caracteres (a mayor longitud, mayor entropía).
2. **Complejidad:** Mezcla de mayúsculas, minúsculas, números y caracteres especiales.
3. **Aleatoriedad:** Evitar palabras de diccionario, información personal o sustituciones predecibles como "L33t" (ej. usar '4' por 'A' o '$' por 'S').
4. **Unicidad:** Una contraseña distinta para cada cuenta. Jamás reutilizar contraseñas personales en el trabajo.

## 3. Políticas Organizacionales

Las empresas deben implementar reglas claras:

- **Caducidad sensata:** Cambios cada 6 a 12 meses. (Intervalos muy cortos de 30 o 90 días suelen provocar que el usuario cree contraseñas más débiles o predecibles).
- **Prohibición de compartir:** Ni siquiera con el CEO o el departamento de TI. El personal de TI tiene cuentas de administrador y no necesita las credenciales del usuario.
- **Capacitación:** Enseñar a los empleados que la empresa **nunca** les pedirá su contraseña por correo o teléfono (prevención de Phishing).

## 4. Malas Prácticas a Evitar

- **Reciclaje:** Usar la misma contraseña base y solo cambiar un número al final (ej. Verano2025, Verano2026).
- **Almacenamiento inseguro:** Escribirlas en post-its o guardarlas en archivos de texto sin cifrar.
- **Password Spraying:** Ataque donde el hacker prueba una contraseña común (como "123456") contra miles de usuarios a la vez para evitar bloqueos por intentos fallidos.
