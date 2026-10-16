# Drivers Arquitectónicos

## Sistema Integral de Gestión Turística de Huamanga

Los drivers arquitectónicos son los requisitos, atributos de calidad y condiciones que influyen de manera significativa en las decisiones de diseño del sistema. Permiten identificar qué aspectos deben priorizarse al definir su arquitectura.

### DA01 — Organización arquitectónica

**Origen:** RC01 — Arquitectura definida.

**Necesidad:** organizar el sistema en partes con responsabilidades diferenciadas.

**Decisión arquitectónica:** estructurar la solución en las capas de presentación, lógica de negocio y acceso a datos.

**Impacto:** facilita la organización del código y la separación de responsabilidades.

### DA02 — Rendimiento

**Origen:** AC01 — Rendimiento.

**Necesidad:** permitir consultas oportunas de atractivos, servicios, eventos y rutas turísticas.

**Decisión arquitectónica:** procurar consultas eficientes y evitar operaciones innecesarias entre los componentes.

**Impacto:** contribuye a reducir los tiempos de respuesta.

**Verificación propuesta:** medir los tiempos de respuesta mediante pruebas de rendimiento.

### DA03 — Escalabilidad

**Origen:** AC03 — Escalabilidad.

**Necesidad:** permitir que el sistema pueda atender un incremento de usuarios y solicitudes.

**Decisión arquitectónica:** organizar los componentes de manera que sea posible ampliar los recursos cuando las necesidades del sistema lo requieran.

**Impacto:** facilita la evolución de la plataforma ante un crecimiento de la demanda.

**Verificación propuesta:** evaluar el comportamiento del sistema mediante pruebas con diferentes niveles de carga.

### DA04 — Seguridad y control de acceso

**Origen:** AC04 — Seguridad y RC04 — Control de acceso.

**Necesidad:** proteger la información y restringir las operaciones según los permisos de cada usuario.

**Decisión arquitectónica:** definir mecanismos de autenticación y autorización, y validar los permisos antes de ejecutar operaciones restringidas.

**Impacto:** reduce el riesgo de accesos y modificaciones no autorizados.

**Verificación propuesta:** probar que cada tipo de usuario solo pueda ejecutar las operaciones que tiene permitidas.

### DA05 — Persistencia de información

**Origen:** RC02 — Persistencia de información.

**Necesidad:** conservar los datos de usuarios, servicios turísticos, establecimientos, atractivos, eventos y rutas.

**Decisión arquitectónica:** establecer una capa de acceso a datos que centralice las operaciones de almacenamiento y recuperación.

**Impacto:** facilita la gestión consistente de la información y reduce el acoplamiento entre el negocio y la base de datos.

**Verificación propuesta:** comprobar que los datos registrados se conserven y puedan recuperarse correctamente.

### DA06 — Mantenibilidad

**Origen:** AC05 — Mantenibilidad y RC06 — Separación de responsabilidades.

**Necesidad:** permitir corregir errores y ampliar funcionalidades sin afectar innecesariamente otras partes del sistema.

**Decisión arquitectónica:** definir responsabilidades claras para cada capa y mantener sus dependencias controladas.

**Impacto:** facilita las modificaciones y la incorporación de nuevas funcionalidades.

**Verificación propuesta:** revisar la organización de los componentes y ejecutar pruebas después de realizar modificaciones.

## Resumen de drivers arquitectónicos

| ID | Driver | Origen | Influencia principal |
|---|---|---|---|
| DA01 | Organización arquitectónica | RC01 | Define la estructura en capas. |
| DA02 | Rendimiento | AC01 | Orienta la eficiencia de las consultas. |
| DA03 | Escalabilidad | AC03 | Orienta la capacidad de crecimiento. |
| DA04 | Seguridad y control de acceso | AC04, RC04 | Orienta la protección y autorización de operaciones. |
| DA05 | Persistencia de información | RC02 | Orienta el almacenamiento y la recuperación de datos. |
| DA06 | Mantenibilidad | AC05, RC06 | Orienta la separación de responsabilidades y el mantenimiento. |

## Conclusión

Los drivers arquitectónicos identificados orientan las principales decisiones de diseño del Sistema Integral de Gestión Turística de Huamanga. Su relación con los requisitos, las restricciones y los atributos de calidad permitirá justificar la arquitectura propuesta y comprobar, mediante pruebas, si responde a las necesidades del proyecto.