# Restricciones

## Sistema Integral de Gestión Turística de Huamanga

Las restricciones son condiciones que deben respetarse durante el diseño, desarrollo e implementación del sistema. Estas condiciones pueden limitar las alternativas tecnológicas y arquitectónicas disponibles.

### RC01 — Arquitectura definida

El diseño del sistema deberá respetar la arquitectura en tres capas establecida para el proyecto: presentación, lógica de negocio y acceso a datos.

### RC02 — Persistencia de información

La información que deba conservarse entre sesiones deberá almacenarse en una base de datos, de acuerdo con las necesidades del sistema.

### RC03 — Acceso mediante aplicación web

El sistema deberá ofrecer sus funcionalidades mediante una aplicación web accesible desde un navegador compatible.

### RC04 — Control de acceso

Las funciones restringidas deberán estar disponibles únicamente para los usuarios que cuenten con los permisos correspondientes.

### RC05 — Compatibilidad tecnológica

Las tecnologías seleccionadas deberán ser compatibles entre sí y permitir implementar las funcionalidades y la arquitectura definidas para el proyecto. Las tecnologías específicas deberán documentarse cuando se confirme su elección.

### RC06 — Separación de responsabilidades

La implementación deberá mantener diferenciadas las responsabilidades de presentación, lógica de negocio y acceso a datos, evitando dependencias innecesarias entre estas capas.

## Resumen de restricciones

| ID | Restricción | Impacto |
|---|---|---|
| RC01 | Arquitectura definida | Condiciona la organización general del sistema. |
| RC02 | Persistencia de información | Requiere conservar los datos necesarios mediante una base de datos. |
| RC03 | Aplicación web | Define el medio principal de acceso al sistema. |
| RC04 | Control de acceso | Limita las operaciones según los permisos de los usuarios. |
| RC05 | Compatibilidad tecnológica | Condiciona la selección y combinación de tecnologías. |
| RC06 | Separación de responsabilidades | Condiciona la organización interna de los componentes. |

## Consideración

Estas restricciones deberán validarse con el alcance real del proyecto. Si la arquitectura en tres capas o alguna tecnología todavía no ha sido aprobada como condición obligatoria, deberá documentarse como una decisión propuesta y no como una restricción definitiva.