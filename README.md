# 5 CSS Grid y Flexbox

## CSS Grid

CSS Grid es un sistema que nos va a permitir acomodar nuestros elementos de una forma dinámica y compleja, refiriéndonos a la estructura y layout.

Para hacer uso de CSS Grid primeramente hacemos lo que a continuación te muestro:

1. Crear un documento HTML con lo siguiente.

```html
<!DOCTYPE html>
<html lang="es">
	<head>
		<title> CSS Grid & Flexbox </title>
	</head>
	<body>
		<div class="grid">
			<div> 1 </div>
			<div> 2 </div>
			<div> 3 </div>
		</div>
	</body>
</html>
```

1. Crear los estilos CSS y agregar propiedad `display` con su valor `grid`. También creamos 3 columnas con su espaciado.

```css
/* Grilla */
body .grid {
	display: grid;
  grid-gap: 16px;
	grid-template-columns: 1fr 1fr 1fr;

  height: 100vh;
}
```

1. Dentro del elemento con la clase grid, tenemos 3 elementos div a los cuales les daremos los siguientes estilos.

```css
/* Grilla */
body .grid {
	display: grid;
	grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 34px;

  height: 100vh;
}

body .grid div {
	background: #12abe2;
	height: 100%;
}
```

Resultado:

![https://i.ibb.co/jDbpdz5/screely-1639271412501.png](https://i.ibb.co/jDbpdz5/screely-1639271412501.png)

Ahora si deseamos agregar 3 filas tendriamos dos opciones, ya sea reemplazar "columns" por "rows" o en otra línea agregar `grid-template-rows` 

Resultado:

![https://i.ibb.co/1QgpnZ7/screely-1639271632344.png](https://i.ibb.co/1QgpnZ7/screely-1639271632344.png)

Mediante las propiedades `grid-template-columns` y `grid-template-rows` podremos agregar filas y columnas, mientras que con `grid-gap` vamos a establecer el espaciado entre filas y columnas, o lo que se conoce como en diseño editorial como "calles".

Los valores para estas 2 propiedades van a variar y las que se suelen usar son:

- px
- fr
- %

## Flexbox

A comparación de CSS Grid, Flexbox es un poco mas complejo y confuso, pero para uso de este taller combinaremos ambos, haciéndote su comprensión mas sencilla.

De antemano debes saber que flexbox se desempeña mejor acomodando los elementos de forma horizontal, mientras que CSS Grid lo hace en ambas direcciones: vertical y horizontal.

Y falta agregar que para usar Flexbox es la misma dinámica que CSS Grid, crearemos un elemento padre con sus respectivos elementos anidados para después aplicar al elemento padre la propiedad `display` con el valor `flex`

Flexbox aplicado a los elementos div anidados:

1. Usando los archivos anteriores de html y css agregaremos solamente las siguiente líneas de código en CSS.

```css
/* Grilla */
body .grid {
	display: grid;
	grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 34px;

  height: 100vh;
}

body .grid div {
	align-items: center
	background: #12abe2;
	display: flex;
	height: 100%;
	justify-content: center;
}
```

<aside>
⚠️ Siguiendo el consejo dado al final de la introducción a CSS, podrás observar que líneas de código se añadieron.

</aside>

Resultado:

![https://i.ibb.co/jD6HnbK/screely-1639271851897.png](https://i.ibb.co/jD6HnbK/screely-1639271851897.png)

Con estas 3 líneas de código el resultado fué, centrar los números que hay dentro de los div.

Ahora crearemos un nuevo documento html, lo enlazamos con su respectiva hoja de estilos css y continuamos con el ejercicio.

1. Creamos nuestro html con nuestros elementos.

```html
<!DOCTYPE html>
<html lang="es">
	<head>
		<title> CSS Grid & Flexbox </title>
	</head>
	<body>
		<div class="flexbox">
			<div> 1 </div>
			<div> 2 </div>
			<div> 3 </div>
			<div> 4 </div>
			<div> 5 </div>
		</div>
	</body>
</html>
```

1. Damos estilos primero a nuestros elementos anidados en el div padre con la clase flexbox

```css
body .flexbox div {
  background: #12a90a;
  height: 100px;
  width: 100px;
}
```

1. Ahora, arriba de las líneas de código añadidas previamente, agregamos lo siguiente.

```css
body .flexbox {
  display: flex;
  gap: 16px;
}

body .flexbox div {
  background: #12a90a;
  height: 100px;
  width: 100px;
}
```

Resultado:

![https://i.ibb.co/4M1ZbTC/screely-1639272314038.png](https://i.ibb.co/4M1ZbTC/screely-1639272314038.png)

Lo que realizamos fué, añadir la propiedad display con su valor flex y además para dar una separación entre los elementos agregamos la propiedad `gap` con valor de una unidad de medida relativa (puedes usar la que tu quieras y usar el número que tu desees).

Y ya por último, ¿Recuerdas que te comente al inicio que flexbox funciona mejor alinenando sus elementos de forma horizontal? Pues éste tiene una opción para hacer que los elementos estén alineados de forma vertical y eso lo hacemos agregando la propiedad `flex-direction` con el valor `column` 

```css
body .flexbox {
  display: flex;
	flex-direction: column;
  gap: 16px;
}

body .flexbox div {
  background: #12a90a;
  height: 100px;
  width: 100px;
}
```

Resultado:

![https://i.ibb.co/fpMqkNr/screely-1639272480425.png](https://i.ibb.co/fpMqkNr/screely-1639272480425.png)

Ya solo falta centrar los números otra vez pero te lo dejo de tarea, no sin antes darte una pista: solamente tienes que añadir 3 líneas de código ¡Éxito! 😉

### **Recursos**

- Guía de Flexbox (inglés)
    
    [https://css-tricks.com/snippets/css/a-guide-to-flexbox/](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
    
- Juegos interactivos de Flexbox
    
    [http://www.flexboxdefense.com/](http://www.flexboxdefense.com/)
    
    [https://flexboxfroggy.com/](https://flexboxfroggy.com/)
    
- Guía de CSS Grid

[Actividad CSS Grid](https://gist.github.com/Alfredprofe/b6a1100ad82e1d4b7d237d974696ffd5)

[Actividad Flexbox](https://gist.github.com/Alfredprofe/d14334e45867b8b2f1c8b59e59134b56)

### Referencia bibliográfica

- Coyier, C., van Damme, T., Merkenich, J., Coyier, C., Coyier, C., Mejia, L., Coyier, C., Coyier, C., Coyier, C., Seyedi, M., Gaebel, D., Gaebel, D., Khare, M., Graham, G., Coyier, C., Coyier, C., Coyier, C., Coyier, C., Coyier, C., . . . Coyier, C. (2021, 9 diciembre). *A Complete Guide to Flexbox*. CSS-Tricks. Recuperado 9 de diciembre de 2021, de https://css-tricks.com/snippets/css/a-guide-to-flexbox/
- House, C. (2021, 10 noviembre). *A Complete Guide to Grid*. CSS-Tricks. Recuperado 9 de diciembre de 2021, de https://css-tricks.com/snippets/css/complete-guide-grid/
- Cruz, R. (s. f.). *CSS Grid cheatsheet*. Devhints.Io Cheatsheets. Recuperado 9 de diciembre de 2021, de https://devhints.io/css-grid
