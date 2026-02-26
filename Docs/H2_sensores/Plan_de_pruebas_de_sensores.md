

# **Plan de Pruebas para la Evaluación de Sensores**



## **1. Objetivo**

Establecer un procedimiento estructurado para ejecutar las pruebas de funcionamiento de los sensores **magnético, infrarrojo, capacitivo e inductivo**, garantizando:

* Repetibilidad
* Control de variables
* Criterios claros de evaluación (**PASS / FAIL**)


## **2. Alcance**

El presente plan contempla:

* Verificación funcional básica de cada sensor
* Evaluación ante distintos materiales
* Identificación de limitaciones operativas
* Registro sistemático de resultados



## **3. Recursos Necesarios**

### **3.1 Sensores**

* 3 Sensores magnéticos
* 1 Sensor infrarrojo (alcance aproximado de 20 cm)
* 1 Sensor capacitivo
* 1 Sensor inductivo



### **3.2 Materiales de Prueba**

* Botella de plástico vacía
* Botella con agua
* Mesa metálica
* Placa de acero
* Dedo de un integrante
* Imán de neodimio
* Malla de fibra de poliéster



### **3.3 Equipo Adicional**

* Fuente de alimentación regulada
* PLC LOGO!
* Multímetro
* Cinta métrica o regla



## **4. Condiciones Generales de Prueba**

* Temperatura ambiente estable
* Sensores correctamente energizados según especificaciones del fabricante
* Superficie de trabajo fija y nivelada
* Distancia medida cuando aplique (especialmente en sensor infrarrojo e inductivo)
* Repetición mínima de cada prueba: **3 veces** para validar consistencia



## **5. Metodología General**

### **5.1 Preparación**

* Verificar conexiones eléctricas
* Confirmar voltaje correcto de alimentación
* Comprobar estado inicial (sensor sin estímulo)



### **5.2 Ejecución**

* Aplicar el estímulo definido
* Registrar respuesta del sensor
* Medir distancia cuando sea necesario
* Repetir el procedimiento **3 veces**



### **5.3 Evaluación**

* Comparar resultado observado con resultado esperado
* Clasificar como **PASS** o **FAIL**
* Documentar observaciones relevantes



## **6. Plan Detallado por Sensor**



### **6.1 Sensor Magnético**

**Objetivo:**
Verificar activación exclusiva ante campo magnético.

**Procedimiento:**

1. Energizar el sensor
2. Mantener sin estímulo durante 10 segundos
3. Acercar imán de neodimio progresivamente
4. Repetir con materiales no magnéticos:

   * Plástico
   * Malla
   * Dedo

**Criterio de aceptación:**

* Activación únicamente con el imán
* No activación con otros materiales


### **6.2 Sensor Infrarrojo**

**Objetivo:**
Evaluar rango de detección y respuesta ante distintos materiales.

**Procedimiento:**

1. Energizar el sensor
2. Colocar objeto a 25 cm (fuera de rango esperado)
3. Acercarlo lentamente hasta 20 cm o menos
4. Repetir con todos los materiales

**Criterio de aceptación:**

* Activación dentro del rango especificado (~20 cm)
* Detección consistente con diferentes materiales reflectivos



### **6.3 Sensor Capacitivo**

**Objetivo:**
Evaluar sensibilidad ante cambios de capacitancia.

**Procedimiento:**

1. Energizar el sensor
2. Aproximar el dedo sin contacto directo
3. Probar botella con agua
4. Probar botella vacía
5. Probar malla y otros objetos

**Criterio de aceptación:**

* Activación con presencia de objetos que generen cambio capacitivo significativo
* No activación ante objetos con mínima variación dieléctrica



### **6.4 Sensor Inductivo**

**Objetivo:**
Verificar detección exclusiva de materiales metálicos.

**Procedimiento:**

1. Energizar el sensor
2. Aproximar placa de acero y mesa metálica
3. Probar con materiales no metálicos

**Criterio de aceptación:**

* Activación únicamente con metales
* No respuesta ante plástico o fibra



## **7. Gestión de Riesgos**

* Evitar contacto prolongado del imán con dispositivos electrónicos sensibles
* No exceder el voltaje nominal de los sensores
* Manipular la placa metálica con cuidado para evitar lesiones



## **8. Criterios de Finalización**

Las pruebas se consideran concluidas cuando:

* Todos los sensores han sido evaluados con todos los materiales
* Se hayan documentado al menos **6 casos de prueba formales**
* Se cuente con evidencia (fotográfica o en video) del procedimiento
* Se tenga un análisis comparativo final del desempeño



## **9. Entregables**

* Registro completo de resultados
* Tabla de casos **PASS / FAIL**
* Conclusiones técnicas sobre aplicabilidad en el proyecto
* Evidencia audiovisual (si se requiere)


