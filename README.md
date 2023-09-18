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

# presentacion del codigo

Claro, puedo explicar el código proporcionado como una presentación estudiantil. Aquí tienes una descripción de las principales partes y funcionalidades del código:

**1. Configuración Inicial:**
   - Seleccionamos elementos del DOM utilizando `document.querySelector` y los almacenamos en variables para su posterior uso, como `fecha`, `lista`, `input`, `botonEnter`, entre otros.

**2. Variables y Constantes:**
   - `check`, `uncheck`, y `lineThrough` almacenan nombres de clases CSS que se utilizan en el código.
   - `id` es una variable para llevar un seguimiento del identificador único de cada tarea.
   - `LIST` es una matriz que almacenará las tareas.

**3. Creación de Fecha:**
   - Se obtiene la fecha actual y se muestra en el formato "día de la semana, mes día" en el elemento con el id `fecha`.

**4. Función para Agregar Tarea:**
   - La función `agregarTarea` toma como argumentos `tarea`, `id`, `realizado` y `eliminado`.
   - Crea un elemento de lista `<li>` con iconos de verificación, texto de tarea y un ícono de eliminación.
   - Aplica clases CSS según el estado de la tarea (realizada o no) y si ha sido eliminada.
   - Agrega el elemento de lista al elemento `<ul>` con el id `lista`.

**5. Función para Marcar Tarea como Realizada:**
   - `tareaRealizada` se llama cuando se hace clic en el ícono de verificación.
   - Cambia el estado de realización de la tarea y actualiza las clases CSS en consecuencia.

**6. Función para Eliminar Tarea:**
   - `tareaEliminada` elimina una tarea de la lista y la marca como eliminada en la matriz `LIST`.

**7. Event Listeners:**
   - Se agregan controladores de eventos para el botón "Agregar" (`botonEnter`), la tecla "Enter" (evento `keyup`), y los clics en la lista (`lista`).

**8. Almacenamiento Local (LocalStorage):**
   - Las tareas se almacenan y recuperan del almacenamiento local (`localStorage`) para que los datos persistan incluso después de cerrar la página.
   - Se verifica si ya existen tareas en el almacenamiento local (`localStorage.getItem("TODO")`) y se cargan en `LIST`.

**9. Función para Cargar Lista:**
   - `cargarLista` recibe una matriz de tareas y las agrega a la lista utilizando la función `agregarTarea`.

En resumen, este código permite al usuario agregar, marcar como realizadas y eliminar tareas de una lista de quehaceres. Los datos de las tareas se almacenan en el almacenamiento local para mantener un registro persistente de las tareas. La interfaz de usuario refleja el estado de las tareas (realizadas o no) y su eliminación.

# algunos conceptos puntuales que se manejan en este codigo:
   
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

 ## El método toggle 
 El método toggle en JavaScript se utiliza para alternar (activar o desactivar) una clase CSS en un elemento HTML. Puede tomar una clase como argumento y la agrega al elemento si no está presente, o la elimina si ya está presente.
 El método toggle es útil para crear interacciones basadas en clics u otros eventos donde deseas cambiar la apariencia o el comportamiento de un elemento al hacer clic en él, alternando entre diferentes estados.

## El comando target
El comando target en JavaScript se usa en eventos para referirse al elemento HTML en el que ocurrió ese evento. Proporciona acceso al elemento específico que desencadenó el evento. Puedes usar event.target para interactuar o manipular ese elemento en respuesta al evento. Por ejemplo, puedes cambiar su contenido, estilo o realizar otras acciones basadas en la interacción del usuario con ese elemento específico. Es una forma clave de trabajar con eventos para crear comportamientos dinámicos en una página web.

## La propiedad classList
Claro, te lo explico de manera sencilla. La propiedad classList en JavaScript se usa para trabajar con las clases CSS de un elemento HTML. Te permite agregar, eliminar o verificar si una clase está presente en el elemento.

### element.parentNode.querySelector(".text"): 
Aquí estamos accediendo al "padre" del elemento. Piensa en esto como si estuviéramos subiendo un nivel en la jerarquía de tu página web para encontrar algo relacionado con la tarea. Luego, estamos buscando algo con la clase "text" dentro de ese padre.

### classList.toggle(lineThrough): 
Esta línea agrega o quita la clase lineThrough a ese elemento encontrado en el paso anterior. lineThrough cambia la apariencia de la tarea para mostrar que está tachada, como cuando marcas una tarea como completada en papel.

##  localStorage y el sessionStorage
El localStorage y el sessionStorage son dos características proporcionadas por los navegadores web que permiten a las aplicaciones web almacenar datos en el lado del cliente (en el navegador) de manera persistente o temporal, respectivamente. Aquí tienes una breve descripción de cada uno:

### localStorage:
- Persistencia: Los datos almacenados en localStorage se mantienen incluso después de cerrar el navegador y reiniciar la computadora. Son persistentes.
- Capacidad: Ofrece una capacidad de almacenamiento mayor en comparación con sessionStorage, generalmente alrededor de 5-10 MB por dominio.
- Uso Común: Se utiliza para almacenar configuraciones de usuario, preferencias, datos de autenticación, y otros datos que deben mantenerse a largo plazo.

### sessionStorage:
- Temporalidad: Los datos almacenados en sessionStorage solo están disponibles durante la duración de una sesión de navegación. Se borran automáticamente cuando se cierra la pestaña o el navegador.
- Capacidad: Ofrece una capacidad de almacenamiento más limitada en comparación con localStorage, generalmente alrededor de 5-10 MB por dominio.
- Uso Común: Se usa para almacenar temporalmente datos que solo son relevantes para la sesión actual del usuario, como detalles de un carrito de compras en línea o el estado temporal de una aplicación web.
#### Ejemplos:
- Almacenar datos en localStorage
<script>
    localStorage.setItem('nombre', 'Juan');
    localStorage.setItem('puntos', 100);
</script>
- Recuperar datos de localStorage
<script>
    const nombre = localStorage.getItem('nombre');
    const puntos = localStorage.getItem('puntos');
</script>

estas funciones se usan para almacenar y recuperar datos relacionados con las tareas pendientes que el usuario ingrese en la lista de tareas.

1. `localStorage.setItem("TODO", JSON.stringify(LIST));`: Almacena un objeto llamado "TODO" en el almacenamiento local del navegador, convirtiendo la lista "LIST" en una cadena JSON.

2. `JSON.parse(...)`: Convierte una cadena JSON en un objeto JavaScript.

3. `localStorage.getItem("TODO");`: Recupera el objeto "TODO" del almacenamiento local del navegador.

## forEach
forEach es un método que se utiliza para recorrer los elementos de un array y ejecutar una función proporcionada una vez por cada elemento. Es una forma conveniente de realizar una acción en cada elemento de una lista sin necesidad de escribir bucles for o while.
aqui se utiliza forEach para recorrer LIST y, para cada tarea, la almacena en localStorage con una clave única basada en el índice.

