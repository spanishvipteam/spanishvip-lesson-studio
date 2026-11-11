# SpanishVIP Lesson Studio

Repositorio de trabajo para convertir los PDF de contenido de las lecciones SpanishVIP en presentaciones terminadas en Figma Slides, con Claude Code.

## Cómo crear una lección

1. Copia `lessons/_plantilla/` a `lessons/<nivel>-<tema>/` (ej.: `lessons/a2-la-familia/`).
2. Guarda el PDF de contenido en `source/`.
3. Abre Claude Code en la raíz del repositorio y ejecuta:

   ```
   /crear-leccion lessons/a2-la-familia
   ```

La primera vez, Claude Code pedirá autorizar las conexiones de Figma y Canva definidas en `.mcp.json`.

## Qué hay en el repositorio

| Ruta | Contenido |
|---|---|
| `CLAUDE.md` | Reglas maestras que Claude sigue en todas las lecciones |
| `docs/prompt-maestro.md` | Especificación completa de una lección |
| `.claude/skills/` | Skills: `crear-leccion`, `brief-direccion-arte`, `qa-leccion`, `portadas-alternativas` |
| `.claude/settings.json` | Configuración compartida (permisos) |
| `.mcp.json` | Conexiones MCP del proyecto |
| `assets/branding/` | Logos SpanishVIP |
| `lessons/` | PDF originales y resultados de cada lección |

Para cambiar cómo se diseñan las lecciones, edita `docs/prompt-maestro.md` y refleja el cambio en `CLAUDE.md` y en la skill afectada.
