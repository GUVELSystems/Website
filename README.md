# GUVEL — Smarter Industrial Systems (v2.0)

Sitio estático, sin dependencias ni proceso de compilación. Listo para GitHub Pages.

## Estructura

```
index.html            Página principal (ES/EN)
404.html              Página de error
css/styles.css        Estilos, colores de marca y modo oscuro
js/app.js             Idioma, demo por turnos, sección "El reto", ventanas de detalle, menú móvil
assets/
  guvel-mark.svg      Favicon (G sobre navy)
  guvel-g-light.svg   G para fondos claros
  guvel-g-dark.svg    G para fondos oscuros
  guvel-logo.png      Logo original
  favicon-32.png, apple-touch-icon.png, icon-512.png
  og-image.png        Imagen al compartir el enlace (1200×630)
.nojekyll             Evita que GitHub procese el sitio con Jekyll
robots.txt
```

## Publicar

### Si ya tienes el repositorio de GitHub Pages
1. Abre el repositorio y borra los archivos anteriores (`index.html`, `css/`, `js/`, `assets/`).
2. **Add file → Upload files** y arrastra *el contenido* de esta carpeta (no la carpeta completa).
   El archivo `.nojekyll` está oculto en algunos sistemas; si no aparece, créalo vacío con **Add file → Create new file**.
3. Escribe un mensaje como `Sitio v2.0` y haz **Commit changes**.
4. En 1–2 minutos el sitio se actualiza en la misma dirección.

### Si es un repositorio nuevo
1. Crea un repositorio público, por ejemplo `guvel-website`.
2. Sube el contenido como en el paso 2 de arriba.
3. **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)` y **Save**.
4. La dirección aparecerá en esa misma pantalla: `https://TU-USUARIO.github.io/guvel-website/`.

### Con Git desde la terminal
```bash
git clone https://github.com/TU-USUARIO/TU-REPO.git
cd TU-REPO
# copia aquí el contenido de esta carpeta
git add -A
git commit -m "Sitio GUVEL v2.0"
git push
```

## Dominio propio (opcional)
Para usar p. ej. `www.guvelsystems.com`:
1. Crea un archivo `CNAME` en la raíz con una sola línea: `www.guvelsystems.com`.
2. En tu proveedor de dominio agrega un registro **CNAME** `www` → `TU-USUARIO.github.io`.
3. En **Settings → Pages** escribe el dominio y activa **Enforce HTTPS**.

Con dominio propio, cambia en `index.html` la etiqueta `og:image` a la URL completa
(`https://www.guvelsystems.com/assets/og-image.png`) para que la vista previa funcione en WhatsApp y LinkedIn.

## Editar contenido
- **Textos:** están en `js/app.js`, objeto `T` (`es` y `en`). Las fichas de cada solución están en el objeto `S`.
- **Correo de contacto:** busca `mailto:contact@guvelsystems.com` en `index.html`.
- **Colores:** variables al inicio de `css/styles.css` (`--navy`, `--ice`, `--cyan`).
- **Datos de la demo:** arreglo `shifts` en `js/app.js`.
