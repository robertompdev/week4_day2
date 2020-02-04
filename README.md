# week4_day2

> MongoDB Queries
>
> Express basic app

## Main points: Express 

- Crear un servidor básico con rutas y archivos estáticos en Express supone:
  - Requerir Express
  - Instanciar la aplicación a partir de Express
  - Incluir el *middleware* de directorio con archivos estáticos `public`
  - Enrutar
  - Levantar el servidor
    ````javascript
    const express = require('express')
    const app = express()
    app.use(express.static('public'))
    app.get('/', (req, res) => res.send(`<h1>Hi there!</h1>`))
    app.listen(3000, () => console.log("Servidor levantado..."))
    ````
  
- Enrutar supone hacer uso del método `.get()`o `.post()` de la aplicación instanciada, recibiendo como argumentos:
  - Endpoint en formato de string.
  - Callback con los parámetros por defecto `req` (petición) y `res` (respuesta).
  
## Main points: Nodemon
- El módulo global Nodemon atiende a los cambios en un archivo, siendo iniciado mediante:
  - `nodemon`: escucha los cambios sobre el archivo indicado como *entry point* (propiedad `main`de `package.json`).
  - `nodemon`*`nombre_archivo`*: escucha los cambios realizados en el archivo indicado.
  
## Main points: objeto response
- El objeto `response` dispone de dos métodos para mostrar información en una ruta:
  - `.send()`: muestra el código pasado como argumento en el cliente.
  - `.sendFile()`: muestra en el cliente el archivo enlazado mediante el path absoluto argumentado.
  
## Additional resources
- El JSON de restaurantes compatible con las queries finales puede descargarse [desde este enlace](https://raw.githubusercontent.com/mongodb/docs-assets/primer-dataset/primer-dataset.json).

