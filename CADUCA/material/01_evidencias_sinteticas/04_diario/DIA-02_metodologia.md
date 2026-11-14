# DIA-01 · Diario de alimentos: protocolo y limitaciones

**Dataset totalmente sintético:** 30 alimentos registrados en 3 hogares ficticios (H01, H02, H03), vinculados a P01, P04 y P07. Periodo de compra/preparación: 30/10–10/11/2026. Corte del seguimiento: 14/11/2026. No representa a España ni a una población.

### Variables

- `hogar_id` / `participante_id`: vinculan diario, encuesta, entrevista y observación.
- `fecha_compra_o_preparacion`: no siempre compra; para una receta significa preparación.
- `tipo_fecha`: `caducidad`, `consumo_preferente`, `sin_etiqueta`, `fecha_preparacion`.
- `fecha_impresa_o_preparacion`: vacía para sin etiqueta. Una fecha de preparación **no es un límite de seguridad**.
- `fecha_resultado_o_corte`: para consumido/descartado, cuando ocurrió; para pendiente, fecha de corte.
- `estado`: consumido, descartado, pendiente. No confundir pendiente con desperdiciado.
- `motivo_reportado`: código atribuido por el narrador ficticio; no es causalidad demostrada.
- `nota_de_contexto`: comentario cualitativo.

### Sesgos e insuficiencias deliberadas

1. Solo tres hogares y una ventana breve; no extrapolar porcentajes a población general.
2. El diario puede subregistrar pequeñas cantidades, restos de comida o compras no anotadas.
3. No hay pesos, importes de compra ni categorías normalizadas: **no calcular kilos ni euros ahorrados**.
4. No existe baseline pre/post intervención ni grupo control: no inferir impacto de la app.
5. Los resultados son parcialmente censurados: hay entradas pendientes en la fecha de corte.
6. `sin_etiqueta` NO permite derivar una caducidad, y `fecha_preparacion` no equivale a fecha segura de consumo.

### Posibles métricas descriptivas (sin prescribir decisión)

- Distribución de resultados **entre los elementos resueltos** y porcentaje aún pendiente.
- Tipos de motivos reportados entre descartes.
- Discrepancia entre autopercepción de frecuencia (ENC-01) y registros específicos (DIA-01), con ventana temporal y definiciones no idénticas.
- Número de elementos sin fecha de etiqueta para evaluar viabilidad de una solución basada exclusivamente en fechas.

### Pregunta importante

¿Puede este diario demostrar cuál es la causa principal del desperdicio, o únicamente ofrecer nuevas hipótesis?
