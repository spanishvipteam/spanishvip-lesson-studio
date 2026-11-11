---
name: brief-direccion-arte
description: Escribe el brief de dirección de arte de una lección SpanishVIP (concepto, estilo de imagen, paleta, tipografía, motivo firma, plan por slide y biblia de estilo). Úsala antes de diseñar cualquier slide, o cuando pidan proponer o rehacer la dirección visual de una lección.
---

# Brief de dirección de arte

Requiere `output/contenido.md` de la lección. La especificación es la sección 3 de `docs/prompt-maestro.md`.

Escribe el brief en el chat y guárdalo en `output/brief.md`. Tiene siete partes:

1. **Concepto visual.** Una frase con la idea central que conecta con el tema.
2. **Estilo de imagen.** Uno solo para toda la lección, con la razón por la que sirve al tema.
3. **Paleta.** 4–6 colores en hex con su rol (dominante 60 %, secundario, acento, fondo claro, fondo oscuro, texto) y de dónde sale.
4. **Tipografía.** Fuente de títulos con personalidad propia del tema y fuente de lectura muy legible. Máximo 3 familias. Comprueba antes qué fuentes hay en Figma.
5. **Motivo firma.** Un elemento gráfico recurrente propio de esta lección.
6. **Plan por slide.** Una línea por slide con su composición.
7. **Biblia de estilo para imágenes.** Un párrafo fijo (técnica, luz, paleta, edad y tipo de personajes) que encabeza todos los prompts de imagen.

## Comprobaciones antes de darlo por bueno

- La paleta no contiene turquesa (≈ `#6CC1B9`) ni naranja coral (≈ `#FF7C42`) ni tonos parecidos, y no combina verde azulado claro con naranja como pareja dominante. Dilo explícitamente en el brief.
- La paleta y el universo visual salen del tema de esta lección, no de una lección anterior. Revisa los `brief.md` de otras carpetas de `lessons/` para no repetir estilo ni paleta.
- En el plan por slide no hay dos slides seguidas con la misma estructura, y alternan fondos claros y oscuros.
- El plan tiene una línea por cada slide del PDF, más las slides de respuestas y las divisiones previstas.
- La fuente de lectura no confunde «l»/«f», «a»/«o» ni «I»/«l».
