# Proyecto Mecatrónico – MR2022

## Problema
Una compañía dedicada a la fabricación de cortinas industriales requiere automatizar la operación de apertura y cierre de sus cortinas para mejorar la eficiencia y seguridad en el proceso. El problema de ingeniería consiste en diseñar un sistema mecatrónico que cumpla con las siguientes especificaciones críticas: Dimensionamiento: La cortina varía entre 3 a 4 metros de ancho y 3 a 7 metros de alto. Carga Mecánica: El material es hule termo-formado (900 gramos por yarda cuadrada) con barras tensoras metálicas de 35 Kg cada una, colocadas cada 2 metros de ancho. Control de Movimiento: El actuador debe enrollar la cortina hasta una altura configurable en un tiempo ajustable entre 3 a 5 segundos mediante interfaz de usuario. Perfil de Velocidad: El movimiento debe contar con dos velocidades: alta al arranque y baja para la detención precisa. Seguridad Operativa: Es obligatorio detectar obstáculos (personas o carros de carga) durante el descenso. Al detectar un obstáculo, el sistema debe detenerse, subir la cortina y repetir el ciclo de espera, suspendiendo el conteo del tiempo mientras persista el obstáculo. Interacción: El sistema debe permitir operación mediante botones físicos (arriba, abajo, paro) y una interfaz de operación (HMI) con niveles de usuario diferenciados.

## Arquitectura del sistema
La arquitectura del sistema se encuentra en "Cortina_Equipo1/Docs/H4_control_hmi/Diagrama_Bloques.md" (No me deja insertar la imagen)

## Componentes utilizados
- Sensor inductivo
- Sensor capacitivo
- Sensor óptico
- Sensor magnético
- Siemens LOGO
- Relés
- Motor DC 24V
- Torre de luces

## Lógica de control
La lógica de control del sistema es el siguiente:
1. Cuando el sensor capacitivo detecta la mano del operador, se baja la cortina. El sistema del LOGO activa el relevador indicado para que el motor cierre la cortina hasta que el sensor magnético inferior detecte que la cortina llegó al límite inferior.
2. Durante el descenso, el sensor óptico monitorea continuamente la presencia de objetos. Si detecta algún obstáculo, el sistema se detiene inmediatamente para evitar algún accidente.
3. Cuando pasan 10 segundos o el sensor inductivo se activa, el sistema activa el relevador para que el motor suba la cortina.
4. Los sensores magnéticos instalados en la cortina detectan las posiciones principales de la cortina:
- Sensor superior: detiene el motor cuando la cortina está completamente arriba.
- Sensor inferior: detiene el motor cuando la cortina está completamente abajo.
- Sensor intermedio: permite cambiar la velocidad del motor antes de llegar al final de la subida o bajada para realizar un cierre más controlado.

5. El sistema incluye interlocks que evitan cualquier acción peligrosa o dañina para el sistema o usuario.

6. El estado del sistema es indicado mediante la torre de señalización:
- Lámpara verde: Cortina totalmente abajo.
- Lámpara roja: Cortina totalmente arriba.


## Resultados de pruebas
### Validación de sensores
| Sensor | Condición probada | Resultado esperado | Resultado obtenido |
|------|------------------|------------------|------------------|
| Sensor capacitivo | Se acerca la mano del operador al sensor | El sensor la detecta y sube la cortina | La cortina subio |
| Sensor inductivo | Se coloca un objeto metálico frente al sensor | El sensor la detecta y baja la cortina | La cortina bajo |
| Sensor óptico infrarrojo | Un objeto o persona interrumpe el haz del sensor | El sensor detecta el obstáculo y detiene la cortina | La cortina se detubo al detectar el objeto |
| Sensor magnético (límite superior) | El imán de la cortina llega a la posición superior | El sensor detecta el iman y detiene el motor | La cortina dejo de subir al llegar al sensor |
| Sensor magnético (límite inferior) | El imán de la cortina llega a la posición inferior | El sensor detecta el iman y detiene el motor | La cortina dejo de bajar al llegar al sensor |

## Validación de actuadores
| Actuador | Acción | Resultado esperado | Resultado obtenido |
|--------|--------|------------------|------------------|
| Motor | Activación del relevador de subida | El motor gira y la cortina comienza a subir | La cortina subio |
| Motor | Activación del relevador de bajada | El motor gira y la cortina comienza a bajar | La cortina bajo |
| Lámpara verde | Activación cuando el motor llega abajo | La lámpara verde se enciende cuando detecta el sensor magnético de abajo | La lámpara verde se encendio cuando la cortina llego hasta abajo |
| Lámpara roja | Activación cuando el motor llega arriba | La lámpara roja se enciende cuando detecta el sensor magnético de arriba | La lámpara roja se encendio cuando la cortina llego hasta arriba |

## Video demo
(link al video)

## Equipo
- Jonathan Uriel Escamilla González
- Juan Carlos Muñoz Enriquez
- Marian Zamarripa Espinoza
- Erik Daniel Puente Hernández 
