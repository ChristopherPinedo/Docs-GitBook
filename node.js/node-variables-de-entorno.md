# 3. Variables de entorno

Las variables de entorno son una forma de llamar información de afuera a nuestro software.

Sirven para definir parámetros sencillos de configuración de los programas de modo que puedan ejecutarse en diferentes ambiente sin necesidad de modificar el código fuente de un script.

El objeto **process** nos da información sobre el procesos que está ejecutando este script.\
La propiedad **env** es la que nos da acceso a las variables de entorno de manera sencilla.

```javascript
let nombre = process.env.NOMBRE || 'Sin nombre'; 
let web = pnorocess.env.MI_WEB || 'no tengo web';
var apiKey = process.env.APIKEY || 'HF33o9oERVERVEEEEs';

console.log('Hola '+ nombre);
console.log('Mi web es '+ web);
```
