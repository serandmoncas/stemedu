# Agenda, personalización y evaluación del piloto (borrador)

> Borrador para T-036, T-039 y T-040 en [[BACKLOG]] (incluye T-041, el cierre con CTA). Construido sobre las 6 horas presenciales definidas en [[PRESUPUESTO-PILOTO]] y los hallazgos de pedagogía y hardware en [[REVISION-EXPERTOS-2026-07-01]]. Asume que el alcance ya se recortó (T-038): el control por celular/web server queda como *stretch goal* opcional, no como entregable base.

## Supuestos que hay que confirmar antes de usar esta agenda

- Grupo de 8-10 personas, todas adultas (si hay menores, ver la nota de [[SEGURIDAD-PILOTO]]).
- Ratio instructor:estudiante resuelto según T-050: idealmente un tercer ayudante para soldadura; si no aparece, esta agenda usa el plan B de **dividir el grupo en dos** para el bloque de soldadura (columnas A/B abajo).
- Los participantes ya vieron (o no) las 2 horas de contenido virtual — la encuesta previa de T-037 debería decir cuántos faltan, pero esta agenda asume que **no todos lo vieron** (el propio equipo estimó ~60% de inasistencia al contenido previo) y reserva tiempo real para eso, no una frase de salvedad sin presupuesto.

## Agenda minuto a minuto (6 horas = 360 min)

| Bloque | Duración | Actividad | Notas |
|---|---|---|---|
| 0:00–0:15 | 15 min | Bienvenida, registro, firma del waiver ([[SEGURIDAD-PILOTO]]), entrega de kits | No empezar nada técnico sin el waiver firmado |
| 0:15–0:45 | 30 min | **Grupo A** (vio el contenido virtual): arranca personalización (ver abajo) · **Grupo B** (no lo vio): refuerzo en vivo con un instructor | Este es el "plan B" del aula invertida — con tiempo real asignado, no gratis |
| 0:45–1:00 | 15 min | Momento de personalización (todos juntos) | Ver worksheet abajo — resuelve T-040 |
| 1:00–1:20 | 20 min | Introducción de seguridad + práctica de soldadura en placa de descarte | Protocolo completo en [[SEGURIDAD-PILOTO]] |
| 1:20–2:50 | 90 min | Soldadura del kit real (matriz LED + ESP32 + regulador + cableado) | Si se dividió el grupo por ratio (T-050), alternar: mientras la mitad suelda con supervisión cercana, la otra mitad instala software/entorno en su laptop |
| 2:50–3:00 | 10 min | Descanso | |
| 3:00–3:20 | 20 min | Verificación con multímetro + primer encendido con firmware base pre-cargado (fallback, T-053) | Todos deberían ver su lámpara prender aunque sea con la animación de fábrica |
| 3:20–4:00 | 40 min | Programación: adaptar/crear animaciones con ayuda de IA, aplicando la personalización elegida a las 0:45 | Aquí es donde ocurre el aprendizaje de "adaptar y construir", no solo copiar |
| 4:00–4:20 | 20 min | Buffer de troubleshooting para quienes van atrasados | No comprimir esto — es el colchón que evita que el taller se sienta apurado |
| 4:20–4:40 | 20 min | Segundo descanso / refrigerio | |
| 4:40–5:20 | 40 min | Terminar carcasa/difusor con el material personalizado, montaje final | |
| 5:20–5:45 | 25 min | Evaluación de aprendizaje (checklist + mini pre/post) + fotos/video de productos terminados | Resuelve T-039 y alimenta T-010 |
| 5:45–6:00 | 15 min | Cierre: CTA hacia el catálogo completo, feedback rápido, despedida | Resuelve T-041 |

**Nota de diseño**: si consiguen el tercer ayudante de soldadura (opción 1 de T-050) en vez de dividir el grupo, el bloque 1:20–2:50 se simplifica (todos sueldan juntos con mejor supervisión) y sobra tiempo — úsenlo para alargar el buffer de las 4:00–4:20, que es el bloque más frágil de toda la agenda.

## Momento de personalización (T-040)

Antes de soldar, cada participante llena una ficha corta (worksheet físico o digital, 10-15 min):

1. **¿Dónde va a vivir tu lámpara?** (escritorio, cuarto, sala, regalo para alguien más — esto conecta el proyecto con un uso real, no un ejercicio abstracto)
2. **¿Qué querés que te transmita?** (relajante, festiva, de concentración para trabajar)
3. **Elegí un patrón base** para programar después: respiración lenta de un solo color, arcoíris en movimiento, o reactivo (cambia con un botón/sensor si hay tiempo).
4. **Elegí el material y forma del difusor**: papel/vellum, acrílico, madera cortada, o algo reciclado que traigan ellos mismos — esta variable ya estaba presupuestada como flexible en [[PRESUPUESTO-PILOTO]].

Estas decisiones se retoman en el bloque de programación (3:20–4:00) para que cada quien programe *su* patrón, no copie el de al lado — es la diferencia entre construccionismo real y ensamblaje guiado que señaló la revisión pedagógica.

## Instrumento de evaluación de aprendizaje (T-039)

### Checklist de competencias observables (lo llena el instructor por participante, al cierre)

- [ ] Soldó al menos el 80% de sus puntos sin que el instructor soldara por él/ella.
- [ ] Puede explicar en sus palabras qué hace el regulador de voltaje (o por qué la matriz no se conecta directo al pin del ESP32).
- [ ] Modificó una animación (color, velocidad o patrón) con ayuda de IA, sin que el instructor tecleara por él/ella.
- [ ] Su lámpara enciende y corre el patrón que eligió en el momento de personalización.
- [ ] Puede nombrar al menos un componente del kit y para qué sirve, sin ayuda.

### Mini pre/post de confianza (una pregunta antes de empezar, la misma después de terminar)

> "En una escala de 1 a 5, ¿qué tan cómodo/a te sentís armando y programando un proyecto de electrónica por tu cuenta?"

La diferencia entre el "antes" y el "después" es el dato más honesto de si el taller funcionó — más confiable que "¿te gustó?".

### Pregunta abierta de cierre

> "¿Qué fue lo más difícil hoy, y qué fue lo que más te sorprendió que sí pudiste hacer?"

Sirve doble: como dato de mejora de diseño del taller y como fuente de citas reales para el material de venta (T-010, T-042).

## Cierre y CTA hacia el catálogo (T-041)

En los últimos 15 minutos, conectar explícitamente lo que acaban de hacer con el resto del catálogo ([[IDEAS-DE-PRODUCTO]]): "hoy soldaron, programaron con IA y armaron su primer proyecto — esto es la base de lo que viene: sensores, robots, hasta el Cyberdeck". No hace falta vender agresivamente aquí; alcanza con nombrar el siguiente peldaño y dejar claro cómo enterarse (Instagram/canal que resulte de T-014).

## Ver también

- [[BACKLOG]] (T-036, T-039, T-040, T-041) · [[REVISION-EXPERTOS-2026-07-01]] · [[PRESUPUESTO-PILOTO]] · [[SEGURIDAD-PILOTO]] · [[IDEAS-DE-PRODUCTO]]
