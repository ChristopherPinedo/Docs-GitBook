# Node: Herramientas utiles

## **Desarrollo**

**Nodemon:**&#x20;

Permite tener procesos que ejecutandose automaticamente.

nodemon + archivo al que quiero acceder detecta cambios, y ejecuta el código.

```bash
npm install -g nodemon
```

* [Nodemon](https://nodemon.io)

## **Producción**

**PM2:**

Es un demonio administrador de procesos que me puede ayudar a administrar y mantener mi aplicación 24/7.

* Voy a poner monitorizar el código para saber si algo se rompe.
* Me permite ver dashboards de mi código, puedo ver que está corriendo.
* Puedo ver el rendimiento de mi cpu
* Con: pm2 stop + id —> me detiene el proceso que está en ejecución con ese ID.

```bash
npm install -g pm2
```

[PM2](https://pm2.keymetrics.io)
