# TIC Solidario · Biblioteca Digital por Intranet

Proyecto de Responsabilidad Social Universitaria de la Facultad de Ingeniería de la
**Universidad del Salvador (USAL)**. 

Biblioteca digital de código abierto que funciona **sin internet**:
se instala en una PC y los usuarios entran desde el navegador por la red local.

---

## Stack

| Parte | Tecnología |
|---|---|
| Backend | Java 23 + Spring Boot |
| Frontend | Next.js + React + TypeScript |
| Base de datos | MySQL 8.0 |
| Tests | JUnit |
| Entorno de QA | Render (Docker) + Aiven (MySQL) |

## Estructura del repo

```
backend/              API en Spring Boot
frontend/             Aplicación web en Next.js
docs/                 Diagramas, diccionario de datos, propuesta funcional
docker-compose.yml    Levanta base, backend y frontend juntos
```

## Instalación

> _Pendiente: completar con el procedimiento paso a paso cuando ya hayamos instalado._

### Para desarrollar

Requisitos:
- JDK 23
- Node.js (LTS)
- Docker Desktop
- Git

Los comandos para levantar backend y frontend se completan cuando cada equipo suba el
esqueleto de su carpeta.

### Para instalar en la PC

Se instala con Docker, igual que el entorno de QA: lo que se prueba es lo mismo que se instala.

```bash
git clone https://github.com/UsalIngenieriaProyectos/BibliotecaVirtualUSAL.git
cd BibliotecaVirtualUSAL
docker compose up -d
```

## Cómo colaborar

1. **Nunca se pushea directo a `main`**, se colabora mediante Pull Request.
2. Antes de empezar una tarea, se actualiza y creá una rama:
   ```bash
   git checkout main
   git pull
   git checkout -b tipo/descripcion-corta
   ```
   Tipos: `feature/` (agregar algo nuevo), `bug/` (arreglo de bugs).
   Ej.: `feature/buscador-de-libros`, `bug/menu-en-celular`.
3. Cuando se hacen cambios en el código, se hace un *commit* con un mensaje claro de qué cambia:
   ```bash
   git commit -m "Agrega filtro por edad en el catálogo"
   ```
4. Una vez terminado, se sube la rama:
   ```bash
   git push -u origin tipo/descripcion-corta
   ```
5. Luego, se crea una *Pull Request* especificando lo aportado
5. Otro compañero revisa el PR y lo aprueba.
6. Se hace un *merge* a la rama Main. 

**IMPORTANTE:** Antes de cualquier PR, se debe probar que compile correctamente y fijarse de no subir datos sensibles.

## Base de datos de QA (Aiven)

El plan de Aiven tiene **1 GB** en total. Para no llenarlo:
- Probar con archivos chicos.
- Borrar los datos de prueba que ya no se usen.
- Las credenciales de conexión **nunca** se suben al repo: van en un `.env` local.

## Reporte de bugs

Los bugs se cargan en [Issues](../../issues/new/choose) con la plantilla **"Reporte de bug"**,
que agrega la etiqueta `bug`. Cuando el bug se corrige y se verifica en QA, se cierra el issue.

## Integrantes

### Owners actuales

| Nombre | Usuario de GitHub | Camada |
|---|---|---|
| Agustín Villalpando | [@ketazolam](https://github.com/ketazolam) | 2026 |
| Julieta Garcia | [@julgar07](https://github.com/julgar07) | 2026 |
| Lucio Palmucci | [@LucioPalmucci](https://github.com/LucioPalmucci) | 2026 |
| _completar_ | [@Roust0406](https://github.com/Roust0406) | 2026 |
| Angela Aguilar | [@Angela-Aguilar](https://github.com/Angela-Aguilar) | 2026 |

### Responsable de la facultad

**Germán Buchniv**, director de la carrera, es **owner** de la organización y administrador de
todas las herramientas del proyecto. 
**Contactar con Germán por problemas de acceso.**

### Traspaso de dueños

Antes de egresar o dejar el proyecto, se deben seguir los siguientes pasos:

1. Agregar como **owners** a los integrantes de una camada nueva.
2. Confirmar que los nuevos owners pueden entrar y administrar la organización.
3. Actualización la tabla de **Owners actuales** de este README.
4. Se revoca el acceso a los owners anteriores (excluyendo a Germán)

**El repositorio NO puede, bajo ninguna circunstancia, quedarse sin owners.**

## Contacto

- Coordinación docente: Germán Buchniv, director de la carrera
