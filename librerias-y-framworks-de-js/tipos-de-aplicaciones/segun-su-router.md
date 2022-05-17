# Según su router

## SSR (Server Side Rendering) - Viejo

El backend tomaba una plantilla de HTML, le daba los datos que se requerían en cada petición y lo enviaba al navegador.

El backend no le dice al navegador como interactuar con el usuario. Este solo recibe HTML con la información requerida.

Cuando el usuario interactuaba se recarga la página con cada nueva información enviada desde backend.

El script contenido no se encarga de render o actualizar nuestra app, solo para cosas como animaciones o menús.



## SPA(Single page appliction) y CSR(Client Side Rendering)

Con la invención del CSR y las API empezamos a renderizar todo con el JS en el navegador.

El servidor enviaba un HTML que solo incluía la petición a nuestro JS y CSS.

Una vez descargado el JS, empezaba a renderizar nuestra App. Lento al inicio rápida después.

No necesita recargarse pues al necesitar información del backend lo hace con una consulta a una API.

### Hash Router y Browser Routing



## Progressive SSR

En lugar de enviar un documento HTML vació al navegador desde el backend se va enviar al navegador una versión HTML de nuestra app que los usuarios pueden ver mientras el navegador descarga el JS y vuelva a hacer render. Esta versión de la app se puede ver pero no tocar, los usuarios no pueden interactuar inmediatamente, como lo haría con una SPA. Pero cuando el navegador termina de descargar nuestras cosas convierte nuestra app en una SPA y los usuarios pueden interactuar a la velocidad de la luz.

## SSG (Static site generator)

Nos permite usar el SSR mientras estamos desarrollando nuestro sitio, pero compilamos en la etapa de desarrollo nos genera paginas estáticas que ya tienen cargado los datos que pediríamos al backend. Cuando hacemos deploy las app funcionan como SPA.
