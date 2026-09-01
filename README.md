# Capitulo-0-
# Plataforma Móvil Integral para Lectores y Autores Independientes

Proyecto desarrollado como parte de la asignatura Capstone de Ingeniería en Informática.

## Descripción

Aplicación móvil Android orientada a lectores y autores independientes.

La plataforma integra tres pilares principales:

- Catalogación social de libros.
- Autopublicación de obras independientes.
- Georreferenciación de espacios físicos de lectura.

El objetivo es centralizar distintas herramientas relacionadas con la lectura dentro de una única plataforma móvil.

## Tecnologías

### Aplicación móvil
- Kotlin
- Jetpack Compose
- Android Studio

### Backend
- Java
- Spring Boot
- Maven

### Base de datos
- PostgreSQL
- Neon.tech

### Autenticación
- Firebase Authentication
- JWT

### Servicios e integraciones
- Google Books API
- Google Maps SDK
- Cloudinary

### Herramientas de desarrollo
- Git
- GitHub
- Visual Studio Code
- Postman
- Figma
- Discord

## Estructura del repositorio

```text
plataforma-lectores/
│
├── android/
│   └── Aplicación móvil Android
│
├── backend/
│   └── API REST desarrollada con Spring Boot
│
├── database/
│   └── Scripts y documentación de base de datos
│
├── docs/
│   └── Documentación del proyecto
│
└── README.md

## Flujo de trabajo con Git

El proyecto utiliza un flujo basado en GitFlow.

### Ramas principales

- `main`: contiene la versión estable del proyecto.
- `develop`: contiene los cambios integrados que todavía están en desarrollo o validación.

### Ramas temporales

Las ramas temporales se crean según la tarea:

- `feature/*`: nuevas funcionalidades.
  - Ejemplo: `feature/login`
  - Ejemplo: `feature/pantalla-inicio`

- `bug-fix/*`: corrección de errores encontrados durante el desarrollo.
  - Ejemplo: `bug-fix/error-validacion-login`

- `hotfix/*`: correcciones urgentes sobre la versión estable de `main`.
  - Ejemplo: `hotfix/error-autenticacion`

Las ramas `feature/*` y `bug-fix/*` normalmente nacen desde `develop` y vuelven a `develop`.

Las ramas `hotfix/*` nacen desde `main` y sus cambios deben quedar posteriormente reflejados también en `develop`.

## Pull Requests

Para integrar cambios se debe utilizar Pull Request.

### Funcionalidades y correcciones normales

1. Actualizar `develop`.
2. Crear una rama temporal desde `develop`.
3. Realizar los cambios.
4. Hacer commit y push.
5. Crear un Pull Request hacia `develop`.
6. Otro integrante debe revisar los cambios.
7. El Pull Request requiere al menos 1 aprobación.
8. Una vez aprobado, realizar `Squash and merge`.
9. La rama temporal se elimina automáticamente después del merge.

Ejemplo:

`feature/login` → Pull Request → `develop`

### Paso de develop a main

Cuando `develop` contenga una versión estable y probada:

1. Crear un Pull Request desde `develop` hacia `main`.
2. Otro integrante debe revisar y aprobar.
3. Realizar `Squash and merge`.

`develop` → Pull Request → `main`

No se pueden realizar cambios directamente sobre `main` o `develop`, ya que por la configuración del repositorio y buenas practicas, se realizaran pruebas de código obligatorias.

## Convención de commits

Los commits deben utilizar los siguientes prefijos:

- `feat:` → nueva funcionalidad.
- `fix:` → corrección de error.
- `docs:` → cambios de documentación.
- `test:` → creación o modificación de pruebas.
- `refactor:` → reorganización de código sin cambiar su comportamiento.
- `chore:` → configuración, mantenimiento, dependencias o archivos auxiliares.

### Ejemplos

`feat: agregar pantalla de inicio de sesión`

`fix: corregir validación del correo`

`docs: actualizar instrucciones del proyecto`

`test: agregar pruebas de autenticación`

`refactor: reorganizar servicio de usuarios`

`chore: actualizar gitignore`