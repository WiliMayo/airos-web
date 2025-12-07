# 🤖 AIROS ESPOL - Sitio Web Oficial

Este repositorio contiene el código fuente del sitio web oficial de **AIROS (Artificial Intelligence and Robotics Society)** de la ESPOL.

El sitio funciona como un portafolio vivo para mostrar nuestros proyectos de robótica, publicaciones científicas (Papers), eventos y presentar a nuestro equipo directivo y miembros.

🔗 **URL del sitio:** [https://wilimayo.github.io/airos-web/](https://wilimayo.github.io/airos-web/)

---

## 🛠 Tecnología

El sitio está construido sobre **Jekyll**, un generador de sitios estáticos, y alojado gratuitamente en **GitHub Pages**.

* **Framework:** Jekyll
* **Estilos:** Bootstrap (Tema base: Agency) + CSS Personalizado
* **Iconos:** FontAwesome 6 (vía CDN)
* **Fuentes:** Google Fonts (Bebas Neue, Michroma, Montserrat, Rajdhani)

---

## 📂 Estructura del Proyecto

A diferencia de una página HTML normal, este sitio es modular. Aquí se explica dónde editar cada cosa:

### 1. Información Dinámica (Carpeta `_data/`)
Para facilitar el mantenimiento, la información repetitiva se encuentra en archivos YAML. **Edita estos archivos para actualizar contenido sin tocar código HTML.**

* `members.yml`: Base de datos de la Directiva y Miembros del club.
* `papers.yml`: Lista de publicaciones científicas y papers aceptados.
* `template.yml`: Configuración de colores y fuentes globales.

### 2. Proyectos y Noticias (Carpeta `_posts/`)
Cada robot, taller o evento es un archivo individual en esta carpeta.
* **Formato de nombre:** `AÑO-MES-DIA-titulo.md` (Ej: `2025-10-17-f1tenth.md`).
* **Requisito:** Cada post debe tener un `modal-id` único en su encabezado para que la ventana emergente funcione correctamente.

### 3. Secciones de la Página (Carpeta `_includes/`)
Aquí están los bloques de HTML que componen la página principal (`index.html`).
* `header.html`: La portada con el logo gigante.
* `papers.html`: La sección de publicaciones científicas.
* `services.html`: La sección de Departamentos (Humanoides, Navegación, etc.).
* `join.html`: La sección de "Únete" con pasos para aspirantes.
* `team.html`: El diseño de la rejilla de miembros.

### 4. Estilos (Archivo `style.css`)
Contiene todas las personalizaciones visuales del club (gradientes azules, ajustes de logos, fuentes futuristas) que sobrescriben al tema original.

---

## 🚀 Guía para Colaboradores

### ¿Cómo agregar un nuevo miembro?
1.  Sube su foto (JPG cuadrada) a `img/team/`.
2.  Abre `_data/members.yml`.
3.  Copia el bloque de un miembro existente y reemplaza los datos.

### ¿Cómo publicar un nuevo proyecto?
1.  Crea un archivo `.md` en `_posts/`.
2.  Usa la plantilla estándar (ver archivos existentes).
3.  Asegúrate de subir las imágenes (normal y thumbnail) a `img/portfolio/`.

### Ejecutar localmente
Si tienes Ruby y Jekyll instalados:

```bash
bundle install
bundle exec jekyll serve
```

Accede a http://localhost:4000.