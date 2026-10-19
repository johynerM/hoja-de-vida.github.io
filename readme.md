# Hoja de vida web · Johyner Martinez
 
Sitio personal con mi hoja de vida, mis proyectos y algunas cosas que me gustan. Está hecho solo con HTML y CSS (sin JavaScript), con diseño responsive: se ve bien en celular, tablet y computador.

## Páginas
 
| Página | Archivo | Qué contiene |
|---|---|---|
| Inicio | `index.html` | Hoja de vida: perfil, habilidades, contacto y redes |
| Proyectos | `proyectos.html` | Mis proyectos: LaCueva, Gimnasio ForceTech y Organizador de horario |
| Más sobre mí | `personalidad.html` | Mis gustos, datos curiosos con animaciones CSS y mi historia de aprendizaje |
 
Las tres páginas comparten el mismo menú de navegación y un único archivo de estilos: `style.css`.

## Mockups
 
Cada mockup tiene marcadas las áreas del grid (`grid-template-areas`) y explica en qué ancho cambia el diseño.

## Breakpoints
 
El diseño es **Mobile First**: el CSS base es para celular y las `@media (min-width: …)` van al final del archivo, de menor a mayor.
 
- **Base (celular, menos de 600px):** todo en una sola columna. El orden es encabezado, banner, menú, contenido y pie. La foto de perfil va encima del nombre, el menú tiene los enlaces apilados y las tarjetas se muestran de a una.
- **Desde 600px (tablet):** el encabezado pasa a fila, con la foto a la izquierda del texto. El menú se vuelve horizontal, el banner y el título crecen, hay más espacio interior y el botón del formulario deja de ocupar todo el ancho.
- **Desde 1024px (computador):** el grid pasa a dos columnas (`18rem 1fr`) con estas áreas:
```css
  grid-template-areas:
      "encabezado banner"
      "menu       principal"
      "pie        pie";
```
 
  El menú queda a la izquierda y se mantiene visible al bajar (`position: sticky`). El encabezado y el banner quedan lado a lado, con la misma altura, y el contenido ocupa la columna derecha.
 
Además, las tarjetas usan `repeat(auto-fit, minmax(15rem, 1fr))`, así que se acomodan solas según el espacio disponible. El contenido tiene un ancho máximo de `62rem` y está centrado.

## Fuentes consultadas
 
- Documentación oficial de GitHub: [Configuring a publishing source for your GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)