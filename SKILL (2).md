---
name: qa-leccion
description: Control de calidad de una lección SpanishVIP en Figma Slides — fidelidad del texto frente al PDF, revisión visual por capturas, paleta y variedad de layouts. Úsala antes de entregar una lección, después de cualquier cambio en las slides, o cuando pidan revisar o auditar una presentación.
---

# Control de calidad

La especificación es la sección 6 de `docs/prompt-maestro.md`. Los cuatro controles son obligatorios. Informa de lo que encuentres tal cual: una diferencia sin corregir se declara, no se oculta.

## 1. Fidelidad

1. Lee por código todo el texto de cada slide del archivo de Figma (nodos de texto, no capturas).
2. Compáralo frase a frase con `output/contenido.md` y, en caso de duda, con el PDF de `source/`.
3. Escribe `output/fidelidad.md` con la tabla: slide del PDF → slide(s) de Figma → «texto completo ✔» o la diferencia exacta.

Cuenta como diferencia: una palabra, un signo, un emoji, una mayúscula, una comilla o un espacio distintos; texto omitido; texto añadido (títulos, etiquetas, instrucciones o ejemplos que no están en el PDF); texto de las «Notas al diseñador» visible en una slide. Los errores del PDF se conservan: corregirlos también es una diferencia.

## 2. Visual

Haz una captura de cada slide, guárdala en `output/capturas/` y mírala. Comprueba:

- Texto cortado o desbordado.
- Elementos superpuestos sin querer o fuera de la slide.
- Contraste insuficiente.
- Logo presente y en la versión correcta para ese fondo.
- Imagen coherente con el texto de su slide; ninguna caja de imagen vacía.
- Ningún texto dentro de las imágenes.
- Texto de lectura de 28 px o más; nada por debajo de 24 px.

## 3. Paleta

Lee por código los rellenos y trazos del archivo. Ninguna slide usa turquesa (≈ `#6CC1B9`) ni naranja coral (≈ `#FF7C42`) ni tonos cercanos, fuera de los logos.

## 4. Variedad

Recorre la secuencia: no hay dos slides consecutivas con el mismo layout. La excepción son los pares estado inicial → estado revelado (ejercicio y sus respuestas), que comparten capas a propósito.

## Cierre

Corrige todo lo encontrado y repite solo los controles afectados sobre las slides corregidas. Actualiza `output/fidelidad.md` con el estado final.
