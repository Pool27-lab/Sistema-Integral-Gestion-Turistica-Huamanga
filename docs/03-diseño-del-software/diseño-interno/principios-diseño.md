# Principios de Diseño de Software

## Sistema Integral de Gestión Turística de Huamanga

### 1. Propósito

Este documento establece los principios que orientarán el diseño interno y la implementación del Sistema Integral de Gestión Turística de Huamanga. Su finalidad es promover una estructura organizada, reducir dependencias innecesarias y facilitar el mantenimiento y la evolución del software.

### 2. Principio de responsabilidad única (SRP)

Cada módulo o componente deberá tener una responsabilidad principal claramente definida.

**Aplicación en el sistema:** el módulo de servicios turísticos gestionará las operaciones relacionadas con los servicios, mientras que el módulo de usuarios y permisos se encargará de las cuentas y autorizaciones.

**Beneficio esperado:** facilitar la comprensión, las pruebas y las modificaciones de cada componente.

### 3. Bajo acoplamiento

Los componentes deberán depender lo menos posible de los detalles internos de otros componentes.

**Aplicación en el sistema:** los módulos de gestión utilizarán interfaces u operaciones definidas para acceder a los servicios de otros módulos, evitando depender de sus implementaciones internas.

**Beneficio esperado:** reducir el impacto de los cambios y facilitar la evolución del sistema.

### 4. Alta cohesión

Las operaciones relacionadas con una misma responsabilidad deberán agruparse dentro del componente correspondiente.

**Aplicación en el sistema:** las operaciones de registro, consulta y actualización de atractivos turísticos se organizarán en el módulo encargado de los atractivos.

**Beneficio esperado:** mantener una estructura comprensible y facilitar el mantenimiento.

### 5. Separación de responsabilidades

La presentación, la lógica de negocio y el acceso a datos deberán mantener funciones diferenciadas.

**Aplicación en el sistema:** las interfaces mostrarán información y recibirán solicitudes; la lógica de negocio procesará las reglas y validaciones; y los componentes de acceso a datos gestionarán la persistencia.

**Beneficio esperado:** evitar la duplicación de reglas y reducir las dependencias entre capas.

### 6. No repetir lógica innecesariamente (DRY)

Las reglas y operaciones comunes deberán reutilizarse cuando compartan realmente la misma responsabilidad.

**Aplicación en el sistema:** las validaciones comunes podrán centralizarse para evitar implementaciones diferentes de una misma regla en varios módulos.

**Beneficio esperado:** reducir inconsistencias y facilitar las actualizaciones.

**Consideración:** la reutilización no deberá crear componentes genéricos innecesarios ni combinar reglas que tengan propósitos diferentes.

### 7. Seguridad desde el diseño

Las operaciones restringidas deberán verificar la identidad y los permisos correspondientes antes de ejecutarse.

**Aplicación en el sistema:** un visitante no deberá acceder a las funciones de administración, y un prestador turístico solo deberá realizar las operaciones autorizadas para su rol.

**Beneficio esperado:** reducir el riesgo de accesos no autorizados y proteger la información gestionada por el sistema.

### 8. Validación e integridad de los datos

Los datos recibidos deberán validarse antes de ser procesados o almacenados. También deberán respetarse las reglas de integridad definidas para la información turística.

**Aplicación en el sistema:** al registrar un evento, se deberán validar los campos obligatorios y los datos correspondientes a sus fechas.

**Beneficio esperado:** reducir errores y conservar la coherencia de la información.

### 9. Simplicidad del diseño

Se deberá elegir la solución más sencilla que satisfaga los requisitos y atributos de calidad del sistema.

**Aplicación en el sistema:** no se incorporarán patrones, capas adicionales o tecnologías complejas sin una necesidad justificada.

**Beneficio esperado:** facilitar el desarrollo, la comprensión y el mantenimiento del software.

### 10. Pruebas y verificabilidad

Los componentes deberán diseñarse de manera que sus operaciones puedan verificarse mediante pruebas.

**Aplicación en el sistema:** se comprobarán las consultas turísticas, las operaciones de gestión, las validaciones y los permisos de acceso.

**Beneficio esperado:** detectar errores y comprobar que los cambios no afecten funcionalidades existentes.

### 11. Relación con los atributos de calidad

| Atributo de calidad | Principios relacionados |
|---|---|
| Mantenibilidad | Responsabilidad única, bajo acoplamiento, alta cohesión y simplicidad. |
| Seguridad | Seguridad desde el diseño y validación de permisos. |
| Rendimiento | Simplicidad y pruebas de rendimiento. |
| Escalabilidad | Bajo acoplamiento y separación de responsabilidades. |
| Integridad de datos | Validación e integridad de los datos. |

Estos principios orientan el diseño, pero su cumplimiento deberá comprobarse durante la implementación y las pruebas.

### 12. Conclusión

La aplicación de estos principios permitirá orientar el desarrollo del Sistema Integral de Gestión Turística de Huamanga hacia un software organizado, comprensible y mantenible. Su cumplimiento deberá revisarse durante el diseño, la programación y las pruebas, de acuerdo con los requisitos definidos para el proyecto.
