# SnetForever

Guía de leveo 1-60 y compañero con IA para **WoW Forever**: addon para el juego y una pequeña app de Windows.

- **Guía paso a paso** para todas las razas y facciones (Skyborne incluida), con flecha, pines en el mapa (también en OpenMap) y cadenas de clase completas.
- **Objetivos cercanos**: botones para poner en el objetivo, con una estrella, a los enemigos y PNJ de la misión.
- **Chat con IA dentro del juego**, con tu propia suscripción de Claude o de ChatGPT. Te arma rutas de zona solo con misiones que existen de verdad.
- **Se actualiza solo** y cada actualización va firmada.

> El addon nunca juega por ti: no pulsa teclas ni mueve al personaje.

## Descargar e instalar

1. Entra en **[Releases → la última versión](https://github.com/alvarezalain262-create/SnetForever/releases/latest)** y descarga **`SnetForever-Instalador-<versión>.exe`**. Solo ese archivo: los demás (`.snfpaq`, `manifiesto`, `.sig`) los usa la app para actualizarse sola.
2. Ábrelo. Windows puede enseñar una pantalla azul («Windows protegió su PC») porque el instalador no tiene firma de código: pulsa **«Más información» → «Ejecutar de todas formas»**. No pide permisos de administrador.
3. Sigue los pasos:
   - elige el idioma;
   - **Carpeta del juego**: el instalador busca solo la carpeta de WoW Forever (la que tiene `Wow.exe`, normalmente `...\World of Warcraft\_forever_`). Si no la encuentra, elígela con «Examinar». Si el juego está abierto, te pedirá cerrarlo;
   - **Chat con la IA**: comprueba si tienes Claude Code o Codex listos (mira más abajo).
4. Listo. Verás una **estrella dorada** en la bandeja de Windows (junto al reloj): es la app. Arranca sola con Windows.

### ¿Y el addon?

**No hay que bajarlo aparte: el instalador pone la app y el addon a la vez.** En el paso «Carpeta del juego» copia en `Interface\AddOns` los tres addons de SnetForever:

- `SnetForever`, el addon;
- `SnetForever_Rutas` y `SnetForever_Misiones`, sus datos;
- las ranuras de respuesta del chat.

En la lista de addons del juego salen agrupados bajo **SnetForever**, con la misma estrella. Después, la app mantiene el addon y los datos al día: cuando hay una versión nueva la descarga, comprueba la firma y la pone **cuando cierras el juego**. Lo que sustituye no se borra: va a una carpeta de cuarentena.

Dentro del juego:

- `/snet` abre el panel de ajustes;
- `/snet chat` abre el chat con la IA;
- `/snet fallo` envía un aviso de fallo.

## La cuenta de IA (para el chat)

El chat usa **tu suscripción**. SnetForever nunca te pide contraseñas, claves ni pagos. Sirve una de estas dos:

- **Claude Pro o Max**, con [Claude Code](https://claude.com/claude-code) instalado y la sesión iniciada. Es la opción más sencilla.
- **ChatGPT**, con Codex CLI instalado (`npm install -g @openai/codex`, necesita Node.js) y la sesión iniciada (`codex login`).

¿Y si tengo la cuenta gratis?

| Cuenta gratis | ¿Sirve? |
|---|---|
| **ChatGPT gratis** | **Sí.** OpenAI incluye Codex también en el plan gratis. Da poco uso: llegarás antes al límite, y el chat te dirá que esperes un rato. |
| **Claude gratis** | **No.** El plan gratis de Claude no incluye Claude Code. Hace falta Pro o Max. |

Si no tienes Claude de pago, la forma gratis de usar el chat es Codex con una cuenta de ChatGPT.

Una cuenta de **pago por uso** (Console de Anthropic o una clave de API de OpenAI) **no sirve**, y la app te lo dice.

### Si te creas la cuenta después de instalar

No hace falta reinstalar nada:

1. Instala Claude Code e inicia sesión: abre Terminal, escribe `claude`, pulsa Intro y luego escribe `/login`. Con ChatGPT: `codex login`.
2. La app lo detecta sola en menos de 30 minutos. Si no quieres esperar, haz **clic derecho en la estrella de la bandeja → «Comprobar Claude Code / Codex»**, o vuelve a abrir SnetForever.

Sin cuenta, todo lo demás funciona igual (la guía, la flecha, el mapa, los objetivos). Solo el chat te dirá qué falta y cómo arreglarlo.

## Desinstalar

Desde **Configuración → Aplicaciones → SnetForever → Desinstalar**. No se borra nada: el programa, el addon y los accesos directos van a una carpeta de cuarentena, de donde se pueden recuperar.

## Licencias

- La app y el addon: MIT.
- Las rutas: CC BY-NC-SA 4.0, derivadas de las guías de RestedXP; no están respaldadas por RestedXP.
- Los datos de misiones: de QuestieDB (GPLv3).

El detalle está en `LICENCIAS.txt`, dentro de la instalación.

---

## English (short)

**SnetForever** is a 1-60 leveling guide plus an in-game AI companion for **WoW Forever**.

1. Download **`SnetForever-Instalador-<version>.exe`** from [the latest release](https://github.com/alvarezalain262-create/SnetForever/releases/latest) and run it. If SmartScreen warns you, choose «More info → Run anyway».
2. The installer installs **both the Windows app and the addon** into your WoW Forever `Interface\AddOns` folder. After that, the app keeps the addon and its data up to date (signed updates, applied when the game is closed).
3. The AI chat uses your own **Claude Pro/Max** (with Claude Code) or **ChatGPT** (with Codex CLI) account. A **free ChatGPT** account works too (with lower usage limits); the **free Claude** plan does not include Claude Code. Pay-as-you-go API accounts are not supported.
4. If you sign in after installing, right-click the tray star and choose «Check Claude Code / Codex», or just wait: the app checks every 30 minutes.
