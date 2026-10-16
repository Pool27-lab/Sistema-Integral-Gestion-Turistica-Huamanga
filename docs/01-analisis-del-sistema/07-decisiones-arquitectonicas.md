# Decisiones Arquitectónicas

## Sistema Integral de Gestión Turística de Huamanga

### 1. Introducción

Este documento describe las principales decisiones arquitectónicas propuestas para el Sistema Integral de Gestión Turística de Huamanga. Su finalidad es justificar la organización del sistema y establecer criterios que orienten su diseño y futura implementación.

Las decisiones se basan en los requisitos funcionales, los atributos de calidad, las restricciones y los drivers arquitectónicos identificados durante el análisis.

### 2. DA-DEC01 — Adopción de una arquitectura en tres capas

**Contexto:** el sistema necesita ofrecer funcionalidades a visitantes, prestadores turísticos y administradores, además de gestionar información de atractivos, servicios, eventos y rutas turísticas.

**Decisión:** adoptar como propuesta inicial una arquitectura en tres capas: presentación, lógica de negocio y acceso a datos.

**Alternativa considerada:** organizar las funcionalidades sin una separación explícita de capas.

**Justificación:** la arquitectura en tres capas permite distinguir las responsabilidades de la interfaz, las reglas del negocio y el almacenamiento de información.

**Ventajas:** facilita la organización del sistema, las pruebas y el mantenimiento.

**Limitaciones:** requiere definir correctamente las responsabilidades y las dependencias entre las capas.

### 3. DA-DEC02 — Separación de responsabilidades

**Contexto:** el sistema tendrá diferentes funcionalidades y tipos de usuarios, por lo que sus componentes deberán tener responsabilidades claras.

**Decisión:** mantener separadas las responsabilidades de presentación, lógica de negocio y acceso a datos.

**Justificación:** esta organización reduce el acoplamiento innecesario y facilita realizar modificaciones.

**Consecuencia:** cada capa deberá comunicarse con las demás mediante mecanismos definidos durante el diseño.

### 4. DA-DEC03 — Control de acceso según roles

**Contexto:** los visitantes, prestadores turísticos y administradores tendrán diferentes responsabilidades y permisos.

**Decisión:** diseñar mecanismos de autenticación y autorización para restringir las operaciones que requieran permisos especiales.

**Justificación:** el sistema necesita proteger las funciones administrativas y evitar modificaciones no autorizadas.

**Consecuencia:** deberán definirse los permisos de cada tipo de usuario y comprobarse mediante pruebas de seguridad.

### 5. DA-DEC04 — Gestión centralizada de datos

**Contexto:** el sistema necesita conservar información relacionada con usuarios, servicios turísticos, establecimientos, atractivos, eventos y rutas.

**Decisión:** separar el acceso a los datos de las reglas del negocio y utilizar un mecanismo de almacenamiento persistente.

**Justificación:** facilita mantener organizada la información y evita que las reglas del negocio dependan directamente de los detalles del almacenamiento.

**Pendiente:** seleccionar el sistema gestor de base de datos después de evaluar los requisitos y las alternativas tecnológicas.

### 6. Tecnologías de implementación

Las tecnologías de frontend, backend, base de datos y alojamiento todavía no han sido seleccionadas. Su elección deberá realizarse posteriormente, considerando los requisitos funcionales, los atributos de calidad, los conocimientos disponibles y los recursos del proyecto.

### 7. Conclusión

Las decisiones propuestas establecen una base inicial para organizar el Sistema Integral de Gestión Turística de Huamanga. Deberán revisarse conforme avance el diseño y se definan los requisitos técnicos y las tecnologías de implementación.