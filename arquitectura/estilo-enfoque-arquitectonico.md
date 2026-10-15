# Estilo Arquitectónico y Enfoque Arquitectónico

## Sistema Integral de Gestión Turística de Huamanga

### 1. Estilo arquitectónico

El sistema utilizará una **arquitectura en tres capas**, que permitirá organizar sus componentes según sus responsabilidades.

- **Capa de Presentación:** permitirá a los visitantes consultar información turística y a los prestadores y administradores utilizar las funciones correspondientes.
- **Capa de Lógica de Negocio:** procesará las operaciones del sistema, como registrar servicios, buscar atractivos turísticos y gestionar eventos.
- **Capa de Datos:** se encargará de almacenar y recuperar la información de usuarios, establecimientos, atractivos, eventos y rutas turísticas.

### 2. Enfoque arquitectónico

Se utilizará un enfoque basado en la **separación de responsabilidades y los atributos de calidad**. Se priorizarán la mantenibilidad, la seguridad, el rendimiento y la escalabilidad.

Este enfoque permitirá organizar mejor los componentes, controlar el acceso según los permisos de cada usuario y facilitar futuras mejoras del sistema.

### 3. Justificación

Se elige este estilo y enfoque porque el sistema necesita administrar diferentes tipos de información turística y ofrecer funcionalidades para visitantes, prestadores turísticos y administradores. La separación en capas facilitará el mantenimiento y la ampliación de la plataforma.

### 4. Relación con los drivers arquitectónicos

- **DA01:** define la arquitectura en tres capas.
- **DA02:** considera el rendimiento de las consultas.
- **DA03:** contempla el crecimiento de usuarios y solicitudes.
- **DA04:** establece la importancia de la seguridad y el control de acceso.
- **DA05:** define la gestión de la información almacenada.
- **DA06:** prioriza la mantenibilidad y la separación de responsabilidades.

### 5. Conclusión

La arquitectura en tres capas y el enfoque basado en la separación de responsabilidades permitirán establecer una estructura organizada para el Sistema Integral de Gestión Turística de Huamanga, facilitando su desarrollo, mantenimiento y evolución.