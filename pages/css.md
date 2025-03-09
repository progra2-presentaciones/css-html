# CSS
- Permite que el **diseño**, la **maquetación** y la **presentación** de una página web se definan por separado de la semántica y la estructura del contenido. 
- Esta separación mantiene el código fuente legible y permite que un diseñado(a) actualice los estilos por separado.
- En una hoja de estilo se definen reglas como la siguiente:
```css
h1 {color: maroon;}
body {background: yellow;}
```

-  Estructura de una regla
![Estructura de una regla](/estructura_regla.png)
<style>
    img{
        margin: 10px auto;
        width:70%;
        height:70%;
    }
</style>

---
# Conceptos del CSS
layout: two-cols
layoutClass: gap-10
---
## Elementos de nivel en línea

- Los elementos de nivel en línea generan una caja de elemento dentro de una línea de texto.
- No generan un salto. 
- Ejemplos en HTML: `<a>`, `<strong>` y `<em>`.

```html
<book>
<maintitle>The Victorian Internet</maintitle>
 <subtitle>The Remarkable Story of the Telegraph and the Nineteenth Century's
   On-Line Pioneers</subtitle>
 <author>Tom Standage</author>
 <publisher>Bloomsbury Pub Plc USA</publisher>
 <pubdate>February 25, 2014</pubdate>
 <isbn type="isbn-13">9781620405925</isbn>
 <isbn type="isbn-10">162040592X</isbn>
</book>
```
<div style="font-size: smaller;">
The Victorian Internet The Remarkable Story of the Telegraph and the Nineteenth Century's On-Line Pioneers Tom Standage Bloomsbury Pub Plc USA February 25, 2014 9781620405925 162040592X
</div>
::right::
## Elementos de nivel de bloque

- Generan una caja de elemento que llena el área de contenido de su elemento padre
- Producen "saltos" antes y después de la caja del elemento. 
- Ejemplos en HTML: `<p>` y `<div>`. 

```css
book, maintitle, subtitle, author, isbn {display: block;}
publisher, pubdate {display: inline;}
```

[¿qué sucede si se le aplica el estilo?](https://webdesignplayground.io/)

---
# Inclusión de un archivo CSS
layout: two-cols
layoutClass: gap-4
---
# Integración de CSS en HTML

## Estilo INLINE
- Las especificaciones CSS se escriben directo en el `elemento` HTML (**NO RECOMENDADO**)
```html 
  <header style="background: #add8e6; padding: 2px;
                 text-align: center;">
  <h1 style="font-family: Verdana;>My cooking blog</h1>
  <p style="font-family: Verdana;>A blog with delicious recipes...</p>
  </header>
  <nav style="text-align: center;>
  <p style="font-family: Verdana;>
    <a href="#>blog</a> | <a href="#>recipes</a> |
    <a href="#>About me</a> | <a href="#>Legal notes</a>
  </p>
  </nav>
```
::right::
## Hoja de estilo INTERNO
- Se especifica la sentencia de estilo en el encabezado del HTML 

```html
<!doctype html>
<html lang="en>
  <head>
    <title>My cooking blog</title>
    <meta charset="UTF-8>
    <style>

       body { margin: 0px; }
       h1 {
         font-family: "Verdana", "Geneva";
         font-size: 200%;
         text-align: center;
       }
       p { font-family: "Verdana", "Geneva"; }
       ...
       </style>
   </head>
       <body>
        ...
        </body>
</html>
```
---
# Inclusión de un archivo CSS
layout: two-cols
layoutClass: gap-4
hideInToc: true
---
# Integración de CSS en HTML
## Sentencias de estilo en un archivo externo CSS
```html
<!doctype html>
<html lang="en>
  <head>
    <title>My cooking blog</title>
    <meta charset="UTF-8>
    <link rel="stylesheet href="style.css>
  </head>
  <body>
  ...
  </body>
</html>
```
::right::

![Integración HTML y CSS](/css_html.png)

- Inspección del documento  [Ctrl] + [Shift] + [I]
---
# Inclusión de un archivo CSS
---
# Inclusión de un archivo CSS
## Hojas de estilo para dispositivos específicos
- ural, braille, embossed, handheld, projection, speech, tty o tv
```html
...
  <head>
    <title>My cooking blog</title>
    <meta charset="UTF-8>
    <style>

      @import url("style.css") screen;
      @import url("print.css") print;

    <style>
  </head>
```
