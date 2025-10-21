Podemos visualizar el resultado de variables dentro de cadenas de texto, así como imprimir el texto final con un print. Durante la lección, aprendimos a utilizar la f-string (formateo de cadena), en la que colocamos una f antes de crear la cadena y las variables se colocan entre llaves {}. Ejemplo:
```python
nombre = "Ana María"
edad = 17
print(f"El nombre de la alumna es {nombre} y su edad es {edad} años.")
```
Copia el código
```python
Salida: 'El nombre de la alumna es Ana María y su edad es 17 años.'
```
Pero existen otros métodos de formateo, como el uso del operador de formateo de cadena o la función .format().

Operador de Formateo:

Este operador de formateo permite la inserción de variables en puntos específicos en la cadena de texto utilizando el operador %. Este operador funciona como un marcador, indicando dónde se expondrá el valor de la variable en la cadena.

El % debe ir acompañado de una palabra clave para cada tipo de variable que se desee agregar. De acuerdo con la tabla siguiente:
```python
Tipo de Variable	Palabra Clave
Cadena de texto	    %s
Entero	            %d
Punto flotante	    %f
Caractér	        %c
```
De esta manera, para insertar una variable, puedes agregar el operador en la cadena en el punto deseado. Luego del final de la cadena, agrega nuevamente el %, especificando la variable entre paréntesis. Podemos ver esta estructura en el ejemplo siguiente:
```python
nombre_alumno = 'Penélope Camacho'
print('Nombre del alumno: %s' %(nombre_alumno))
```
Copia el código
```python
Salida: 'Nombre del alumno: Penélope Camacho'
```
Si tienes más de una variable, debes ordenarlas según su aparición en el texto y separarlas por comas. Por ejemplo:
```python
nombre_alumno = 'Penélope Camacho'
edad_alumno = 11
media_alumno = 9.95
print('Nombre del alumno es %s, tiene %d años y su media es %f.' %(nombre_alumno, edad_alumno, media_alumno))
```
Copia el código
```python
Salida: 'Nombre del alumno es Penélope Camacho, tiene 11 años y su media es 9.950000.'
```
Cuando trabajamos con números de coma flotante (float), podemos determinar la cantidad de decimales después del punto utilizando la sintaxis %.xf, donde x es el número de decimales deseados. Utilizando las mismas variables del ejemplo anterior, el código con %.xf se vería así:
```python
print('Nombre del alumno es %s, tiene %d años y su media es %.2f.' %(nombre_alumno, edad_alumno, media_alumno))
```
Copia el código
```python
Salida: 'Nombre del alumno es Penélope Camacho, tiene 11 años y su media es 9.95.'
```
Un detalle importante es que los operadores de formateo de cadena con % no funcionan directamente con valores booleanos. Una forma de manejarlo es convirtiendo el valor booleano en una cadena antes de utilizarlo en el formateo con la función str(). Por ejemplo:
```python
x = True
print("Valor de x: %s" % str(x))
```
Copia el código
```python
Esto no es un problema con las f-strings o .format.
 ```
```python
Método .format():
```
También es posible utilizar el método .format() para formatear cadenas. Es más flexible y permite pasar las variables directamente dentro de la cadena, sin necesidad de operadores %. Los marcadores son simplemente {}. Por ejemplo:
```python
nombre_alumno = 'Penélope Camacho'
print('Nombre del alumno: {}'.format(nombre_alumno))
```
Copia el código

Del mismo modo que se hace con el operador, puedes usarlo con varias variables:
```python
nombre_alumno = 'Fabricio Daniel'
edad_alumno = 15
media_alumno = 9.95
print('Nombre del alumno es {}, tiene {} años y su media es {}.' .format(nombre_alumno, edad_alumno, media_alumno))
```
Copia el código
Nota que con .format(), no tienes el problema de los decimales de coma flotante. Tampoco tienes este problema con las f-strings.

En resumen, cada uno de estos métodos tiene sus ventajas y desventajas. Se recomienda utilizar f-strings, ya que son más legibles y fáciles de usar. Sin embargo, cada desarrollador puede elegir el método que le parezca más apropiado.

Caracteres Especiales:

Además de la formateo de inserción de variables en una cadena, también existen caracteres especiales. Se utilizan para representar acciones especiales o caracteres que no se pueden escribir directamente, como el “Enter” y la tabulación. A continuación, presentamos algunos de ellos. Intenta replicar todos los ejemplos y observa el resultado final.

\n es el carácter de nueva línea y se usa para saltar una línea en el texto (similar a la función "Enter"). Ejemplo:

```python
print("Estudiar es un esfuerzo constante,\nEs como cultivar una planta,\nNecesitamos dedicación y paciencia,\nPara ver madurar el fruto.")
```
Copia el código
\t es el carácter de tabulación y se utiliza para agregar un espacio de tabulación en el texto. Ejemplo:

```python
print('Cantidad\tCalidad\n5 muestras\tAlta\n3 muestras\tBaja')
```
Copia el código
\\ se usa para imprimir una sola barra invertida. Si no se utiliza una doble barra invertida, el código podría generar un error o un resultado inesperado, ya que Python considera \ como un carácter especial. Usamos esta sintaxis para garantizar que no ocurran errores. Ejemplo:

```python
print("Ruta del archivo: C:\\archivos\\documento.csv")
```
Copia el código
\" se utiliza para imprimir comillas dobles cuando estamos trabajando con una cadena creada con comillas dobles " en el interior. Sin embargo, esto no es necesario si la cadena se crea con comillas simples '. Ejemplo:

```python
print("Una vez oí: \"Los frutos del conocimiento son los más dulces y duraderos de todos.\"")
```
Copia el código
\' se utiliza para imprimir comillas simples cuando estamos trabajando con una cadena creada con comillas simples '. Si la cadena se crea con comillas dobles ", esto no es necesario. Ejemplo:

```python
print('Mi profesora una vez dijo: \'Estudiar es la clave del éxito.\'')
```
Copia el código


Una condición no es más que una comparación entre datos a partir de la cual podemos obtener el resultado verdadero o falso de una condición. La comparación puede realizarse mediante operadores relacionales cuya misión es comparar valores y determinar si una expresión es verdadera o falsa. A continuación, conoceremos los operadores lógicos y cómo utilizarlos.

##Mayor que (>)

Devuelve verdadero si el valor a la izquierda del símbolo es mayor que el de la derecha. Su sintaxis, valor_1 > valor_2, representa una comparación que solo será verdadera si valor_1 es mayor que valor_2. Con este operador relacional, podemos verificar si una persona es mayor que otra al comparar sus edades, como se muestra en el siguiente ejemplo:

edad_maria = int(input('Ingrese la edad de María: '))
edad_beatriz = int(input('Ingrese la edad de Beatriz: '))

if edad_maria > edad_beatriz:
  print('María es mayor que Beatriz.')


  El operador mayor que (>) devuelve un valor falso si los valores comparados son iguales o si el valor a la izquierda del símbolo es inferior al de la derecha.

  ##Menor que (<)

Devuelve verdadero si el valor a la izquierda del símbolo es menor que el de la derecha. Su sintaxis es valor_1 < valor_2. Esta comparación solo será verdadera si valor_1 es menor que valor_2. Con este operador relacional, también podemos verificar si una persona es menor que otra al comparar sus edades, como se muestra a continuación:

edad_maria = int(input('Ingrese la edad de María: '))
edad_beatriz = int(input('Ingrese la edad de Beatriz: '))

if edad_maria < edad_beatriz:
  print('María es menor que Beatriz.')

Este operador también devuelve un valor falso si los valores comparados son iguales o si el valor a la izquierda del símbolo es superior al de la derecha.

  ##Mayor o igual a (>=)

Devuelve verdadero si el valor a la izquierda del símbolo es mayor o igual al valor a la derecha. Su sintaxis es valor_1 >= valor_2. Esta comparación solo será verdadera si valor_1 es mayor o igual a valor_2. Con este operador relacional, podemos verificar, por ejemplo, si una empresa tiene una cantidad mayor o igual a la de otra, como se muestra a continuación:

empleados_empresa_1 = int(input('Ingrese la cantidad de empleados de la empresa 1: '))
empleados_empresa_2 = int(input('Ingrese la cantidad de empleados de la empresa 2: '))

if empleados_empresa_1 >= empleados_empresa_2:
  print('La empresa 1 tiene una cantidad de empleados mayor o igual a la empresa 2.')

  ##Menor o igual a (<=)

Devuelve verdadero si el valor a la izquierda del símbolo es menor o igual al valor de la derecha. Su sintaxis es valor_1 <= valor_2. Esta comparación solo será verdadera si valor_1 es menor o igual a valor_2. Con este operador relacional, podemos verificar si una empresa tiene una cantidad menor o igual a otra, como se muestra a continuación:

empleados_empresa_1 = int(input('Ingrese la cantidad de empleados de la empresa 1: '))
empleados_empresa_2 = int(input('Ingrese la cantidad de empleados de la empresa 2: '))

if empleados_empresa_1 <= empleados_empresa_2:
  print('La empresa 1 tiene una cantidad de empleados menor o igual a la empresa 2.')

  
##Igual a (==)

Devuelve verdadero si el valor a la izquierda del símbolo es igual al valor de la derecha. Su sintaxis, valor_1 == valor_2, representa una comparación que solo será verdadera si valor_1 es igual a valor_2. Con este operador relacional, podemos verificar si dos libros tienen el mismo título mediante una comparación de cadenas, como se muestra en el siguiente ejemplo:

libro_1 = input('Ingrese el título del 1° libro: ')
libro_2 = input('Ingrese el título del 2° libro: ')

if libro_1 == libro_2:
  print('Los libros tienen el mismo título.')


  Diferente de (!=)

Devuelve verdadero si el valor a la izquierda del símbolo es diferente del valor a la derecha. Su sintaxis, valor_1 != valor_2, representa una comparación que solo será verdadera si valor_1 es diferente de valor_2. Este operador es el inverso de ==. Con él, podemos verificar si dos libros tienen títulos diferentes mediante una comparación de cadenas, como se muestra a continuación:

libro_1 = input('Ingrese el título del 1° libro: ')
libro_2 = input('Ingrese el título del 2° libro: ')

if libro_1 != libro_2:
  print('Los libros tienen títulos diferentes.')

  También es posible realizar esta comparación con valores numéricos.

  

 
