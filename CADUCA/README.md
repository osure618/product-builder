# CADUCA · caso de ejemplo (v1.3)

Carpeta de trabajo para practicar el flujo de **idea a producción** con los plugins de este repositorio: Product Builder v0.4, Product Setup v0.2 y Product Quality v0.1. Descárgala y úsala como carpeta del proyecto: las skills leen de `material/` y escriben en `docs/`.

## Qué contiene

- `material/00_contexto/`: contexto público con fuentes reales, el brief abierto y un índice de 16 fuentes (`03_indice_fuentes.csv`).
- `material/01_evidencias_sinteticas/`: 5 entrevistas, 24 respuestas de encuesta, 3 observaciones, un diario de 30 alimentos y dos artefactos. **Todo es ficticio**: no es investigación real ni representa a consumidores reales. No generalices sus resultados.
- `docs/`: carpetas vacías de destino. Los documentos los crean las skills cuando sus entradas y aprobaciones están listas; no los rellenes a mano.

Las fuentes públicas dan contexto, pero no explican cuánto desperdicio puede evitar CADUCA ni qué parte se debe a las fechas.

## Dónde escribe cada skill

```txt
CADUCA/
├── material/                     ← fuentes del caso (solo se leen)
├── AGENTS.md                     ← paquete-construccion, cuando toque (no se entrega)
└── docs/
    ├── backlog.md                ← definir-mvp
    ├── README.md                 ← paquete-construccion (índice)
    ├── product/                  ← evidence-summary, problem, benchmark, mvp, decision-log
    ├── design/                   ← design-brief, encargo-sistema, encargo-pantallas-{ID}, README
    ├── features/                 ← {ID}-{nombre}.md, {ID}-encargo.md, {ID}-correccion-{n}.md
    ├── tech/                     ← data-model.md, entorno.md
    └── quality/                  ← test-data, {ID}-verificacion, seguridad, {ID}-informe
```

`supabase/migrations/` y `tests/` no están aquí: aparecen en el repositorio que genera Lovable, cuando se construye.

## Cómo empezar

Con Product Builder instalado, en un chat sobre esta carpeta:

> «Utiliza `analizar-evidencias` de Product Builder para analizar todas las fuentes de `material/`. Produce el resumen en BORRADOR con citas a IDs, preguntas o filas; distingue datos públicos de evidencia sintética, discrepancias y vacíos. No formules ni apruebes aún el problema, no propongas features y no ejecutes cambios externos. Indícame qué debo revisar antes de aprobar.»

El resultado se guarda en `docs/product/evidence-summary.md`.

## Reglas del caso

- Sigue el orden de Product Builder sin saltar fases. Nada pasa a aprobado sin que el PM lo diga: el framing lo aprueba el PM, y el benchmark aporta opciones antes de fijar el MVP.
- No ejecutes Product Setup ni cambios externos (Supabase, Lovable, GitHub, Vercel) hasta llegar a F00, y cada cambio con su «adelante».
- No hay MVP fijado. Los límites del brief (máximo 4 features, 1 tipo de usuario, preferiblemente 1 tabla y un flujo sencillo) son límites de tiempo del ejercicio, no necesidades demostradas de usuarios.
- Los ejemplos de interfaz de otras conversaciones son referencias, no requisitos aprobados.

## Seguridad alimentaria

La **fecha de caducidad** y la **fecha de consumo preferente** son conceptos distintos. La app no puede garantizar la seguridad de un alimento a partir de un campo introducido a mano. No sugerir consumo tras la fecha de caducidad. Los alimentos sin etiqueta y los productos abiertos no deben recibir una fecha inventada.

## Material reservado

Existe una entrevista adicional, **INT-06**, que el docente facilita **después de la primera decisión aprobada**, para practicar cómo se incorpora evidencia nueva («incorpora esta entrevista nueva»). No está en esta carpeta.
