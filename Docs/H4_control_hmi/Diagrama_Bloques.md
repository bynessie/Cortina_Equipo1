# Diagrama de Bloques
<img width="1086" height="809" alt="image" src="https://github.com/user-attachments/assets/39625570-3cdc-4883-9642-d4738ccba6d0" />

Este es el código final que se implemento dentro del LOGO.

| Entrada |Numero de sensor | Sensor                  | Función                                                |
| ------- |-------| ----------------------- | ------------------------------------------------------ |
| I1      | S1 | Sensor capacitivo       | Orden para bajar la cortina                        |
| I2      | S2 | Sensor inductivo        | Orden para subir la cortina                       |
| I3      | S3 | Sensor óptico           | Sensor de seguridad que detecta objetos |
| I4      | S4 |Sensor magnético arriba | Detecta cuando la cortina llegó al límite superior |
| I5      | S5 | Sensor magnético medio  | Detecta posición intermedia                       |
| I6      | S6 | Sensor magnético abajo  | Detecta cuando la cortina llegó al límite inferior |

| Salida | Actuador      | Función           |
| ------ | ------------- | ----------------- |
| Q1     | Motor abajo   | Cierra la cortina |
| Q2     | Motor arriba  | Abre la cortina   |
| Q3     | Lámpara roja  | Indica que la cortina esta completamente abierta |
| Q4     | Lámpara verde | Indica que la cortina esta completamente cerrada |

La lógica que sigue este código es la siguiente:
Para que la cortina baje se debe activar Q1, para lo cual se deben cumplir las condiciónes de que S4 debe estar activado, S5 y S6 deben estar desactivados, Q2 debe estar desactivado, S3 no debe estar detectando nada y S1 debe aber detectado una señal.
Mientras que para que suba se debe activar Q2, con lo cual S6 debe estar activado, S5 y S4 deben estar desactivados, Q1 debe estar desactivado y S2 debe aber detectado una señal.

Por otro lado, para indicar que la cortina esta completamente abajo se debe encender Q4, lo cual solo pasa si S6 detecta algo. Mientras que para indicar que la cortina esta completamente arriba se debe encender Q3, lo cual solo pasa si S4 detecta algo.

Y aparte de ello tambien se implemento un temporizador de 10 segundos cuando la cortina llega hasta abajo (Cuando se activa S6), para que esta no suba apenas llega abajo durante el ciclo automatico.


# Video de Funcionamiento

https://github.com/user-attachments/assets/22ac012c-6e12-4cab-a0a4-d0a3bc289b93

