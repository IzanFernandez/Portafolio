# WebTA04 - Página Web Personalizada

Este es un proyecto web alojado en GitHub Pages, que presenta varias páginas HTML estáticas, recursos estáticos (como imágenes y archivos CSS/JS), y una configuración automatizada para copias de seguridad utilizando **GitHub Actions**.

## Estructura del Proyecto

La estructura de archivos de este repositorio es la siguiente:


### Descripción de los Archivos y Carpetas

- **`assets/`**:
  - Carpeta que contiene recursos estáticos como imágenes, hojas de estilo CSS y otros archivos que se utilizan en las páginas HTML.
  
- **`src/`**:
  - Contiene el archivo **`proyectos.js`**, que es un archivo de JavaScript utilizado para agregar interactividad o manejar funcionalidades dinámicas en el sitio web.
  
- **`workflows/`**:
  - Carpeta que contiene los flujos de trabajo de **GitHub Actions**.
  - **`backup.yml`**: Un archivo de configuración para hacer copias de seguridad automáticas del repositorio utilizando GitHub Actions.

- **`CNAME`**:
  - Archivo utilizado para configurar un **dominio personalizado** en GitHub Pages. Si deseas usar tu propio dominio, este archivo debe contener el nombre del dominio, como `www.misitio.com`.

- **`alberto.html`**, **`izan.html`**, **`oscar.html`**:
  - Archivos HTML que contienen contenido estático específico sobre diferentes personas o secciones en el sitio web. 
  - Estos archivos son páginas adicionales dentro del sitio web, cada uno relacionado con un tema específico (por ejemplo, "Alberto", "Izan", "Oscar").

- **`index.html`**:
  - La **página principal** del sitio web. Este archivo sirve como la entrada principal para los usuarios al acceder al dominio o repositorio. Contiene el contenido principal y el menú de navegación.

- **`googlef9cdad30c7a90d88.html`**:
  - Un archivo utilizado para **verificar** el sitio en **Google Search Console**. Este archivo se utiliza cuando deseas agregar tu sitio a la herramienta de análisis de Google para mejorar el SEO (Search Engine Optimization).

## Flujo de Trabajo de GitHub Actions

El archivo **`backup.yml`** dentro de la carpeta **`workflows/`** está configurado para realizar una copia de seguridad automática del repositorio en otro repositorio de respaldo cada vez que se realiza un **push** a la rama principal (`main`). 

### Pasos del Flujo de Trabajo:
1. **Clonación del Repositorio Original**: Se realiza un `checkout` del repositorio actual para tener los archivos más recientes.
2. **Clonación del Repositorio de Respaldo**: Se clona el repositorio de respaldo en el cual se almacenarán las copias.
3. **Copia de Archivos**: Los archivos del repositorio original se copian al repositorio de respaldo.
4. **Commit y Push**: Se realizan un `git commit` y `git push` para guardar los cambios en el repositorio de respaldo.

Este flujo de trabajo asegura que tus archivos estén siempre respaldados y actualizados automáticamente en otro repositorio.

## Configuración del Dominio Personalizado

Si deseas utilizar un **dominio personalizado** para tu página web, asegúrate de agregar tu dominio en el archivo **`CNAME`**. Solo debes incluir el nombre de dominio, por ejemplo:
