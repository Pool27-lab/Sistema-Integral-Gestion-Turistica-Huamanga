# Estilo Arquitectónico

## Sistema Integral de Gestión Turística de Huamanga

### 1. Propósito

Este documento identifica el estilo arquitectónico propuesto para el Sistema Integral de Gestión Turística de Huamanga y justifica su elección según las necesidades identificadas durante el análisis del sistema.

### 2. Estilo arquitectónico seleccionado

Se propone utilizar el **estilo arquitectónico en capas**, organizado en tres capas principales:

- **Presentación:** gestiona la interacción con los usuarios y muestra la información del sistema.
- **Lógica de negocio:** procesa las operaciones, aplica las reglas del sistema y valida los permisos correspondientes.
- **Acceso a datos:** gestiona las operaciones de consulta y modificación de la información persistente.

Cada capa tendrá responsabilidades específicas y colaborará con las demás para atender las funcionalidades del sistema.

### 3. Justificación de la elección

Se propone este estilo porque el sistema debe atender diferentes tipos de usuarios y gestionar información relacionada con atractivos, establecimientos, servicios, eventos y rutas turísticas.

La separación en capas permitirá:

- **Organización:** distribuir las responsabilidades de manera clara.
- **Mantenibilidad:** facilitar la corrección de errores y la modificación de funcionalidades.
- **Seguridad:** centralizar las validaciones y el control de permisos en la lógica de negocio.
- **Evolución:** incorporar nuevas funcionalidades procurando reducir el impacto sobre los componentes existentes.
- **Gestión de datos:** separar las operaciones del sistema de los mecanismos utilizados para almacenar la información.

Estos beneficios dependerán de que la arquitectura se implemente respetando las responsabilidades y relaciones definidas.

### 4. Relación con los drivers arquitectónicos

El estilo seleccionado se relaciona con los siguientes drivers:

| Driver | Relación con el estilo arquitectónico |
|---|---|
| DA01 — Organización de la arquitectura | Define la separación de responsabilidades en tres capas. |
| DA02 — Rendimiento | Orienta la evaluación de los tiempos de respuesta de las consultas. |
| DA03 — Escalabilidad | Proporciona una estructura organizada para futuras ampliaciones. |
| DA04 — Seguridad | Favorece la centralización de las validaciones y los permisos. |
| DA05 — Persistencia de datos | Separa la lógica de negocio del acceso a la información almacenada. |
| DA06 — Mantenibilidad | Facilita la organización y modificación de los componentes. |

La adopción de este estilo no garantiza por sí sola el cumplimiento de los atributos de calidad. Estos deberán verificarse mediante los escenarios y las pruebas correspondientes.

### 5. Consideraciones

El estilo en capas constituye una decisión arquitectónica inicial. No se ha seleccionado todavía un lenguaje de programación, un framework, un gestor de base de datos ni una tecnología específica para la comunicación entre capas.

Estas decisiones se definirán posteriormente, considerando los requisitos del sistema, las restricciones identificadas y los recursos disponibles para el proyecto.

### 6. Conclusión

El estilo arquitectónico en capas se propone como base para organizar el Sistema Integral de Gestión Turística de Huamanga. Su principal aporte será separar las responsabilidades del sistema y proporcionar una estructura clara para su desarrollo, mantenimiento y evolución.
