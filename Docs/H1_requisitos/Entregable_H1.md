# Hito 1 – Análisis y Requerimientos

## Descripción del problema
Describe el problema de ingeniería que se resolverá.
El problema de ingeniería consiste en diseñar e implementar un sistema automatizado que permita optimizar un proceso operativo (por ejemplo control, monitoreo o automatización) para mejorar la eficiencia, reducir errores humanos y garantizar un funcionamiento seguro.
Actualmente el proceso presenta limitaciones como falta de control automático, retrasos en la respuesta del sistema o riesgos operativos, lo que justifica el desarrollo de una solución tecnológica basada en sensores, actuadores y un sistema de control programable.
## Requerimientos del sistema
### Requerimientos Funcionales

#### RF-01
- Enunciado: El sistema deberá permitir operación manual donde la cortina se mueva únicamente mientras el botón esté presionado y se detenga al soltarlo.
- Criterio verificable: Si el botón manual se mantiene presionado, la cortina se mueve; al soltarlo, el movimiento se detiene en menos de 0.5 s.
- Prioridad: Must
- Riesgo si falla: Movimiento incontrolado / riesgo para el usuario.

#### RF-02
- Enunciado: El sistema deberá ejecutar el ciclo completo en modo automático al activarse, salvo que se detecte una interferencia.
- Criterio verificable: Al activar el modo automático, la cortina realiza apertura o cierre completo sin intervención; si se detecta obstáculo, se detiene en <0.5 s.
- Prioridad: Must
- Riesgo si falla: Operación incompleta / daño al sistema.

#### RF-03
- Enunciado: El sistema deberá mostrar en la interfaz la altura actual de la cortina y el número total de ciclos realizados.
- Criterio verificable: Durante la operación, la pantalla muestra la altura en tiempo real y el contador incrementa al finalizar cada ciclo completo.
- Prioridad: Should
- Riesgo si falla: Falta de monitoreo y control operativo.

#### RF-04
- Enunciado: El sistema deberá detectar obstáculos durante el cierre de la cortina.
- Criterio verificable: Si se coloca un objeto en la trayectoria durante el cierre, el sistema detecta la interferencia y detiene el movimiento en <0.5 s.
- Prioridad: Must
- Riesgo si falla: Daño material / riesgo de lesión.

#### RF-05
- Enunciado: El sistema deberá permitir modificar los tiempos de apertura, pausa y cierre desde la interfaz.
- Criterio verificable: El usuario puede cambiar los tiempos desde la interfaz y el sistema aplica los nuevos valores en el siguiente ciclo.
- Prioridad: Should
- Riesgo si falla: Falta de flexibilidad operativa.

#### RF-06
- Enunciado: El sistema deberá contar con una interfaz que permita la interacción del usuario.
- Criterio verificable: El usuario puede seleccionar modo de operación y configurar parámetros desde la interfaz sin acceso al PLC.
- Prioridad: Must
- Riesgo si falla: Imposibilidad de operación adecuada.


### Requerimientos Técnicos

#### RT-01
- Enunciado: El sistema deberá contar con una fuente eléctrica estable y protegida.
- Criterio verificable: La fuente mantiene ±10% del voltaje nominal y cuenta con protección contra sobrecorriente.
- Prioridad: Must
- Riesgo si falla: Daño a componentes / fallas eléctricas.

#### RT-02
- Enunciado: El sistema deberá detectar los límites de subida y bajada mediante sensores.
- Criterio verificable: Al alcanzar el límite superior o inferior, el sensor activa la señal y el motor se detiene automáticamente.
- Prioridad: Must
- Riesgo si falla: Daño mecánico / sobreesfuerzo del motor.

#### RT-03
- Enunciado: El software del sistema deberá estar documentado y estructurado de forma robusta.
- Criterio verificable: El programa cuenta con comentarios, diagrama de flujo y manual técnico entregado junto con el proyecto.
- Prioridad: Should
- Riesgo si falla: Dificultad de mantenimiento o corrección de errores.

#### RT-04
- Enunciado: La estructura y materiales de montaje deberán soportar el peso de la cortina sin deformación.
- Criterio verificable: La estructura soporta 1.5 veces el peso de la cortina sin fallas durante prueba de carga.
- Prioridad: Must
- Riesgo si falla: Caída de la cortina / riesgo físico.

#### RT-05
- Enunciado: El sistema deberá utilizar un PLC en condiciones óptimas de funcionamiento.
- Criterio verificable: El PLC enciende correctamente, ejecuta el programa sin errores y pasa prueba de entradas/salidas antes de la instalación.
- Prioridad: Must
- Riesgo si falla: Falla total del sistema.


### Requerimientos de Seguridad

#### RS-01
- Enunciado: El sistema deberá detener la cortina al detectar un obstáculo durante el descenso.
- Criterio verificable: Si un objeto interrumpe el recorrido durante la bajada, el motor se detiene en <0.5 s.
- Prioridad: Must
- Riesgo si falla: Lesiones / daño material.

#### RS-02
- Enunciado: El sistema deberá contar con un botón de paro de emergencia que detenga toda operación inmediatamente.
- Criterio verificable: Al presionar el paro de emergencia, el motor y salidas se desactivan en <0.3 s.
- Prioridad: Must
- Riesgo si falla: Incapacidad de detener emergencia.

#### RS-03
- Enunciado: Todos los componentes eléctricos deberán estar correctamente aislados.
- Criterio verificable: Inspección visual y prueba de continuidad confirman ausencia de partes energizadas expuestas.
- Prioridad: Must
- Riesgo si falla: Riesgo de descarga eléctrica.

#### RS-04
- Enunciado: El sistema deberá impedir la activación simultánea de subida y bajada.
- Criterio verificable: Si se activan ambas órdenes, el sistema bloquea la acción y mantiene estado seguro.
- Prioridad: Must
- Riesgo si falla: Cortocircuito / daño al motor.

#### RS-05
- Enunciado: El sistema deberá cumplir con las normativas de seguridad industrial aplicables.
- Criterio verificable: El sistema cumple con lista de verificación de normas vigentes y cuenta con documentación de cumplimiento.
- Prioridad: Must
- Riesgo si falla: Sanciones legales / operación insegura.


## Diagrama de bloques
-Entrada/Sensores → Controlador → Actuadores/Salida
        ↓             ↓              ↓
   Usuario/Interfaz ← Sistema de monitoreo
Descripción:

Sensores capturan información.

Controlador procesa datos.

Actuadores ejecutan acciones.

Usuario supervisa y controla.
## Imagen diagrama final
<img width="1279" height="791" alt="image" src="https://github.com/user-attachments/assets/0f64d28a-a868-4ccb-b0dd-bfb6907a13b1" />
[
](https://youtu.be/qtntj3IrM4I)

## Conclusiones del análisis
Breve reflexión técnica.
El análisis permitió identificar las necesidades técnicas y operativas del sistema, así como los requisitos de funcionalidad y seguridad necesarios para su implementación.
La solución propuesta mejora la eficiencia del proceso, reduce la intervención humana y aumenta la confiabilidad operativa. Además, se establecieron bases claras para el diseño e implementación del sistema automatizado.
