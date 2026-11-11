# SpanishVIP Lesson Studio

Estudio de producción de lecciones de español para adultos. Cada lección parte de un PDF de contenido y termina como una presentación acabada en **Figma Slides** (1920×1080), con nivel de estudio de diseño profesional.

La especificación completa está en `docs/prompt-maestro.md`. Es la fuente de verdad: si algo de este archivo o de una skill la contradice, manda el prompt maestro.

## Estructura del repositorio

| Ruta | Contenido |
|---|---|
| `CLAUDE.md` | Reglas maestras (este archivo) |
| `docs/prompt-maestro.md` | Especificación completa de una lección |
| `.claude/skills/` | Skills del flujo de producción |
| `.claude/settings.json` | Configuración compartida del equipo |
| `.mcp.json` | Conexiones MCP del proyecto (Figma, Canva) |
| `assets/branding/` | Logos SpanishVIP (únicos archivos de marca permitidos) |
| `lessons/` | Una carpeta por lección: PDF original y resultados |

## Reglas maestras (por orden de prioridad)

1. **Fidelidad absoluta al contenido.** Todo el texto de la columna «Contenido» del PDF va en la presentación exactamente igual: mismas palabras, signos, emojis, mayúsculas, puntuación e incluso errores. No se resume, parafrasea, corrige, reordena, traduce ni añade nada. Esta regla está por encima del diseño.
2. **Una slide del PDF = una slide de la presentación.** Única libertad: dividir una slide demasiado cargada en dos o más consecutivas, repitiendo su título. Nunca juntar dos slides ni reducir el texto para que quepa.
3. **Las «Notas al diseñador» se ejecutan, no se muestran.** Las respuestas van en una slide de respuestas después del ejercicio (marcada solo con ✅) y en las notas del presentador. Las transcripciones de audio nunca van en la slide del ejercicio.
4. **Texto siempre vivo y editable.** Nunca texto dentro de imágenes generadas. Las cajas para escribir son cuadros de texto editables y vacíos.
5. **Prohibida la identidad de color de SpanishVIP.** Ni turquesa (≈ `#6CC1B9`) ni naranja coral (≈ `#FF7C42`) ni tonos parecidos. Solo los logos llevan esos colores. La paleta sale del tema de la lección y cada lección parece de una colección distinta.
6. **Logo en todas las slides**, sin deformar, recolorear ni recrear con texto:
   - `assets/branding/logo_spanishvip_blanco.png` sobre fondos oscuros o fotos oscuras.
   - `assets/branding/logo_spanishvip_color.png` sobre fondos claros.
   - Logo a color sobre pastilla blanca si el fondo es un color medio o una imagen con mucho detalle.
   - El nivel de la lección aparece en la portada.
7. **Un solo sistema por lección:** un estilo de imagen, una paleta y un sistema tipográfico. Nunca dos slides consecutivas con el mismo layout.
8. **Texto de lectura legible:** mínimo 28 px, nada por debajo de 24 px, sin efectos.
9. **Solo assets con licencia clara** y sin personajes, logos ni marcas de terceros. Cada asset se registra (slide, fuente, licencia o autor).

## Flujo de trabajo

Para producir una lección, usa la skill `crear-leccion` con la carpeta de la lección. Recorre las cuatro fases en orden y no se salta ninguna:

1. **Brief de dirección de arte** — skill `brief-direccion-arte`. Se escribe antes de diseñar y luego se cumple.
2. **Construcción** en Figma Slides — secciones 4 y 5 del prompt maestro.
3. **Control de calidad** — skill `qa-leccion`. Obligatorio antes de entregar.
4. **Portadas alternativas** — skill `portadas-alternativas`. 6 estilos × 2 paletas.

Trabaja de forma autónoma de principio a fin. Solo detente a preguntar si falta una herramienta imprescindible (Figma, generación de imágenes) o si el PDF es contradictorio y estas reglas no lo resuelven. Si una fuente de assets no está disponible, usa la siguiente y menciónalo en la entrega.

## Convenciones de `lessons/`

Cada lección vive en `lessons/<nivel>-<tema-en-kebab-case>/` (ej.: `lessons/a2-la-familia/`). Copia `lessons/_plantilla/` para empezar.

```
lessons/a2-la-familia/
├── source/            PDF original de contenido. No se modifica nunca.
└── output/
    ├── contenido.md   Texto extraído del PDF, slide por slide (Contenido / Notas)
    ├── brief.md       Brief de dirección de arte
    ├── fidelidad.md   Tabla de fidelidad PDF → Figma
    ├── assets.md      Registro de assets (slide, fuente, licencia o autor)
    ├── entrega.md     Entrega final, con el enlace al archivo de Figma
    └── capturas/      Captura de cada slide usada en el control de calidad
```

Las imágenes generadas y de stock viven en el archivo de Figma, no en el repositorio.

## Herramientas

- **Figma** (servidor MCP `figma`) es la herramienta principal. Sigue las instrucciones del propio servidor: carga la skill que exige antes de escribir en un archivo y abre una sesión por archivo.
- **Canva** (servidor MCP `canva`) es la alternativa si se trabaja allí.
- Antes de elegir fuentes, comprueba cuáles hay disponibles en Figma.
