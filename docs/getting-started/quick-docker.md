# Índice

1. [Requisitos](#requisitos)
2. [Pasos rápidos](#pasos-rápidos)
    - Clonar el repositorio
    - Iniciar la aplicación
    - Verificar los servicios
3. [Cerrar la aplicación](#cerrar-la-aplicación)

--- 

# ⚡ Despliegue rápido de Knowy con Docker

Si quieres **probar Knowy en tu equipo** en menos de 5 minutos, esta es la forma más rápida.

---

## Requisitos

- [Docker](https://www.docker.com/get-started) instalado
- [Docker Compose](https://docs.docker.com/compose/install/) instalado
- [Java 21](https://adoptium.net/en-GB/temurin/releases) instalado
- [Maven 3](https://maven.apache.org/download.cgi) instalado

> Solo necesitas estos dos elementos, no es necesario configurar Java, Maven ni base de datos manualmente.

---

## Pasos rápidos

1. **Clona el repositorio de Knowy**

```bash
git clone https://github.com/Knowy-Learn/knowy.git
cd knowy
```

2. **Inicia la aplicación mediante el script de Bash**

```bash
./knowy up thymeleaf
```

La versión oficial de arranque es **Thymeleaf**

3. **Verifica que los servicios estén corriendo**

```bash
docker compose ps
```

Abre tu navegador y visita:
👉 http://localhost:8080

## Cerrar la aplicación

```bash
./knowy down thymeleaf
```

> [!CAUTION]
> Este comando detiene y elimina los contenedores asociados al perfil especificado. Los datos creados durante esta
> sesión (mazos, tarjetas, progresos) no se guardarán. Esta configuración es solo para pruebas rápidas.
