# W3Reproductor

Visor de repeticiones (*replays*) `.w3g` de **Warcraft III**, enfocado en partidas de **Survival Chaos**. Es una página HTML autocontenida (sin dependencias ni build): se abre directamente en el navegador.

## Uso

1. Abrí `Nuevo Documento de texto.html` en un navegador moderno (Chrome, Edge o Firefox).
2. Hacé clic en **Cargar Replay** o arrastrá un archivo `.w3g` a la ventana.
3. Usá los controles de la barra inferior para reproducir, pausar y moverte por la línea de tiempo.

## Controles

| Acción | Control |
|---|---|
| Reproducir / pausar | Botón ▶/⏸ o barra espaciadora |
| Adelantar / retroceder 5s | Flecha derecha / izquierda |
| Adelantar / retroceder 30s | Shift + flecha derecha / izquierda |
| Velocidad de reproducción | Botones ¼x, ½x, 1x, 2x, 4x, 8x |
| Zoom del mapa | Rueda del mouse, o botones ＋ / － / ⊙ |
| Mover la vista | Arrastrar con el mouse sobre el área del mapa |
| Pantalla completa | Botón ⛶ |

## Cómo funciona

El visor lee el archivo `.w3g`, descomprime sus bloques de datos (`DecompressionStream`) y extrae:

- Los jugadores, sus equipos y colores de slot.
- Las acciones relevantes para Survival Chaos (entrenar/investigar, dirigir ataques de torre, chat, etc.).

Luego dibuja en un `<canvas>` un indicador por jugador que se anima según sus acciones a medida que avanza la línea de tiempo.

## Requisitos

Un navegador con soporte para `DecompressionStream` (Chrome/Edge 80+, Firefox 113+). No requiere instalación ni servidor: es un único archivo HTML.
