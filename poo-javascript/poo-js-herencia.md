# 4.3. Herencia

Cuando observemos 👀 en nuestras clases o en el proceso de abstracción que hay clases que pueden compartir atributos, métodos (o simplemente porque la lógica del negocio nos lo indica).&#x20;

Podemos abstraer aun más nuestras clases y crear así las Suuuuuuper clases. Estas serán moldes que nos permitirán “heredar” atributos y métodos a nuestras sub-clases.

No lo olviden, DRY(Don’t Repeat Yourself). Mejor utiliza una SUUUUPEEER Class.



### **Super**

\
La palabra clave super es usada para acceder y llamar funciones del padre de un objeto.

Las expresiones super.prop y super\[expr] son válidas en cualquier definición de método tanto para clases como para objetos literales (en-US).

**Sintaxis**\
// llama al método constructor del objeto padre.\
super(\[arguments]);

// llama cualquier otro método del objeto padre.\
super.functionOnParent(\[arguments]);\
**Descripción**\
Cuando es usado en un constructor, la palabra clave super aparece sola lo cual invoca el constructor del objeto padre. En este caso debe usarse antes de que la palabra clave this sea usada. La palabra clave super también puede utilizarse para llamar otras funciones del objeto padre.\
\*\*\
Ejemplo\*\*\
Usando super en clases\
Este fragmento de código se toma del ejemplo de clases (demo en vivo). Aquí se llama a super() para evitar la duplicación de las partes del constructor que son comunes entre Rectangle y Square.

```javascript
class Rectangle {
  constructor(height, width) {
    this.name = 'Rectangle';
    this.height = height;
    this.width = width;
  }
  sayName() {
    console.log('Hi, I am a ', this.name + '.');
  }
  get area() {
    return this.height * this.width;
  }
  set area(value) {
    this.height = this.width = Math.sqrt(value);
  }
}

class Square extends Rectangle {
  constructor(length) {
    this.height; // ReferenceError, super necesita ser llamado primero!

    // Aquí, llama al constructor de la clase padre con las longitudes
    // previstas para el ancho y la altura de Rectangle
    super(length, length);

    // Nota: En las clases derivadas, se debe llamar a super() antes de
    // poder usar 'this'. Salir de esto provocará un error de referencia.
    this.name = 'Square';
  }
}va
```
