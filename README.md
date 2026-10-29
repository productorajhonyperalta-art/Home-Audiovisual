# HOME — Audiovisual Checkout

Aplicación web instalable (PWA) para inventario audiovisual, preparación de maletas y control de devolución.

## Funciones
- Inventario local de equipos propios, alquilados o prestados.
- Fotos desde cámara o galería; imágenes comprimidas y guardadas localmente.
- Cantidades agrupadas o unidades identificadas mediante etiquetas/códigos.
- Rodajes con fecha, cliente, responsables y notas.
- Maletas/sets personalizados con selección de equipos del inventario.
- Plantillas reutilizables de maletas y rodajes.
- Checklist de devolución con cantidades encontradas, faltantes, dañadas y pendientes.
- Cierre explícito completo o con incidencias; no cierra si quedan unidades pendientes.
- Acta de devolución imprimible / guardable como PDF desde el navegador.
- Copia JSON restaurable que incluye fotografías.
- IndexedDB y caché PWA para trabajo sin conexión tras la primera carga.

## Cómo usarla en Android
1. Descomprime el ZIP en una carpeta.
2. Publica la carpeta en un hosting HTTPS estático (por ejemplo GitHub Pages) o ejecútala en `localhost` durante pruebas. La instalación PWA y el modo offline no funcionan correctamente abriendo `index.html` directamente como `file://`.
3. Abre la dirección HTTPS con Chrome.
4. Menú ⋮ → **Instalar aplicación** o **Añadir a pantalla de inicio**.
5. Entra a Ajustes y descarga una copia de seguridad después de cargar tu inventario.

## Privacidad y límites
- No hay cuentas, nube ni sincronización entre dispositivos.
- Los datos viven en el almacenamiento del navegador/dispositivo. No borres los datos del sitio ni desinstales la app sin exportar una copia.
- Para generar el PDF se abre la ventana de impresión del navegador; elige **Guardar como PDF**.
- HOME no actualiza automáticamente las cantidades del inventario general al devolver un rodaje: mantiene el inventario maestro separado de las cantidades asignadas a cada salida.
- Las plantillas guardan referencias y cantidades de equipo. Las actas históricas guardan una instantánea de la descripción y foto del equipo al preparar el rodaje.

## Archivos
- `index.html`: estructura de la app.
- `styles.css`: diseño responsive.
- `app.js`: lógica y base de datos local.
- `manifest.webmanifest`: instalación PWA.
- `sw.js`: caché de la app shell.
