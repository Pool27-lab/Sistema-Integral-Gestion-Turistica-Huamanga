# Arquitectura Inicial

## Sistema Integral de Gestión Turística de Huamanga

El sistema se organizará mediante una arquitectura de tres capas, separando la presentación, la lógica de negocio y el acceso a los datos.

---

# 1. Capa de Presentación

La capa de Presentación será responsable de la interacción entre los usuarios y el sistema.

### Responsabilidades

* Mostrar la información turística al visitante.
* Permitir la búsqueda y consulta de servicios turísticos.
* Permitir la consulta de atractivos, eventos y rutas.
* Proporcionar interfaces para que los prestadores turísticos gestionen sus servicios.
* Proporcionar interfaces para que el administrador gestione la información del sistema.
* Enviar las solicitudes de los usuarios hacia la capa de Lógica de Negocio.
* Mostrar al usuario las respuestas generadas por el sistema.

### Componentes principales

* Interfaz web del visitante.
* Interfaz web del prestador turístico.
* Panel de administración.
* API de acceso al sistema.

---

# 2. Capa de Lógica de Negocio

La capa de Lógica de Negocio contendrá las reglas y funcionalidades principales del sistema.

### Responsabilidades

* Gestionar usuarios y permisos.
* Gestionar establecimientos turísticos.
* Gestionar servicios turísticos.
* Gestionar atractivos turísticos.
* Gestionar eventos y festividades.
* Gestionar rutas turísticas.
* Procesar búsquedas y consultas.
* Aplicar las reglas de negocio.
* Validar la información recibida desde la capa de Presentación.
* Coordinar el acceso a la información almacenada.

### Módulos principales

* Módulo de usuarios.
* Módulo de establecimientos.
* Módulo de servicios turísticos.
* Módulo de atractivos turísticos.
* Módulo de eventos y festividades.
* Módulo de rutas turísticas.

---

# 3. Capa de Datos

La capa de Datos será responsable de almacenar y recuperar la información utilizada por el sistema.

### Responsabilidades

* Almacenar información de usuarios.
* Almacenar información de establecimientos.
* Almacenar información de servicios turísticos.
* Almacenar información de atractivos turísticos.
* Almacenar información de eventos y festividades.
* Almacenar información de rutas turísticas.
* Consultar y actualizar la información solicitada por la capa de Lógica de Negocio.

### Componentes principales

* Base de datos.
* Repositorios o componentes de acceso a datos.

---

# 4. Flujo entre las capas

La comunicación del sistema seguirá el siguiente flujo:

```text
Usuario
   │
   ▼
┌──────────────────────────────┐
│     Capa de Presentación     │
│      Web / API / Interfaz    │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│   Capa de Lógica de Negocio  │
│      Módulos y reglas        │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│        Capa de Datos         │
│       Base de Datos          │
└──────────────────────────────┘
```

La capa de Presentación no accederá directamente a la base de datos. Las solicitudes serán procesadas por la Lógica de Negocio, que será responsable de comunicarse con la capa de Datos.

---

# 5. Justificación de la arquitectura

La arquitectura en tres capas permite separar las responsabilidades principales del sistema. Esta separación facilita el mantenimiento, permite modificar una capa sin afectar innecesariamente a las demás y proporciona una estructura inicial para el crecimiento del Sistema Integral de Gestión Turística de Huamanga.

La arquitectura propuesta responde principalmente a los drivers arquitectónicos identificados durante el análisis:

* DA01 — Arquitectura en tres capas.
* DA02 — Rendimiento.
* DA03 — Escalabilidad.
* DA04 — Seguridad y control de acceso.
* DA05 — Persistencia de información.
* DA06 — Mantenibilidad.

# 6. Diagrama de Arquitectura Inicial

```mermaid
flowchart TD

    A01["A01 - Visitante"]
    A02["A02 - Prestador turístico"]
    A03["A03 - Administrador"]

    subgraph PRESENTACION["Capa de Presentación"]
        P1["Interfaz web"]
        P2["API"]
        P3["Panel de administración"]
    end

    subgraph NEGOCIO["Capa de Lógica de Negocio"]
        B1["Módulo de usuarios"]
        B2["Módulo de establecimientos"]
        B3["Módulo de servicios turísticos"]
        B4["Módulo de atractivos turísticos"]
        B5["Módulo de eventos y festividades"]
        B6["Módulo de rutas turísticas"]
    end

    subgraph DATOS["Capa de Datos"]
        D1["Repositorios"]
        D2["Base de datos"]
    end

    A01 --> P1
    A02 --> P1
    A03 --> P3

    P1 --> P2
    P3 --> P2

    P2 --> B1
    P2 --> B2
    P2 --> B3
    P2 --> B4
    P2 --> B5
    P2 --> B6

    B1 --> D1
    B2 --> D1
    B3 --> D1
    B4 --> D1
    B5 --> D1
    B6 --> D1

    D1 --> D2