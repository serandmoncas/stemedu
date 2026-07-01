# Piloto — definición y presupuesto

> Decisiones tomadas el 2026-06-30 (post-llamada) para cerrar las preguntas abiertas de [[PLAN-DE-ACCION]]. Este documento fija el piloto concreto a ejecutar y su presupuesto. Los números marcados como **SUPUESTO** son estimaciones basadas en la llamada, no cotizaciones reales — hay que reemplazarlos antes de comprometerse con nadie (ver checklist al final).

## Qué se decidió

| Decisión | Resultado |
|---|---|
| Proyecto piloto | Lámpara / matriz de LEDs controlada por ESP32 |
| Público | Círculo cercano, sin segmentar todavía (validación de interés, no de nicho) |
| Formato | 8 horas totales: 2 virtuales (async, pregrabadas) + 6 presenciales |
| Espacio | Alquilado (no casa/oficina propia) |
| Objetivo de precio | Simbólico — cubrir costos duros, no generar margen ni pagarle a los instructores en esta ronda |
| Tamaño del grupo | 8-10 personas |

Esto resuelve 4 de las 6 preguntas abiertas que quedaron en [[PLAN-DE-ACCION]] (proyecto, público, espacio, precio). Quedan pendientes: nombre del taller y si se ofrece en un solo plan o en niveles — no hacen falta para presupuestar el piloto.

## Lista de materiales por kit (1 persona)

Basado en los precios que Sergio mencionó en la llamada para este proyecto específico:

| Componente | Costo estimado (COP) | Notas |
|---|---|---|
| ESP32 (dev board) | 40.000 | Precio citado en la llamada |
| Matriz de LEDs direccionables (5x5, tipo WS2812B) | 30.000 | 2 unidades a ~15.000 c/u, para que la lámpara tenga volumen |
| Regulador de voltaje | 20.000 | Citado en la llamada |
| Cables, protoboard/perfboard, estaño, resistencias | 15.000 | **SUPUESTO** — no se cotizó en la llamada |
| Carcasa/difusor (impresión 3D o material simple) | 15.000 | **SUPUESTO** — puede bajar si se usa material reciclado para el piloto |
| Cable USB / fuente de alimentación | 10.000 | **SUPUESTO** |
| **Total por kit** | **130.000** | Sergio mencionó "menos de 100.000-200.000" para este tipo de proyecto — este desglose cae dentro de ese rango |

## Presupuesto del piloto (grupo de 9 personas, punto medio de 8-10)

| Rubro | Costo unitario | Cantidad | Subtotal (COP) |
|---|---|---|---|
| Kits de materiales | 130.000 | 9 | 1.170.000 |
| Espacio alquilado (sesión presencial, ~6h) | **250.000 (SUPUESTO — falta cotizar)** | 1 | 250.000 |
| Refrigerio/alimentación | 20.000 | 9 | 180.000 |
| Dominio + cuenta de marca (Instagram es gratis) | 80.000 | 1 | 80.000 |
| Contingencia (10%) | — | — | ~168.000 |
| **Total piloto** | | | **~1.848.000** |
| **Costo por persona (break-even)** | | | **~205.000** |

**Precio recomendado por persona: 200.000–220.000 COP.** Cubre materiales, espacio, comida, contingencia y el arranque de marca (dominio). No incluye pago a Sergio/Diego como instructores — para el piloto se tratan como aporte de "sweat equity" (coherente con la meritocracia que mencionaron), no como costo en efectivo.

### Sensibilidad al tamaño del grupo

| # Participantes | Costo total aprox. | Precio por persona (break-even) |
|---|---|---|
| 8 | ~1.760.000 | ~220.000 |
| 9 | ~1.848.000 | ~205.000 |
| 10 | ~1.930.000 | ~193.000 |

Mientras más gente se sume, más barato sale por persona — sobre todo porque el espacio y el dominio son costos fijos que se reparten entre todos.

## Lo que este presupuesto NO incluye (a propósito)

- Pago por hora a Sergio o Diego como instructores — el piloto se trata como inversión de tiempo, no como ingreso.
- Herramientas reutilizables (cautín, multímetro, etc.) — Sergio ya las tiene, no son costo del piloto.
- Marketing pago (pauta) — el piloto se vende por círculo cercano y redes orgánicas, según lo acordado.
- Presupuesto del curso completo (50-60 horas) — este documento es solo del piloto de 8 horas; el presupuesto del curso grande se hace después de validar con este piloto (ver [[MODELO-DE-NEGOCIO]]).

## Checklist antes de cobrar a alguien

- [ ] Cotizar el espacio real (reemplazar el supuesto de 250.000 COP) — candidatos: sala de coworking, laboratorio prestado, casa de alguno de los tres como respaldo si no cuadra el alquiler.
- [ ] Cotizar el kit real con un proveedor (Cascada, Mercado Libre, u otro) — reemplazar los tres rubros marcados SUPUESTO.
- [ ] Confirmar fecha y convocar a las 8-10 personas del círculo cercano.
- [ ] Grabar las 2 horas de contenido virtual (aula invertida) antes de la fecha presencial.
- [ ] Decidir si el precio final es 200.000, 210.000 o 220.000 COP según el número real de inscritos.
- [ ] Guardar fotos/video del piloto — es el material de venta para el resto del catálogo (ver [[IDEAS-DE-PRODUCTO]]).

## Ver también

- [[CONTEXTO]] · [[PERSONAS]] · [[IDEAS-DE-PRODUCTO]] · [[MODELO-DE-NEGOCIO]] · [[PLAN-DE-ACCION]]
