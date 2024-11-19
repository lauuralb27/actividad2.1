# Ejercicio 1: Despliegue del Tema "Minima" en GitHub Pages

En este documento voy a explicar paso a paso cómo instalar y configurar el tema "Minima" de Jekyll en un servidor local y, después, desplegarlo en GitHub Pages. Además, he creado tres publicaciones en mi blog: una sobre el Real Madrid, otro sobre el juego Valorant y otra sobre inteligencia artificial.

## Paso 1: Preparación e instalación de Jekyll

Primero, debemos asegurarnos de tener Ruby y Bundler instalados.

1. **Instalar Ruby y Bundler**:
   - Verifico si tengo Ruby instalado ejecutando:
     ```bash
     ruby -v
     ```
   - Si ya está, paso a instalar Bundler con:
     ```bash
     gem install bundler
     ```

2. **Instalar Jekyll**:
   - Ahora instalo Jekyll ejecutando:
     ```bash
     gem install jekyll
     ```

3. **Crear un nuevo sitio de Jekyll**:
   - Para crear el sitio usando el tema "Minima", ejecuto:
     ```bash
     jekyll new nombre_del_sitio --theme minima
     ```
   - Luego entro en el directorio que acabo de crear:
     ```bash
     cd nombre_del_sitio
     ```

4. **Instalar dependencias**:
   - Finalmente, instalo todas las dependencias necesarias con:
     ```bash
     bundle install
     ```

## Paso 2: Configuración del archivo _config.yml

Aquí voy a abrir y personalizar el archivo `_config.yml` para ajustar los detalles de mi blog.

1. **Abrir el archivo _config.yml**:
   - Dentro del directorio de mi proyecto, busco el archivo `_config.yml` y lo abro en un editor de texto.

2. **Personalizar la configuración**:
   - Modifico algunos valores, como el título y la descripción. Por ejemplo:
     ```yaml
     title: "Blog sobre Real Madrid, el Valorant e Inteligencia Artificial"
     description: "El Real Madrid, el Valorant y las innovaciones en IA"
     author: "Laura"
     email: "laura.alonsoborbolla@educantabria.es"
     ```

## Paso 3: Creación de Contenido

Ahora, voy a personalizar las páginas que vienen con el tema "Minima" y crear algunas publicaciones nuevas.

1. **Personalizar páginas existentes**:
   - El tema incluye algunas páginas como `index.markdown` y `about.markdown`. Las edito para que contengan mi información.

2. **Crear una nueva página**:
   - Para añadir una nueva página, creo un archivo `pagina.md` en el directorio raíz y le añado lo siguiente:
     ```markdown
     ---
     layout: page
     title: "Nueva Página"
     permalink: /nueva-pagina/
     ---
     Contenido de la nueva página.
     ```

3. **Agregar publicaciones**:
   - En la carpeta `_posts`, creo al menos tres publicaciones. Los archivos deben tener este formato de nombre: `yyyy-mm-dd-titulo.md`. Aquí un ejemplo para mi publicación sobre el Real Madrid:
     ```markdown
     ---
     layout: post
     title: "El Real Madrid"
     date: 2024-01-01
     categories: Real Madrid
     ---
     Esta es mi publicación sobre el Real Madrid.
     ```

## Paso 4: Probar el Sitio en el Servidor Local

Por último, pruebo el sitio en mi servidor local ejecutando:

```bash
bundle exec jekyll serve
