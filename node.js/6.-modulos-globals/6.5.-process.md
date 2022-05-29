# Modulos: Process



El objecto process es una instancia de `EventEmitter`; podemos suscribirnos a el para escuchar eventos de node.

*   **UncaughtException**: Permite capturar cualquier error que no fue caputurado previamente. Esto evita que Node cierre todos los hijos al encontrar un error no manejado.

    ```js
    process.on('uncaughtException', (error, origen) => console.log(error, origen));
    ```
*   **exit**: Se ejecuta cuando node detiene el `eventloop` y cierra su proceso principal.

    ```js
    process.on('exit', () => console.log('Adios'));
    ```
