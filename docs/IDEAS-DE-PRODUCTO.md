# Ideas de producto / catálogo de proyectos

> Lluvia de ideas cruda de la llamada del 2026-06-30. Nada de esto está priorizado ni validado todavía — ver [[PLAN-DE-ACCION]] para eso. Ver [[MODELO-DE-NEGOCIO]] para cómo se empaquetaría y vendería.

## 1. Computación tangible / ESP32-Arduino — el eje técnico más desarrollado

Idea base: microcontroladores baratos (ESP32 ronda los 25.000 COP) + capa de abstracción por IA como puerta de entrada a electrónica, programación y automatización. Proyectos concretos que se mencionaron, de más simple a más complejo:

- **Matriz/lámpara de LEDs controlada por ESP32**: matriz de LEDs (~12-15.000 COP c/u) + ESP32 (~40.000 COP) + regulador de voltaje — menos de 100-200.000 COP en materiales. Se puede controlar por web server local, cambiar colores/animaciones desde el celular. Ejemplo motivador real: a Diego se le dañaron las luces LED de su escritorio y en vez de comprar una tira nueva se armó la suya — casaría perfecto con un video "problema → solución → te enseño a hacerlo" para redes.
- **Sensor de calidad de luz ambiental** que replica esa luz adentro (extensión del proyecto anterior).
- **Radar de aviones en tiempo real**: toma el GPS del usuario, cruza con una base de datos pública de vuelos y muestra qué avión está pasando, de dónde viene, cuántos pasajeros lleva, etc.
- **Introducción a sensores y actuadores**: humedad, temperatura (gama de precios 12.000–60.000 COP según calidad/uso), servomotores, motores paso a paso, pantallas, protocolos de comunicación (radiofrecuencia, largo alcance, Bluetooth), interfaces gráficas. Suficiente contenido para varias clases completas.
- **Kit de robot básico tipo "Big Robot"**: sensor ultrasonido + placa Arduino + sensor de línea + puente H para motores + baterías — menos de 300.000 COP en componentes, sirve de base para muchísimo contenido (seguidor de línea, evasión de obstáculos, etc.).
- **Automatización/IoT para cultivos**: controladores para hongos, cannabis y agricultura de precisión — conecta directo con el otro proyecto personal de Sergio (laboratorio de hongos).

## 2. Cyberdeck

Mini-computadores personalizados ensamblados a partir de piezas sueltas (pantalla, teclado, batería 18650, SP32/Raspberry Pi, carcasa impresa en 3D o tallada). Tendencia real en TikTok. Validado en vivo por el hijo de Diego (18 años, entra a ingeniería), que se entusiasmó al escuchar la idea de pasada.

- Se puede escalar en complejidad/costo: desde algo simple con Raspberry Pi Pico (~25.000 COP) hasta un "compute module" de gama alta para ingeniería más seria.
- Enseña de paso: soldadura, diseño y manufactura de carcasas (impresión 3D o corte CNC/láser en madera), ensamblaje, personalización — la propuesta de valor es que el estudiante no compra un Mac armado, sino que entiende y construye el suyo.
- Diego lo ve como proyecto "high level" — requiere más presupuesto en componentes, así que no sería el primer piloto sino algo a lo que se escala.

## 3. Cultura maker general (fabricación digital)

- Impresión 3D (sigue siendo el imán de atención número uno del mundo maker).
- Corte CNC y corte láser — carpintería computarizada como alternativa/complemento a la impresión 3D para carcasas y estructuras.
- Ejemplos de proyectos "gancho" mencionados: carro RC con impresión 3D controlado por FPV (sistema tipo DJI), robot fútbol.

## 4. IA práctica para profesionales y adultos mayores

Curso corto centrado en **perder el miedo y ganar autonomía**, no en teoría de IA:

- Crear cuenta, aprender comandos de voz y de texto, ir de preguntas triviales a dar contexto real (ejemplo real: la mamá de Sergio ahora paga la suscripción de Claude y la usa en vez de Google para planear un viaje a Portugal).
- Casos de uso cotidianos como gancho (ejemplo de Diego: "tengo tomate, cebolla, tres papas, cinco huevos, ¿qué cocino?").
- Público: adultos mayores intimidados por el tema, profesionales que sienten que su rol está cambiando y no saben por dónde actualizarse, y curiosamente también gente de la misma edad de Diego (su vecino).

## 5. Astronomía y astroturismo (aporte de Diego)

- Curso vivencial: la narrativa mitológica detrás de las constelaciones (Orión huyendo del Escorpión, las Pléyades, Andrómeda y Perseo, etc.) como gancho emocional para "recuperar el cielo".
- Astronomía ancestral: cómo los incas predecían el fenómeno de El Niño leyendo el cielo, observatorios incas en piedra.
- Navegación sin GPS (ubicarse por estrellas) — conecta con la idea de "podemos vivir sin depender 100% de la tecnología aunque la usemos a diario".
- **Planetario propio**: hoy se puede alquilar uno, pero la aspiración es tener espacio propio; conecta con el software "Catalejo" que Diego está desarrollando con un tercer socio.
- **Expediciones de astroturismo**: Cusco (con contacto real, directora del planetario), Desierto de la Tatacoa, La Guajira, Nevado del Ruiz, Chile, observatorios en España.

## 6. Proyecto social — donatón de basura electrónica

Idea de crecimiento/marca vía impacto social real, no solo utilitarismo de marketing:

- Campaña de donación de electrónica en desuso (Nintendos, drones, carros RC, impresoras 3D) que la gente tiene guardada.
- Ingeniería inversa sobre esa "basura" para armar proyectos → contenido + narrativa de economía circular/reciclaje.
- Alianza con universidades/empresas para becas a jóvenes talento sin recursos para estudiar.
- Charlas en colegios (grados décimo/once) para motivar interés temprano en STEM — Diego ya tiene una anécdota real de un niño de 7-8 años enganchado tras una charla de astronomía.

## 7. Proyecto ambiental

- Cámaras trampa para monitorear fauna y flora en montañas, páramos, cuencas — mencionado como extensión natural del espíritu maker + causa ambiental, sin desarrollar más allá de la idea.

## 8. Visión de largo plazo — "la Jobiteca"

Concepto paraguas que Sergio trae de tiempo atrás: un club de hobbies tipo membresía de gimnasio, con espacio físico compartido (herramientas, impresoras 3D, talleres), comunidad, eventos, merchandising, comida/cerveza — la versión "club social" de todo lo anterior. **No es el punto de partida**; es el horizonte hacia el que estas ideas podrían crecer si el piloto funciona.

## Ver también

- [[CONTEXTO]] — de dónde sale todo esto.
- [[MODELO-DE-NEGOCIO]] — cómo empaquetar y priorizar este catálogo.
- [[PLAN-DE-ACCION]] — qué se decidió mover primero.
