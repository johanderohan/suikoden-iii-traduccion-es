# Suikoden III — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/playstation-2/suikoden-iii)**.

Traducción al **español de España** de *Suikoden III* (PlayStation 2, 2002), el RPG de Konami de las
tres historias (Hugo, Chris y Geddoe) con el sistema Trinity Sight, que nunca salió en español.

Se ha traducido **desde la versión americana en inglés** (no desde el japonés), con una biblia de
términos propia para nombres, lugares, runas y objetos.

La traducción se reparte como **parche**: no incluye el juego. Necesitas tu propia copia de la
versión USA para aplicarlo.

## Estado

Última versión: **[v1.0.3 — Correcciones de texto y de género](../../releases/tag/v1.0.3)**.

v1.0.3 corrige tres errores avisados por un jugador y los parecidos que aparecieron al revisar:

- opciones y avisos que salían pegados al nombre del objeto («AceptoGuion 2» → «Aceptar Guion 2»);
- la condición de victoria «Sobrevivir \_x\_ turnos» de las guerras (el marcador también sale tal
  cual en el original inglés) pasa a «Sobrevivir varios turnos»;
- personajes que hablaban en el género equivocado (Salome, Cecile, Lilly, Sharon, Mua...) y
  tratamientos mal dirigidos: 25 líneas corregidas tras extraer del juego quién dice cada frase de
  8.300 diálogos de escena. No cubre las elecciones del jugador, los PNJ de pueblo ni los minijuegos.

v1.0.2 no cambiaba la traducción respecto a v1.0: solo hizo el parche pequeño (1,6 MB) y rápido.

| Parte | Estado |
|---|---|
| Diálogos de las tres historias, escenas y PNJ | Traducidos (unas 33.500 entradas revisadas) |
| Menús, objetos, runas, habilidades, ayudas, tarjeta de memoria | Traducidos (12.000 cadenas del ejecutable) |
| Nombres de enemigo en combate | Traducidos (sin tildes: esa fuente solo tiene ASCII) |
| Periódico, cartas, teatro, biblioteca, guerra, epílogos | Traducidos; no todos vistos en pantalla |
| Texto dentro de imágenes | 80 rótulos rehechos (menús, Estado, combate, mapa del mundo) |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿ « »**, también al escribir el nombre |
| Revisión durante una partida | Parcial (ver abajo) |

Se mantienen a propósito el logotipo, la pantalla de título (START / CONTINUE), los vídeos y algunos
rótulos pequeños de las imágenes.

### Comprobaciones y trabajo pendiente

Se ha jugado en emulador (PCSX2) desde partida nueva y tarjeta de memoria sin formatear:

- arranque, escritura del nombre con letras españolas (Íñigo, Ñúñez), aviso de datos de Suikoden II
  y Trinity Sight;
- la introducción de Hugo completa en Karaya y la de Chris con el Consejo de Vinay del Zexay;
- herrería (mejorar el arma y pagar), guardado formateando la tarjeta, mapa del mundo;
- cinco combates con órdenes, runas y magia, objetos, mensajes, victoria y subida de nivel de Lulu;
- los menús (Objetos, Runas, Habilid., Equipo, Estado con perfil, Formac.) y Ajustes con todos sus
  valores; el combate, la herrería, el guardado y Ajustes se han comparado con las mismas pantallas
  del original en inglés.

Una auditoría automática comprueba en la imagen final los límites de memoria de cada zona, todos los
punteros, las tablas de sectores, las imágenes y la fuente. El parche se ha aplicado sobre el ISO USA
original y el resultado coincide byte a byte con la imagen probada.

**No se ha jugado el juego entero**: no se han visto en pantalla las guerras, los duelos, las tiendas
de compraventa, el castillo, el periódico ni los finales. Esos textos están traducidos y medidos
con las fuentes del juego, pero sin comprobar en partida. **No se ha probado en una PS2 real.**
La traducción y su revisión se han hecho con asistencia de IA, sin revisores humanos independientes.

Si encuentras un texto cortado, en inglés o un error, abre una incidencia con una captura.

## Cómo aplicar el parche

1. Descarga el parche `.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia del juego en versión **USA** (SLUS-20387), como imagen ISO completa.
3. **Comprueba que tu copia es la correcta** antes de nada:

   | | |
   |---|---|
   | Archivo | `Suikoden III (USA).iso` |
   | Tamaño | 4.295.000.064 bytes |
   | MD5 | `904a882671d0c1f1b8cc46c51ef473ff` |
   | SHA-1 | `e6d5afb003904c34fa18306c96e2982d92935490` |

   ```bash
   md5sum "Suikoden III (USA).iso"     # Linux
   md5 "Suikoden III (USA).iso"        # macOS
   CertUtil -hashfile "Suikoden III (USA).iso" MD5   # Windows
   ```

   Si no coincide, el parche fallará o dará un resultado corrupto.
4. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "Suikoden III (USA).iso" suikoden-iii-traduccion-es-v1.0.3.xdelta "Suikoden III (ES).iso"`
5. Para **v1.0.3**, comprueba que el ISO resultante tiene MD5 **`8b74ab3a16bbf54dd8da7db5cdcb5b2c`**
   (mismo tamaño que el original). Con v1.0.2 era `ee0d007d48d9edb2550a511257f27d56`.
6. Carga el ISO resultante en tu emulador (PCSX2) o en tu método habitual para PS2.

Aplica cada versión sobre el **ISO USA original**, no sobre uno ya traducido.

No se ha probado a continuar con partidas guardadas con la versión inglesa: empieza una partida nueva.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin relación alguna con
Konami. Aquí no se distribuye el juego ni ninguna parte de él: solo un parche que modifica una copia
que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia y lo hago.
