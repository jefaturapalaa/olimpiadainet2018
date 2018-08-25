# Implementación del lavarropas

Arrancamos definiendo nuestra función principal.
Utilizamos las pre y post condiciones anotadas previamente para establecer un orden entre las funciones, por ejemplo: el enjuague tiene como pre condición a la ropa con jabón y mojada, por lo que debe ir después del ciclo de lavado.
 

~~~{.python}
def lavarropas:
    cargar_jabon()
    cargar_ropa()
    cargar_agua()
    iniciar_lavado()
    enjuague()
    descargar_agua()
    centrifugado()
    descargar_ropa()
~~~

Después definimos cada una de estas funciones.

En esta primer implementación buscamos que el procesador haga cada una de las tareas en orden y no haga nada mientras espera que estas tareas se completen. Este tipo de tareas se llaman *bloqueantes*.

Utilizar tareas bloqueantes nos ayuda a tener control sobre las tareas (sabemos qué se ejecuta paso a paso), pero sacrificamos libertad del procesador para atender otras tareas.

~~~
def cargar_jabon:
    bloquear hasta cargar el jabón

def cargar_ropa:
    bloquear hasta cargar ropa

def cargar_agua:
    mientras no agua_completo:
        abrir valvula de agua
    cerrar valvula de agua
~~~

A fin de simplificar la implementación, asumimos que el tambor gira de igual forma cuando está lavando que cuando está centrifugando.

~~~
def iniciar_ciclo_lavado:
    temporizador = 0
    motor_accionado = true
    mientras (temporizador < duracion_lavado):
        esperar 1 segundo
        temporizador += 1
    # una vez terminado el tiempo, apago el motor    
    motor_accionado = false

def centrifugado:
    temporizador = 0
    motor_accionado = true
    mientras (temporizador < duracion_centrifugando):
        esperar 1 segundo
        temporizador += 1    
    motor_accionado = false
~~~

Iniciar lavado y centrifugar son dos acciones muy parecidas entre si, ambas consisten en activar el motor durante una cierta cantidad de tiempo.

Definimos el control del motor como una funcion que puede recibir una cantidad de tiempo variable (duracion en segundos)

~~~
def controlar_motor(duracion):
    temporizador = 0
    motor_accionado = true
    mientras (temporizador < duracion):
        esperar 1 segundo
        temporizador += 1
    # una vez terminado el tiempo, apago el motor    
    motor_accionado = false
~~~

Y definimos las funciones de iniciar ciclo de lavado y centrifugado.

~~~
def iniciar_ciclo_lavado:
    controlar_motor(duracion_lavado)

def centrifugado:
    controlar_motor(duracion_centrifugado)
~~~

Este proceso de reutilizar funciones se lo conoce como *refactorización*.
Es aconsejable refactorizar una vez terminada la implementación.

No refactorizar lleva a tener código repetido (lo que es malo), y una refactorización muy temprana lleva a tener código complejo dificil de mantener.

Enjuagar también es una composición de funciones ya definidas previamente:

~~~
def enjuagar:
    cargar agua
    iniciar ciclo lavado
~~~

Defino las ultimas funciones

~~~
def descargar_agua:
	activar desagote

def descargar ropa:
    ropa cargada = false
~~~