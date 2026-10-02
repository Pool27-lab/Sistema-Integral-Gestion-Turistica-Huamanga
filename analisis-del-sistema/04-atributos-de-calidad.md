# Atributos de Calidad

## Sistema Integral de Gestión Turística de Huamanga

Los atributos de calidad representan características no funcionales que debe cumplir el sistema y que influyen directamente en las decisiones de arquitectura.

---

## AC01 — Rendimiento

El sistema deberá responder a las consultas de los usuarios en un tiempo adecuado, especialmente durante las búsquedas de servicios turísticos, atractivos, eventos y rutas.

**Consideración arquitectónica:** se deberá considerar una arquitectura que permita procesar múltiples solicitudes de manera eficiente.

---

## AC02 — Disponibilidad

El sistema deberá mantenerse disponible para los usuarios durante la mayor parte del tiempo, permitiendo consultar la información turística sin interrupciones frecuentes.

**Consideración arquitectónica:** se deberá considerar mecanismos que permitan mantener la disponibilidad del sistema ante posibles fallos.

---

## AC03 — Escalabilidad

El sistema deberá poder soportar un incremento progresivo de usuarios y solicitudes sin afectar significativamente su funcionamiento.

**Consideración arquitectónica:** la arquitectura deberá permitir aumentar los recursos del sistema conforme crezca la cantidad de usuarios.

---

## AC04 — Seguridad

El sistema deberá proteger la información de los usuarios y restringir el acceso a las funciones administrativas según los permisos correspondientes.

**Consideración arquitectónica:** se deberán considerar mecanismos de autenticación, autorización y protección de la información.

---

## AC05 — Mantenibilidad

El sistema deberá estar organizado de manera que sus componentes puedan modificarse, corregirse y ampliarse sin afectar innecesariamente otras partes del sistema.

**Consideración arquitectónica:** se deberá mantener una separación clara de responsabilidades mediante una arquitectura organizada en capas.
