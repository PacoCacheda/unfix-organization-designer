# unFIX Organization Designer

> Diseñador visual de organizaciones basado en el modelo **unFIX** de Jurgen Appelo.
> Un solo archivo HTML. Sin build, sin servidor, sin dependencias.

**▶️ [Abrir la herramienta](https://pacocacheda.github.io/unfix-organization-designer/)**

*[English version below](#english)*

---

## Qué es

Una herramienta de lienzo para dibujar cómo está —o cómo podría estar— estructurada una organización usando la biblioteca de patrones de [unFIX](https://unfix.com): Bases, Crews, Forums, Turfs, Leagues, Crowds y todo el escalado intermedio.

Arrastras patrones desde la biblioteca lateral, los anidas dentro de contenedores, los conectas entre sí y anotas misión, personas y estado de madurez de cada elemento. La herramienta valida el resultado contra las reglas estructurales del modelo y te avisa de lo que chirría.

## Características

- **Biblioteca completa de patrones unFIX** — 10 familias y 38 subtipos, cada uno con su descripción y enlace a la documentación oficial:
  - **Crew Types** (7): Value Stream, Experience, Facilitation, Capability, Platform, Governance, Partnership
  - **Base Types** (4): Fully Integrated, Strongly Aligned, Loosely Aligned, Fully Segregated
  - **Forum Types** (10): Business Model, Channel, Customer Journey, Functional, Market, Organizational, Product, Regional, Seasonal, Technological
  - **Turf Types** (4): Team of Teams, House, Product Area, Business Unit
  - **Escalado · League**: League, Clusters (7 tipos), Assembly
  - **Escalado · Crowd**: Crowd, Coalition, Congress
- **Contención real** — suelta un Crew dentro de una Base o un Turf y queda contenido en ella; al mover el contenedor se mueve todo su contenido.
- **Tres tipos de conexión** — Flujo de valor (continua), Dependencia (discontinua) y Alineación (punteada, doble flecha).
- **Estados de madurez** — Turmoil, Forming, Performing y Reforming, con codificación visual por color y bordes.
- **Diagnóstico del diseño** — revisa el lienzo contra las reglas estructurales de unFIX y resume el conteo de elementos y personas.
- **Inspector por elemento** — nombre, tipo, misión, lead, número de personas, notas y conexiones.
- **Exportación** — JSON reimportable, PNG a doble resolución y SVG vectorial editable en Figma, Illustrator o Inkscape.
- **Bilingüe** — interfaz completa en español e inglés.
- **Guardado automático** en el navegador (`localStorage`); nada sale de tu equipo.
- **Guía interactiva** para la primera vez.

## Uso

No hay nada que instalar. Tienes dos opciones:

1. **Online** — abre [pacocacheda.github.io/unfix-organization-designer](https://pacocacheda.github.io/unfix-organization-designer/).
2. **Local** — descarga `index.html` y ábrelo con doble clic en cualquier navegador moderno. Funciona sin conexión (solo las tipografías se cargan de Google Fonts; sin ellas usa las del sistema).

### Atajos de teclado

| Acción | Atajo |
|---|---|
| Zoom | `Rueda del ratón` |
| Mover el lienzo | `Arrastrar el fondo` |
| Desactivar ajuste a rejilla | `Alt` mientras arrastras |
| Tipos de conexión | `1` `2` `3` |
| Volver a seleccionar | `V` |
| Cancelar conexión | `Esc` |
| Eliminar | `Supr` |
| Deshacer / Rehacer | `Ctrl+Z` / `Ctrl+Shift+Z` |
| Duplicar | `Ctrl+D` |

## Sobre el modelo unFIX

unFIX **no es un framework**: es una biblioteca de patrones. Nada es obligatorio, el enfoque es de abajo arriba y el modelo es fractal — los mismos patrones se repiten en Base, League y Crowd.

El modelo es obra de **Jurgen Appelo** y está documentado en **[unfix.com](https://unfix.com)**. Este proyecto es una herramienta independiente, no oficial y sin afiliación con unFIX ni con su autor. Si el modelo te interesa, la fuente es la web oficial.

## Tecnología

HTML, CSS y JavaScript en un único archivo de ~2.700 líneas. Renderizado en SVG. Cero dependencias, cero build, cero backend.

## Licencia

[MIT](LICENSE) — el código de la herramienta. El modelo unFIX y su terminología pertenecen a sus respectivos autores.

---

<a name="english"></a>

# English

> Visual organization designer based on Jurgen Appelo's **unFIX** model.
> A single HTML file. No build, no server, no dependencies.

**▶️ [Open the tool](https://pacocacheda.github.io/unfix-organization-designer/)**

## What it is

A canvas tool for mapping how an organization is — or could be — structured, using the [unFIX](https://unfix.com) pattern library: Bases, Crews, Forums, Turfs, Leagues, Crowds and everything in between.

Drag patterns from the side library, nest them inside containers, connect them, and annotate each element with its mission, people and maturity state. The tool checks the result against the model's structural rules and flags what looks off.

## Features

- **Full unFIX pattern library** — 10 families and 38 subtypes, each with a description and a link to the official docs (7 Crew Types, 4 Base Types, 10 Forum Types, 4 Turf Types, plus League- and Crowd-level scaling patterns).
- **Real containment** — drop a Crew inside a Base or Turf and it belongs to it; moving the container moves its contents.
- **Three connection types** — Value flow (solid), Dependency (dashed) and Alignment (dotted, double arrow).
- **Maturity states** — Turmoil, Forming, Performing and Reforming, visually encoded.
- **Design diagnostics** — checks the canvas against unFIX structural rules and summarizes element and headcount totals.
- **Per-element inspector** — name, type, mission, lead, people, notes and connections.
- **Export** — re-importable JSON, 2× PNG and vector SVG (editable in Figma, Illustrator or Inkscape).
- **Bilingual** — full UI in Spanish and English.
- **Auto-save** to `localStorage`; nothing leaves your machine.
- **Interactive guided tour** on first run.

## Usage

Nothing to install. Either open it [online](https://pacocacheda.github.io/unfix-organization-designer/), or download `index.html` and double-click it in any modern browser. Works offline (only web fonts are remote; without them it falls back to system fonts).

## About the unFIX model

unFIX is **not a framework** — it's a pattern library. Nothing is mandatory, the approach is bottom-up, and the model is fractal: the same patterns repeat at Base, League and Crowd level.

The model is the work of **Jurgen Appelo** and is documented at **[unfix.com](https://unfix.com)**. This project is an independent, unofficial tool with no affiliation to unFIX or its author.

## License

[MIT](LICENSE) for the tool's code. The unFIX model and its terminology belong to their respective authors.
