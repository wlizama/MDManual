# Configurando el entorno de desarrollo de Google Cloud - Python

1. Descargar el DSK de [AppEngine para Python](https://cloud.google.com/appengine/downloads)

2. Descomprimirlo

3. Abrir la consola, ir a la carpeta donde lo descomprimimos, ejecutar el comando ``./install.sh``

4. Reiniciar la consola (Abriéndola nuevamente)

5. Generar una serie de archivos para que GCloud sepa cómo correrlo

   _app.yml_ : Qué ambiente vamos a necesitar, y a dónde va a enviar el tráfico.

   _appengine_config.py_: Dónde se encuentran las librerías que instalamos con pip, google no corre ese comando, por lo que debemos subir las librerías. Este archivo lleva por código:

   ```py
    from google.appengine.ext import vendor
    vendor.add("lib") # Donde lib es la carpeta donde guardaremos las librerías.
   ```

6. Crear un folder _/lib_ para guardar las librerías (en el proyecto actual)

7. Abrir consola, movernos a nuestro folder del proyecto actual

8. Iniciar ambiente virtual: ``source venv/bin/activate``

9. Instalar requirements.txt en este folder ``pip install -r requirements.txt -t lib``

   ``-t lib`` significa que ese es el directorio destino donde las instalará

10. Indicar en app.yaml

    ```yaml
      service: default
      runtime: python27 # Ambiente a utilizar (python 27 es Python 2.7)
      api_version: 1
      threadsafe: yes
    
          # Hacia dónde tiene qué mandar el tráfico  
          handlers:
          - url: .*
            script: main.app # módulo main, variable app, en el main.py, en la variable app = Flask(name)
            secure: always
    ```

11. Correr el servidor local ``dev_appserver.py .``, poner un punto al final, significa que el archivo yaml está en el mismo directorio

12. Subir el archivo a internet

    12.1. Entrar a console.cloud.google.com

    12.2. Crear un Proyecto

    12.3. Ir al menú App Engine (barra lateral izq)

    12.4. Escoger el lenguaje de nuestra aplicación.

    12.5. Autenticarnos con Google desde la consola ``gcloud auth login``

13. Hacer deploy de la aplicación ``gcloud app deploy --project <projectid>``

14. Después de eso nos dirá la URL donde se deployó

