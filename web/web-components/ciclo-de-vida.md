# Ciclo de vida

* **constructor:** Directamente desde el JavaScript Engine, el constructor nos servirá para definir y cargar todas las variables en memoria que necesitemos, **es mala práctica pintar el componente aquí**
* **connectedCallback:** Cuando el componente ya está pintado dentro del DOM ypodemos hacer uso de él.
* **attributeChangedCallback:** Cuando un atributo de nuestro componente cambia
* **disconnectedCallback:** Cuando el componente se “destruye” o se quita del DOM
* **adoptedCallback:** Cuando el componente es movido a un nuevo DOM, básicamente cuando es pintado desde un iframe por ejemplo
