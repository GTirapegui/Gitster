# Hitster Chile (app propia)

App web para jugar con las cartas impresas de Hitster Chile: escaneas el QR con la cámara
dentro de la app, la canción suena en tu Spotify sin mostrar el nombre, y al final tocas
«Revelar» para ver año, título y artista.

Archivos: `index.html` (la app), `cards.js` (las 308 cartas), `manifest.json` e `icon.svg`
(para instalarla como app en el celular).

## Requisitos
- Cuenta **Spotify Premium** (Spotify la exige para apps de desarrollador y para controlar la reproducción).
- Cuenta de **GitHub** (gratis).

## Paso 1 · Subir la app a GitHub
1. Entra a https://github.com/new
2. En **Repository name** escribe `hitster-chile`.
3. Deja marcado **Public** y toca **Create repository**.
4. En la página del repo vacío, toca el enlace **uploading an existing file**.
5. Arrastra los 4 archivos (`index.html`, `cards.js`, `manifest.json`, `icon.svg`). Sube los archivos sueltos, no la carpeta.
6. Abajo toca **Commit changes**.

## Paso 2 · Activar GitHub Pages
1. En el repo, entra a **Settings** (pestaña de arriba).
2. En el menú izquierdo toca **Pages**.
3. En **Source** elige **Deploy from a branch**.
4. En **Branch** elige `main` y la carpeta `/ (root)`, y toca **Save**.
5. Espera 1 a 2 minutos y recarga. Arriba aparecerá la dirección:
   `https://gtirapegui.github.io/hitster-chile/`

## Paso 3 · Crear tu app en Spotify (para obtener el Client ID)
1. Entra a https://developer.spotify.com/dashboard e inicia sesión con tu cuenta Premium.
2. Acepta los términos si te los pide y toca **Create app**.
3. Completa:
   - **App name:** `Hitster Chile`
   - **App description:** `Juego Hitster casero`
   - **Redirect URIs:** pega `https://gtirapegui.github.io/hitster-chile/` (con la `/` final) y toca **Add**.
   - En **Which API/SDKs are you planning to use?** marca **Web API**.
4. Marca la casilla de términos y toca **Save**.
5. Dentro de la app, toca **Settings** y copia el **Client ID** (32 letras y números).

> La propia app te muestra el Redirect URI exacto en la primera pantalla, con botón para copiarlo.
> Tiene que coincidir letra por letra con el de Spotify.

## Paso 4 · Abrirla en el celular
1. En el celular abre `https://gtirapegui.github.io/hitster-chile/` en Chrome (Android) o Safari (iPhone).
2. Pega el **Client ID** y toca **Conectar con Spotify**. Acepta los permisos.
3. Instálala como app:
   - Android/Chrome: menú **⋮** → **Agregar a pantalla de inicio**.
   - iPhone/Safari: botón **Compartir** → **Agregar a inicio**.

## Paso 5 · Jugar
1. Abre la app de **Spotify** en el celular y reproduce cualquier canción un segundo (así aparece como dispositivo).
2. Vuelve a Hitster Chile y toca el punto de arriba a la derecha para elegir dónde suena (celular o parlante).
3. Toca **Escanear carta**, apunta al QR y la canción empieza sola.
4. Cuando todos apostaron, toca **Revelar respuesta**.
5. **Siguiente carta** para seguir.

Extras: **Carta al azar** (sin escanear, no repite cartas), **Por número** (escribes el # de la carta)
y **Empezar partida nueva** para reiniciar el conteo.

## Problemas comunes
- **«INVALID_CLIENT: Invalid redirect URI»**: el Redirect URI en Spotify no es idéntico al de la app (revisa la `/` final).
- **«No hay dónde reproducir»**: abre Spotify en el celular, dale play a algo y toca «Desde el inicio».
- **«se necesita Premium»**: la cuenta conectada no es Premium.
- **Otra persona quiere usarla con su Spotify**: en el dashboard de Spotify, en tu app, ve a **User Management** y agrega su correo (máximo 5 personas en modo desarrollo).
- **Spoiler**: la notificación de Spotify muestra la canción; no bajes la cortina de notificaciones mientras juegas.
