FLAG BATTLE
===========

ESPAÑOL
-------

Descripción
-----------
Flag Battle es un juego de eliminación en el que el jugador selecciona,
entre cuatro banderas, la que considera más bonita. Las elecciones de todos
los jugadores alimentan un ranking global.

Funcionamiento del juego
------------------------
1. Al comenzar una partida, se cargan las 195 banderas desde Supabase.
2. Se seleccionan aleatoriamente 64 banderas para esa partida.
3. Las 64 banderas compiten en una eliminatoria:
   - Ronda 1: 64 → 16
   - Ronda 2: 16 → 4
   - Ronda 3: 4 → 1
4. En cada grupo aparecen cuatro banderas.
5. El jugador elige una.
6. La bandera elegida avanza a la siguiente ronda.
7. La bandera ganadora de la eliminatoria se muestra al finalizar la partida.

Ranking global
--------------
Cada elección se registra en Supabase mediante la función `record_choice()`.
El sistema utiliza una puntuación ELO para valorar las banderas.

El ranking es compartido entre todos los jugadores: las elecciones realizadas
por un jugador modifican las puntuaciones que posteriormente verán los demás.

La sección Ranking permite ordenar las banderas por:
- ELO
- Victorias
- Porcentaje de victorias

Estadísticas
------------
La sección Estadísticas consulta Supabase y muestra información de la bandera
que actualmente ocupa la primera posición por ELO, incluyendo:
- ELO
- Victorias
- Derrotas
- Partidas

Idiomas
-------
La aplicación permite seleccionar:
- ES — Español
- EN — English

La selección de idioma se guarda en el dispositivo mediante `localStorage`.

Los nombres de los países también se muestran en el idioma seleccionado.

Navegación
----------
La barra inferior contiene tres opciones:
- Jugar
- Ranking
- Estadísticas

La antigua opción Favoritos ha sido eliminada.

Datos y backend
---------------
Frontend:
- HTML
- CSS
- JavaScript
- Emojis Unicode para representar las banderas

Backend:
- Supabase

Proyecto Supabase:
https://wcvktwqbvzgccqlvbuln.supabase.co

La aplicación utiliza la Publishable Key de Supabase desde el navegador.
No utiliza la `service_role` key.

Catálogo
--------
El catálogo contiene 195 banderas:
- 193 Estados miembros de Naciones Unidas
- Palestina
- Vaticano (Santa Sede)

La aplicación comprueba que Supabase contiene exactamente 195 registros.

Fallback
--------
Si Supabase no está disponible temporalmente, la aplicación dispone de un
catálogo local de las 195 banderas para poder iniciar el juego.

En ese caso, las elecciones no pueden actualizar el ranking global hasta que
la conexión con Supabase vuelva a estar disponible.

Publicación
-----------
La aplicación está diseñada para ejecutarse como una página web estática,
por ejemplo mediante GitHub Pages.

Para actualizarla:
1. Sustituir `index.html` en el repositorio de GitHub.
2. Hacer Commit changes.
3. Esperar a que GitHub Pages publique la nueva versión.
4. Abrir la URL de la aplicación en Safari o Chrome.


ENGLISH
-------

Description
-----------
Flag Battle is an elimination game in which the player chooses, from four
flags, the one they consider the most beautiful. All players' choices
contribute to a shared global ranking.

Game flow
---------
1. When a game starts, the 195 flags are loaded from Supabase.
2. 64 flags are selected randomly for that game.
3. The 64 flags compete in an elimination tournament:
   - Round 1: 64 → 16
   - Round 2: 16 → 4
   - Round 3: 4 → 1
4. Four flags are displayed in each group.
5. The player selects one flag.
6. The selected flag advances to the next round.
7. The tournament winner is displayed at the end of the game.

Global ranking
--------------
Each choice is recorded in Supabase through the `record_choice()` function.
The system uses an ELO score to rank the flags.

The ranking is shared by all players: choices made by one player modify the
scores that other players will subsequently see.

The Ranking section can sort flags by:
- ELO
- Wins
- Win rate

Statistics
----------
The Statistics section queries Supabase and displays information about the
flag currently ranked first by ELO, including:
- ELO
- Wins
- Losses
- Games

Languages
---------
The application supports:
- ES — Español
- EN — English

The selected language is stored on the device using `localStorage`.

Country names are also displayed in the selected language.

Navigation
----------
The bottom navigation bar contains three options:
- Play
- Ranking
- Statistics

The former Favorites option has been removed.

Data and backend
----------------
Frontend:
- HTML
- CSS
- JavaScript
- Unicode emojis to represent flags

Backend:
- Supabase

Supabase project:
https://wcvktwqbvzgccqlvbuln.supabase.co

The application uses the Supabase Publishable Key from the browser.
It does not use the `service_role` key.

Flag catalogue
--------------
The catalogue contains 195 flags:
- 193 United Nations Member States
- Palestine
- Vatican City (Holy See)

The application checks that Supabase contains exactly 195 records.

Fallback
--------
If Supabase is temporarily unavailable, the application contains a local
catalogue of all 195 flags so that the game can still start.

In this situation, choices cannot update the global ranking until the
connection to Supabase is restored.

Deployment
----------
The application is designed to run as a static web page, for example through
GitHub Pages.

To update the application:
1. Replace `index.html` in the GitHub repository.
2. Click Commit changes.
3. Wait for GitHub Pages to publish the new version.
4. Open the application URL in Safari or Chrome.
