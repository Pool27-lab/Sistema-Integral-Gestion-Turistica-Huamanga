# Patrones de Diseño

## Sistema Integral de Gestión Turística de Huamanga

### 1. Propósito

Este documento identifica los patrones de diseño que podrían utilizarse para organizar el desarrollo interno del Sistema Integral de Gestión Turística de Huamanga.

Los patrones de diseño proporcionan soluciones reutilizables para problemas habituales del diseño de software. Su aplicación deberá responder a las necesidades del sistema y no generar complejidad innecesaria.

### 2. Criterios de selección

La selección de patrones considerará los siguientes criterios:

- Reducir el acoplamiento entre los componentes.
- Facilitar el mantenimiento y las modificaciones.
- Separar las responsabilidades del sistema.
- Favorecer la reutilización de operaciones comunes.
- Mantener una estructura comprensible para el equipo de desarrollo.

Los patrones propuestos podrán revisarse cuando se definan las tecnologías y la estructura definitiva del código.

### 3. Patrones propuestos

#### 3.1. Repository (Repositorio)

**Problema que aborda:** mezclar las reglas de negocio con los detalles de almacenamiento y consulta de datos.

**Aplicación propuesta:** utilizar repositorios para centralizar el acceso a la información de usuarios, establecimientos, servicios, atractivos, eventos y rutas turísticas.

**Beneficio esperado:** separar las operaciones de negocio de los detalles de persistencia y facilitar el mantenimiento del acceso a datos.

**Consideración:** la implementación deberá evitar crear abstracciones innecesarias para operaciones que no lo requieran.

#### 3.2. Service Layer (Capa de servicios)

**Problema que aborda:** distribuir las reglas de negocio entre las interfaces, los controladores y los componentes de acceso a datos.

**Aplicación propuesta:** organizar las operaciones principales en servicios responsables de ejecutar las reglas de negocio, como registrar un servicio turístico, actualizar un atractivo o consultar eventos.

**Beneficio esperado:** centralizar las operaciones de negocio y facilitar su reutilización desde distintas interfaces.

**Consideración:** los servicios deberán mantener responsabilidades claras y evitar concentrar funcionalidades no relacionadas en un único componente.

#### 3.3. Strategy (Estrategia)

**Problema que aborda:** mantener una lógica excesivamente compleja cuando una operación necesita aplicar diferentes criterios o comportamientos.

**Aplicación potencial:** utilizar estrategias intercambiables si en el futuro se incorporan distintos métodos de búsqueda, ordenamiento o filtrado de información turística.

**Beneficio esperado:** permitir cambiar el comportamiento de una operación sin modificar innecesariamente el resto del módulo.

**Consideración:** su uso dependerá de que existan comportamientos alternativos reales. No es necesario implementarlo si las búsquedas pueden resolverse de forma sencilla.

### 4. Patrones relacionados con la arquitectura

Los patrones propuestos complementan la arquitectura en capas, pero no la reemplazan:

- **Repository:** organiza el acceso a datos.
- **Service Layer:** organiza las operaciones de negocio.
- **Strategy:** permite encapsular comportamientos alternativos cuando sea necesario.

La arquitectura define la organización general del sistema; los patrones ayudan a resolver problemas específicos dentro de esa estructura.

### 5. Relación con los atributos de calidad

| Atributo de calidad | Contribución esperada |
|---|---|
| Mantenibilidad | Separar responsabilidades y facilitar cambios localizados. |
| Escalabilidad del diseño | Facilitar la incorporación de nuevos comportamientos cuando sea necesario. |
| Seguridad | Permitir organizar las operaciones de negocio donde se aplicarán las validaciones de permisos. |
| Rendimiento | Facilitar la organización de consultas, sin garantizar por sí solo una mejora en los tiempos de respuesta. |

La aplicación de estos patrones no garantiza automáticamente los atributos de calidad. Su contribución deberá evaluarse durante la implementación y las pruebas.

### 6. Decisiones pendientes

Antes de implementar los patrones, será necesario:

- Seleccionar las tecnologías de desarrollo.
- Definir la estructura interna del código.
- Determinar qué operaciones necesitan una capa de servicios.
- Evaluar si los repositorios aportan una separación útil en la tecnología seleccionada.
- Identificar comportamientos alternativos que justifiquen el uso de Strategy.

Los patrones incluidos son propuestas iniciales, no decisiones de implementación definitivas.

### 7. Conclusión

Los patrones Repository y Service Layer se proponen para organizar el acceso a datos y las operaciones de negocio. Strategy se considera una alternativa para futuras necesidades de búsqueda o filtrado con comportamientos diferentes. Su adopción definitiva dependerá del diseño detallado y de las tecnologías seleccionadas.
