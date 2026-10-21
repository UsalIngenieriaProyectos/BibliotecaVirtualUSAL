# TIC Solidario · Biblioteca Digital por Intranet

Proyecto de Responsabilidad Social Universitaria de la Facultad de Ingeniería de la
**Universidad del Salvador (USAL)**. Es una biblioteca digital que funciona **sin internet**:
se instala en una PC de la institución y los chicos entran desde el navegador por la red local.

El código es abierto a propósito: cualquier universidad u organización puede usarlo y replicarlo.

---

## Qué hay en este repo (y qué no)

| Va al repo | NO va al repo |
|---|---|
| Tema y plugins propios de WordPress | El núcleo de WordPress (se baja de wordpress.org) |
| Guía y scripts de instalación | La carpeta `wp-content/uploads` (libros, imágenes) |
| Documentación y decisiones del proyecto | La base de datos |
| | Contraseñas, IPs reales o cualquier credencial |

El contenido (libros, materiales) y la base de datos viven en la PC de la institución.

## Instalación

> _Pendiente: completar con el procedimiento paso a paso._

## Cómo trabajamos

1. **Nunca se pushea directo a `main`.** `main` está protegida: todo entra por Pull Request.
2. Antes de empezar una tarea, actualizá y creá una rama:
   ```bash
   git checkout main
   git pull
   git checkout -b tipo/descripcion-corta
   ```
   Tipos: `feat/` (algo nuevo), `fix/` (arreglo), `docs/` (documentación).
   Ej.: `feat/buscador-de-libros`, `fix/menu-en-celular`.
3. Commits chicos y con mensaje claro de qué cambia:
   ```bash
   git commit -m "Agrega filtro por edad en el catálogo"
   ```
4. Subí la rama y abrí un PR contra `main`:
   ```bash
   git push -u origin tipo/descripcion-corta
   ```
5. Otro compañero revisa el PR y lo aprueba. Recién ahí se mergea.
6. Después del merge, borrá la rama.

**Antes de un PR:** probalo en tu máquina y fijate de no subir contraseñas ni archivos pesados.

## Quién administra esto

### Owners actuales

| Nombre | Usuario de GitHub | Camada |
|---|---|---|
| Agustín Villalpando | [@ketazolam](https://github.com/ketazolam) | 2026 |
| _completar_ | [@julgar07](https://github.com/julgar07) | 2026 |
| Lucio _completar_ | [@LucioPalmucci](https://github.com/LucioPalmucci) | 2026 |
| _completar_ | [@Roust0406](https://github.com/Roust0406) | 2026 |
| Angela Aguilar | [@Angela-Aguilar](https://github.com/Angela-Aguilar) | 2026 |

Siempre tiene que haber **al menos 3 owners**. Nunca uno solo.

### Responsable por la facultad

**Germán Buchniv**, director de la carrera, es **owner** de esta organización y admin de
todas las herramientas del proyecto. Es el vínculo permanente con la facultad:
**si sos de una camada nueva y necesitás acceso, pedíselo a él.**

### Traspaso entre camadas

Antes de egresar o dejar el proyecto, los owners salientes:

1. Agregan como **owners** a 2 o 3 integrantes de la camada nueva.
2. Confirman que los nuevos owners pueden entrar y administrar la organización.
3. Actualizan la tabla de **Owners actuales** de este README.
4. Recién ahí se quitan ellos como owners.

**Nunca se sale un owner sin haber dejado a otro en su lugar.**

## Contacto

- Facultad de Ingeniería, USAL — _completar contacto institucional_
- Coordinación docente: Germán Buchniv, director de la carrera
