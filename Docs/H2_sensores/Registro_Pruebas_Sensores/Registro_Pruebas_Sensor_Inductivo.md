

# MR2022 -- Registro Experimental de Pruebas de Sensores de Proximidad

## Curso: Análisis de Elementos de Mecatrónica

## Práctica: Conexión y validación de sensores con Siemens LOGO

## Equipo: MR2022

## Integrantes: equipo

## Fecha:26 Febrero 2026

---

# 1️⃣ Identificación del Sensor

*(Se presenta registro individual por tipo de sensor evaluado)*

---

## 🔹 Sensor Inductivo

| Parámetro                     | Información                              |
| ----------------------------- | ---------------------------------------- |
| Tipo de sensor                | Inductivo                                |
| Marca / Modelo                | Genérico industrial M12                  |
| Tipo de salida                | PNP                                      |
| Alimentación                  | 24 VDC                                   |
| Distancia nominal (datasheet) | 4 mm                                     |
| Tipo de conexión al LOGO      | Digital                                  |
| Observaciones iniciales       | Activación rápida, LED indicador estable |

---

## 🔹 Sensor Capacitivo

| Parámetro                     | Información                           |
| ----------------------------- | ------------------------------------- |
| Tipo de sensor                | Capacitivo                            |
| Marca / Modelo                | Genérico ajustable                    |
| Tipo de salida                | PNP                                   |
| Alimentación                  | 24 VDC                                |
| Distancia nominal (datasheet) | 8 mm                                  |
| Tipo de conexión al LOGO      | Digital                               |
| Observaciones iniciales       | Sensible a líquidos y contacto humano |

---

## 🔹 Sensor Infrarrojo

| Parámetro                     | Información                        |
| ----------------------------- | ---------------------------------- |
| Tipo de sensor                | Óptico infrarrojo                  |
| Marca / Modelo                | IR difuso 20 cm                    |
| Tipo de salida                | PNP                                |
| Alimentación                  | 24 VDC                             |
| Distancia nominal (datasheet) | 20 cm                              |
| Tipo de conexión al LOGO      | Digital                            |
| Observaciones iniciales       | Variación leve según reflectividad |

---

## 🔹 Sensor Magnético

| Parámetro                     | Información                              |
| ----------------------------- | ---------------------------------------- |
| Tipo de sensor                | Magnético                                |
| Marca / Modelo                | Reed switch industrial                   |
| Tipo de salida                | PNP                                      |
| Alimentación                  | 24 VDC                                   |
| Distancia nominal (datasheet) | ≤5 mm                                    |
| Tipo de conexión al LOGO      | Digital                                  |
| Observaciones iniciales       | Respuesta exclusiva ante campo magnético |

---

# 2️⃣ Resultados por Material Evaluado

## 🔹 Sensor Inductivo

| Material | ¿Detecta? | Dist. mín estable (mm) | Dist. máx estable (mm) | Dist. promedio efectiva (mm) | Zona inestable (mm) | Falsas detecciones | Observaciones técnicas       |
| -------- | --------- | ---------------------- | ---------------------- | ---------------------------- | ------------------- | ------------------ | ---------------------------- |
| Acero    | Sí        | 1                      | 4                      | 3                            | 4–5                 | No                 | Activación sólida            |
| Aluminio | Sí        | 1                      | 3                      | 2.5                          | 3–4                 | No                 | Menor alcance                |
| Cobre    | Sí        | 1                      | 3                      | 2.5                          | 3–4                 | No                 | Respuesta estable            |
| Plástico | No        | —                      | —                      | —                            | —                   | No                 | No conductor                 |
| Madera   | No        | —                      | —                      | —                            | —                   | No                 | No conductor                 |
| Vidrio   | No        | —                      | —                      | —                            | —                   | No                 | No conductor                 |
| Agua     | No        | —                      | —                      | —                            | —                   | No                 | No conductor                 |
| Imán     | Sí        | 1                      | 4                      | 3                            | 4–5                 | No                 | Detecta por carcasa metálica |

---

## 🔹 Sensor Capacitivo

| Material      | ¿Detecta? | Dist. mín | Dist. máx | Promedio | Zona inestable | Falsas det. | Observaciones                   |
| ------------- | --------- | --------- | --------- | -------- | -------------- | ----------- | ------------------------------- |
| Acero         | Sí        | 1         | 6         | 5        | 6–8            | No          | Alta respuesta                  |
| Plástico      | Sí        | 1         | 4         | 3        | 4–6            | No          | Depende grosor                  |
| Agua          | Sí        | 2         | 8         | 7        | 8–10           | No          | Alta constante dieléctrica      |
| Botella vacía | No        | —         | —         | —        | —              | No          | Cambio dieléctrico insuficiente |
| Madera        | Sí        | 1         | 3         | 2        | 3–5            | No          | Respuesta moderada              |

---

## 🔹 Sensor Infrarrojo

Detectó todos los materiales dentro de 18–20 cm sin falsos positivos.

---

## 🔹 Sensor Magnético

Detectó únicamente el imán de neodimio a ≤5 mm.

---

# 3️⃣ Prueba de Distancia Incremental

*(Sensor Inductivo – referencia metálica)*

| Distancia (mm) | LED | Entrada LOGO | ¿Consistente? | Comentarios      |
| -------------- | --- | ------------ | ------------- | ---------------- |
| 0              | ON  | 1            | Sí            | Contacto directo |
| 2              | ON  | 1            | Sí            | Estable          |
| 4              | ON  | 1            | Sí            | Límite nominal   |
| 6              | OFF | 0            | Sí            | Fuera de rango   |

---

# 4️⃣ Comparación vs Especificación del Fabricante

## Sensor Inductivo

| Parámetro            | Datasheet | Experimental       | Error (%) |
| -------------------- | --------- | ------------------ | --------- |
| Distancia nominal    | 4 mm      | 4 mm               | 0%        |
| Tiempo respuesta     | <10 ms    | Instantáneo visual | —         |
| Material recomendado | Metales   | Metales            | 0%        |

---

# 5️⃣ Análisis Técnico del Equipo

## 5.1 ¿Coincide la distancia real con la nominal?

Sí. La distancia experimental fue consistente con la especificación del fabricante.

---

## 5.2 ¿Qué fenómeno físico explica el comportamiento observado?

* Inductivo → Corrientes de Foucault
* Capacitivo → Variación de constante dieléctrica
* Infrarrojo → Reflexión óptica
* Magnético → Interacción de campo magnético

---

## 5.3 ¿Qué materiales generan mejor desempeño? ¿Por qué?

* Inductivo → Acero (alta conductividad y permeabilidad magnética)
* Capacitivo → Agua (alta constante dieléctrica)
* IR → Materiales reflectivos
* Magnético → Imán permanente

---

## 5.4 ¿Detectaron zonas muertas o inestabilidad?

Leve zona inestable en el límite máximo de detección (±1 mm).

---

## 5.5 ¿Este sensor sería adecuado para la situación problema del curso?

Sí. Técnicamente cumple precisión y confiabilidad.
Económicamente es viable por su bajo costo y fácil integración con LOGO.

---

# 6️⃣ Matriz de Decisión Técnica (Sensor Inductivo)

| Criterio             | Peso | Evaluación | Resultado |
| -------------------- | ---- | ---------- | --------- |
| Precisión            | 5    | 5          | 25        |
| Distancia útil       | 4    | 4          | 16        |
| Robustez industrial  | 5    | 5          | 25        |
| Inmunidad a ruido    | 4    | 5          | 20        |
| Costo                | 3    | 4          | 12        |
| Integración con LOGO | 5    | 5          | 25        |
| **TOTAL**            |      |            | **123**   |

---

# 7️⃣ Conclusión Ingenieril

Los sensores evaluados cumplen con su principio físico de operación.

* El sensor magnético es ideal para detección exclusiva de campo magnético.
* El sensor infrarrojo es versátil y adecuado para detección general sin contacto.
* El sensor capacitivo permite aplicaciones táctiles y detección de nivel.
* El sensor inductivo es el más robusto para detección industrial de metales.

Se recomienda su uso según el tipo de material del sistema.
El principal riesgo industrial identificado es la instalación incorrecta que genere zonas muertas o falsas lecturas en el límite de detección.

---

# 8️⃣ Evidencia

* Fotografías del montaje: Incluidas en repositorio
* Capturas del programa en LOGO: Incluidas
* Video de funcionamiento: Adjuntado
* Datasheet utilizado: Carpeta `/datasheets/`

---

# 9️⃣ Bitácora de Aprendizaje

Se aprendió que cada sensor responde estrictamente a su principio físico y que la selección incorrecta puede generar fallos operativos. También se comprobó la importancia de validar experimentalmente la distancia real y no depender únicamente del datasheet.

---


------------------------------------------------------------------------

> ⚙️ Este documento forma parte del proceso de validación experimental
> para la selección de sensores dentro del proyecto integrador MR2022.
