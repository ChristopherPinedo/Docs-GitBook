# Redux

### Definición

Sistema que ayuda a mantener y modificar el estado de la aplicacion

### ¿Que necesitamos?

* Donde almacenar
  * Store
* Como acceder
  * Selectores
* Como actualizar
  * Actions
  * Reducers

Principios

* Unica fuente de verdad (store)
* El estado es de solo lectura (actions)
* Los cambios deben realizarse a traves de funciones puras (reducers)

### Glosario

1.  **Funciones puras**

    El resultado de una funcion pura dependera unicamente de lo que le pase como parametros, no va a consultar variables externas.

    Caracteristicas:

    1. Valor retornado cambia si la funcion cambia
    2. Misma entrada, misma salida
    3. Sin efectos colaterales

