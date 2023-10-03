# DOM (Document Object Model)

## Introducción al DOM

El DOM, o Document Object Model, es una representación en forma de árbol de la estructura de un documento HTML. Con JavaScript, podemos acceder y manipular los elementos de una página web mediante el DOM. Esto nos permite realizar cambios dinámicos en la página y responder a eventos del usuario.

## El elemento `<script>`

Para incluir código JavaScript en una página HTML, podemos usar el elemento `<script>`. Hay dos formas principales de hacerlo:

**Incluir código en línea:** Colocamos JavaScript directamente dentro de una etiqueta `<script>` en el `<head>` del documento HTML.

```html
<html>
<head>
    <script>
        // Código JavaScript en línea
        alert('Hola, mundo!');
    </script>
</head>
</html>
```
1. Incluir código desde un archivo externo: Enlazamos un archivo JavaScript externo a nuestra página HTML usando la etiqueta <script>.
```html
<html>
<head>
    <script src="mi-script.js"></script>
</head>
</html>
```

## El objeto "document"

El objeto "document" es una parte fundamental del DOM. Proporciona acceso a los elementos HTML de la página y nos permite manipularlos con JavaScript.

## Selectores
Los selectores son métodos que nos permiten buscar y seleccionar elementos en el DOM. Aquí hay algunos selectores comunes:

### getElementById
```javascript
const elemento = document.getElementById('miElemento');
```
### getElementsByClassName
```javascript
const elementos = document.getElementsByClassName('miClase');
```
### querySelector
```javascript
const elemento = document.querySelector('.miClase');
```
### querySelectorAll
```javascript
const elementos = document.querySelectorAll('p');
```

## Métodos de Elementos
Una vez que tenemos una referencia a un elemento, podemos utilizar métodos y propiedades para interactuar con él:

### .innerHTML
```javascript
const miElemento = document.getElementById('miElemento');
miElemento.innerHTML = '<b>Nuevo contenido</b>';
```
### .setAttribute
```javascript
const miEnlace = document.getElementById('miEnlace');
miEnlace.setAttribute('href', 'https://www.ejemplo.com');
```
### .style

```javascript
const miDiv = document.getElementById('miDiv');
miDiv.style.color = 'blue';
```

## Event Listeners

Los event listeners nos permiten responder a eventos como clics de ratón, pulsaciones de teclas, y más. Aquí hay un ejemplo con el evento click:

```javascript
const miBoton = document.getElementById('miBoton');
miBoton.addEventListener('click', function() {
    alert('¡Botón clickeado!');
});
```


