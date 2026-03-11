# Hito 3 – Control e Integración

## Descripción de la lógica de control
El funcionamiento del sistema es el siguiente:

1. Cuando el sensor capacitivo detecta la mano del operador, se sube la cortina. El sistema del LOGO activa el relevador indicado para que el motor abra la cortina hasta que el sensor magnético superior detecte que la cortina llegó al límite superior.

2. Cuando el sensor inductivo se activa, el sistema activa el relevador para que el motor baje la cortina.

3. Durante el descenso, el sensor óptico monitorea continuamente la presencia de objetos. Si detecta algun obstáculo, el sistema se detiene inmediatamente y se sube la cortina para evitar algun accidente.

4. Los sensores magnéticos instalados en la cortina detectan las posiciones principales de la cortina:
   - Sensor superior: detiene el motor cuando la cortina está completamente arriba.
   - Sensor inferior: detiene el motor cuando la cortina está completamente abajo.
   - Sensor intermedio: permite cambiar la velocidad del motor antes de llegar al final de la subida o bajada para realizar un cierre más controlado.

5. El sistema incluye interlocks que evitan cualquier acción peligrosa o dañina para el sistema o usuario.

6. El estado del sistema es indicado mediante la torre de señalización:
   - Lámpara verde: operación normal.
   - Lámpara roja: detección de obstáculo o condición de alarma.

---

## Entradas y salidas
| Entrada | Tipo | Función |
|--------|------|---------
| Sensor capacitivo | Digital 24V | Detecta la mano del operador y sube la cortina |
| Sensor inductivo | Digital 24V | Detecta el activador metálico y baja la cortina |
| Sensor óptico infrarrojo | Digital 24V | Detecta si no hay obstaculos mientras baja la cortina para evitar cualquier accidente |
| Sensor magnético superior | Digital 24V | Detecta cuando la cortina llega al límite superior |
| Sensor magnético intermedio | Digital 24V | Detecta cuando la cortina llega a la posición intermedia para cambio de velocidad |
| Sensor magnético inferior | Digital 24V | Detecta cuando la cortina llega al límite inferior |

---

| Salida | Tipo | Función |
|--------|------|---------|
| Relevador motor subir | Digital 24V | Activa el motor para subir la cortina |
| Relevador motor bajar | Digital 24V | Activa el motor para bajar la cortina |
| Lámpara verde | Digital 24V | Indica funcionamiento normal del sistema |
| Lámpara roja | Digital 24V | Indica presencia de obstáculo o condición de alarma |

## Pruebas realizadas
| Prueba | Resultado esperado | Resultado obtenido |
|------|------------------|------------------|
| Activación del sensor capacitivo | La cortina debe iniciar el movimiento de subida | La cortina subio |
| Activación del sensor inductivo | La cortina debe iniciar el movimiento de bajada | La cortina bajo |
| Activación del sensor infrarrojo durante el descenso | El sistema debe detener la cortina y subirla | La cortina se detubo |
| Activación del sensor magnético superior | El motor debe detenerse | La cortina se detubo arriba |
| Activación del sensor magnético inferior | El motor debe detenerse | La cortina se detubo abajo |
| Señalización | El semaforo deben indicar el estado del sistema |  El semaforo se mantubo en verde mientras no hubo ninguna obstrucción en el sistema |

## Ajustes realizados
Describe cambios hechos tras las pruebas.
Uno de los cambios que se tuvo que realizar fue en el código inicial que se nos proporciono para el proyecto, esto debido a que el código no funcionaba del todo bien y aparte este no tomaba en consideración los interlocks debidos para mantener la seguridad tanto del usuario como del sistema.
