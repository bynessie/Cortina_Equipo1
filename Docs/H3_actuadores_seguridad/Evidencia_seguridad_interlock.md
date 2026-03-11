# Evidencia del Interlock
En este caso, estubimos experimentando algunas dificultades con el código por lo cual este no se logro probar en el LOGO. Sin embargo, al final si logramos crear de forma correcta el codigo más basico (Contiene el interlock de no activar el motor hacia arriba y abajo simultaneamente, y el sistema de seguridad del sensor infrarojo)

https://github.com/user-attachments/assets/783c976e-7f60-467d-b6e2-9eaf39a9774b

En el video se puede notar el funcionamiento correcto de la cortina y en el segundo 36s se puede ver como cuando el motor esta bajando (o subiendo) no se puede ejecutar la acción contraria, cumpliendo de esta manera el interlock de "Acción simultánea de subida y bajada de la cortina".
Esto funciona gracias a que una de las condiciones para que Q2 se prenda es que Q1 debe estar apagado y viceverza.

---

Igual seguimos mejorando el código, nuestro ultimo prototipo es el siguiente:
<img width="976" height="630" alt="image" src="https://github.com/user-attachments/assets/10d765f1-0b03-47f5-a0ab-977ef44efcdd" />

Donde ya se bloquena acciónes como:
- Acción simultánea de subida y bajada de la cortina
- El motor continua en movimiento despues del limite establecido (Ya sea superior o inferior)

Y parcialmente
- La cortina sigue bajando aunque exista un obstaculo
- Ejecutar el sistema automático o manual con un sensor fallando

Por lo cual aun nos falta pulir el código, agregar cosas como que cuente los ciclos que ha realizado, a qque altura se encuentra y también entender que esta fallando en este ultimo.
