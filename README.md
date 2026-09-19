# ThinkingInPortals

Cinco simulaciones interactivas sobre la física real detrás de las mecánicas de *Portal* (2007). Parte de **Bitácora Glitch** (v0raonline.substack.com).

**[→ Ver la landing en vivo](https://v0raonline.github.io/ThinkingInPortals/)** *(activa GitHub Pages para que este enlace funcione — ver más abajo)*

## Qué es esto

Una puerta-portal de entrada seguida de cinco demos jugables, cada una centrada en una mecánica concreta: ajustas parámetros, sueltas el objeto, y compruebas tú mismo qué se conserva y qué no. No es una guía para pasarte el juego ni un curso de física — es "compruébalo tú mismo".

## Estructura

| Carpeta | Simulación | Tesis |
|---|---|---|
| `index.html` | Landing (puerta-portal + las cinco tarjetas) | — |
| `01-conservacion-rapidez/` | Conservación de velocidad | La magnitud de la velocidad no cambia. La dirección sí. |
| `02-trayectorias/` | Trayectorias y ángulo de disparo | La velocidad no elige el camino. El ángulo, sí. |
| `03-esfera-energia/` | Redirección de la esfera de energía | Esta no cae. Solo cambia de dirección. |
| `04-fling-cadena/` | Fling en cadena / caída infinita | Con un salto no llega. Encadenando, sí. |
| `05-velocidad-terminal/` | Velocidad terminal (contraste real) | Sigue cayendo. Has dejado de acelerar. |

Cada simulación es un HTML autocontenido — sin build, sin frameworks, sin dependencias más allá de Google Fonts. Cada una incluye:

- Lectura de resultados en vivo (velocidad, ángulo, distancias)
- Objetivo con bandera/plataforma en posición aleatoria (fija por carga de página, no por intento), con margen de precisión
- Convención de color: **naranja = acierto, azul = fallo**
- Mensajes de resultado con tono de laboratorio de pruebas, rotando entre varias frases
- Barra de navegación (pills) para saltar directamente a cualquier otra simulación, y enlace "← Inicio" a la landing
- Footer con enlaces a GitHub, licencia y al artículo hermano en Bitácora Glitch
- Cabecera legal, `meta description` y Open Graph completos en cada página
- Soporte `prefers-reduced-motion` y temas claro/oscuro automáticos

## Tecnología

Vanilla HTML + CSS + JS. Sin paso de compilación. Pensado para servirse tal cual desde GitHub Pages.

## Publicar con GitHub Pages

1. **Settings → Pages → Source: Deploy from a branch**
2. Branch: `main`, carpeta `/ (root)`
3. La landing queda accesible en `https://v0raonline.github.io/ThinkingInPortals/`, y cada simulación en `https://v0raonline.github.io/ThinkingInPortals/01-conservacion-rapidez/` (etc.)

## Artículos

**[Aprender a pensar en portales](https://v0raonline.substack.com/p/aprender-a-pensar-en-portales)** — artículo 1, hermano de la demo de conservación de velocidad. El resto de simulaciones tendrán su propio artículo; los enlaces se añadirán a medida que se publiquen.

## Backlog

- **Interruptor para forzar animaciones** cuando el sistema tiene activado `prefers-reduced-motion` pero la persona quiere verlas igualmente (esto puede activarse sin que se pida realmente — modo ahorro de batería, ciertas actualizaciones de Windows). Implica sustituir los `@media (prefers-reduced-motion: no-preference)` de las seis páginas por una clase JS combinada con la preferencia del sistema, guardada en `localStorage`. No es trivial: toca las seis páginas, una por una.

## Licencia

[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) — Reconocimiento-NoComercial. Puedes explorar, copiar y construir sobre este trabajo libremente, con atribución a V0ra / Bitácora Glitch. No se permite el uso comercial. Ver [LICENSE](LICENSE).
