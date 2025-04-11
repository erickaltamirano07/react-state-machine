## Propiedades de los estados

# Value

Indica el nombre del estado actual
Cuando se tiene una máquina padre y esta tiene una máquina hija, este nombre del estado actual pasa de ser una cadena de texto a un objeto
Dicho objeto dice el estado tanto de la máquina padre como la máquina hija

# Context

Da el contexto del estado actual
Nos permite guardar valores (Objetos, arrays, etc.)
Es un pedazo de la máquina donde se va guardando y actualizando los valores

# Event

El nombre del evento anterior que nos trajo al estado actual

# Action

Es un array que contiene las acciones que ejecutan algún estado
Son funciones de ejecutar y olvidar

# Activities (⚠️ Deprecated)

Listado de actividades indicando si están en progreso o no
Las actividades a diferencia de las acciones (ejecutar y olvidar) son cosas más permanentes (Invocar un servicio, observable)

# History

Indica el estado anterior
Se implementa cuando deseamos saber cuál fue el estado anterior en caso de condicionales

# Meta

Sección de metadata dentro del estado
Nos permite poner valores asociados al estado, los cuales serán permanentes

# NextEvents

Es un array de los posibles eventos que podemos ejecutar a partir del estado actual
Métodos de los estados
matches(nombre del estado) ⇒ Pasando el nombre de un estado nos responde si dicho estado es el actual o no
Nos ayuda a ver si estamos en un estado tanto de la máquina padre o hijo
can(nombre del evento) ⇒ Pasando el nombre de un evento nos indica si podemos ejecutarlo
