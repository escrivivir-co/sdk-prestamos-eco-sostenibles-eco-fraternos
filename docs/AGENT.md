# AGENT — instrucciones para el agente

> Este fichero describe cómo operar el directorio `docs/` para que
> cualquier agente pueda construir páginas nuevas sin necesidad de
> leer todo el código. Los marcadores `@@AGENT` en los HTML son pistas
> adicionales en el punto exacto de edición.

---

## Estructura

```
docs/
  .nojekyll                 ← bypass Jekyll en GitHub Pages
  style.css                 ← estilos compartidos (B&W, Courier + Caveat)
  index.html                ← página principal (showcase SDK / mods / DRY)
  AGENT.md                  ← este fichero
  sections/
    _template.html          ← plantilla para nuevas secciones
    {slug}.html             ← secciones creadas
```

**URLs:**
- Web pública: `https://escrivivir-co.github.io/sdk-prestamos-eco-sostenibles-eco-fraternos/`
- Repo (main): `https://github.com/escrivivir-co/sdk-prestamos-eco-sostenibles-eco-fraternos/blob/main/`
- Rama mod: `https://github.com/escrivivir-co/sdk-prestamos-eco-sostenibles-eco-fraternos/blob/mods/{nombre}/`

---

## Cómo crear una nueva sección

### Instrucción tipo

    nueva sección enlazada a index para "{tema}"

### Pasos

**1. Crear el fichero**

Copiar `docs/sections/_template.html` → `docs/sections/{slug}.html`
donde `{slug}` es el tema en kebab-case sin tildes (ej. `cadena-etica`, `plan-oro`, `escenarios`).

**2. Rellenar los placeholders**

| Placeholder     | Qué es                                        |
|-----------------|-----------------------------------------------|
| `{{TITULO}}`    | Título legible de la sección (con tildes)     |
| `{{SLUG}}`      | Identificador kebab-case (= nombre del .html) |
| `{{DESCRIPCION}}`| Frase corta para el `<meta description>`    |
| `{{CONTENIDO}}` | Bloque HTML entre `@@CONTENIDO-START/END`     |
| `{{GITHUB_SRC}}`| URL completa al fichero del repo fuente       |

**3. Enlazar desde `index.html`**

En `docs/index.html`, localizar el marcador:

```html
<!-- @@SECTIONS-NAV-START -->
<!-- @@SECTIONS-NAV-END -->
```

Insertar entre los dos comentarios:

```html
<li><a href="sections/{slug}.html">{titulo corto}</a></li>
```

**4. Commit**

```bash
git add docs/sections/{slug}.html docs/index.html
git commit -m "docs: sección {titulo} — {slug}.html"
git push origin main
```

---

## Cómo añadir un mod nuevo al index

En `docs/index.html`, localizar el marcador `<!-- @@MODS-END -->`.
Insertar antes de él un bloque `.mod-card` con:

```html
<div class="mod-card">
  <div class="mod-head">
    <h3>{Nombre mod} <span class="mod-branch">rama: mods/{nombre}</span></h3>
  </div>
  <div class="mod-body">
    <blockquote style="font-size:1.15rem;">{frase del lore del mod}</blockquote>
    <table>
      <tr><th>Activo</th><td>{activo}</td></tr>
      <tr><th>Proveedor</th><td>{proveedor}</td></tr>
      <tr><th>Jurisdicción</th><td>{jurisdiccion}</td></tr>
      <tr><th>Estado</th><td>{estado}</td></tr>
    </table>
    <div class="mod-links">
      <a class="src-link"
         href="https://github.com/escrivivir-co/sdk-prestamos-eco-sostenibles-eco-fraternos/tree/mods/{nombre}"
         >→ rama mods/{nombre}</a>
      <a class="src-link"
         href="https://github.com/escrivivir-co/sdk-prestamos-eco-sostenibles-eco-fraternos/blob/mods/{nombre}/mod-{nombre}/README.md"
         >→ README del mod</a>
    </div>
  </div>
</div>
```

---

## Estilos disponibles (sin tocar style.css)

| Elemento HTML / clase | Resultado visual |
|---|---|
| `<blockquote>` | Cita en Caveat (handwriting), borde izquierdo |
| `<pre>` | Bloque monoespaciado con borde |
| `<div class="inv">` | Bloque fondo negro, texto blanco |
| `<a class="src-link">` | Botón-etiqueta con borde, hover invertido |
| `<table>` | Tabla full-width con cabecera negra |
| `<div class="dry-cols">` | Grid 2 columnas para comparaciones |
| `<span class="inherited">` | Texto tenue (heredado) |
| `<span class="nuevo">` | Texto en negrita (nuevo en el mod) |
| `<span class="hand">` | Inline Caveat |
| `<hr>` | Línea punteada separadora |

---

## Convenciones de enlace al repo

- Fichero en `main`: `https://github.com/escrivivir-co/sdk-prestamos-eco-sostenibles-eco-fraternos/blob/main/{ruta}`
- Directorio en `main`: `https://github.com/escrivivir-co/sdk-prestamos-eco-sostenibles-eco-fraternos/tree/main/{dir}`
- Fichero en rama mod: `https://github.com/escrivivir-co/sdk-prestamos-eco-sostenibles-eco-fraternos/blob/mods/{nombre}/{ruta}`
- Vista de rama: `https://github.com/escrivivir-co/sdk-prestamos-eco-sostenibles-eco-fraternos/tree/mods/{nombre}`
