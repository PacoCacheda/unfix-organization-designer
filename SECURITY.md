# Política de seguridad

*[English version below](#security-policy)*

## Modelo de seguridad del proyecto

Antes de reportar, conviene entender la superficie de ataque real de esta herramienta:

| Aspecto | Situación |
|---|---|
| **Backend** | No existe. No hay servidor, API, base de datos ni cuentas. |
| **Datos del usuario** | Nunca salen del navegador. Se guardan en `localStorage` (`unfix-designer-v1`, `unfix-tour-v1`). |
| **Dependencias de terceros** | Ninguna en tiempo de ejecución. La única petición externa es a Google Fonts, y es opcional. |
| **Autenticación** | No aplica. |
| **Distribución** | `index.html` servido como estático desde GitHub Pages. |

Esto significa que la mayoría de las clases de vulnerabilidad habituales —inyección SQL, SSRF, escalada de privilegios, fuga de secretos— **no aplican**. Lo que sí aplica está abajo.

## Vectores relevantes

Nos interesan especialmente los reportes sobre:

1. **XSS almacenado vía importación de JSON.** El importador acepta ficheros arbitrarios y sus campos (`name`, `mission`, `notes`, `lead`, `title`, `label`) se pintan en la interfaz. Toda ruta que llegue al DOM o al SVG debe pasar por `esc()`. Si encuentras una que no lo hace, es un fallo de seguridad válido.
2. **Inyección en la exportación SVG/PNG.** Contenido del usuario que acabe en el SVG independiente sin escapar.
3. **Prototype pollution** al parsear el JSON importado.
4. **Denegación de servicio del navegador** — un fichero importado que congele o cuelgue la pestaña de forma trivial.
5. **Filtración de datos** — cualquier ruta por la que el contenido del lienzo salga del equipo del usuario. Esto sería un fallo grave: el proyecto se compromete a que nada salga.

### Fuera de alcance

- Ausencia de cabeceras de seguridad al abrir por `file://`.
- Que `localStorage` sea legible por otro script en el mismo origen si el usuario ya está comprometido.
- Vulnerabilidades del propio navegador o del sistema operativo.
- Ausencia de cifrado en reposo del diseño local.
- Configuración de GitHub Pages ajena a este repositorio.
- Resultados brutos de escáneres automáticos sin un impacto demostrado.

## Versiones soportadas

| Versión | Soporte |
|---|:---:|
| `main` (lo que sirve GitHub Pages) | ✅ |
| Copias locales de `index.html` anteriores | ❌ — descarga la versión actual |

Al ser un archivo único sin versionado de releases, **la versión soportada es siempre la última de `main`**. Si usas una copia local antigua, actualízala antes de reportar.

## Cómo reportar una vulnerabilidad

**No abras un issue público** para un fallo de seguridad.

Vía preferente — **GitHub Security Advisories**:
[Reportar de forma privada](https://github.com/PacoCacheda/unfix-organization-designer/security/advisories/new)

Vía alternativa — correo a **francisco.lopez.cacheda@gmail.com** con el asunto `[SECURITY] unfix-organization-designer`.

### Qué incluir

- Tipo de vulnerabilidad y componente afectado (idealmente, la sección numerada del script).
- Pasos de reproducción, con un fichero JSON de prueba si aplica.
- Impacto: qué consigue un atacante realmente.
- Navegador y versión.
- Si tienes propuesta de parche, adelante — se agradece.

### Qué esperar

| Momento | Compromiso |
|---|---|
| **72 horas** | Acuse de recibo. |
| **7 días** | Evaluación inicial: confirmado, no aplica o necesita más información. |
| **30 días** | Corrección publicada en `main` para fallos confirmados, o un plan con fechas si es más complejo. |

Este es un proyecto mantenido por una sola persona en su tiempo libre. Los plazos son un compromiso de buena fe, no un SLA contractual.

### Divulgación

Se pide **divulgación coordinada**: dame margen para publicar la corrección antes de hacerlo público. Cuando se publique el arreglo, se te acreditará en el aviso salvo que prefieras el anonimato.

No hay programa de recompensas. Sí hay agradecimiento sincero y crédito público.

---

# Security Policy

## Project security model

Before reporting, it helps to understand this tool's actual attack surface:

| Aspect | Status |
|---|---|
| **Backend** | None. No server, API, database or accounts. |
| **User data** | Never leaves the browser. Stored in `localStorage` (`unfix-designer-v1`, `unfix-tour-v1`). |
| **Third-party dependencies** | None at runtime. The only external request is to Google Fonts, and it is optional. |
| **Authentication** | Not applicable. |
| **Distribution** | `index.html` served as a static file from GitHub Pages. |

This means most common vulnerability classes — SQL injection, SSRF, privilege escalation, secret leakage — **do not apply**. What does apply is below.

## Relevant vectors

We are especially interested in reports covering:

1. **Stored XSS via JSON import.** The importer accepts arbitrary files and their fields (`name`, `mission`, `notes`, `lead`, `title`, `label`) are painted into the UI. Every path reaching the DOM or the SVG must go through `esc()`. If you find one that doesn't, that is a valid security bug.
2. **Injection into the SVG/PNG export.** User content ending up unescaped in the standalone SVG.
3. **Prototype pollution** when parsing imported JSON.
4. **Browser denial of service** — an imported file that trivially freezes or hangs the tab.
5. **Data exfiltration** — any path by which canvas content leaves the user's machine. This would be severe: the project's promise is that nothing leaves.

### Out of scope

- Missing security headers when opening over `file://`.
- `localStorage` being readable by another script on the same origin if the user is already compromised.
- Browser or operating system vulnerabilities.
- Lack of at-rest encryption for the local design.
- GitHub Pages configuration outside this repository.
- Raw automated scanner output with no demonstrated impact.

## Supported versions

| Version | Supported |
|---|:---:|
| `main` (what GitHub Pages serves) | ✅ |
| Older local copies of `index.html` | ❌ — download the current version |

Being a single file with no release versioning, **the supported version is always the latest on `main`**. If you are running an old local copy, update it before reporting.

## Reporting a vulnerability

**Do not open a public issue** for a security flaw.

Preferred — **GitHub Security Advisories**:
[Report privately](https://github.com/PacoCacheda/unfix-organization-designer/security/advisories/new)

Alternative — email **francisco.lopez.cacheda@gmail.com** with subject `[SECURITY] unfix-organization-designer`.

### What to include

- Vulnerability type and affected component (ideally the numbered script section).
- Reproduction steps, with a proof-of-concept JSON file where applicable.
- Impact: what an attacker actually achieves.
- Browser and version.
- A proposed patch, if you have one — very welcome.

### What to expect

| Timeframe | Commitment |
|---|---|
| **72 hours** | Acknowledgement of receipt. |
| **7 days** | Initial assessment: confirmed, not applicable, or more info needed. |
| **30 days** | Fix published on `main` for confirmed issues, or a dated plan if more complex. |

This is a single-maintainer project run in spare time. These timelines are a good-faith commitment, not a contractual SLA.

### Disclosure

**Coordinated disclosure** is requested: give me room to ship the fix before going public. When the fix lands you will be credited in the advisory unless you prefer to remain anonymous.

There is no bounty program. There is sincere gratitude and public credit.
