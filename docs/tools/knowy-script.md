# Índice

1. [Operaciones, Artefactos y Perfiles](#operaciones-artefactos-y-perfiles)
    - [Operaciones](#operaciones)
    - [Artefactos](#artefactos)
    - [Perfiles](#perfiles)
2. [Ejemplos](#ejemplos)

---

# Knowy Script Usage

Este script permite gestionar los contenedores de los proyectos **knowy-devenv-compose** y **knowy-thymeleaf-compose**
usando Podman o Docker Compose.

```bash
./knowy <operación> [artifact] [profile] [opciones adicionales]
```

# Operaciones, Artefactos y Perfiles

> Para ver esta ayuda en terminal, ejecutar: `./knowy help`

## Operaciones

- **help**  
  Muestra esta ayuda.
- **clean `<artifact>`**  
  Limpia, recompila, apaga y elimina todos los contenedores del artefacto especificado, incluyendo sus volúmenes.
- **up `<artifact>` [`profile`]**  
  Inicia los contenedores del artefacto con el perfil especificado.
- **down `<artifact>` [`profile`]**  
  Apaga y elimina los contenedores del artefacto con el perfil especificado.
- **restart `<artifact>` [`profile`]**  
  Reinicia los contenedores del artefacto con el perfil especificado.

## Artefactos

- **devenv**  
  Proyecto `knowy-devenv-compose`.
- **thymeleaf**  
  Proyecto `knowy-thymeleaf-compose`.

## Perfiles

- **default**  
  Por defecto, busca y ejecuta `compose.yaml`.
- **local**  
  Ejecuta `compose-local.yaml`.

## Ejemplos

```bash
./knowy up thymeleaf
./knowy up thymeleaf local
./knowy down devenv default -v
./knowy restart devenv
```