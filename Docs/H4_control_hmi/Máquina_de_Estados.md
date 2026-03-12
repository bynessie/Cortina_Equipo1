# Tabla de estados del sistema
| Estado             | Descripción                       |
| ------------------ | --------------------------------- |
| Sistema detenido   | La cortina se encuantra quieta |
| Subiendo | El motor está subiendo la cortina |
| Bajando | El motor está bajando la cortina |
| Cortina arriba | La cortina llega al límite superior (Se prende la luz roja) |
| Cortina abajo | La cortina llega al límite inferior (Se prende la luz verde) |
| Bloqueo de seguridad | Se detectó un obstáculo mientras la cortina baja |

# Tabla de eventos del sistema
| Evento                  | Acción               |
| ----------------------- | -------------------- |
| Sensor capacitivo activado | Se pasa de "Sistema detenido" a "Bajando" |
| Sensor magnético arriba activado | Se pasa de "Subiendo" a "Cortina arriba" |
| Sensor inductivo activado | Se pasa de "Cortina abajo" a "Subiendo" |
| Sensor magnético abajo activado | Se pasa de "Bajando" a "Cortina abajo" |
| Sensor óptico activado | Se pasa de "Bajando" a "Bloqueo de seguridad"|
| Sensor óptico desactivado | Se pasa de "Bloqueo de seguridad" a "Bajando"|


## Maquina de estados
<img width="589" height="720" alt="image" src="https://github.com/user-attachments/assets/d99cd645-9502-4a0f-8552-ca362b5836ff" />
