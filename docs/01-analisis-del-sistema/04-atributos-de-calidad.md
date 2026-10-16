# Atributos de Calidad

## Sistema Integral de Gestión Turística de Huamanga

Los atributos de calidad describen las características que deberá cumplir el sistema para funcionar de manera segura, eficiente y sostenible. Estos atributos orientarán las decisiones arquitectónicas y servirán como referencia para las pruebas del sistema.

### AC01 — Rendimiento

El sistema deberá responder oportunamente a las consultas de atractivos turísticos, servicios, eventos y rutas.

**Criterio de evaluación propuesto:** las consultas principales deberán responder en un máximo de 3 segundos en al menos el 95 % de las solicitudes, bajo una carga de prueba y unas condiciones de red previamente definidas.

**Consideración arquitectónica:** se deberá procurar que las consultas y el acceso a los datos sean eficientes.

### AC02 — Disponibilidad

El sistema deberá estar disponible para que los usuarios puedan consultar la información turística durante los periodos previstos de funcionamiento.

**Criterio de evaluación propuesto:** definir un porcentaje objetivo de disponibilidad mensual y registrar los periodos en que el sistema no pueda utilizarse.

**Consideración arquitectónica:** se deberán identificar los posibles puntos de fallo y establecer procedimientos de recuperación acordes con el alcance del proyecto.

### AC03 — Escalabilidad

El sistema deberá permitir ampliar su capacidad para atender un crecimiento en el número de usuarios y solicitudes.

**Criterio de evaluación propuesto:** realizar pruebas con diferentes cantidades de solicitudes y comparar los tiempos de respuesta y el comportamiento del sistema.

**Consideración arquitectónica:** la organización de los componentes deberá facilitar la ampliación de recursos cuando sea necesario.

### AC04 — Seguridad

El sistema deberá restringir las operaciones administrativas a los usuarios autorizados y proteger la información gestionada.

**Criterios de evaluación:**
- Un visitante no deberá acceder a funciones exclusivas del administrador.
- Un prestador turístico solo deberá modificar la información para la que tenga autorización.
- El sistema deberá validar los permisos antes de ejecutar operaciones restringidas.

**Consideración arquitectónica:** se deberán definir mecanismos de autenticación y autorización, además de medidas de protección para los datos.

### AC05 — Mantenibilidad

El sistema deberá estar organizado de forma que sus componentes puedan corregirse, modificarse y ampliarse sin generar cambios innecesarios en otras partes.

**Criterio de evaluación:** comprobar que una modificación localizada en un componente pueda realizarse sin alterar las funcionalidades no relacionadas y que las pruebas correspondientes continúen funcionando.

**Consideración arquitectónica:** se deberá mantener una separación clara de responsabilidades entre la presentación, la lógica de negocio y el acceso a los datos.

## Relación con la arquitectura

Los atributos de calidad orientarán la elección de la arquitectura en tres capas y las decisiones técnicas posteriores. Su cumplimiento deberá verificarse mediante pruebas y revisiones durante el desarrollo del sistema.

Los valores y condiciones de evaluación deberán validarse de acuerdo con el alcance, los recursos y las expectativas del proyecto.