# Guía: instalar la skill `/humanize` en Claude

Aquí tienes las 4 formas de tener disponible una skill llamada `/humanize`, pensada para quitarle a un texto el tono robótico y las muletillas típicas de un LLM:

1. **VS Code** (extensión de Claude Code)
2. **Todo el PC** (disponible en todos tus proyectos vía Claude Code)
3. **Un proyecto concreto** (solo ese repo)
4. **Claude Desktop** y **Claude Web** (claude.ai)

Está basada en la documentación oficial vigente a agosto de 2026 (`code.claude.com/docs` y `support.claude.com`).

> Un detalle de terminología: desde 2026, Anthropic fusionó los "custom commands" dentro de las skills. Un archivo en `.claude/commands/humanize.md` y una skill en `.claude/skills/humanize/SKILL.md` generan el mismo comando `/humanize` y funcionan igual. Usa el formato de skill (carpeta + `SKILL.md`): admite más funciones, como archivos de apoyo, control de quién la invoca o scripts.

---

## 0. Estructura base de una skill

Toda skill de Claude Code es una carpeta con un archivo `SKILL.md` obligatorio:

```
humanize/
└── SKILL.md
```

El `SKILL.md` tiene **frontmatter YAML** (metadatos) + **instrucciones en markdown**:

```yaml
---
name: humanize
description: Reescribe un texto para que suene natural y humano, eliminando muletillas y tono robótico típico de IA. Úsala cuando el usuario pida "humanizar", "que no suene a IA" o "que suene más natural" un texto.
---

# Humanize

Cuando se invoque esta skill, reescribe el texto proporcionado siguiendo estas reglas:

1. Elimina frases de relleno típicas de IA ("es importante destacar que...", "en resumen...", "cabe mencionar...").
2. Varía la longitud de las frases; evita ritmo monótono.
3. Sustituye vocabulario genérico por vocabulario concreto y específico del contexto.
4. Elimina listas y estructuras excesivamente ordenadas si el registro pide un tono conversacional.
5. Conserva el significado y los datos originales; no inventes información nueva.
6. Ajusta el tono al registro que pida el usuario (formal, cercano, técnico, etc.).

Al terminar, entrega el texto reescrito sin explicaciones adicionales, salvo que el usuario pida comentarios sobre los cambios.
```

Guarda este contenido como referencia: lo usarás en las 4 instalaciones de abajo (solo cambia la ruta donde lo colocas).

---

## 1. VS Code (extensión de Claude Code)

La extensión de Claude Code para VS Code **lee las mismas skills que la CLI de Claude Code** (`~/.claude/skills/` y `.claude/skills/` del proyecto). No hay un mecanismo distinto: instalar la extensión y luego seguir los pasos de "todo el PC" o "proyecto concreto" de abajo es suficiente.

Requisitos previos:
- Extensión "Claude Code" instalada desde el Marketplace de VS Code.
- Sesión iniciada con tu cuenta de Claude (Pro/Max/Team/Enterprise) o API key.

Una vez creada la skill en `~/.claude/skills/humanize/SKILL.md` (todo el PC) o en `.claude/skills/humanize/SKILL.md` (proyecto), VS Code la detecta automáticamente gracias a la **detección de cambios en vivo** (live change detection): no hace falta reiniciar VS Code si ya tenías una sesión abierta, salvo que hayas creado la carpeta `skills/` desde cero (en ese caso, reinicia el panel de Claude Code).

Para comprobar que se cargó:
- Escribe `/` en el cuadro de prompt de Claude Code dentro de VS Code y busca `humanize` en el listado.
- O pregunta directamente: `¿Qué skills tienes disponibles?`

---

## 2. Todo el PC (disponible en todos tus proyectos)

Esto crea una **skill personal**, disponible en cualquier proyecto que abras con Claude Code (terminal, VS Code o Claude Desktop en modo "Code").

### Pasos

1. Crea la carpeta en tu directorio personal:

   ```bash
   mkdir -p ~/.claude/skills/humanize
   ```

2. Crea el archivo `~/.claude/skills/humanize/SKILL.md` con el contenido de la sección 0.

3. Guarda el archivo. No hace falta reiniciar Claude Code si ya tienes una sesión abierta (detección en vivo). Si es la primera vez que creas `~/.claude/skills/`, reinicia la sesión de Claude Code una vez.

4. Verifica en cualquier proyecto:

   ```
   /humanize
   ```

   o pregúntale a Claude: `¿qué skills tienes disponibles?`

### Notas

- Ruta en Windows: normalmente `%USERPROFILE%\.claude\skills\humanize\SKILL.md` (equivalente a `~/.claude/skills/`).
- Si tienes una skill con el mismo nombre a nivel de proyecto (`.claude/skills/humanize/`) y otra a nivel personal, **gana la personal** cuando ambas coexisten a distintos niveles jerárquicos (empresa > personal > proyecto).

---

## 3. Un proyecto concreto

Esto crea una **skill de proyecto**, que solo está disponible cuando trabajas dentro de ese repositorio, y que puedes versionar con git para compartirla con tu equipo (o contigo mismo en otro PC).

### Pasos

1. Sitúate en la raíz del proyecto (por ejemplo, tu repo de ArribaIA o de Veritas):

   ```bash
   cd /ruta/a/tu/proyecto
   mkdir -p .claude/skills/humanize
   ```

2. Crea `.claude/skills/humanize/SKILL.md` con el contenido de la sección 0.

3. (Opcional pero recomendado) Añádelo a git para que viaje con el repo:

   ```bash
   git add .claude/skills/humanize/SKILL.md
   git commit -m "Añadir skill /humanize"
   ```

4. Abre Claude Code (terminal o VS Code) dentro de ese proyecto. La skill se carga automáticamente al iniciar sesión desde esa carpeta o cualquier subcarpeta.

### Notas importantes

- Las skills de proyecto también se cargan si abres Claude Code en una **subcarpeta** del repo; Claude Code busca `.claude/skills/` desde el directorio actual hasta la raíz del repo.
- Si el proyecto no es de confianza (workspace trust), Claude Code puede pedirte que aceptes el diálogo de confianza antes de que ciertos permisos de la skill (como `allowed-tools`) surtan efecto. Revisa el contenido antes de aceptar si la skill viene de otra persona.
- Si quieres que la skill funcione también en **sesiones cloud / Claude Code on the web**, al estar comprometida en `.claude/skills/` dentro del repo clonado, se carga igualmente ahí sin pasos adicionales.

---

## 4. Claude Desktop y Claude Web (claude.ai)

Aquí ya no hablamos de Claude Code, sino del chat normal de Claude: la app de escritorio y claude.ai en el navegador. Comparten cuenta y configuración de skills, así que lo que actives en uno aparece en el otro sin nada más, porque las skills viven en tu cuenta de claude.ai y no en tu disco.

### Requisito previo: activar ejecución de código

Las skills en claude.ai requieren que **"Ejecución de código y creación de archivos"** (Code execution and file creation) esté activado:

- **Free / Pro / Max:** ve a `claude.ai/settings/capabilities` y activa "Code execution and file creation".
- **Team:** viene activado por defecto a nivel de organización.
- **Enterprise:** un Owner debe activar tanto "Code execution and file creation" como "Skills" en `claude.ai/admin-settings/skills`.

### Pasos para subir la skill `/humanize`

1. Prepara la carpeta `humanize/` con su `SKILL.md` (sección 0) en tu ordenador.
2. Comprímela en un **.zip**, asegurándote de que:
   - La carpeta raíz del zip se llama `humanize` (igual que el nombre de la skill).
   - El `SKILL.md` está dentro de esa carpeta, no suelto en la raíz del zip ni dentro de una carpeta contenedora extra.
3. Abre Claude (web o app de escritorio, es indistinto) y ve a **Customize → Skills** (`claude.ai/customize/skills`).
4. Pulsa el botón **"+"** y luego **"+ Create skill"**.
5. Elige **"Upload a skill"** y selecciona tu archivo `.zip`.
6. Una vez subida, aparecerá en tu lista de skills. **Actívala con el toggle.**

A partir de aquí, la skill está disponible tanto en Claude Web como en Claude Desktop (y también en los complementos de Microsoft 365 — Excel, Word, PowerPoint, Outlook — si usas Claude ahí), sin ningún paso adicional: no hace falta "instalarla" por separado en cada superficie.

### Cómo se invoca

- Escribiendo `/humanize` en el cuadro de chat.
- O simplemente pidiendo algo como: *"humaniza este texto"* — Claude detecta la skill por su campo `description` y la aplica automáticamente si coincide con lo pedido.

### Compartir con tu equipo (Team/Enterprise, opcional)

Si en el futuro quieres compartir `/humanize` con colaboradores (por ejemplo Rubén en Veritas, o tu equipo de ArribaIA si creces):

1. Un Owner debe activar **"Skill sharing"** en `Organization settings → Skills`.
2. En `Customize → Skills`, abre la skill → **"Share"** → elige personas concretas o "toda la organización".
3. Los destinatarios la reciben en su lista, desactivada hasta que ellos mismos la activan. Las skills compartidas son de solo lectura para quien las recibe: si tú la actualizas, a ellos les llega la nueva versión automáticamente.

---

## Resumen rápido (tabla comparativa)

| Dónde | Ruta / ubicación | Alcance | Requiere |
|---|---|---|---|
| VS Code | usa las mismas rutas de abajo | según dónde la pongas | Extensión Claude Code |
| Todo el PC | `~/.claude/skills/humanize/SKILL.md` | todos tus proyectos locales | Claude Code (CLI o VS Code) |
| Un proyecto | `.claude/skills/humanize/SKILL.md` (dentro del repo) | solo ese proyecto | Claude Code (CLI o VS Code) |
| Claude Desktop | `Customize → Skills` en tu cuenta | tu cuenta, en cualquier dispositivo | Code execution activado |
| Claude Web | `Customize → Skills` en tu cuenta | tu cuenta, en cualquier dispositivo | Code execution activado |

**Nota clave:** las skills de Claude Code (PC/proyecto) y las skills de claude.ai (Desktop/Web) son **dos sistemas de almacenamiento distintos**. Si quieres `/humanize` disponible en ambos mundos, tienes que instalarla en ambos sitios (aunque el contenido del `SKILL.md` puede ser idéntico, copia-pega). No se sincronizan automáticamente salvo que uses la sincronización explícita de Claude Code (`CLAUDE_CODE_SYNC_SKILLS`), pensada para sesiones no interactivas/cloud.

---

## Solución de problemas

- **No aparece en `/`:** revisa que el frontmatter YAML no tenga errores de sintaxis (indentación, comillas). Un YAML roto hace que Claude cargue la skill sin `description`, por lo que no se activa sola (pero `/humanize` seguirá funcionando si la invocas a mano).
- **Claude no la usa automáticamente:** haz la `description` más específica y con las palabras que sueles usar tú al pedirlo ("humanizar", "que no suene a IA", "quita el tono robótico"...).
- **Error al subir el zip en claude.ai:** revisa que el nombre de la carpeta raíz del zip coincida exactamente con el nombre de la skill, y que el `SKILL.md` esté presente.
- **Aparece en gris en claude.ai:** significa que "Code execution and file creation" está desactivado a nivel de cuenta u organización.
