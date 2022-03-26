# Que es Flask
Flask es un framework minimalista escrito en Python que permite crear aplicaciones web rápidamente y con un mínimo número de líneas de código. Está basado en la especificación WSGI de Werkzeug y el motor de templates Jinja2 y tiene una licencia BSD. Fuente: https://es.wikipedia.org/wiki/Flask

## Flask
Una aplicacion Flask es una instancia de la clase __Flask__. Todo acerca de esa aplicacion, como configuraciones y URLs debe ser configurado en esta clase.
La mejor forma de manejarlo es crearlo dentro de una funcion. Esta aplicacion es conocida como *application factory*. Todas las configuraciones se deben realizar dentro de esta funcion y luego debe retornar la aplicacion.

~~~
from flask import Flask
app = Flask(__name__)
~~~
El primer parametro al instanciar una app Flask es __import_name__. Este parametro le da una idea a Flask de lo que contiene tu aplicacion. Sirve para buscar recursos en los archivos de sistema, ayuda a depurar a ciertas extensiones. Por ejemplo, si nuestra aplicacion esta definida en __yourapplication/app.py__ entonces podemos hardcodear el nombre del paquete o usar __name__. La aplicacion necesita saber donde se encuentran para definir algunas rutas.
~~~
app = Flask('yourapplication')
app = Flask(__name__.split('.')[0])
~~~
