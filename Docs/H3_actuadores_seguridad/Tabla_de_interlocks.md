 # Tabla de interlocks
 | Condiciones prohibidas | Causa | Riesgo asociado | Acción de bloqueo |
 |------------------------|-------|-----------------|-------------------|
 | Acción simultánea de subida y bajada de la cortina | Activación simultánea de subida y bajada de la cortina | Cortocircuito / daño al motor | Si se activan ambas ordenes al mismo tiempo, el sistema bloqueara la acción |
 | La cortina sigue bajando aunque exista un obstaculo | Fallo del sensor | Daño en el obstaculo | Boton de paro de emergencia |
 | El motor continua en movimiento despues del limite establecido (Ya sea superior o inferior) | Fallo del sensor o código | Sobrecarga mecánica, forzamiento o daño estructural | Establecer un temporizador de recorrido máximo |
 | Ejecutar el sistema automático o manual con un sensor fallando | Sensor desconectado, sin señal o descompuesto | Movimiento inseguro | Cancelar el ciclo automático o movimiento manual y parar el sistema |
 | Operar el sistema sin alimentación suficiente o estable | Bajo voltaje o pico eléctrico | Daño a PLC o sensores | No habilitar el sistema hasta tener alimentación suficiente y estable |
