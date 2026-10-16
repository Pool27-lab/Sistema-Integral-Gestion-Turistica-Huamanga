# Enfoque Arquitectónico

## Sistema Integral de Gestión Turística de Huamanga

### 1. Propósito

Este documento establece los criterios que orientarán el diseño y la evolución de la arquitectura del Sistema Integral de Gestión Turística de Huamanga. Estos criterios se basan en los requisitos funcionales, las restricciones, los drivers arquitectónicos y los escenarios de atributos de calidad identificados durante el análisis del sistema.

### 2. Enfoque seleccionado

Se propone un enfoque arquitectónico basado en la **separación de responsabilidades y la consideración de los atributos de calidad desde las primeras etapas del diseño**.

Este enfoque busca que los componentes tengan funciones claramente definidas y que las decisiones técnicas respondan a las necesidades del sistema, sin depender prematuramente de una tecnología específica.

### 3. Principios de diseño arquitectónico

#### 3.1. Separación de responsabilidades

Cada componente deberá cumplir una función definida. Las interfaces gestionarán la interacción con los usuarios, la lógica de negocio procesará las operaciones y los componentes de datos gestionarán el acceso a la información persistente.

#### 3.2. Seguridad desde el diseño

El sistema deberá verificar los permisos de acuerdo con el rol del usuario antes de permitir operaciones restringidas. Las funciones de administración y gestión de servicios no deberán estar disponibles para usuarios sin autorización.

#### 3.3. Rendimiento de las consultas

El diseño deberá considerar que los visitantes necesitan consultar atractivos, servicios, eventos y rutas de manera oportuna. El rendimiento se evaluará mediante los escenarios de calidad y pruebas con condiciones definidas.

#### 3.4. Preparación para el crecimiento

La organización de los componentes deberá facilitar la incorporación de nuevas funcionalidades y la atención de un posible incremento de usuarios. Las decisiones concretas para ampliar la capacidad del sistema se tomarán cuando los requisitos y las pruebas lo justifiquen.

#### 3.5. Integridad y persistencia de la información

Las operaciones sobre la información turística deberán mantener la coherencia de los datos. El diseño deberá contemplar validaciones y mecanismos apropiados para almacenar, consultar y actualizar la información.

#### 3.6. Facilidad de mantenimiento

Los componentes deberán organizarse de manera que los cambios y las correcciones puedan realizarse con el menor impacto posible sobre otras partes del sistema. También se deberá considerar la documentación y las pruebas para verificar las modificaciones.

### 4. Relación con los drivers arquitectónicos

| Driver | Criterio de diseño |
|---|---|
| DA01 — Organización de la arquitectura | Mantener las responsabilidades separadas. |
| DA02 — Rendimiento | Evaluar los tiempos de respuesta de las consultas. |
| DA03 — Escalabilidad | Facilitar futuras ampliaciones del sistema. |
| DA04 — Seguridad | Aplicar controles de acceso según los roles. |
| DA05 — Persistencia de datos | Mantener la integridad y consistencia de la información. |
| DA06 — Mantenibilidad | Organizar los componentes para facilitar las modificaciones. |

### 5. Verificación del enfoque

El cumplimiento de estos criterios deberá evaluarse durante el desarrollo:

- Mediante pruebas de rendimiento para comprobar los tiempos de respuesta.
- Mediante pruebas de autorización para verificar los permisos de cada rol.
- Mediante pruebas funcionales para comprobar las operaciones de gestión y consulta.
- Mediante pruebas de integridad para verificar la consistencia de la información.
- Mediante pruebas de regresión para identificar posibles errores después de los cambios.

Los criterios y valores medibles se tomarán de los escenarios de atributos de calidad definidos en el análisis del sistema.

### 6. Consideraciones de implementación

El enfoque arquitectónico orientará las decisiones posteriores sobre módulos, interfaces, almacenamiento y mecanismos de seguridad. La selección de tecnologías y las estrategias técnicas específicas quedan pendientes hasta que se evalúen los requisitos y las restricciones del proyecto.

### 7. Conclusión

El enfoque basado en la separación de responsabilidades y los atributos de calidad permitirá orientar el diseño del Sistema Integral de Gestión Turística de Huamanga hacia una estructura organizada, segura y mantenible. Su cumplimiento deberá comprobarse mediante la implementación y las pruebas correspondientes.
