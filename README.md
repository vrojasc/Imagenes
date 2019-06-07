# Graph Bot LP

GraphBotLP es un bot encargado de responder, de manera textual y gráfica, a preguntas relacionadas con grafos geométricos definidos sobre la población.
Este README te ayudará a entender y empezar a trabajar con el bot. Este documento se actualizará constantemente a medida que se actualice el bot.

### ¿Para que sirve GraphBotLP?

GraphBotLP utilizará un grafo geométrico sobre la población para ofrecernos información sobre:
- Número de ciudades (nodos) con población superior a un número enviado por el usuario.
- Cercanía entre ciudades (edges).
- Ruta mas corta entre 2 ciudades dependiendo del grafo.
- Densidad de población.

### Prerrequisitos

Es necesario tener instalado:
- python 3+

Antes de empezar a trabajar con el bot, es necesario instalar las librerías que implementa.
El archivo **"requirements.txt"** contendrá una lista de elementos a instalar usando ```pip3.x install```


```
pip3.x install -r requirements.txt
```

### Librerias necesarias
Las librerias necesarias para ejecutar GraphBotLP son:
```
fuzzywuzzy==0.17.0
networkx==2.3
pandas==0.24.2
python-telegram-bot==11.1.0
staticmap==0.5.4
```
### Instalando

Si haz realizado los pasos previos, estas listo para empezar. Solo es necesario que inicies el programa con:
```
python3.x bot.py
```
Ahora solo tienes que iniciar una conversacion en Telagram con ```GraphBotLP```
### Probando el bot

Dispondras de diversos comandos que, junto al grafo, generarán diversas soluciones a preguntas relacionadas con la población:
- `/start`: El comando por defecto. Ofrece un cordial saludo y te da un pequeño consejo para empezar

- `/help`: Comando de ayuda que te explicará todas las posibilidades del bot. Tanto `/start` como `/help` no necesitan argumentos y descartarán cualquier entrada posterior.
![help](https://raw.githubusercontent.com/vrojasc/Imagenes/master/imagen_help.png)

- `/graph distance population`: Este comando generará el grafo con las ciudades con población mayor a **population** como nodos y una arista por cada par de ciudades con distancia menor a **distance**. Es necesario escribir los 2 argumentos para su correcto funcionamiento. Este es un ejemplo del comando bien utilizado.
![graph](https://raw.githubusercontent.com/vrojasc/Imagenes/master/imagen_graph.png)
  
  Todas las siguientes funciones actuan sobre el grafo generado. Si este no ha sido creado, creará uno automáticamente con **distance = 300** y **population = 100000** .
  ![graph automático](https://raw.githubusercontent.com/vrojasc/Imagenes/master/imagen_generar_automatico.png)
  
  Es posible que el tiempo de lectura de los datos dependa de la calidad de vuestra conexión de Internet.

- `/nodes`: Muestra el numero de nodos del grafo o, lo que es lo mismo, la ciudades representadas.

- `/edges`: Muestra el numero de aristas del grafo o, lo que es lo mismo, la conexión de las ciudades del grafo.

- `/components`: Muestra el numero de componentes conexas del grafo.

- `/plotpop distance lat lon`: Representará las ciudades en un mapa con una esfera de tamaño en función a su población. La distancia será el filtro para saber que ciudades coger y las coordenadas serán el punto del centro.
![plotpop](https://raw.githubusercontent.com/vrojasc/Imagenes/master/imagen_plotpop.png)

- `/plotgraph distance lat lon`: Representará las ciudades en un mapa con una esfera de tamaño estático. La distancia será el filtro para saber que ciudades coger y las coordenadas serán el punto del centro.
![plotgraph](https://raw.githubusercontent.com/vrojasc/Imagenes/master/imagen_plotgraph.png)

- `/route src dst`: Encontrará la ruta mas corta entre **src** y **dst** dependiendo del grafo generado.
![route](https://raw.githubusercontent.com/vrojasc/Imagenes/master/imagen_route.png)

  Tambien dispones de funciones adicionales que facilitarán la escritura del comando como:

- `Envio de ubicación`: Puedes compartir tu ubicación y el bot se encargará de guardarla. Usará esta ubicación en los comandos que utilizan **lot** y **lat** si estos argumentos no son incluidos.
![ubicacion](https://raw.githubusercontent.com/vrojasc/Imagenes/master/imagen_ubi.png)

- `Buscar ciudades similares`: GraphBotLP se encargará de corregir los errores gramaticales utilizados en el comando **route**. Tener cuidado que no corrige **paises**
![correcion](https://raw.githubusercontent.com/vrojasc/Imagenes/master/imagen_arreglando_fallos.png)

## Versioning

Esta version es la 1.0.1

## Authors

* **Victor Vidal Roja Condori** - *victor.vidal.rojas@est.fib.upc.edu* - [GraphBotLP](https://github.com/vrojasc/Imagenes)

## License

Este proyecto esta pendiente de licencia

**Free Software**
