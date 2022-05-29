# 2.1. Componentes

Son piezas de codigo independientes y reusables, ellos sirven para el mismo proposito que las funciones JS pero trabajan de forma isolada (En react retornar html).

### Composicion de componentes (Pensando en react)

#### Paso 1: Divide la interfaz de usuario en una jerarquía de componentes <a href="#step-1-break-the-ui-into-a-component-hierarchy" id="step-1-break-the-ui-into-a-component-hierarchy"></a>

Lo primero que vas a querer hacer es dibujar cajas alrededor de cada componente (y subcomponente) en el mock y darles nombres a todos ellos. Si trabajas con un diseñador, probablemente ya lo hayan hecho ¡Así que ve a hablar con ellos! ¡Los nombres de sus capas de Photoshop podrían terminar siendo los nombres de tus componentes de React!

¿Pero cómo sabes qué debería ser su propio componente? Usa las mismas técnicas para decidir si deberías crear una función u objeto nuevo. Una técnica es el [principio de responsabilidad única](https://es.wikipedia.org/wiki/Principio\_de\_responsabilidad\_%C3%BAnica), esto significa que un componente debe, idealmente, hacer solo una cosa. Si termina creciendo entonces debería ser dividido en componentes más pequeños.

#### Paso 2: Crea una versión estática en React <a href="#step-2-build-a-static-version-in-react" id="step-2-build-a-static-version-in-react"></a>

Para construir una versión estática de tu aplicación que muestre tu modelo de datos vas a necesitar construir componentes que reusen otros componentes y pasen datos usando _props_. _props_ son una forma de pasar datos de un padre a su hijo. Si estás familiarizado con el concepto de _estado_, **no uses para nada el estado** para crear esta versión estática. El estado está reservado para interactividad, esto es, cuando los datos cambian a través del tiempo.

#### Paso 3: Identificar la versión mínima (pero completa) del estado de tu interfaz de usuario <a href="#step-3-identify-the-minimal-but-complete-representation-of-ui-state" id="step-3-identify-the-minimal-but-complete-representation-of-ui-state"></a>

Pensemos cuales son parte del estado. Hazte estas tres preguntas por cada pieza de información:

1. ¿Viene del padre como props? Entonces probablemente no sea estado.
2. ¿Se queda sin cambios con el tiempo? Entonces, probablemente no sea estado.
3. ¿Puedes calcularlo con base a otro estado o prop en tu componente? Entonces, no es parte del estado.

#### Paso 4: Identificar dónde debe vivir tu estado <a href="#step-4-identify-where-your-state-should-live" id="step-4-identify-where-your-state-should-live"></a>

Para cada parte del estado de tu aplicación:

* Identifica qué componentes muestran algo con base a este estado.
* Busca un componente común a estos más arriba en la jerarquía.
* Este componente o uno más arriba en la jerarquía debería poseer el estado.
* Si no puedes encontrar un componente en el que tenga sentido manejar el estado, crea un nuevo componente solo para guardar el estado y ubícalo dentro de la jerarquía en algún lugar por encima de los componentes que lo necesitan.

#### Paso 5: Agregar flujo de datos inverso <a href="#step-5-add-inverse-data-flow" id="step-5-add-inverse-data-flow"></a>

Hemos creado una aplicación que funciona correctamente como una función de los props y estado fluyendo hacia abajo en la jerarquía. Es momento entonces de empezar a soportar que los datos fluyan en el otro sentido
