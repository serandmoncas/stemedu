# Contenido técnico del piloto (borrador)

> Borrador para T-053, T-037 y T-038 en [[BACKLOG]]. Revisar y ajustar antes de usar con participantes reales — el firmware en particular hay que probarlo en hardware real antes del taller, no confiar en que compile a la primera.

## Alcance del piloto — versión formal (T-038)

Ya se venía asumiendo en [[AGENDA-Y-EVALUACION-PILOTO]], pero quedaba sin decisión explícita en el backlog. Queda así:

**Incluido en el piloto (obligatorio, cabe en las 6 horas presenciales):**
- Soldar la matriz LED, el ESP32 y el regulador/fuente.
- Cargar un firmware base (ver abajo) y verificar que la lámpara prende.
- Adaptar/personalizar una animación (color, velocidad o patrón) con ayuda de IA, aplicando lo elegido en el momento de personalización (T-040).
- Armar la carcasa/difusor.

**Fuera del piloto — *stretch goal* opcional para quien termine antes o quiera seguir en casa:**
- Control por celular vía web server local (WiFi + interfaz web para cambiar color/patrón en tiempo real). Esto fue lo que originalmente describía [[IDEAS-DE-PRODUCTO]] como parte del proyecto, pero la revisión pedagógica identificó que es demasiado para un principiante en 6 horas junto con soldadura — ver hallazgo de pedagogía #3 en [[REVISION-EXPERTOS-2026-07-01]].

Esta separación ya está reflejada en el firmware de abajo (el control web queda comentado como referencia, no como parte del entregable base).

## Encuesta previa a inscritos (T-037)

> Enviar 48h antes de la sesión presencial, una vez estén confirmados los inscritos (T-006). Formato sugerido: Google Form de 3-4 preguntas, menos de 2 minutos de responder.

1. **¿Cuál es tu rango de edad?** (menor de 18 / 18-30 / 31-50 / 51+) — si aparece algún menor de edad, activa la nota de [[SEGURIDAD-PILOTO]] sobre autorización de acudientes, distinta del waiver estándar.
2. **¿Alguna vez has soldado electrónica?** (nunca / una o dos veces / tengo experiencia) — para dimensionar cuánto tiempo real de práctica en placa de descarte necesita cada quien.
3. **¿Ya viste el contenido virtual del taller?** (sí, completo / lo empecé / no lo he visto) — esta es la pregunta que dimensiona el bloque de refuerzo de la agenda (Grupo A/B en [[AGENDA-Y-EVALUACION-PILOTO]]); sin este dato el refuerzo se diseña a ciegas.
4. *(Opcional)* **¿Hay algo que debamos saber?** (alergias, condición médica relevante, o cualquier inquietud) — campo abierto, conecta con el botiquín/protocolo de [[SEGURIDAD-PILOTO]].

## Firmware base de respaldo (T-053)

> "Camino mínimo garantizado": si alguien no logra programar su propio código en el tiempo disponible, este sketch se carga en &lt;2 minutos y la lámpara sale funcionando con 3 animaciones. Requiere la librería **FastLED** (Arduino IDE: *Sketch → Incluir Librería → Administrar Bibliotecas* → buscar "FastLED"). Probarlo en hardware real antes del taller — este código no ha sido compilado ni probado en un ESP32 físico, es un punto de partida técnico, no un firmware validado.

```cpp
/*
  De Cero a Luz — firmware base de respaldo
  ESP32 + matriz de LEDs WS2812B (2x 5x5 = 50 LEDs en serie)

  Camino mínimo garantizado: si alguien no termina de programar su
  propio código, cargamos esto y su lámpara igual prende con 3
  animaciones. Requiere la librería FastLED.
*/

#include <FastLED.h>

#define LED_PIN     5      // pin de datos conectado a la matriz (ajustar según cableado real)
#define NUM_LEDS    50     // 2 matrices de 5x5 = 25 + 25
#define BRILLO_MAX  80     // 0-255 — NO usar 255: con 50 LEDs a full blanco el consumo
                           // supera lo que aguanta una fuente mal dimensionada (ver T-047)
#define LED_TYPE    WS2812B
#define COLOR_ORDER GRB

CRGB leds[NUM_LEDS];

const unsigned long DURACION_ANIMACION = 8000; // ms antes de pasar a la siguiente
unsigned long tiempoInicio = 0;
int animacionActual = 0;
const int TOTAL_ANIMACIONES = 3;

void setup() {
  FastLED.addLeds<LED_TYPE, LED_PIN, COLOR_ORDER>(leds, NUM_LEDS);
  FastLED.setBrightness(BRILLO_MAX);
  tiempoInicio = millis();
}

void loop() {
  if (millis() - tiempoInicio > DURACION_ANIMACION) {
    animacionActual = (animacionActual + 1) % TOTAL_ANIMACIONES;
    tiempoInicio = millis();
  }

  switch (animacionActual) {
    case 0: respiracion(CRGB::Blue); break;
    case 1: arcoiris();              break;
    case 2: destellos();             break;
  }

  FastLED.show();
  delay(20);
}

// Animación 1: respiración lenta de un solo color
void respiracion(CRGB color) {
  static uint8_t brillo = 10;
  static int8_t direccion = 2;
  fill_solid(leds, NUM_LEDS, color);
  FastLED.setBrightness(brillo);
  brillo += direccion;
  if (brillo >= BRILLO_MAX || brillo <= 10) direccion = -direccion;
}

// Animación 2: arcoíris en movimiento
void arcoiris() {
  static uint8_t inicioHue = 0;
  fill_rainbow(leds, NUM_LEDS, inicioHue, 255 / NUM_LEDS);
  inicioHue++;
  FastLED.setBrightness(BRILLO_MAX);
}

// Animación 3: destellos aleatorios (twinkle)
void destellos() {
  fadeToBlackBy(leds, NUM_LEDS, 10);
  if (random8() < 80) {
    leds[random16(NUM_LEDS)] = CHSV(random8(), 200, 255);
  }
  FastLED.setBrightness(BRILLO_MAX);
}

/*
  STRETCH GOAL — fuera del alcance del piloto (ver T-038 arriba).
  Control por celular vía web server local (WiFi.softAP + WebServer.h)
  para cambiar color/patrón en tiempo real desde el teléfono.
  No incluido a propósito: el piloto llega hasta soldar + cargar/adaptar
  animaciones. Quien termine antes puede explorarlo en casa con ayuda de IA.
*/
```

**Nota para el bloque de personalización (T-040):** este firmware ya trae 3 animaciones base (respiración, arcoíris, destellos) que corresponden directamente a las 3 opciones de "patrón base" del worksheet de personalización en [[AGENDA-Y-EVALUACION-PILOTO]] — así que la conversación de "elegí tu patrón" en el taller mapea 1 a 1 con lo que el código ya soporta, sin que el instructor tenga que improvisar.

## Ver también

- [[BACKLOG]] (T-037, T-038, T-053) · [[AGENDA-Y-EVALUACION-PILOTO]] · [[SEGURIDAD-PILOTO]] · [[REVISION-EXPERTOS-2026-07-01]] · [[IDEAS-DE-PRODUCTO]]
