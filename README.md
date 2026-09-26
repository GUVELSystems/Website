# GUVEL — Smarter Industrial Systems (v4.0)

Sitio estático, sin dependencias ni proceso de compilación. Listo para GitHub Pages.

## Estructura

```
index.html            Página principal (ES/EN)
404.html              Página de error
css/styles.css        Estilos, colores de marca y modo oscuro
js/app.js             Idioma, explorador, recorrido de sistemas, efectos de desplazamiento, red hexagonal animada, mapa, calculadora OEE, formulario
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
- **Textos generales:** `js/app.js`, objeto `T` (`es` y `en`).
- **Sistemas (nombre, estado, descripción, funciones):** arreglo `SYS` en `js/app.js`.
  Para marcar un sistema como disponible cambia `rel:0` por `rel:1`; el sitio lo mueve solo a la fila de disponibles, cambia su botón a "Solicitar demo" y actualiza el mapa.
  Ajusta también la frase "Dos sistemas ya están disponibles…" (`sysP` en `T`).
- **Pantallas de ejemplo de cada sistema:** objetos `P` (textos y datos) y `R` (diseño) en `js/app.js`.
- **Flujos del ecosistema:** objeto `FL` en `js/app.js`.
- **Valores iniciales de la calculadora:** objeto `DEF` en `js/app.js`.
- **Correo de contacto:** busca `contact@guvelsystems.com` en `index.html` y `js/app.js`.
- **Colores:** variables al inicio de `css/styles.css` (`--navy`, `--ice`, `--cyan`).

## Animaciones nuevas
- **Fondo del inicio:** una red hexagonal animada detrás del titular, con paralaje al mover el mouse y pequeños pulsos de luz que viajan por sus líneas, evocando el paso de información entre sistemas.
- **Logo en "Ecosistema":** brillo pulsante continuo y anillos hexagonales que emanan del logo (efecto de transmisión de datos hacia los sistemas conectados).
Ambas se desactivan automáticamente si el visitante tiene activada la opción de reducir movimiento.
