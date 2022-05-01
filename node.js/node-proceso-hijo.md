# Node: Proceso hijo

El módulo de procesos secundarios de Node.js (**child\_process**) tiene dos funciones **spawn** y **exec**, mediante las cuales podemos iniciar un proceso secundario para ejecutar otros programas en el sistema.

La diferencia más significativa entre child\_process.spawn y child\_process.exec está en lo que spawn devuelve un stream y exec devuelve un buffer.

* Usa **spawn** cuando quieras que el proceso hijo devuelva datos binarios enormes a Node.
* Usa **exec** cuando quieras que el proceso hijo devuelva mensajes de estado simples.
* Usa **spawn** cuando quieras recibir datos desde que el proceso arranca.
* Usa **exec** cuando solo quieras recibir datos al final de la ejecución.vajs

Podemos llamar a `exec` para ejecuciones sencillas:

```javascript
const { exec } = require('child_process')
exec('ls', (e, stdout) => {
    (e) ?
    console.log(e) :
    console.log(stdout)
})
```

Podemos llamar a `spawn` para obtener el proceso: _La ventaja de este enfoque es que obtienes mayor control del proceso, y del estado en el que se encuenta_

```javascript
const { spawn } = require('child_process')
const myprocess = spawn('ls')

process.stdout.on("data", data => console.log(data.toString()));
process.on("exit", () => console.log("process end"));
```
