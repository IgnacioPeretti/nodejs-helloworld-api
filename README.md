# NodeJs, helloworld API for test propouses.

This is a simple API that returns a welcome message.

## Run your local environment

### Clone the repository
```bash
git clone https://github.com/edgaregonzalez/nodejs-helloworld-api.git
```

### Install dependencies
```bash
npm install
```

### Run the tests
```bash
npm test
```

### Start the server
```bash
npm start
```

### Make a request
```bash
curl http://localhost:3000
```


## GUIA DETALLADA DE COMO UTILIZAR EL JOB DE JENKINS.

1. **INSTALAR NGROK**

     - Comenzamos instalando NGROK, podremos encontrar una guía en [su sitio web](https://ngrok.com/download), donde ejecutaremos una serie de comandos para completar la instalación.

   
3. **Ejecutar NGROK para obtener nuestro entorno:**
   - Abre una terminal y ejecuta el siguiente comando para levantar Jenkins localmente a través de ngrok:
     ```sh
     ngrok http http://localhost:8080
     ```
   - Esto nos dará un enlace público que puedes utilizar para acceder a Jenkins.

4. **Accedemos a jenkins con NGROK y configuramos:**
   - Abre tu navegador web y dirígete al enlace proporcionado por ngrok. Por ejemplo:
     ```
     https://d56e-152-170-177-208.ngrok-free.app/
     ```
   - Inicia sesión en Jenkins con tus datos.
  
   - Creamos un nuevo Pipeline en el cual tendremos que activar una opción en la parte de BUILD TRIGGERS
    esta opcíon se llama *GitHub hook trigger for GITScm polling* esto nos permitirá recibir las notificaciones de GitHub.

     Completamos poniendo la ubicación de nuestro repositorio y nuestras credenciales.

5. **Configuramos el webhook en GitHub:**
   - En nuestro repositorio de GitHub, nos diriimos a la  sección de Configuración (Settings) y luego a Webhooks.
      Agregamos la URL que nos dió NGROK para ingresar a jenkins y le tendremos que sumar esto `/github-webhook/`.
     Quedaría así: 
     ```
     https://08e9-152-170-177-208.ngrok-free.app/github-webhook/
     ```
   - Seleccionamos los eventos que tendrá el webhook, en este caso "push" y "pull request".


6. **Instalar NVM para NODEJS**

  - Para instalar NVM utilizaremos una guía que podemos enncontrar en este [enlace](https://nodejs.org/en/download/package-manager/),
    esto nos permite correr distintas versiones de nodejs en nuestro entorno local.


¡TODO LISTO!

   - A partir de ahora, cada vez que hagamos un commit en nuestro repositorio, Jenkins responderá automáticamente si es un push o pull request a la rama principal.

  
