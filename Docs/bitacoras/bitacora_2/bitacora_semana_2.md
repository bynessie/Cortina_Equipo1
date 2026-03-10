# Bitácora – Semana 2

## Tema de la semana
Sensores - elección + pruebas

## Actividades realizadas
Durante esta semana aprendimos conceptos basicos de los sensores, se trabajó en la creación del circuito del LOGO que llevara la cortina y junto con esto se estuvieron definiendo, probando y validando los sensores que se utilizaran en este sistema.

Como prácticas para estas actividades, se investigó, definió y justifico cada sensor y actuador a usar junto con sus posibles riesgos y consideraciones, para posteriormente evaluar las características de los sensores (confiabilidad, costo, montaje, inmunidad, mantenimiento) dentro de una matriz de selección.
Después se elaboró un plan de pruebas de sensores en el cual se cubrieron 5 de los escenarios más normales y uno de fallo.
Ya con esto se elaboró el diagrama del circuito que llevara el sistema LOGO, se montó este y finalmente se realizaron experimentos con los distintos sensores, los cuales se registraron en la sección de "Registro_Pruebas_Sensores".

## Decisiones de ingeniería
| Decisión | Alternativas | Justificación |
|--------|-------------|---------------|
| Uso de sensor inductivo | Sensor Hall | Es fácil de montar, No necesita mucho mantenimiento, es accesible, barato y se usara para detecta una placa metálica o activador |
| Uso de sensor capacitivo | Botón pulsador industrial | No necesita mucho mantenimiento, es accesible y permite activar manualmente la subida de la cortina mediante contacto físico, siendo una solución simple y confiable |
| Uso de sensor óptico infrarrojo | Barrera fotoeléctrica | Es fácil de montar, no necesita mucho mantenimiento, es accesible y detecta la interrupción de un haz de luz entre emisor y receptor, ofreciendo mayor confiabilidad para sistemas de seguridad |
| Uso de sensor magnético | Final de carrera mecánico | Es excelente para detectar posiciones, no genera desgaste mecánico, no necesita mucho mantenimiento, es accesible, barato y podra detectar físicamente cuando la cortina llega al punto máximo superior o inferior, deteniendo el motor de forma directa |
| Control del sistema mediante PLC Siemens LOGO | Arduino | El PLC ofrece mayor confiabilidad industrial, facilidad de programación, integración directa con sensores de 24V y funciones de seguridad |


## Problema técnico encontrado
Durante el armado del sistema, al poner el LOGO sobre el riel descubrimos que este no se sujetaba bien, por lo cual se deslizava sobre el riel.

## Solución aplicada
Este problema lo solucionamos poniendo el LOGO en medio de dos bloques terminal de riel.
Aparte de esto no tubimos inconvenientes.

## Conexión con el curso
**Concepto MR2022 aplicado:** *Sensores - Procedimiento Selección de Sensor*

Estos conceptos los aplicamos al momento de seleccionar los sensores que llevara el sistema, definiendo la funcionalidad que queremos alcanzar con estos, los parámetros de cada sensor y sobre todo entendiendo las capacidades de cada uno de estos junto con sus principales características y limitaciones.
Además de saber cómo usarlos y gestionarlos.

---

## Reflexión grupal:
Durante esta semana se logro crear de forma efectiva el circuito base del sistema que se estara usando junto con un entendimiento correcto de cada uno de los sensores. Aun así, nos falta mejorar la organización en el tema de la ddocumentación y los entregables, por lo cual estaremos trabajando más en ello.

## Autoevaluación

* [ ] Muy perdido
* [ ] Con dudas
* [x] **Entendiendo** ✓
* [ ] Dominando
