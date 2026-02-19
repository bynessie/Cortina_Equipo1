# Bitácora de Proyecto – Semana 1

## Tema de la semana

**Control** – Introducción al relé programable Siemens LOGO

---

## Actividades realizadas

Durante esta semana se trabajó con el relé programable Siemens LOGO, comenzando por la identificación de sus partes principales, como la alimentación, entradas y salidas. Posteriormente, se instaló y configuró el software LOGO! Soft Comfort para poder programar el controlador.

Como práctica, se desarrolló un programa secuenciador de luces que controla tres salidas, cada una con tiempos distintos. Para ello, se utilizó un diagrama de bloques que incluye temporizadores, compuertas lógicas y salidas. Finalmente, el programa fue simulado para verificar que el ciclo se repitiera correctamente y que la secuencia funcionara como se esperaba.

---

## Decisiones de ingeniería

| Decisión                                 | Alternativas consideradas          | Justificación                                                                                                                                                                |
| ---------------------------------------- | ---------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Uso de compuertas AND para la activación | Compuertas OR o contactos directos | Las compuertas AND permiten que cada salida se active únicamente cuando se cumplen todas las condiciones previas de tiempo y estado, lo que garantiza una secuencia ordenada |
| Configuración de salidas tipo relé       | Salidas transistorizadas           | Las salidas a relé ofrecen mayor flexibilidad al poder manejar distintos tipos de carga (AC y DC), lo cual es más adecuado para aplicaciones industriales básicas            |

---

## Problema técnico encontrado

No aplica en este caso

---

## Solución aplicada

Para corregir el problema, se modificó el diagrama de bloques de la siguiente manera:

1. Se configuró correctamente el reset de los temporizadores, asegurando que todos regresaran a su estado inicial al finalizar el ciclo completo.
2. Se estableció un encadenamiento lógico, donde la salida de un temporizador funciona como condición para activar el siguiente.
3. Se revisó que los bloques de retardo a la conexión estuvieran bien configurados, verificando los parámetros de tiempo correspondientes.
4. Finalmente, se validó el funcionamiento mediante simulación paso a paso en LOGO! Soft Comfort antes de considerar una implementación física.

---

## Conexión con el curso

**Concepto MR2022 aplicado:** *Elementos que conforman un sistema mecatrónico – Computadoras y lógica de control*

En esta semana se aplicó directamente el uso de controladores programables como parte fundamental de un sistema mecatrónico. El LOGO permite observar claramente la integración entre el hardware, a través de las entradas y salidas digitales, y el software, mediante la programación con bloques lógicos. Además, se trabajó el secuenciamiento temporal de actuadores, lo cual es esencial en sistemas de control básicos.

---

## Autoevaluación

* [ ] Muy perdido
* [ ] Con dudas
* [x] **Entendiendo** ✓
* [ ] Dominando

**Reflexión grupal:**
Se logró comprender la estructura básica del Siemens LOGO y el desarrollo de programas sencillos utilizando temporizadores y lógica de control. No obstante, aún es necesario reforzar el uso de funciones más avanzadas y la conexión con sensores y actuadores reales para afianzar el aprendizaje.
