# Funcionalidad requerida

Con los alumnos identificamos las siguientes funciones que debe tener el lavarropas:

* Cargar jabón

* Cargar ropa

* Iniciar el ciclo de lavado

* Descargar ropa

* Cargar agua

* Descargar agua

* Centrifugado

* Enjuague

Una vez identificadas estas funciones procedemos a analizar las *pre* y *post condiciones* de cada función.

Una **precondición** es un estado que consideramos necesario para poder llamar a determinada función. Por ejemplo, no puedo lavar ropa si no hay agua.

Una **postcondición** es un estado con el que queda nuestro sistema después de llamar a determinada función. Por ejemplo, llamar a `cargar agua` deja a nuestr lavarropas con agua.

## Carga jabón

*Precondición*: ninguna

*Postcondición*: el lavarropas tiene jabón

## Iniciar ciclo de lavado

*Precondición*: cargar agua y hay ropa

*Postcondición*: ropa con jabón y mojada

## Controlar motor del tambor

*Precondición*: ninguna

*Postcondición*: ninguna

## Verificar temporizador

*Precondición*: ninguna

*Postcondición*: ninguna

Vamos a separar esta tarea en dos subtareas:

* Validar que se haya cumplido (o no) el ciclo de trabajo

* Actualizar el contador

## Cargar ropa

*Precondición*: el lavarropas está parado y sin agua

*Postcondición*: el lavarropas tiene ropa

## Descargar ropa

*Precondición*: el lavarropas está parado y sin agua

*Postcondición*: el lavarropas está vacío

## Cargar agua

*Precondición*: que haya ropa y jabón

*Postcondición*: el lavarropas tiene agua

## Descargar agua

*Precondición*: que haya agua

*Postcondición*: el lavarropas no tiene agua

## Centrifugado

*Precondición*:  el lavarropas no tiene agua y la ropa está mojada

*Postcondición*: la ropa está seca

## Enjuague

*Precondición*: la ropa tiene jabón y está mojada

*Postcondición*: la ropa no tiene jabón y está mojada
