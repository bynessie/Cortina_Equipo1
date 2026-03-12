# Hito 4 – Validación Funcional y HMI

## Objetivo del hito
Validar el funcionamiento integrado del sistema mecatrónico y la interacción con el usuario mediante HMI.

---

## Estado general del sistema
Marca el estado actual del sistema:

- [ ] No funcional
- [ ] Parcialmente funcional
- [ ] Funcional con fallas
- [x] Funcional estable

---

## Secuencia de operación validada
Describe paso a paso cómo opera el sistema completo:

1. La fuente de alimentación convierte los 110 VAC a 24 VDC para alimentar el PLC, sensores y relevadores.
2. El sistema PLC LOGO se enciende y queda en espera de una señal por parte de los sensores
3. Cuando el sensor capacitivo detecte la presencia del operador envía una señal al LOGO en la entrada I1.
4. El LOGO procesa la acción y posteriormente activa Q1
5. Esto prende el relevador de bajada, el cual hace que el motor gire y baje la cortina 
6. La cortina baja hasta toparse con el sensor magnético de abajo, el cual al detectar la precencia de la cortina (Gracias a un iman que se le instalo) manda una señal al LOGO mediante I6 (Al llegar a este sensor se prende la luz verde)
7. El LOGO procesa esta señal y detiene la cortina en esa posicion durante 10 segundos
8. Al terminar los 10 segundos el LOGO manda una señal a Q2 para activar el relevador de subida y subir la cortina 
9. La cortina sube hasta detectar al sensor magnético superior, y cuando lo detecta este manda una seña al LOGO mediante I4 que detiene la cortina, culminando de esa manera el ciclo. (Al llegar a este sensor se prende la luz roja)

---

## Validación de sensores
| Sensor | Condición probada | Resultado esperado | Resultado obtenido |
|------|------------------|------------------|------------------|
| Sensor capacitivo | Se acerca la mano del operador al sensor | El sensor la detecta y sube la cortina | La cortina subio |
| Sensor inductivo | Se coloca un objeto metálico frente al sensor | El sensor la detecta y baja la cortina | La cortina bajo |
| Sensor óptico infrarrojo | Un objeto o persona interrumpe el haz del sensor | El sensor detecta el obstáculo y detiene la cortina | La cortina se detubo al detectar el objeto |
| Sensor magnético (límite superior) | El imán de la cortina llega a la posición superior | El sensor detecta el iman y detiene el motor | La cortina dejo de subir al llegar al sensor |
| Sensor magnético (límite inferior) | El imán de la cortina llega a la posición inferior | El sensor detecta el iman y detiene el motor | La cortina dejo de bajar al llegar al sensor |

---

## Validación de actuadores
| Actuador | Acción | Resultado esperado | Resultado obtenido |
|--------|--------|------------------|------------------|
| Motor | Activación del relevador de subida | El motor gira y la cortina comienza a subir | La cortina subio |
| Motor | Activación del relevador de bajada | El motor gira y la cortina comienza a bajar | La cortina bajo |
| Lámpara verde | Activación cuando el motor llega abajo | La lámpara verde se enciende cuando detecta el sensor magnético de abajo | La lámpara verde se encendio cuando la cortina llego hasta abajo |
| Lámpara roja | Activación cuando el motor llega arriba | La lámpara roja se enciende cuando detecta el sensor magnético de arriba | La lámpara roja se encendio cuando la cortina llego hasta arriba |

---

## Validación del controlador (LOGO)
Describe:
- Temporizaciones
- Condiciones lógicas
- Interlocks o seguridades implementadas
En este proyecto las condiciones lógicas del sistema se basaron en la activación de distintos sensores para el funciónamiento del sistema, donde cada uno realizaba lo siguiente:
- Capacitivo: Al activarse bajaba la cortina
- Inductivo: Al activarse subia la cortina
- Magnetico superior: Al activarse detenia la cortina en la parte superior
- Magnetico inferior: Al activarse detenia la cortina en la parte inferior
- Óptico infrarrojo: Al activarse detenia la cortina
Este sistema también usa un temporizador para el modo automatico el cual sube la cortina despues de que esta dure 10 segundos en la parte inferior.

Y como metodo de seguridad, se implementaron interlocks al sistema como uno que evita que el motor resiba la orden de subir y bajar al mismo tiempo, y se instalo el sensor infrarojo para que en caso de que existan obstaculos al bajar la cortina, está se pueda detener.

---

## HMI – Interfaz Humano-Máquina
No se implemento al LOGO la interfas HMI debido a un cambio en el proyecto

Aun así, se llego a diseñar lo siguiente:
<img width="764" height="519" alt="image" src="https://github.com/user-attachments/assets/56b6e833-63a6-4114-a21e-f1c4be48768a" />


---

## Fallas detectadas
En este sistema una surgieron dos fallas:
1. El sensor magnético de hasta abajo por algun motivo no detectava del todo bien el iman, lo que probocaba que en algunas ocaciones la cortina siguiera bajando cuando ya no debia
2. Despues de varios usos el motor fue disminuyendo su eficacia, lo cual proboco que ya por el final subiera lentisimo la cortina o no soportara el peso de está. Creemos que esto paso debido al peso bajo de la cortina.

---

## Ajustes realizados
| Falla | Ajuste realizado | Resultado |
|----|-----------------|----------|
| Sensor magnético de abajo no siempre detecta | se hacerco más a la cortina | logro detectar muchas más veces la cortina en comparación a cuando estaba más alegado |
| El motor fue disminuyendo su eficacia despues de varios usos | El ajuste abria sido cambiar de motor, aunque se logro concluir la practica y obtener los resultados antes de ello | A pesar de no ser cambiado, se logro obtener la evidencia requerida |

---

## Preparación para demostración final
Indica qué está listo y qué falta por afinar:

- [x] Lógica de control
- [ ] HMI (No se tomara en cuenta)
- [x] Cableado
- [x] Seguridad
- [x] Evidencias (video/fotos)

---

## Reflexión breve del equipo
Durante está etapa no sufrimos muchos percances, por lo cual lo más crítico fue el que el sensor magnético de abajo no detectara del todo bien lo que se supone que deberia detectar. Aun así, esto no nos adjudico muchos problemas.
