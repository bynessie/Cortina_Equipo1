# Hito 2 – Selección de Componentes

## Sensores seleccionados
| Sensor | Variable | Tipo de señal | Justificación |
|--------|----------|--------------|---------------|
| Capacitivo | Presencia de material no metálico | Digital PNP – 24 VDC | Permite detectar materiales no metálicos, bajo costo y fácil integración al PLC |
| Inductivo | Presencia de material metálico | Digital PNP – 24 VDC | Alta precisión, robusto y resistente al polvo y la suciedad |
| Óptico Infrarrojo | Detección de obstáculos / presencia | Digital PNP – 24 VDC | Ideal para seguridad anti-atrapamiento; detecta múltiples materiales sin contacto físico |
| Magnético (Arriba) | Posición superior | Digital PNP – 24 VDC | Sin desgaste mecánico, alta confiabilidad y bajo mantenimiento |
| Magnético (Medio) | Posición intermedia | Digital PNP – 24 VDC | Permite referencia intermedia para control de altura y lógica de operación |
| Magnético (Abajo) | Posición inferior | Digital PNP – 24 VDC | Confirma cierre completo de la cortina y garantiza seguridad operativa |


## Actuadores seleccionados
| Actuador | Variable | Tipo de señal | Justificación |
|-----------|-----------|--------------|---------------|
| Motor para la cortina | Movimiento (subida/bajada) | Señal de potencia controlada por relevador (24 VDC) | Actuador principal encargado del desplazamiento mecánico bidireccional de la cortina |
| Bobinas de relevadores | Conmutación de potencia | Digital 24 VDC (control PLC) | Permiten que el PLC controle cargas de mayor potencia aislando el circuito de control |
| Torre de señalización | Estado del sistema | Digital 24 VDC | Proporciona advertencia visual del estado (listo, movimiento, alarma) aumentando seguridad operativa |
| PLC Siemens LOGO | Control lógico del sistema | Entradas y salidas digitales 24 VDC | Controlador central que procesa señales de sensores y activa actuadores con lógica segura e interlocks. También es la interfas para el usuario |

## Riesgos y consideraciones

| # | Elemento / Riesgo | ¿Qué podría fallar? | Consecuencia | Mitigación |
|---|-------------------|---------------------|--------------|------------|
| 1 | Sensor infrarrojo (obstáculo) | No detectar objeto, suciedad, mala alineación | Atrapamiento o daño material | Limpieza periódica, no operar en límite máximo, paro inmediato ante señal incoherente, señalización visual/sonora |
| 2 | Sensores magnéticos (posición) | Desalineación, desconexión, daño físico | Motor no se detiene, sobrecarga mecánica | Temporizador máximo de recorrido, inspección periódica, estado seguro si no se detecta señal |
| 3 | Activación simultánea subir/bajar | Error de programación, relevador pegado | Cortocircuito, daño al motor | Interlock lógico en PLC, interlock eléctrico físico, protección termomagnética |
| 4 | Motor eléctrico | Sobrecalentamiento, sobrecarga, desgaste | Paro total o riesgo eléctrico | Protección térmica, selección adecuada, mantenimiento preventivo |
| 5 | Falla eléctrica general | Cortocircuito, picos de voltaje, mala conexión | Daño a PLC y sensores | Fuente regulada 24VDC, fusibles/breakers, aislamiento adecuado |
| 6 | PLC (hardware o programación) | Error lógico, bloqueo, pérdida de energía | Movimiento inesperado o pérdida de control | Programación estructurada, pruebas previas, estado seguro por defecto |
| 7 | Operación en límite de sensores | Lecturas inestables, falsas detecciones | Movimiento errático | Instalar dentro de zona estable, margen de seguridad 20–30%, validación experimental |
| 8 | Error humano | Uso indebido, mantenimiento energizado | Lesiones o daño al sistema | Botón de paro de emergencia, señalización clara, capacitación básica |
