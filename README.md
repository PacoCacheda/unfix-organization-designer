# unFIX Organization Designer

> Diseñador visual de organizaciones basado en el modelo **unFIX** de Jurgen Appelo.
> Un solo archivo HTML. Sin build, sin servidor, sin dependencias.

**▶️ [Abrir la herramienta](https://pacocacheda.github.io/unfix-organization-designer/)**

*[English version](README-EN.md)*

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
