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

## Lista de materiales por kit (1 persona) — actualizada con precios reales (2026-07-01)

> Reemplaza la primera versión (basada solo en lo que Sergio recordaba de memoria en la llamada). Incluye los componentes de seguridad que agregó la revisión de hardware ([[REVISION-EXPERTOS-2026-07-01]], T-047/T-048/T-049). Fuentes: [Electronilab.co](https://electronilab.co) (tienda colombiana real, Bogotá).

| Componente | Costo (COP) | Estado | Notas |
|---|---|---|---|
| ESP32 (dev board) | 35.000 | **Real** | Verificado en Electronilab: rango real 28.900–39.900 según modelo |
| Matriz de LEDs direccionables (5x5, tipo WS2812B) x2 | 30.000 | SUPUESTO | No se encontró un proveedor colombiano con precio público — cotizar directo en Mercado Libre o La Cascada (Bogotá) |
| Fuente 5V/3A con inyección directa a la matriz (reemplaza el "regulador de voltaje" genérico — ver T-047) | 40.000 | Parcial | Electronilab sí vende un adaptador 5V/3A USB-C tipo Raspberry Pi 4 (confirma que existe y es fácil de conseguir), pero no se pudo extraer el precio exacto de la ficha — usar 40.000 como estimado conservador |
| Protoboard/perfboard | 15.900 | **Real** | Protoboard MB102 830 puntos, verificado en Electronilab |
| Resistencia línea de datos (300-500Ω) + capacitor de desacople ~1000µF (T-048) | 5.000 | Estimado | Componentes pasivos muy baratos |
| Consumibles de soldadura: estaño con plomo, flux, esponja/lana de bronce, cinta aislante (T-048, [[SEGURIDAD-PILOTO]]) | 10.000 | Estimado | Prorrateado por kit, se compran a granel |
| Carcasa/difusor (impresión 3D o material simple/reciclado) | 15.000 | SUPUESTO | Variable a propósito — es parte del momento de personalización, T-040 |
| **Total por kit** | **~151.000** | | Sube de 130.000 a ~151.000 COP frente al primer borrador — principalmente por la fuente de alimentación más robusta y los componentes de seguridad que faltaban en la primera versión |

**Lo que sigue pendiente de cotizar en firme**: el precio exacto de la matriz WS2812B y de la fuente 5V/3A específica. El ESP32 y el protoboard ya tienen precio real verificado.

## Presupuesto del piloto (grupo de 9 personas, punto medio de 8-10)

| Rubro | Costo unitario | Cantidad | Subtotal (COP) |
|---|---|---|---|
| Kits de materiales | 151.000 | 9 | 1.359.000 |
| Repuestos por fallas de soldadura (12%, T-049) | — | — | ~163.000 |
| Espacio alquilado (sesión presencial, ~6h) | **300.000 (SUPUESTO — ver rango real abajo)** | 1 | 300.000 |
| Refrigerio/alimentación | 20.000 | 9 | 180.000 |
| Contingencia (15% — subida desde 10% por recomendación de [[REVISION-EXPERTOS-2026-07-01]] mientras el espacio no esté confirmado) | — | — | ~300.000 |
| **Total piloto** | | | **~2.302.000** |
| **Costo por persona (break-even)** | | | **~256.000** |

**Precio recomendado por persona: 250.000–260.000 COP** (subió frente al estimado inicial de 200.000-220.000, principalmente por las correcciones de seguridad del kit). No incluye pago a Sergio/Diego como instructores — para el piloto se tratan como aporte de "sweat equity", no como costo en efectivo. El dominio (80.000 COP) ya no se incluye aquí — se saca del cálculo por persona del piloto y se trata como gasto de marca aparte (T-029, [[REVISION-EXPERTOS-2026-07-01]] negocio #2).

### Espacio: rango real encontrado (T-003, todavía sin reservar)

Investigación de escritorio, no una cotización formal — falta contactar directamente y **confirmar explícitamente que permiten soldadura** (ninguna fuente lo confirma, es el hallazgo de seguridad #3 de [[REVISION-EXPERTOS-2026-07-01]]):

- **Regus** (salas de reuniones/capacitación en Medellín): COP 39.000–149.000 por hora según categoría → para 6 horas, entre **234.000 y 894.000 COP**. El extremo bajo es consistente con el supuesto original de 250.000.
- **Quokka Coworking** (El Poblado): desde $10.000 COP **por hora por persona** (no por sala) — si se cobrara así para un taller privado de 9 personas × 6h, saldría en **540.000 COP**, mucho más caro. Hay que preguntarles directamente si tienen tarifa de sala privada en vez de tarifa por persona.
- Ninguna de las dos opciones parece pensada para actividades con herramientas/soldadura — vale la pena explorar también el **makerspace de la Universidad Nacional** (hallazgo de [[INVESTIGACION-MERCADO]]) o un espacio tipo "taller creativo/manualidades", que suelen estar mejor preparados para actividades manuales.

Se usó **300.000 COP** como estimado de trabajo (punto medio conservador dentro del rango real de Regus), pero sigue marcado SUPUESTO hasta que T-003 se cierre con una reserva confirmada.

### Sensibilidad al tamaño del grupo

| # Participantes | Costo total aprox. | Precio por persona (break-even) |
|---|---|---|
| 8 | ~2.085.000 | ~261.000 |
| 9 | ~2.302.000 | ~256.000 |
| 10 | ~2.520.000 | ~252.000 |

Mientras más gente se sume, más barato sale por persona — el espacio es el costo fijo más grande y se reparte entre todos.

## Lo que este presupuesto NO incluye (a propósito)

- Pago por hora a Sergio o Diego como instructores — el piloto se trata como inversión de tiempo, no como ingreso.
- Herramientas reutilizables (cautín, multímetro, etc.) — Sergio ya las tiene, no son costo del piloto.
- Marketing pago (pauta) — el piloto se vende por círculo cercano y redes orgánicas, según lo acordado.
- Presupuesto del curso completo (50-60 horas) — este documento es solo del piloto de 8 horas; el presupuesto del curso grande se hace después de validar con este piloto (ver [[MODELO-DE-NEGOCIO]]).

## Checklist antes de cobrar a alguien

- [x] Investigar precios reales de materiales — hecho por escritorio (2026-07-01): ESP32 y protoboard confirmados con proveedor real; matriz LED y fuente 5V/3A siguen sin precio exacto confirmado.
- [ ] Confirmar precio exacto de la matriz WS2812B y de la fuente 5V/3A (cotizar directo en Mercado Libre/La Cascada — la búsqueda web no devolvió precio final).
- [ ] Reservar el espacio real y **confirmar explícitamente que permiten soldadura** — candidatos investigados: Regus (sala por hora), Quokka Coworking (aclarar si cobran por sala o por persona para un evento privado), makerspace UNAL, espacio tipo taller creativo/manualidades.
- [ ] Confirmar fecha y convocar a las 8-10 personas del círculo cercano.
- [ ] Grabar las 2 horas de contenido virtual (aula invertida) antes de la fecha presencial — después de cerrar T-038 (recorte de alcance).
- [ ] Decidir si el precio final es 250.000, 255.000 o 260.000 COP según el número real de inscritos.
- [ ] Guardar fotos/video del piloto — es el material de venta para el resto del catálogo (ver [[IDEAS-DE-PRODUCTO]]).

## Fuentes consultadas (precios reales, 2026-07-01)

- [ESP32 — Productos, Electronilab](https://electronilab.co/etiqueta-producto/esp32/)
- [Board de desarrollo con ESP32 WiFi Bluetooth BLE CH9102F 30 pines — Electronilab ($34.900)](https://electronilab.co/tienda/board-de-desarrollo-con-modulo-esp32-wifibluetooth-ble/)
- [Protoboard Adhesiva MB102 830 Puntos — Electronilab ($15.900)](https://electronilab.co/tienda/protoboard-adhesiva-mb102-830-puntos-transparente/)
- [Salas de reuniones en Medellín — Regus](https://www.regus.com/es-es/colombia/medellin/meeting-rooms)
- [Quokka Coworking Medellín](https://quokkacoworking.com/en/)

## Ver también

- [[CONTEXTO]] · [[PERSONAS]] · [[IDEAS-DE-PRODUCTO]] · [[MODELO-DE-NEGOCIO]] · [[PLAN-DE-ACCION]] · [[REVISION-EXPERTOS-2026-07-01]] · [[SEGURIDAD-PILOTO]] · [[INVESTIGACION-MERCADO]]
