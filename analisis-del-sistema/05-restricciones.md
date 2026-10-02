# Restricciones

## Sistema Integral de Gestión Turística de Huamanga

Las restricciones representan condiciones, reglas o limitaciones que deben considerarse durante el diseño y desarrollo del sistema.

---

## RC01 — Arquitectura en capas

El sistema deberá organizarse utilizando una arquitectura de tres capas:

* Capa de Presentación.
* Capa de Lógica de Negocio.
* Capa de Datos.

Esta organización permitirá separar las responsabilidades principales del sistema.

---

## RC02 — Uso de base de datos

La información del sistema deberá almacenarse en una base de datos, incluyendo usuarios, servicios turísticos, establecimientos, atractivos, eventos y rutas.

---

## RC03 — Acceso mediante aplicación web

El sistema deberá estar disponible mediante una aplicación web que permita a los usuarios acceder a las funcionalidades desde un navegador.

---

## RC04 — Control de acceso

Las funciones de administración deberán estar restringidas a usuarios con los permisos correspondientes.

---

## RC05 — Tecnologías de desarrollo

La implementación deberá utilizar tecnologías compatibles con el desarrollo de aplicaciones web y con la arquitectura definida para el proyecto.

---

## RC06 — Separación de responsabilidades

Los componentes del sistema deberán mantener responsabilidades claramente separadas para facilitar el mantenimiento y evolución de la solución.

---

## Resumen de restricciones

| ID   | Restricción                     | Impacto                                                 |
| ---- | ------------------------------- | ------------------------------------------------------- |
| RC01 | Arquitectura en capas           | Define la organización estructural del sistema.         |
| RC02 | Uso de base de datos            | Condiciona la gestión y persistencia de información.    |
| RC03 | Aplicación web                  | Define el medio principal de acceso al sistema.         |
| RC04 | Control de acceso               | Condiciona el acceso a funciones administrativas.       |
| RC05 | Tecnologías de desarrollo       | Limita las alternativas tecnológicas de implementación. |
| RC06 | Separación de responsabilidades | Condiciona la organización de los componentes.          |
