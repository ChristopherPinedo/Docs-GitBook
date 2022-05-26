# APIs de Web Components

### 1. Custom Elements

* Es la API que te permite definir la etiqueta usando un web component
* HTML 5 implico una mejora en semántica
  * Brinda nuevas etiquetas como ser `<header> <main> <section <footer>` las cuales mejoran temas como ser:
    * Accesibilidad
    * Marcar secciones el código de una mejor forma
    * Mejorar la lectura del código
  * Actualmente se sigue aumentando el standard
    * Eso implica que si generamos etiquetas propias puede haber un conflicto de nombres
* Para evitar el problema de colisión de nombres se debe nombrar los elementos con dos palabras `my-component`
  * Debido a que el standard sigue la regla que las nuevas etiquetas que se introducen son con solo una palabra

### 2. Shadow DOM

* No es una alternativa al virtual DOM
* La etiqueta `video` cuenta con Shadow DOM
  * Esta etiqueta cuenta con cosas programadas como ser
    * Botones de play, pausa y agrandar
    * Barras interactivas como ser el avance del video y el volumen del mismo
    * Estilos propios
  * Los estilos nunca tendrán un conflicto con nuestros estilos debido a que está usando el shadow DOM
* Es decir que el código vive dentro del shadow DOM y no coexiste con el código de afuera
  * Resolviendo el problema de conflictos con los estilos

### 3. HTML Template

* Es una etiqueta de HTML
* No se puede usar directamente con HTML
  * Se debe usar JS para utilizarla
* Regresa un `document fragment`
  * Es un fragmento, parte del document que necesita ser clonado para ser renderizado
* Utilizar esta etiqueta hace que todo el contenido no se muestre
  * Nos da performance, porque no se renderiza directamente

### 4. ES Modules

* Nos permite re utilizar el código de otros archivos
* HTML Imports
  * Importaba el contenido HTML de otro
  * Pero no fue standard
