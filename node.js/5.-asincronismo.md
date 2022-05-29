# Node: Asincronismo

## CallBack

Una funcion callback es una funcion que es pasada como argumento a otra funcion, para ser llamada(`called back`) en otro momento.\
La funcion que recibe como argumento otras funciones es denominada funcion de orden superior (higher-order function), esta contiene la logica correspondiente para ejecutar adecuadamente la funcion callback.

### Callback Hell

Los callback Hell se dan cuando empiezo a pasar una función como parámetro que a su vez llama a otra función como parámetro, y así hasta n.\
Una estrategia para trabajar con estas estructuras lógicas tan monolíticas es usar estructuras de control y funciones recursivas.

<mark style="color:green;">Las funciones recursivas</mark> se llaman así mismas y mediante la estructura de control le digo cuantas veces voy a necesitar llamar la función así misma

## Promise

Son una sintaxis mas elegante y legible de realizar callbacks, creando así un código mucho más escalable y entendible para todas las personas.

Una promesa al final no deja de ser un callback, solo que, con la novedad de tener estados, las promesas cuentan con 3 estados, resuelta, en progreso y en fallo.&#x20;

Para utilizar una promesa solo debemos de instanciar una nueva, una promesa en si es una función que recibe dos parámetros, resolve y reject, que son los dos estados de una promesa.

Utilizamos resolve para retornar el valor deseado cuando una función se ejecute y utilizamos reject para cuando una función retorna un valor no deseado.

Para poder obtener los valores que retorna una función debemos utilizar su propiedad .then, esta propiedad es una función que recibe un callback el cual tendrá como parámetro el valor retornado con resolve o reject.

Siempre que usemos una promesa además de realizar la propiedad .then debemos invocar la propiedad .catch, la cual es un callback que recibe como parámetro el error ocurrido en caso de haber sucedió uno.

## Async / Await

Es azucar sintactico, es decir, una forma muy legible y entendible de realizar código, un Async/Await no deja de ser una función asíncrona, la diferencia es que al usar esta sintaxis se podrá ver un código más legible.

Para usar correctamente esta sintaxis usamos Async para declarar una función asíncrona, cuando una función es asíncrona podremos usar dentro de su contexto el Await.

El Await es la manera en que le indicaremos a nuestro código que ha de “esperar” a que el evento al cual le indiquemos Await es importante para el proceso del código, por ende, para poder seguir ejecutando el proceso espere a que el evento se resuelva y retorne un valor.
