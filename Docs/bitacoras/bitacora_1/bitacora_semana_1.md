# Bitácora de Proyecto - Semana 1

## Tema de la semana
**Control** - Introducción al relé programable Siemens LOGO

---

## Actividades realizadas
- Identificación y estudio de las partes del controlador Siemens LOGO! (alimentación, entradas, salidas).
- Instalación y configuración del software LOGO! Soft Comfort.
- Creación de un programa secuenciador de luces que controla 3 salidas con tiempos diferentes.
- Implementación del diagrama de bloques utilizando temporizadores, compuertas lógicas y salidas.
- Simulación del programa y verificación del ciclo repetitivo.

---

## Decisiones de ingeniería

| Decisión | Alternativas | Justificación |
|----------|-------------|---------------|
| **Selección de compuertas AND para activación** | Compuertas OR o contactos directos | Las compuertas AND aseguran que las salidas solo se activen cuando se cumplan TODAS las condiciones de tiempo y estado anteriores |
| **Configuración de salidas tipo relé** | Salidas transistorizadas | Los relés permiten manejar diferentes tipos de carga (AC/DC) y son más versátiles para aplicaciones industriales básicas |

---

## Problema técnico encontrado
**Descripción:** Al simular el programa inicialmente, las salidas no se apagaban correctamente al finalizar su tiempo asignado, causando que múltiples salidas permanecieran activas simultáneamente en lugar de encenderse secuencialmente. Esto violaba el requerimiento de que cada salida se encendiera de forma independiente y consecutiva.

---

## Solución aplicada
Se reestructuró el diagrama de bloques implementando:
1. **Reset adecuado de temporizadores:** Se configuró la entrada de reset (R) de cada temporizador para que se activara al finalizar el ciclo completo, asegurando que todos los bloques volvieran a estado inicial.
2. **Encadenamiento lógico:** La salida de cada temporizador se convirtió en la condición de activación del siguiente, creando una secuencia dependiente.
3. **Uso de bloques de retardo a la conexión (Ton):** Se verificó que los bloques B001, B002 y B003 estuvieran configurados correctamente con los parámetros Ta (tiempo de activación) y T (tiempo total).
4. **Validación mediante simulación:** Se probó el programa paso a paso en LOGO! Soft Comfort antes de la carga física.

---

## Conexión con el curso
**Concepto MR2022 aplicado:** *"Elementos que conforman un sistema mecatrónico - Computadoras y lógica de control"*

Esta semana aplicamos directamente el concepto de **controladores programables (PLCs/microcontroladores)** como elemento central de los sistemas mecatrónicos. El LOGO representa la integración de:
- **Hardware:** Entradas/salidas digitales que interactúan con el mundo físico.
- **Software:** Programación mediante bloques lógicos que implementan algoritmos de control.
- **Secuenciamiento:** Control temporal de actuadores (luces/motores) basado en condiciones lógicas.

---

## Autoevaluación
 
- [ ] Muy perdido
- [ ] Con dudas
- [x] **Entendiendo** ✓
- [ ] Dominando

**Reflexión grupal:** Comprendemos la estructura básica del LOGO! y cómo crear programas simples con temporizadores y bloques lógicos. Sin embargo, necesitamos más práctica con funciones avanzadas  y con la integración física de sensores y actuadores reales. 
