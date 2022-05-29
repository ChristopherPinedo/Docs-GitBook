# 6.1. File system

Provee una API para interactuar con el sistema de archivos cerca del estándar POSIX.\
POSIX es el estándar para interfaces de comando y shell, las siglas las significan: “Portable Operating System Interface for uniX”.

El file system nos permite acceder archivo del sistema, leer, modificar., escribirlos, es muy útil para precompiladores, para lo que requiera hacer grabados de disco, o bases de datos en node requieren un uso intensivo de Node.Todo lo que hagamos con modulos por buenas prácticas son asincronos, pero tienen una version sincrona no recomendada pues pordría bloquear el event loop con más facilidad.

Para ver más sobre la documentación de FileSystem:

* [FileSystem Docs](https://nodejs.org/dist/latest-v12.x/docs/api/fs.html#fs\_file\_system)
