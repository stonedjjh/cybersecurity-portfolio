# Conceptos de Cifrado y Criptografía

El cifrado transforma el **Texto Plano** (legible) en **Texto Cifrado** (ilegible) mediante algoritmos y claves.

## 1. Estados de los Datos

- **Datos en Reposo (At rest):** Datos almacenados en discos o nubes. Se protegen con cifrado de archivos o de disco completo (como BitLocker).
- **Datos en Movimiento (In transit):** Datos viajando por la red. Se protegen con HTTPS, VPN y cifrado de extremo a extremo.

## 2. Cifrado Simétrico vs. Asimétrico

| Característica    | Cifrado Simétrico                                | Cifrado Asimétrico (Clave Pública)                      |
| :---------------- | :----------------------------------------------- | :------------------------------------------------------ |
| **Claves**        | Una sola clave (se usa para cifrar y descifrar). | Dos claves: una Pública y una Privada.                  |
| **Velocidad**     | Muy rápido.                                      | Más lento y complejo.                                   |
| **Uso principal** | Grandes volúmenes de datos (discos duros).       | Intercambio de claves, firmas digitales y certificados. |
| **Ejemplos**      | AES, 3DES, CAST.                                 | RSA.                                                    |

## 3. Infraestructura de Clave Pública (PKI) y Certificados

La **PKI** utiliza una **Autoridad de Certificación (CA)** para validar identidades.

- **Certificado Digital:** Contiene la clave pública del propietario y está firmado por la CA.
- **Firma Digital:** Proceso inverso. El remitente cifra con su clave privada. Si el receptor puede descifrarlo con la clave pública, se garantiza la autenticidad (No repudio).

## 4. Hash Criptográfico (Repaso y Uso)

El hash no es cifrado (no se puede "descifrar"). Su función es la **Integridad**:

- Si el archivo cambia aunque sea un bit, el hash cambia completamente.
- Se usa para verificar que un mensaje no fue manipulado en el camino.
