# Markdown

## ¿Qué es Markdown?
Es un *lenguaje de marcado* que facilita la aplicación de formato a un texto empleando una serie de caracteres de una forma especial.

En principio, fue pensado para elaborar textos cuyo destino iba a ser la web con más rapidez y sencillez que si estuviésemos empleando directamente HTML. Y si bien ese suele ser el mejor uso que podemos darle, también podemos emplearlo para cualquier tipo de texto, independientemente de cual vaya a ser su destino.

## Sintaxis de Markdown
### Cabeceras
Para poder visualizar cabeceras de distinto tamaño, se emplearán más o menos caracteres `#`, siendo necesario uno como mínimo:
```
# Esto es una etiqueta <h1>
## Esto es una etiqueta <h2>
### Esto es una etiqueta <h3>
```

# Esto es una etiqueta <h1>
## Esto es una etiqueta <h2>
### Esto es una etiqueta <h3>



### Énfasis


Se puede modificar el énfasis de las palabras mediante los siguientes caracteres:
* *Negrita*:  

    ```
    **Este texto está en negrita**

    __Este texto también está en negrita__
```

**Este texto está en negrita**

__Este texto también está en negrita__

* *Itálica*:  

    ```
    *Este texto está en itálica*

    _Este texto también está enitálica_
```

*Este texto está en itálica*

_Este texto también está enitálica_
***

### Listas
Se pueden realizar listas tanto ordenadas como no ordenadas mediante los siguientes caracteres:

* *No ordenada*:  

    ```
    * Elemento 1
      * Elemento 1a
    * Elemento 2
      * Elemento 2a
      * Elemento 2b
```
* Elemento 1
  * Elemento 1a
* Elemento 2
  * Elemento 2a
  * Elemento 2b




* *Ordenada*:  

    ```
    1. Item 1
    2. Item 2
    3. Item 3
      * Item 3a
      * Item 3b
```
1. Item 1
2. Item 2
3. Item 3
  * Item 3a
  * Item 3b

### Enlaces
Existen  dos maneras de crear enlaces:
* Con título
```
[Con titulo](http://google.com "titulo")
```
[Titulo](http://google.com "titulo")

* Sin título
```
[Sin titulo](http://google.com)
```
[Sin titulo](http://google.com)

### Imágenes
La manera de enlazar imágenes es básicamente la misma de crear enlaces, con un única diferencia, se añade el carácter exclamación ! al principio de la pareja de corchetes que definen el nombre del enlace:

* Con título
```
![Con titulo](img/markdown.png "titulo")
```
![Con titulo](img/markdown.png "titulo")

* Sin título
```
![Sin titulo](pictures/avatar.png)
```

### Citas
Para crear bloques de cita, se emplea el carácter mayor que `>` antes del bloque de texto. A continuación se pueden ver las opciones para crearlo.

*
```
Esto es una línea normal

> Esto es parte de un bloque de cita.
> Esto es parte del mismo bloque de cita.
```
Esto es una línea normal

> Esto es parte de un bloque de cita.
> Esto es parte del mismo bloque de cita.


***
```
> Esto es parte de un bloque de cita.
Esto continúa el bloque incluso aunque no hay símbolo 'mayor que'.

La línea en blanco finaliza el bloque.
```
> Esto es parte de un bloque de cita.
Esto continúa el bloque incluso aunque no hay símbolo 'mayor que'.

La línea en blanco finaliza el bloque.

***
```
Esto es una línea normal

> Esto es parte de un bloque de cita.
> Esto es parte del mismo bloque de cita.
>
> > Esto es otro bloque de cita anidado.
> > Esto es parte del bloque anidado.
>
> Esto es parte del bloque de cita de primer nivel.
```
Esto es una línea normal

> Esto es parte de un bloque de cita.
> Esto es parte del mismo bloque de cita.
>
> > Esto es otro bloque de cita anidado.
> > Esto es parte del bloque anidado.
>
> Esto es parte del bloque de cita de primer nivel.

### Tablas

Se pueden crear tablas indicando cuales son los elementos de la cabecera y separar los campos con el símbolo `|`.

* **Sin estética**
```
Cabecera A | Cabecera B
-- | --
Campo A0 | Campo B0
Campo A1 | Campo B1
```
* **Con estética**
```
| Cabecera A | Cabecera B |
| ---------- | ---------- |
| Campo A0   | Campo B0   |
| Campo A1   | Campo B1   |
```

Cabecera A | Cabecera B
-- | --
Campo A0 | Campo B0
Campo A1 | Campo B1

Se puede especificar la alineación de cada columna mediante la adición de dos puntos a las líneas de separación.
* Dos puntos a la izquierda de la línea de separación hará que la columna esté alineada a la izquierda.
* Dos puntos a la derecha de la línea hará que la columna esté alineada a la derecha.
* Dos puntos en ambos lados significa que la columna se alinea al centro.

```
| Elemento | Cantidad | Precio |
| :------- | :------: | -----: |
| Item 1   | 15       | 150€   |
| Item 2   | 3250     | 23,65€ |

```
| Elemento | Cantidad | Precio |
| :------- | :------: | -----: |
| Item 1   | 15       | 150€   |
| Item 2   | 3250     | 23,65€ |

### Código
Se pueden crear bloques de código para albergar extractos de código fuente de un lenguaje de programación o para reproducir literalmente cualquier tipo de texto sin que sea interpretado por markdown.

```
```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```
```javascript
function fancyAlert(arg) {
  if(arg) {
    $.facebox({div:'#foo'})
  }
}
```

Existe otro modo de crear un bloque de código, encerrándolo entre dos líneas formadas por tres o más caracteres tilde `~`
