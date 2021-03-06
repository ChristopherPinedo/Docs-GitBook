# 4.2.1. Reducer



**¿Qué es un reducer?**

* Son una herramienta que nos permite declarar todos los posibles estados de nuestra App para llamarlos de forma declarativa.
* Necesitan 2 objetos esenciales: los estados compuestos y las acciones.

**Los estados compuestos:**

* Son un objeto donde van a vivir como propiedades todos nuestros estados

**Acciones**

* Responsables, al ser disparados, de pasar de un estado a otro.
* Este objeto tiene 2 propiedades: action type y action payload.

**Action type:**

* Define el nombre clave para encontrar el nuevo estado.

**Action payload:**

* Es opcional e importante con estados dinámicos. Un estado es dinamico cuando depende del llamado de un API, de lo escrito por el usuario en un input, etc. Estos son estados dinámicos y los recibimos con un payload.

**Flujo de trabajo:**

* Definimos distintos tipos de acciones con type y payload.
* Enviamos estas acciones a nuestro reducer.
* El reducer define los posibles estados por donde pasara nuestra App.
* Con action type elegimos cual de esos estados queremos disponer con el cambio o evento del usuario.
* Con action payload damos dinamismo a dicho estado. Será el mismo estado pero le daremos características especiales
