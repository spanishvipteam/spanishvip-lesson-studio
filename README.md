# Lecciones

Una carpeta por lección, con el nombre `<nivel>-<tema-en-kebab-case>` (ej.: `a2-la-familia`, `b1-el-cine`).

```
<nivel>-<tema>/
├── source/            PDF original de contenido. No se modifica nunca.
└── output/
    ├── contenido.md   Texto extraído del PDF, slide por slide
    ├── brief.md       Brief de dirección de arte
    ├── fidelidad.md   Tabla de fidelidad PDF → Figma
    ├── assets.md      Registro de assets
    ├── entrega.md     Entrega final, con el enlace al archivo de Figma
    └── capturas/      Captura de cada slide
```

Para empezar una lección, copia `_plantilla/` y guarda el PDF en `source/`.
