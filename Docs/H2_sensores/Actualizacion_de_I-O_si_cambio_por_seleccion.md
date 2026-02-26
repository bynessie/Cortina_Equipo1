Actualizar la tabla I/O  según los sensores seleccionados. Incluye tipo de señal, descripción funcional y notas relevantes derivadas de las pruebas.

Tabla I/O Actualizada del Sistema
### Tabla I/O del Sistema

| Dispositivo        | Tipo de Sensor | Dirección I/O | Tipo de Señal | Descripción Funcional                                                        | Notas Derivadas de Pruebas                                                                 |
|--------------------|----------------|---------------|---------------|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Sensor Magnético 1 | Magnético      | I0.0          | Digital (PNP) | Detecta presencia de campo magnético en piezas con imán integrado             | Alta confiabilidad de activación; requiere proximidad < 5 mm para respuesta consistente    |
| Sensor Magnético 2 | Magnético      | I0.1          | Digital (PNP) | Confirmación de posicionamiento en estación intermedia                        | No presenta falsos positivos; dependiente de correcta orientación del campo magnético      |
| Sensor Magnético 3 | Magnético      | I0.2          | Digital (PNP) | Verificación de paso de pieza en punto final del trayecto                     | Tiempo de respuesta estable; adecuado para detección discreta en movimiento                |
| Sensor Infrarrojo  | Óptico IR      | I0.3          | Digital       | Detecta presencia de objeto sin contacto físico mediante reflexión de luz IR | Alcance efectivo real: 18–20 cm; variación según reflectividad del material detectado      |
| Sensor Capacitivo  | Capacitivo     | I0.4          | Digital       | Detecta materiales con variación dieléctrica (plástico, líquido, tejido)     | Alta sensibilidad a líquidos; detección limitada en materiales de baja constante dieléctrica |
| Sensor Inductivo   | Inductivo      | I0.5          | Digital       | Detecta exclusivamente objetos metálicos mediante campo electromagnético     | Selectividad adecuada; sin respuesta ante materiales no metálicos                          |

Observaciones Derivadas de Pruebas
- El sensor infrarrojo presenta variación en el rango dependiendo de la reflectividad del material.
- El sensor capacitivo muestra mayor sensibilidad ante presencia de líquidos.
- El sensor inductivo mantiene selectividad adecuada únicamente para materiales metálicos.
- Los sensores magnéticos no presentan falsos positivos ante materiales no imantados.
