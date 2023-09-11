# Proyecto de Lista de Tareas
## Introducción

El objetivo principal de este proyecto es poner en práctica los siguientes conceptos de JavaScript:

1. Creación de variables y constantes __let__ y __const__.
2. Como traer elementos desde HTML para integrarlos con JavaScript (__document.querySelector__).
3. Uso de la función fecha del navegador __new Date()__.
4. Uso de funciones declaradas y __arrow functions__ tambien.
5. Implementación de __Arrays__ para guardar información.
6. Uso de condicionales __if__ para definir condiciones y operadores ternarios (__?:__).
7. Uso del __localStorage__ del navegador para guardar información y poderla usar para almacenar nuestras tareas (uso del __SetItem__ y __GetItem__, formato __JSON__, __Parse__ y __Stringify__).
8. Uso de __return__.
   
## Métodos y Propiedades.

Durante el desarrollo de este proyecto, utilizaremos una variedad de métodos y propiedades de JavaScript, como:

__Classlist__ y __toggle__ para manipular las clases de un elemento desde JavaScript.
__parentNode__ para definir elementos padre.
__remove.child__ para eliminar elementos hijo.
__addEventListener__ para agregar eventos de clic y teclas en elementos del HTML.
__Push__ usado para ingresar elementos dentro de un array.
__Value__ para ver los valores que obtienen ciertos elementos.
__Attributes__ para obtener los atributos de un elemento.
__forEach__ para recorrer elementos dentro de un array.
__insertAdjacentHTML__ nos permite pegar código en cualquier parte de mi HTML desde el JS.

Este proyecto nos permitirá aplicar estos conceptos en un contexto práctico y crear una aplicación funcional que nos ayudará a gestionar nuestras tareas diarias.

#librerías

- librería de iconos: https://fontawesome.com/
- Background gradient: https://cssgradient.io/
- Fonts: https://fonts.google.com/specimen/Kosugi+Maru?query=to

### insertAdjacentHTML 
Es un método de JavaScript que permite agregar contenido HTML a un elemento del documento HTML en una posición específica. Tiene cuatro opciones de posición para agregar contenido: "beforebegin", "afterbegin", "beforeend" y "afterend".

beforebegin: Inserta el contenido HTML justo antes del elemento en sí.
afterbegin: Inserta el contenido HTML como el primer hijo del elemento.
beforeend: Inserta el contenido HTML como el último hijo del elemento.
afterend: Inserta el contenido HTML justo después del elemento en sí.

 la función agregarTarea utiliza insertAdjacentHTML con la posición "beforeend" para agregar contenido HTML al final del elemento con el id "lista".

 