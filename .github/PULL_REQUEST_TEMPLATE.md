<!--
  Gracias por contribuir a unFIX Organization Designer.
  Rellena lo que aplique y borra lo que no. Un PR pequeño y bien descrito se fusiona antes.
  Thanks for contributing — fill in what applies, delete what doesn't.
-->

## Descripción

<!-- Qué cambia y por qué. Dos o tres frases bastan. -->

## Issue relacionado

<!-- Closes #123 · Fixes #123 · Relates to #123 -->
Closes #

## Tipo de cambio

- [ ] 🐛 **fix** — corrige un fallo sin cambiar el comportamiento esperado
- [ ] ✨ **feat** — funcionalidad nueva
- [ ] 🧩 **catalog** — patrón, subtipo o icono nuevo en el catálogo unFIX
- [ ] 🩺 **diagnostics** — regla de diagnóstico nueva o modificada
- [ ] 🌍 **i18n** — traducciones o textos de interfaz
- [ ] 🎨 **style** — visual, tokens, CSS
- [ ] ♻️ **refactor** — reorganización sin cambio funcional
- [ ] 📝 **docs** — solo documentación
- [ ] 🔧 **chore** — mantenimiento del repositorio

## Restricciones del proyecto

> Estas cuatro son innegociables. Si alguna no se cumple, explica por qué en la descripción.

- [ ] Sigue siendo **un único `index.html`** — no he añadido ficheros `.js`, `.css` ni assets
- [ ] **Cero dependencias** de runtime — sin CDNs, sin librerías
- [ ] **Cero build** — el fichero del repo es el que se sirve, sin transpilar ni empaquetar
- [ ] Todo el código sigue dentro de la **IIFE**, sin contaminar `window`

## Calidad del código

- [ ] Sigue el estilo del código existente (2 espacios, comillas simples, `camelCase`, ES conservador)
- [ ] El código nuevo está en su **sección numerada** correspondiente
- [ ] Todo lo que viene del usuario pasa por **`esc()`** antes de llegar al DOM o al SVG
- [ ] Las mutaciones deshacibles llaman a **`pushHistory()`** antes de mutar `S`
- [ ] Los colores nuevos son **tokens de `:root`**, no hex sueltos
- [ ] **Ningún texto visible en duro** — todo pasa por `I18N` / `t()` / `T(es, en)`
- [ ] Las claves de `I18N` están completas en **`es` y `en`**

<!-- Solo si tocas el catálogo o el diagnóstico -->
- [ ] El cambio está respaldado por documentación de [unfix.com](https://unfix.com) — enlace:

<!-- Solo si tocas el formato de exportación -->
- [ ] He incrementado `version` y el importador sigue leyendo el formato anterior

## Verificación manual

> No hay tests automatizados todavía. Marca lo que hayas probado de verdad.

- [ ] Abre por `file://` y por HTTP sin errores en consola
- [ ] Arrastrar desde la paleta crea el elemento correctamente
- [ ] La contención funciona: soltar dentro reparenta, mover el contenedor arrastra el contenido
- [ ] Los tres tipos de conexión (`1` `2` `3`) se crean y dibujan bien
- [ ] Deshacer / rehacer restaura geometría **y** `parent`
- [ ] Recargar conserva el diseño (`localStorage`)
- [ ] Exportar JSON e importarlo reproduce el diseño idéntico
- [ ] Export SVG y PNG correctos
- [ ] El diagnóstico se recalcula y el badge cuadra
- [ ] Conmutar ES ↔ EN no deja texto sin traducir
- [ ] El layout móvil (< 900 px) funciona
- [ ] El tour de primera visita se completa sin desalinearse

**Navegadores probados:** <!-- p. ej. Chrome 141 (macOS), Firefox 140 (Windows) -->

## Capturas

<!--
  OBLIGATORIO si el cambio es visible. Es un editor visual: una imagen ahorra media revisión.
  Antes / después, o un GIF corto de la interacción.
-->

| Antes | Después |
|---|---|
|  |  |

## Notas para quien revise

<!-- Decisiones discutibles, alternativas descartadas, deuda que dejas a propósito. -->
