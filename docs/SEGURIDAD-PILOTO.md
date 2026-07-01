# Seguridad del piloto — ratio, protocolo y waiver (borrador)

> Borrador para T-050, T-051 y T-031 en [[BACKLOG]], a partir de los hallazgos de hardware/seguridad y legal en [[REVISION-EXPERTOS-2026-07-01]]. **No reemplaza asesoría legal formal** para el waiver, pero da un punto de partida serio. Revisar y ajustar antes de usarlo con participantes reales.

## Ratio instructor:estudiante (T-050)

El estándar recomendado para talleres de soldadura con principiantes es **3:1 a 4:1**, con supervisión activa (no solo estar en el salón). Con 8-10 participantes y hoy solo dos instructores (Sergio y Diego, ver [[PERSONAS]]), el ratio queda en ~4-5:1 — al límite o por encima de lo recomendado.

**Dos opciones, no excluyentes:**

1. **Conseguir un tercer ayudante para el bloque de soldadura.** No necesita ser un tercer "profesor" del taller completo — basta alguien que sepa soldar y pueda supervisar 2-3 estaciones mientras Sergio/Diego cubren el resto. Candidatos naturales: Pineda o Jorge/Jorgito (ya mencionados en [[PERSONAS]] como posibles sumas), o incluso Alejandra si se le da una guía rápida de qué vigilar (quemaduras, postura del cautín), aunque su rol natural es más logístico/comercial.
2. **Partir el grupo en dos tandas de soldadura** dentro de las 6 horas: mientras un subgrupo de 4-5 suelda con supervisión más cercana, el otro subgrupo avanza en otra estación de la agenda (instalación de software, revisión del código, práctica en placa de descarte — ver T-036). Esto además resuelve parte del cuello de botella de herramientas si no hay 9 cautines disponibles (T-052).

**Recomendación**: intentar primero la opción 1 (tercer ayudante) porque es más simple de coordinar; si no aparece nadie a tiempo, usar la opción 2 como plan B — y en ese caso, la agenda de T-036 debe reflejar el split desde el diseño, no improvisarlo el día del taller.

## Protocolo de seguridad de soldadura (T-051)

**Materiales:**
- **Usar estaño con plomo (60/40 o similar)** para el piloto, no sin plomo. Funde a menor temperatura (~183°C vs 217°C+ del sin plomo), lo que lo hace más fácil de trabajar para principiantes y reduce el riesgo de quemaduras por sobrecalentamiento del cautín. A cambio, exige la regla siguiente sin excepción.
- **Regla no negociable: lavarse las manos antes de comer/beber, y prohibido comer o beber en la mesa de trabajo.** Es la medida de seguridad más importante contra exposición al plomo y es gratis.

**Ventilación:**
- Verificar que el espacio (T-032) tenga ventilación natural (ventanas abiertas, corriente de aire) o forzada (ventilador/extractor) — el humo de fundente de resina irrita vías respiratorias incluso sin plomo de por medio.
- Si el espacio es cerrado sin buena ventilación, es motivo para descartarlo o exigir un ventilador por cada 2-3 estaciones.

**Equipo por estación de soldadura:**
- Soporte/base para el cautín (nunca apoyarlo directo sobre la mesa).
- Esponja húmeda o lana de bronce para limpiar la punta.
- Gafas de protección (salpicaduras de estaño fundido).
- Idealmente, extractor de humo local o al menos posición cerca de la fuente de ventilación.

**Botiquín:**
- Gel para quemaduras menores, gasas, y algún protocolo simple de "si alguien se quema: agua fría 10 min, gel, avisar al instructor a cargo" — dejarlo dicho en voz alta al inicio del taller, no asumido.

**Antes de tocar el kit real:**
- 15-20 minutos de práctica de soldadura en una placa de descarte/chatarra antes de soldar el ESP32 o la matriz LED — evita que el primer punto soldado en frío sea en el componente caro (ver hallazgo de hardware en [[REVISION-EXPERTOS-2026-07-01]]).

## Waiver de responsabilidad + autorización (T-031) — borrador

> Este texto es un punto de partida. Antes de usarlo, revisar con alguien con criterio legal — sobre todo la cláusula de exoneración, que en Colombia no exime responsabilidad por negligencia grave o dolo, solo reduce exposición por lesiones menores derivadas del uso normal de las herramientas.

---

**AUTORIZACIÓN DE PARTICIPACIÓN Y TRATAMIENTO DE DATOS — [NOMBRE DEL TALLER]**

Fecha: ______________ Nombre del participante: ______________________________
Cédula/documento: _______________ Contacto de emergencia (nombre y teléfono): ______________________________

**1. Descripción del taller y riesgos.** Declaro que fui informado de que este taller incluye el uso de herramientas de soldadura (cautín eléctrico a alta temperatura) y componentes electrónicos de bajo voltaje, y que esto conlleva un riesgo de quemaduras menores, cortes leves o irritación por exposición a humo de fundente. Entiendo que se siguen medidas de mitigación (ventilación, equipo de protección, supervisión), pero que ningún taller de este tipo está exento de riesgo.

**2. Participación voluntaria.** Declaro que mi participación es voluntaria y que puedo retirarme de cualquier actividad específica del taller sin necesidad de justificarlo.

**3. Exoneración de responsabilidad.** Eximo a los organizadores de responsabilidad por lesiones menores derivadas del uso normal de las herramientas y materiales del taller, siempre que se hayan seguido las instrucciones de seguridad indicadas por los instructores. Esto no aplica en caso de negligencia grave comprobada por parte de los organizadores.

**4. Autorización de datos personales (Ley 1581 de 2012).** Autorizo el tratamiento de mis datos de contacto (nombre, teléfono, correo) para fines de organización del taller y comunicación de futuras actividades relacionadas, pudiendo revocar esta autorización en cualquier momento escribiendo a [correo/contacto del proyecto].

**5. Autorización de imagen (opcional, marcar si aplica).** ☐ Autorizo el uso de fotografías/video tomadas durante el taller en las que aparezca, con fines de difusión y marketing del proyecto (redes sociales, sitio web). ☐ No autorizo el uso de mi imagen.

Firma: ______________________________

---

*(Si algún participante es menor de edad, este documento no es suficiente — requiere autorización firmada por el padre/madre/acudiente, y activa el régimen del hallazgo legal #8 en [[REVISION-EXPERTOS-2026-07-01]]. No aplica al piloto actual si el círculo cercano convocado son todos adultos, pero hay que confirmarlo en la encuesta previa de T-037.)*

## Ver también

- [[BACKLOG]] (T-031, T-050, T-051) · [[REVISION-EXPERTOS-2026-07-01]] · [[PRESUPUESTO-PILOTO]] · [[PERSONAS]]
