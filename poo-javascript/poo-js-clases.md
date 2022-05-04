# POO JS: Clases

> Classes are only syntactical sugar for constructor functions. Everything still works the same way!

![](<../.gitbook/assets/clases es6.gif>)

## Patron RORO

“Receive an object, return an object” (Recibe un objeto, devuelve un objeto).

Nos ayuda cuando tenemos muchos parámetros en nuestro constructor, ya que al instanciar la clase debemos acordarnos del orden de los parámetros y, además, no podemos tener parámetros por defecto.

No obstante, si recibimos un objeto, sí podemos poner parámetros por defecto y no recibir un parámetros si fuere el caso, sin que pase nada.\
A la hora de enviar los argumentos al instanciar la clase, también debe enviarse un objeto, y otra ventaja es que esos argumentos no hace falta que estén en el mismo orden que están los parámetros del constructor.
