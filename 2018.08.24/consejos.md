# Consejos generales

## Al analizar funcionalidad

El análisis funcional nos da un pantallazo de las tareas que tenemos que desarrollar. Es muy importante comenzar con este análisis, porque nos **permite planificar** la implementación y es parte de la organización del proyecto.

Un mal análisis puede ser costoso ya que deriva en imprevistos o inconsistencias al momento de planificar. Sin embargo, **no existe** el análisis funcional perfecto.
El análisis, la planificación de tareas y la implementación son tareas iterativas, las vamos refinando y repitiendo hasta lograr el objetivo.
La habilidad para analizar se gana con práctica y experiencia.

El análisis debe ser independiente de la tecnología que usemos, no tiene que responder el *cómo*, sino el *qué*.

## Al planificar las tareas

Comenzar desde el *problema general* y dividir en *subtareas*.

Describir las subtareas: si la descripción se vuelve compleja, dividir en más subtareas (ver más adelante *métricas*)

*Evitar pensar en la implementación*: la descripción en pseudocódigo debe ser genérica y sencilla, sirviendo de guía al programador. 

Incorporar la planificación a la documentación. El pseudocódigo es una forma muy común de documentar funcionalidad, describiéndola.

## Al desarrollar

Programar *para personas* y no *para computadoras*. Priorizar legilibilidad a optimización de código.

Utilizar nombres de variables y funciones **claros** y **descriptivos**

## Métricas

Establecerse métricas generales:

¿Qué tan compleja es mi función? ¿Puedo describirlo en 4 o 5 lineas?
Si mi función tiene más de cierta cantidad de lineas, dividirla en subfunciones.

¿Estoy usando muchas estructuras de control? (condiciones if, ciclos while o for) ¿Se anidan mucho? Si tengo muchas estructuras de control, analizar si reordenando o dividiendo en subfunciones ayuda a clarificar el código.

¿Estoy usando muchas variables? Si hay muchas variables relacionadas entre si, usar estructuras.
