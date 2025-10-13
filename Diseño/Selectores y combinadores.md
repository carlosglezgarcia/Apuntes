# Selectores CSS
---
Los **selectores** definen sobre qué elementos se aplicará un conjunto de reglas CSS.

## Selectores básicos
---
[Selectores de tipo](https://developer.mozilla.org/es/docs/Web/CSS/Type_selectors)

Selecciona todos los elementos que coinciden con el nombre del elemento especificado.

Ejemplo:
```html
<input type="text"/>
<!-- Este input tendrá el fondo azul -->
```
```css
input {
	background-color: blue;
}
/* Esto hará que el input tenga fondo azul */
```

[Selector de clase](https://developer.mozilla.org/es/docs/Web/CSS/Type_selectors)

Seleccionan todos los elementos que tienen el atributo de clase especificado.

Ejemplo:
```html
<input class="azul" type="text"/>
```
```css
.azul {
	background-color: blue;
}
```

[Selector de ID](https://developer.mozilla.org/es/docs/Web/CSS/ID_selectors)

Selecciona un elemento basándose en el valor de su atributo **id**. Solo puede haber un elemento con un determinado ID dentro de un documento.

Ejemplo:
```html
<input id="azul" type="text"/>
```
```css
#azul {
	background-color: blue;
}
```

[Selector universal](https://developer.mozilla.org/es/docs/Web/CSS/Universal_selectors)

Selecciona todos los elementos. Opcionalmente, puede estar restringido a un espacio de nombre específico o a todos los espacios de nombres.

Ejemplo:
```html
<!DOCTYPE html>
<html lang="es">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>A ver quien lee esto</title>
	<style>
		* {
		  margin: 10px;
		  }
		  /* Todos los elementos dentro del html tendrán un margin de 10 pixeles
	</style>
</head>
<body>
	<header>
		<h1>Todos los elementos tendrán un margin de 10 píxeles</h1>
	</header>
</body>
</html>
```

[Selector de atributo](https://developer.mozilla.org/es/docs/Web/CSS/Attribute_selectors)

Selecciona elementos basándose en un valor de un determinado atributo.

Ejemplo:
```html
<input type="text" required/>
<input type="number" required/>
```
```css
[required] {
	background-color: red;
}
```

## Combinadores

[Combinador de hermanos adyacentes](https://developer.mozilla.org/es/docs/Web/CSS/Next-sibling_combinator)

El combinador `+` selecciona hermanos adyacentes. Esto quiere decir que el segundo elemento sigue directamente al primero y ambos comparten un mismo elemento padre.

Ejemplo:
```html
<header>
	<h2>Título</h2>
	<p>Texto cualquiera</p>
</header>
<main>
	<section>
		<h2>Título de sección</h2>
		<p>Texto de sección</p>
	</section>
</main>
```
```css
h2 + p {
	background-color: blue;
}
```
La regla `h2 + p` se aplicará a todos los elementos `<p>` que siguen directamente a un elemento `<h2>`.

[Combinador general de hermanos](https://developer.mozilla.org/es/docs/Web/CSS/Subsequent-sibling_combinator)

El combinador `~` selecciona hermanos. Esto quiere decir que el segundo elemento sigue al primero (no necesariamente de forma inmediata) y ambos comparten el mismo elemento padre.

Ejemplo:
```html
<span>Este span no es rojo.</span>
<p>Pues un párrafo cualquiera</p>
<code>let mi_variable = "Hola Mundo"</code>
<span>Este span sí que es rojo</span>
```
```css
p ~ span {color: red;}
```

[Combinador de hijo](https://developer.mozilla.org/es/docs/Web/CSS/Child_combinator)

El combinador `>` selecciona los elementos que son hijos directos del primer elemento.

Ejemplo:
```html
<div>
	<span>Afecta a este
		<span>A este no</span>
	</span>
</div>
<span>A este tampoco</span>
```
```css
div > span {background-color: gray;}
/* Esto funcionará para todos los span que sean hijos de div pero solo un nivel por debajo */
```

[Combinador de descendientes](https://developer.mozilla.org/es/docs/Web/CSS/Descendant_combinator)

El combinador (espacio) selecciona los elementos que son descendientes del primer elemento.

Ejemplo:
```html
<div>
	<span>Afecta a este
		<span>A este también afecta</span>
	</span>
</div>
<span>A este no</span>
```
```css
div span {background-color: blue;}
/* Este afecta a todos los span que sean hijos de div sin importar si son hijos o nietos de div. */
```
