# Rutina Luis — Cómo instalarla en tu iPhone 11

Tienes 4 archivos en esta carpeta. Para que funcione como una app en tu iPhone 11
(con ícono en la pantalla de inicio y sin la barra de Safari), todos los
archivos deben estar en la misma carpeta en un servidor web. iOS NO permite
"Añadir a pantalla de inicio" como app desde un archivo local — necesita una URL.

Abajo tienes 3 opciones de más fácil a más técnico. La **Opción A** te deja
todo funcionando en menos de 2 minutos.

---

## OPCIÓN A — Netlify Drop (la más rápida, sin cuenta)

**Pros:** 2 minutos, sin registrarte, URL permanente, HTTPS incluido.
**Contras:** Nombre de URL aleatorio (tipo `https://divine-cactus-abc123.netlify.app`).
Si NO borras el sitio, dura indefinidamente. Si quieres hacerle cambios, toca
volver a subirlo (te da una URL nueva) a menos que crees cuenta gratis.

### Pasos:

1. Desde tu computador, abre **https://app.netlify.com/drop** en cualquier navegador.
2. Arrastra la carpeta entera `rutina-luis/` al recuadro grande de la página.
   (Alternativa: selecciona los 4 archivos — `FITNESS.html`, `icon-180.png`,
   `icon-512.png`, `manifest.json` — y arrástralos juntos).
3. Netlify te muestra una URL tipo `https://algo-aleatorio.netlify.app`.
   **Copia esa URL.**
4. Tu URL de la rutina será esa URL + `/FITNESS.html`. Por ejemplo:
   `https://divine-cactus-abc123.netlify.app/FITNESS.html`

### Instalarla en el iPhone 11:

5. **Abre Safari** en el iPhone 11. (NO funciona con Chrome en iOS para esto —
   Chrome en iOS no tiene "Añadir a pantalla de inicio" real, solo un marcador).
6. Ve a la URL de arriba.
7. Espera a que cargue completo (fuentes y todo).
8. Toca el botón **Compartir** (el cuadradito con la flecha hacia arriba, abajo al
   centro de la pantalla).
9. En el menú, baja y toca **"Añadir a pantalla de inicio"** (o "Add to Home Screen").
10. Verás el preview: ícono dorado/naranja con pesas y "Rutina Luis" como nombre.
    El nombre ya viene configurado, pero puedes editarlo si quieres.
11. Toca **"Añadir"** (arriba a la derecha).

Listo. El ícono aparece en tu pantalla de inicio. Al tocarlo, abre la rutina
**sin la barra de Safari** — se siente como una app nativa. Funciona offline
una vez cargada (iOS cachea automáticamente después de la primera visita con señal).

---

## OPCIÓN B — GitHub Pages (para control total y URL permanente)

**Pros:** URL permanente, gratis, puedes editar el HTML y se actualiza solo.
**Contras:** Requiere cuenta de GitHub y ~10 minutos de setup inicial.

### Pasos:

1. Crea cuenta en https://github.com (si no tienes).
2. Click en "New repository". Nombre: `rutina-luis`. Marca **Public**. Crea.
3. En el repo vacío, click en "uploading an existing file".
4. Arrastra los 4 archivos (`FITNESS.html`, `icon-180.png`, `icon-512.png`,
   `manifest.json`). Commit.
5. Ve a **Settings → Pages** (menú izquierdo).
6. En "Source" selecciona **Deploy from a branch** → Branch: **main** → Folder: **/ (root)** → Save.
7. Espera 1-2 min. GitHub te dará una URL tipo
   `https://tu-usuario.github.io/rutina-luis/FITNESS.html`.
8. Abre esa URL en **Safari** del iPhone y sigue los pasos 8-11 de la Opción A.

---

## OPCIÓN C — Solo local (iCloud Drive) — CON LIMITACIONES

**Pros:** 100% privado, funciona offline.
**Contras:** ⚠️ **NO permite "Añadir a pantalla de inicio" como app**.
Desde iOS solo podrás abrirlo con la app Archivos, que abrirá una vista previa
sin el modo standalone ni ícono propio. Se siente más como un PDF que como app.

Si aun así quieres hacerlo:

1. Sube los 4 archivos a iCloud Drive desde tu computador (o arrastra
   la carpeta al Finder → iCloud Drive).
2. En el iPhone, abre la app **Archivos**.
3. Ve a iCloud Drive → carpeta `rutina-luis` → toca `FITNESS.html`.
4. Se abre en una vista embebida. Puedes agregar un marcador en Safari
   Compartido, pero no tendrá ícono propio en la pantalla de inicio.

**Recomendación:** Usa la Opción A si solo quieres tenerlo listo ya.
Opción B si eres mañoso y quieres poder editarlo y que se actualice solo.

---

## Cómo se ve cuando queda instalada

- **Ícono en home screen:** dorado/naranja con dos discos de pesa y texto
  "LUIS FIT · 5D". iOS redondeará las esquinas automáticamente.
- **Al tocar el ícono:** abre directo en pantalla completa, sin barra de URL
  ni botones de Safari. Solo tu rutina.
- **Nombre debajo del ícono:** "Rutina Luis".
- **Status bar:** translúcido oscuro — se funde con el fondo de la app.
- **Navegación por días:** las pestañas LUN/MAR/MIÉ/JUE/VIE/TIPS se quedan
  fijas arriba y son más grandes en móvil (más fáciles de tocar con dedo).

## Si quieres hacer cambios después

- **Opción A (Netlify Drop)**: vuelve a netlify.com/drop, arrastra la carpeta
  actualizada. Te dará una URL nueva. Tendrás que re-instalar en el iPhone
  (borra el ícono viejo, añade de nuevo con URL nueva). Para evitar URL nueva,
  crea cuenta gratis en Netlify y haz "deploy" al mismo sitio.
- **Opción B (GitHub Pages)**: edita los archivos en GitHub, haz commit. La
  URL nunca cambia. El iPhone recarga automáticamente (a veces hay que abrir
  Safari primero para que limpie cache, luego re-abrir la app desde el ícono).

## Cambios que incluí vs. tu versión original

1. **Mapa de músculos** debajo de cada ejercicio — silueta frontal + trasera
   con los músculos trabajados resaltados en naranja (primarios) y dorado
   (secundarios), más etiquetas de texto.
2. **Optimización iOS** — meta tags PWA, safe areas para el notch, tap
   targets más grandes en móvil, modo standalone sin barra de Safari.
3. **Íconos personalizados** en dos tamaños.
4. **Manifest PWA** para Android también (si algún día lo instalas ahí).
5. Los SVGs originales de cada ejercicio **se conservaron intactos** — no
   se tocó ninguna ilustración de ejecución, solo se añadió el mapa muscular
   abajo.

## Si algo falla

- **Safari no muestra "Añadir a pantalla de inicio"**: asegúrate de estar en
  Safari real (no Chrome ni un navegador in-app de Instagram/WhatsApp).
- **El ícono se ve pixelado o genérico**: iOS a veces cachea. Elimina el
  ícono, cierra Safari completo (desliza hacia arriba y tira hacia arriba la
  tarjeta de Safari), vuelve a abrir la URL y re-añadir.
- **La página no carga offline**: la primera vez necesitas conexión. Después,
  iOS cachea. Si dejó de funcionar offline, abre la URL con conexión una vez
  para re-cachear.
