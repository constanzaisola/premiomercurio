# Premios Mercurio 2026 · Sitio web

Sitio de una sola página para la convocatoria de los Premios Mercurio 2026 de la Asociación Argentina de Marketing (AAM).

Es HTML estático: no necesita compilación ni dependencias. Las tipografías (Jost y Archivo) se cargan desde Google Fonts.

## Archivos

```
index.html                          la página completa (estilos y scripts incluidos)
assets/premios-mercurio-trofeos.webp  trofeos del hero
assets/infinita-logo-blanco.png       logo del footer
assets/favicon.svg                    ícono de la pestaña (isotipo)
assets/og-premios-mercurio.jpg        imagen para compartir en redes / WhatsApp (1200×630)
.nojekyll                           le indica a GitHub Pages que publique los archivos tal cual
```

## Publicar en GitHub Pages

1. Crear un repositorio nuevo en GitHub (por ejemplo `premios-mercurio`).
2. Subir todo el contenido de esta carpeta a la raíz del repositorio (botón **Add file → Upload files**, arrastrando los archivos y la carpeta `assets`).
3. En el repositorio ir a **Settings → Pages**, elegir **Deploy from a branch**, rama `main`, carpeta `/ (root)` y guardar.
4. En uno o dos minutos el sitio queda en `https://<usuario>.github.io/premios-mercurio/`.

### Dominio propio (opcional)

Para usar, por ejemplo, `premiomercurio.aam.com.ar`: en **Settings → Pages → Custom domain** cargar el dominio y, en el DNS de aam.com.ar, crear un registro `CNAME` de `premiomercurio` apuntando a `<usuario>.github.io`.

## Formulario

El formulario envía los datos con [FormSubmit](https://formsubmit.co) a **marketing@aam.com.ar**. Para cambiar el destino, editar esta línea en `index.html`:

```js
var DESTINO = "marketing@aam.com.ar";
```

**Importante:** el primer envío desde el sitio publicado hace que FormSubmit mande un mail de activación a esa casilla. Hay que confirmarlo una sola vez; a partir de ahí llegan todas las inscripciones. Conviene hacer un envío de prueba apenas se publique.

## Imagen para compartir

`og:image` usa una ruta relativa. Algunas redes (Facebook, LinkedIn) solo la leen con la URL completa: cuando el sitio tenga su dirección definitiva, reemplazar en `index.html`

```html
<meta property="og:image" content="assets/og-premios-mercurio.jpg">
```

por la URL absoluta, por ejemplo `https://premiomercurio.aam.com.ar/assets/og-premios-mercurio.jpg`.

---

Desarrollado por [Infinita Mkt](https://infinitamkt.com).
