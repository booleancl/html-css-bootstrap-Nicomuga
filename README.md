# HTML CSS BOOTSTRAP

Html CSS y Javascript son los pilares de toda aplicación o sitio web. Cualquier cosa que funcione dentro de un navegador web (chrome, mozilla, safari) utiliza estos pilares. Y no solo eso, hoy también se pueden hacer aplicaciones "nativas" con estas tecnologías.

## HTML

Significa **Hyper Text Markup Language**, que en castellano sería algo como Lenguaje de marcado de hyper texto. Lenguaje de marcado es por la *Etiquetas*. Dependiendo de su etiqueta el navegador lo procesa de diferente forma. Y el hyper texto se refiere a que estos documentos están enlazados por *links*.

Con HTML crearemos *documentos estructurados* mediante etiquetas que el navegador puede interpretar.

El documento principal de un sitio o aplicación de debe llamar **index.html**. Todo junto y en minúsculas.

### Doctype

Esta primera etiqueta indica al navegador la versión de HTML. En este caso indica que es la versión 5.
```html
  <!DOCTYPE html>
```

### html
Luego de eso viene la primera etiqueta que es parte del documento. la famosa etiqueta **html**:
```html
<html lang="es">
  ...
</html>
```

Del ejemplo anterior vemos que esta etiqueta se compone de 2 partes principales. La etiqueta de apertura `<html>` y la de cierre `</html>`.

Entremedio de las etiquetas de apertura y cierre irá el contenido.

Además vemos la etiqueta de apertura tiene el **atributo** `lang="es"`, lo que le indica al navegador en qué idioma está el contenido del documento.

>**ATENCIÓN**: Solo las etiquetas de apertura pueden tener atributos, Las etiquetas de cierre no.

### head

A continuación viene etiqueta `head`. Esta etiqueta entrega información al **Navegador** sobre como visualizar el contenido que vendrá en las siguientes secciones. Por ejemplo se indica mediante etiquetas `meta` el set de caracteres que utilizará la página. Ejemplo:

```html
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hola Microsystem</title>
</head>
```

La tercera etiqueta `meta` que tiene el atributo `name="viewport"` permite que el contenido se cargue inicialmente considerando el tamaño de pantalla disponible, desde grandes a muy pequeños.

Además dentro del head se encuentra la etiqueta `title`, que es la encargada de mostrar el nombre del sitio en la pestaña del navegador.

Por otra parte dentro del `head` podemos cargar otros recursos que utilizará el documento como por ejemplo hojas de estilo CSS o archivos Javascript

### Estructura Jerárquica

Algo que es muy muy muy importante notar y que no es tan evidente, es que los documentos HTML forman una estructura jerárquica bien definida del tipo árbol. Donde la etiqueta raíz es la etiqueta `html`. Lo podemos visualizar de la siguiente forma

```html
  <html>
    <head></head>
    <body></body>
  </html>
``` 

Esto es muy importante de comprender ya que luego manejaremos las etiquetas pensando en su ubicación relativa dentro del árbol. Y pensaremos que las etiquetas son **nodos** que tienen **nodos padre**, **hermanos** y **nodos hijos**.

## Etiquetas principales

### Títulos

Las etiquetas para hacer títulos son las etiquetas **h** con números del 1 al 6. Ejemplos

```html
  <h1>Súper título</h1>
  <h2>Súper sub título</h2>
  <h3>Súper sub sub título</h3>
  <h4>...</h4>
  <h5>...</h5>
  <h6>...</h6>
```

### Links

Los links son el corazón de internet y los crearemos frecuentemente. Se componen de el atributo `href` que indica el destino del link y su contenido, que es lo que se muestra al usuario

```html
  <a href="headings.html">Títulos</a>
```

### Imágenes

Las imágenes son una de las etiquetas que no require de cierre ya que la imagen que se despliega se indica mediante el atributo `src` y en caso de que la imagen no esté disponible se despliega el texto indicado en el atributo `alt` conocido como texto alternativo.


### Listas

#### Ordenadas

```html
  <ol>Dias de la semana
    <li>Lunes</li>
    <li>Martes</li>
    <li>Miércoles</li>
    <li>Jueves</li>
    <li>Viernes</li>
  </ol> 
```

#### No ordenadas

```html
  <ul>Pilares de la Web
    <li>HTML</li>
    <li>CSS</li>
    <li>Javascript</li>
  </ul>
```

### Tablas

```html
  <table>
    <tr>
      <th>Italiano</th>
      <th>Chacarero</th>
    </tr>
    <tr>
      <td>Tomate</td>
      <td>Lechuga</td>
    </tr>
    <tr>
      <td>Palta</td>
      <td>Porotos</td>
    </tr>
    <tr>
      <td>Mayo</td>
      <td>Ají</td>
    </tr>
  </table>
```

## Formularios