# Pesca Cádiz

App web (PWA) de índice de pesca para playas de Cádiz. Sin dependencias ni compilación: HTML, CSS y JavaScript.

## Publicar en GitHub Pages
1. Crea un repositorio nuevo en github.com (por ejemplo `pesca-cadiz`).
2. Pulsa *Add file → Upload files* y sube todos los archivos de esta carpeta (sin la carpeta en sí).
3. En *Settings → Pages* elige *Deploy from a branch*, rama `main`, carpeta `/ (root)`.
4. Espera un minuto: tu app estará en `https://TU-USUARIO.github.io/pesca-cadiz/`.

## Instalar en el iPhone
Abre la URL en Safari → Compartir → *Añadir a pantalla de inicio*.

## Datos
- **En vivo (Open-Meteo, gratis para uso no comercial, sin clave):** viento, presión, oleaje, mar de fondo y temperatura del agua en un punto frente a cada playa. Si falla la conexión, la app avisa y usa datos simulados.
- **Estimada:** la marea (cálculo astronómico aproximado).
- **Pendiente:** IHM (mareas oficiales), AEMET (avisos) y EMODnet (batimetría). AEMET exige clave y no suele permitir llamadas directas desde el navegador, así que necesita un pequeño proxy (por ejemplo un Cloudflare Worker).
- Las coordenadas de `B` en `index.html` son aproximadas: ajústalas a tus puestos.
- El diario se guarda en el dispositivo (`localStorage`).
- Las playas interiores de la bahía (La Cachucha, La Ministra, El Conchal, Bocana del Río, La Casería, La Anegada) llevan el oleaje atenuado en el modelo, pero tienen corrientes de marea fuertes que el índice no mide.
- Si el modelo marino no tiene datos en el punto de una playa interior, usa los del punto marino más cercano con datos.
