

**El Document Object Model (DOM)**: es una representación de la estructura de un documento HTML (o XML) en forma de un árbol de objetos que pueden ser manipulados mediante lenguajes de programación como JavaScript. El DOM representa cada elemento del documento, como etiquetas HTML, atributos, texto y otros elementos, como nodos en un árbol jerárquico. Cada nodo en el árbol representa una parte del documento, como un elemento HTML, un atributo, un fragmento de texto, etc.

El DOM permite a los desarrolladores web acceder y manipular dinámicamente los elementos y contenido de una página web. Esto significa que puedes usar JavaScript para cambiar el contenido de una página web en tiempo real, responder a eventos del usuario, modificar estilos, agregar o eliminar elementos, entre otras acciones.

El DOM es una parte fundamental de la programación web en el lado del cliente y es esencial para crear aplicaciones web interactivas y dinámicas. 


Recibe como argumento un string, y retorna un único nodo cuyo atributo `id` se corresponda con el:

```JavaScript
JavaScript:
getElementById( ):

Jquery:
var elementoTitulo = $("#miTitulo");
```


Para seleccionar un elemento padre o hijo en el Document Object Model (DOM) desde JavaScript, puedes utilizar métodos como `parentNode` o `childNodes` para acceder a los elementos adyacentes en el árbol DOM. También puedes usar métodos como `querySelector` `querySelectorAll` para seleccionar elementos específicos por sus selectores CSS. 


```javascript
JavaScript:
// Supongamos que tienes un elemento con el id "miHijo"
var hijo = document.getElementById("miHijo");

// Para seleccionar el elemento padre
var padre = hijo.parentNode;
```


```javascript
var elementoPadre = document.getElementById("miPadre");

// Para seleccionar todos los nodos hijos del elemento padre
var nodosHijos = elementoPadre.childNodes;
```


```javascript
var elementoPadre = document.getElementById("miPadre");

// Para seleccionar solo elementos hijos
var elementosHijos = [];
for (var i = 0; i < elementoPadre.childNodes.length; i++) {
  if (elementoPadre.childNodes[i].nodeType === 1) { // 1 representa nodos de elementos
    elementosHijos.push(elementoPadre.childNodes[i]);
  }
}
```


```javascript
var elementoPadre = document.getElementById("miPadre");

// Para seleccionar el primer elemento hijo que cumple con el selector CSS
var primerHijo = elementoPadre.querySelector(".claseHijo");

// Para seleccionar todos los elementos hijos que cumplen con el selector CSS
var todosLosHijos = elementoPadre.querySelectorAll(".claseHijo");
```


En jQuery, puedes seleccionar elementos padres e hijos del DOM utilizando los métodos de selección proporcionados por la biblioteca. 
### Para seleccionar un elemento padre:


```html
Estructura HTML:
<div id="padre">
<p>Hijo 1</p> 
<p>Hijo 2</p> 
</div>
```


```javascript
Javascript:
var elementoPadre = $("#padre");
```


### Para seleccionar un elemento hijo:

```javascript
/*Para seleccionar un elemento hijo dentro de un elemento padre, puedes usar métodos como `find()` o `children()`. Supongamos que deseas seleccionar el segundo párrafo (`<p>`) dentro del div con el ID "padre":
*/
var elementoHijo = $("#padre").find("p:eq(1)");

//También puedes seleccionar elementos hijos directos usando `children()`:
var elementoHijo = $("#padre").children("p:eq(1)");
```


