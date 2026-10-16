# Escenarios de Atributos de Calidad

## Sistema Integral de Gestión Turística de Huamanga

### 1. Introducción

Los escenarios de atributos de calidad permiten describir situaciones específicas para evaluar el comportamiento esperado del sistema. Estos escenarios orientarán las decisiones arquitectónicas y servirán como referencia para las pruebas durante el desarrollo.

### 2. AC-ESC01 — Rendimiento

**Atributo:** Rendimiento.

**Estímulo:** un visitante realiza una búsqueda de atractivos turísticos.

**Respuesta esperada:** el sistema procesa la consulta y muestra los resultados correspondientes sin demoras excesivas.

**Medida de evaluación propuesta:** al menos el 95 % de las consultas de prueba deberán responder en un máximo de 3 segundos, bajo condiciones de carga y red previamente definidas.

### 3. AC-ESC02 — Disponibilidad

**Atributo:** Disponibilidad.

**Estímulo:** un usuario intenta acceder al sistema durante el horario previsto de funcionamiento.

**Respuesta esperada:** el sistema permite consultar la información turística y muestra un mensaje comprensible cuando el servicio no está disponible.

**Medida de evaluación:** registrar el tiempo total de funcionamiento y las interrupciones durante un periodo de observación definido. El porcentaje objetivo de disponibilidad deberá acordarse antes de realizar las pruebas.

### 4. AC-ESC03 — Escalabilidad

**Atributo:** Escalabilidad.

**Estímulo:** aumenta el número de usuarios que realizan consultas simultáneamente.

**Respuesta esperada:** el sistema continúa atendiendo las solicitudes y mantiene un comportamiento aceptable.

**Medida de evaluación:** ejecutar pruebas con diferentes niveles de usuarios concurrentes y comparar los tiempos de respuesta, los errores y el uso de recursos.

### 5. AC-ESC04 — Seguridad

**Atributo:** Seguridad.

**Estímulo:** un visitante intenta ejecutar una operación reservada al administrador.

**Respuesta esperada:** el sistema deniega la operación y no permite modificar información restringida.

**Medida de evaluación:** realizar pruebas con diferentes roles y comprobar que cada uno pueda ejecutar únicamente las operaciones autorizadas.

### 6. AC-ESC05 — Mantenibilidad

**Atributo:** Mantenibilidad.

**Estímulo:** un desarrollador necesita modificar una funcionalidad de consulta turística.

**Respuesta esperada:** la modificación puede realizarse en los componentes correspondientes sin alterar innecesariamente otras funcionalidades.

**Medida de evaluación:** revisar los componentes modificados y ejecutar pruebas de regresión para comprobar que las funcionalidades relacionadas continúen operativas.

### 7. Resumen de escenarios

| ID | Atributo | Situación evaluada | Verificación principal |
|---|---|---|---|
| AC-ESC01 | Rendimiento | Consulta de atractivos turísticos | Tiempo de respuesta |
| AC-ESC02 | Disponibilidad | Acceso al sistema | Registro de funcionamiento e interrupciones |
| AC-ESC03 | Escalabilidad | Incremento de usuarios concurrentes | Pruebas de carga |
| AC-ESC04 | Seguridad | Acceso a funciones restringidas | Pruebas de autorización |
| AC-ESC05 | Mantenibilidad | Modificación de una funcionalidad | Revisión y pruebas de regresión |

### 8. Conclusión

Los escenarios definidos permiten establecer cómo se evaluarán los principales atributos de calidad del Sistema Integral de Gestión Turística de Huamanga. Las medidas propuestas deberán ajustarse a los recursos y objetivos del proyecto antes de realizar las pruebas correspondientes.