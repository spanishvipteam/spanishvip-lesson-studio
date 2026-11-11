---
name: crear-leccion
description: Convierte el PDF de contenido de una lección SpanishVIP en una presentación terminada en Figma Slides, recorriendo las cuatro fases (brief, construcción, control de calidad, portadas alternativas). Úsala cuando pidan crear, diseñar o producir una lección, o cuando den una carpeta de `lessons/` o un PDF de lección.
---

# Crear lección

Argumento: la carpeta de la lección (ej.: `lessons/a2-la-familia`). Si solo dan un PDF, crea la carpeta copiando `lessons/_plantilla/` y guarda el PDF en `source/`.

Lee `docs/prompt-maestro.md` completo antes de empezar. Es la especificación; esta skill solo ordena el trabajo.

## 0. Preparación

1. Lee el PDF de `source/` entero, página por página.
2. Escribe `output/contenido.md`: para cada slide del PDF, su número, el texto de la columna «Contenido» copiado carácter a carácter, y aparte las «Notas al diseñador». Este archivo es la referencia para la fidelidad; no lo corrijas ni lo normalices.
3. Comprueba que el servidor MCP de Figma responde y que hay generación de imágenes. Si falta Figma, detente y dilo. Si falta una fuente de imágenes, sigue con la siguiente.
4. Crea el archivo de Figma Slides con el nombre de la lección y sube los dos logos de `assets/branding/`.

## 1. Brief de dirección de arte

Usa la skill `brief-direccion-arte`. Escríbelo en el chat y guárdalo en `output/brief.md` antes de crear la primera slide.

## 2. Construcción

Sigue las secciones 1, 2, 4 y 5 del prompt maestro. Orden recomendado:

1. Estilos del archivo: paleta y tipografías del brief.
2. Todas las slides con su texto exacto, pegado desde `output/contenido.md`, nunca reescrito de memoria.
3. Assets, uno por uno, con la biblia de estilo al inicio de cada prompt. Registra cada asset en `output/assets.md` y en las notas del presentador de su slide.
4. Slides de respuestas, transcripciones y notas del presentador.
5. Transiciones.

## 3. Control de calidad

Usa la skill `qa-leccion`. Corrige todo lo que encuentre y vuelve a revisar lo corregido.

## 4. Portadas alternativas

Usa la skill `portadas-alternativas`.

## 5. Entrega

Escribe `output/entrega.md` y el mensaje final del chat con los puntos de la sección 8 del prompt maestro, en ese orden: enlace al archivo de Figma, brief resumido, tabla de fidelidad, slides divididas y por qué, interpretación de cada nota al diseñador, fuentes usadas, registro de assets, animaciones para aplicar a mano y limitaciones reales.

Haz commit de la carpeta `output/` al terminar.
