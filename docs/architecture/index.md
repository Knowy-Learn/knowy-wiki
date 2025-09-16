# Arquitectura

Esta sección explica la arquitectura del proyecto, su organización en módulos y las decisiones de diseño que la guían.  
El sistema está construido en **Java**, usando **Maven modularizado**, y sigue los principios de **Arquitectura
Hexagonal (Ports & Adapters)** junto con **Domain-Driven Design (DDD)**.

---

## Contenido

1. [Visión general](overview.md) Presenta un diagrama de alto nivel que muestra cómo se organizan los módulos
   principales (application, infrastructure, scripts) y cómo se separa el dominio de la infraestructura y los
   adaptadores.
    - [Visión general de la arquitectura](overview.md#visión-general-de-la-arquitectura)
    - [Estructura a alto nivel](overview.md#estructura-a-alto-nivel)
    - [Builds](overview.md#-builds)
    - [Modules](overview.md#-modules)
        - [Módulos de application](overview.md#módulos-de-application)
        - [Módulos de infrastructure](overview.md#módulos-de-infrastructure)
    - [Scripts](overview.md#-scripts)

---

## Resumen

El núcleo del proyecto se centra en el **dominio** (reglas de negocio puras), rodeado de adaptadores que manejan la
infraestructura (base de datos, API externas, interfaces de usuario).  
Gracias a esta separación, el dominio se mantiene independiente de frameworks y tecnologías específicas, favoreciendo la
mantenibilidad y las pruebas unitarias.