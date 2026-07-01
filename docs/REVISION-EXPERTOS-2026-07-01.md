# Revisión de expertos — 2026-07-01

> Cinco revisiones independientes (modelo de negocio, pedagogía, marketing/growth, legal/riesgo Colombia, hardware maker/seguridad) sobre el estado del proyecto en `docs/` al cierre del piloto definido en [[PRESUPUESTO-PILOTO]]. Cada revisión fue de solo lectura. Los hallazgos accionables ya están convertidos en tareas en [[BACKLOG]] (T-026 en adelante); este documento guarda el razonamiento completo detrás de cada una.

## Modelo de negocio

1. **La prueba está contaminada**: cobrarle al círculo cercano el costo pleno sin depósito no reembolsable mide lealtad social, no demanda de mercado. → T-027.
2. El costo del dominio (80.000 COP) no debería estar en el cálculo de precio por persona del piloto — es gasto de marca, no del taller puntual. → T-029.
3. Falta un criterio numérico de éxito/fracaso definido *antes* de convocar (ej. "6 de 10 pagan en 5 días"), o cualquier resultado se racionaliza como éxito. → T-028.
4. El piloto no valida ningún segmento real de [[MODELO-DE-NEGOCIO]] (solo "amigos") — correr en paralelo un mini-test con desconocidos vía redes mide algo distinto y complementario. → T-030.
5. Riesgo no mencionado: competencia gratuita o casi gratuita (SENA, semilleros universitarios) frente al precio de 1-5M COP del curso completo — debe entrar en la investigación de mercado (T-017).
6. Riesgo de exclusividad/cesión de IP en el contrato con la Universidad Nacional, sin evaluar todavía. → T-034.
7. No hay figura legal/tributaria definida para cobrar, ni siquiera al círculo cercano. → T-026.
8. El diseño de dos niveles (premium/económico) ya está bien priorizado como Baja en el backlog (T-024) — no gastar más ciclo de diseño ahí hasta tener datos del piloto.

## Pedagogía / diseño instruccional

1. El "plan B" del aula invertida (sesiones de refuerzo) no tiene presupuesto de tiempo dentro de las 6 horas presenciales. → T-036.
2. Falta una encuesta previa (edad, experiencia con soldadura, ¿vio el contenido virtual?) 48h antes, para no improvisar el plan B a ciegas. → T-037.
3. El alcance del proyecto (soldadura + web server + control por celular) está sobrecargado para 6 horas con principiantes — mover el control por celular a stretch goal opcional. → T-038.
4. No existe una agenda minuto a minuto del taller — sin ella no se sabe si el refuerzo, la soldadura y la programación caben en el tiempo. → T-036 (mismo entregable).
5. El diseño actual es "kit de ensamblaje guiado", no construccionismo genuino — falta un momento de elección/personalización propia (patrón, color, forma). → T-040.
6. Mezclar niños, adultos mayores y profesionales técnicos en la misma sesión de soldadura sin protocolo es riesgo pedagógico y de seguridad a la vez (cruza con hallazgo de hardware/seguridad #4 y #5).
7. No hay ningún instrumento de evaluación de aprendizaje, solo evidencia de marketing (fotos/video). → T-039.
8. Falta conectar el piloto como primer peldaño de la ruta de aprendizaje completa — hoy se siente autocontenido, sin CTA hacia el catálogo. → T-041.

## Marketing y growth

1. El video "problema→solución→CTA" (T-016) necesita mostrar el objeto terminado funcionando y un paso de bajo compromiso antes de pedir pago directo. → T-042.
2. El catálogo (8 ejes distintos) diluye la marca en esta etapa — anclar toda la comunicación inicial en computación tangible/ESP32, dejar astronomía e IA para adultos mayores como líneas de contenido futuras.
3. Riesgo de re-branding costoso si se crea Instagram/dominio con nombre provisional bajo presión de publicar — cerrar T-012 antes de que exista esa presión.
4. Depender 100% de círculo cercano + orgánico sin ningún presupuesto de pauta no es una estrategia de escalamiento real, aunque sea correcto para validar el piloto. → alimenta T-046.
5. El piloto no está usando un embudo digital replicable (invitación manual) — montar el flujo mínimo real (link → WhatsApp/Typeform → pago) aunque sea para el círculo cercano. → T-043.
6. Falta un paso intermedio de "prueba social barata" (mini-reto, lead magnet) entre ver el contenido y pagar — la propia UNAL ya usa esa lógica con su masterclass gratuita.
7. La fuerza de venta directa de Alejandra no está asignada a ninguna tarea de conversión (DMs/WhatsApp) — hoy el marketing digital recae en quien menos experiencia tiene en eso. → T-044.
8. Riesgo de ancla de precio: si el material de venta del piloto (200-220k COP) se reutiliza después para vender el catálogo completo a precio full, hay disonancia — dejar explícito en el video/testimonios que es "precio de fundadores". → T-045.

## Legal y riesgo (Colombia)

1. No hay figura legal/tributaria definida para cobrar ni siquiera al círculo cercano — riesgo de DIAN si se repite el patrón sin soporte. → T-026.
2. Falta exoneración de responsabilidad (waiver) firmada antes de que nadie suelde — soldadura implica riesgo real de quemaduras/incendio menor. → T-031.
3. Falta verificar que el espacio alquilado permite soldadura y tiene protocolo de seguridad (extintor, ventilación) antes de firmar el contrato de alquiler. → T-032.
4. Seguro de responsabilidad civil/accidentes: bajo riesgo para el piloto (son conocidos), pero casi indispensable en cuanto se repita con público pagador desconocido. → T-033.
5. No está confirmado por escrito si la Universidad Nacional permite 2-3 docentes bajo un solo aval — pedirlo antes de invertir tiempo en contenido pensado para reutilizar ahí. → T-034.
6. Propiedad intelectual del contenido (videos, guías, código) no está definida frente a la universidad — negociar la cláusula antes de firmar, no después. → T-034 (mismo hallazgo, cruza con negocio #6).
7. Riesgo de depender de un solo profesor avalador individual sin plan de continuidad si cambia o se cae el aval. → T-035.
8. Si el público se extiende a menores de edad (colegios, vacaciones), el régimen legal cambia por completo (Ley 1098/2006) — no bloquea el piloto actual, pero hay que anticiparlo en [[MODELO-DE-NEGOCIO]] antes de vender a colegios.
9. Riesgo adicional: manejo de datos personales de los inscritos (Ley 1581/2012) — agregar una línea de autorización en la misma ficha del waiver. → T-031 (mismo entregable).

## Hardware maker y seguridad

1. El regulador de voltaje de 20.000 COP está subespecificado: con 2 matrices WS2812B el peor caso ronda 3A/15W, más de lo que aguanta un cargador USB genérico o el regulador on-board del ESP32. Necesita fuente 5V/3A con inyección directa a la matriz y GND común. → T-047.
2. Faltan en la lista de materiales: resistencia en la línea de datos (300-500Ω), capacitor de desacople (~1000µF), flux, esponja/lana de bronce, cinta aislante. → T-048.
3. 6 horas presenciales son ajustadas (30-50% de riesgo de que no todos terminen funcionando) si no se separa tiempo de práctica de soldadura previa y se verifica si el ESP32 viene con pines pre-soldados. → alimenta T-036 y T-038.
4. Preparar un firmware base pre-probado como fallback (o flasher web) para que todos salgan con algo funcionando aunque no completen la programación desde cero. → T-053.
5. No hay ratio instructor:estudiante definido para soldadura — el estándar recomendado es 3:1 a 4:1 con supervisión activa; hoy el piloto asume ~4.5:1 con solo dos instructores. → T-050.
6. Falta protocolo completo de seguridad de soldadura: tipo de estaño (con/sin plomo), ventilación, gafas, soportes de cautín, botiquín. → T-051.
7. El presupuesto no contempla consumibles ni repuestos por fallas de soldadura (10-15% recomendado) ni confirma cuántas estaciones de soldadura/multímetros existen realmente. → T-049, T-052.
8. La contingencia del presupuesto (10%) es baja dado que los dos rubros más grandes siguen sin cotizar — considerar subirla a 20-25% hasta cerrar T-003 y T-004.

## Ver también

- [[BACKLOG]] — tareas T-026 en adelante, derivadas de esta revisión.
- [[PRESUPUESTO-PILOTO]] · [[MODELO-DE-NEGOCIO]] · [[CONTEXTO]] · [[PERSONAS]]
