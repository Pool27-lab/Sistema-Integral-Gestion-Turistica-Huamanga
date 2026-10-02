# Drivers Arquitectónicos

## Sistema Integral de Gestión Turística de Huamanga

Los drivers arquitectónicos son los requisitos, atributos de calidad y restricciones que tienen una influencia significativa en las decisiones de diseño de la arquitectura del sistema.

---

## DA01 — Arquitectura en tres capas

**Origen:** RC01 — Arquitectura en capas.

El sistema deberá organizarse en tres capas principales:

* Presentación.
* Lógica de Negocio.
* Datos.

**Decisión arquitectónica:** separar las responsabilidades del sistema en capas independientes.

**Impacto:** facilita la organización, mantenimiento y evolución del sistema.

---

## DA02 — Rendimiento

**Origen:** AC01 — Rendimiento.

El sistema deberá responder de manera eficiente ante las consultas realizadas por los usuarios.

**Decisión arquitectónica:** separar las responsabilidades mediante capas y organizar los componentes para evitar procesos innecesarios.

**Impacto:** permite mejorar el procesamiento de las solicitudes y mantener tiempos de respuesta adecuados.

---

## DA03 — Escalabilidad

**Origen:** AC03 — Escalabilidad.

El sistema deberá poder soportar un crecimiento progresivo de usuarios y solicitudes.

**Decisión arquitectónica:** diseñar componentes desacoplados y una estructura que permita ampliar los recursos del sistema.

**Impacto:** facilita el crecimiento de la plataforma sin modificar completamente su estructura.

---

## DA04 — Seguridad y control de acceso

**Origen:** AC04 — Seguridad y RC04 — Control de acceso.

El sistema deberá controlar el acceso a las funcionalidades según el tipo de usuario.

**Decisión arquitectónica:** incorporar mecanismos de autenticación y autorización en la aplicación.

**Impacto:** protege las funciones administrativas y la información gestionada por el sistema.

---

## DA05 — Persistencia de información

**Origen:** RC02 — Uso de base de datos.

El sistema deberá almacenar de manera persistente la información de usuarios, servicios turísticos, establecimientos, atractivos, eventos y rutas.

**Decisión arquitectónica:** establecer una capa de datos responsable de la comunicación con la base de datos.

**Impacto:** permite centralizar el acceso y gestión de la información persistente.

---

## DA06 — Mantenibilidad

**Origen:** AC05 — Mantenibilidad y RC06 — Separación de responsabilidades.

El sistema deberá permitir realizar modificaciones y ampliaciones sin afectar innecesariamente otros componentes.

**Decisión arquitectónica:** mantener responsabilidades separadas entre Presentación, Lógica de Negocio y Datos.

**Impacto:** facilita el mantenimiento, las modificaciones y la incorporación de nuevas funcionalidades.

---

# Resumen de Drivers Arquitectónicos

| ID   | Driver                        | Origen     | Influencia en la arquitectura                              |
| ---- | ----------------------------- | ---------- | ---------------------------------------------------------- |
| DA01 | Arquitectura en tres capas    | RC01       | Define la estructura principal del sistema.                |
| DA02 | Rendimiento                   | AC01       | Influye en la organización y procesamiento de solicitudes. |
| DA03 | Escalabilidad                 | AC03       | Influye en la capacidad de crecimiento del sistema.        |
| DA04 | Seguridad y control de acceso | AC04, RC04 | Define mecanismos de autenticación y autorización.         |
| DA05 | Persistencia de información   | RC02       | Define la responsabilidad de la capa de Datos.             |
| DA06 | Mantenibilidad                | AC05, RC06 | Influye en la separación de responsabilidades.             |
