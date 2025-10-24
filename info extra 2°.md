# Operadores

Durante la construcción de comandos a veces necesitamos de una elaboración mayor de la expresión condicional, necesitando que algunos operadores lógicos se encuentren integrados.

AND, OR, NOT
Los operadores lógicos and, or y not son usados para combinar expresiones lógicas en Python. Ellos son usados frecuentemente en conjunto con el comando if para crear estructuras condicionales más complejas.

## AND
es usado para verificar si dos condiciones son verdaderas. La expresión lógica¹ x and y se evalúa como True tan solo si ambas condiciones x y y son verdaderas, y como False en caso contrario.

## OR
es usado para verificar si al menos una de las condiciones es verdadera. La expresión lógica x or y se evalúa como True si al menos una de las condiciones x o y es verdadera, y como False si ambas condiciones son falsas.

## NOT
es usado para negar una condición. La expresión lógica not x es evaluada como True si la condición x es falsa, y como False si la condición x es verdadera.

- Una expresión lógica es una declaración que puede ser evaluada como verdadera o falsa. Ella se compone por operandos lógicos² y por operadores lógicos³, que son usados ​​para combinar varias expresiones lógicas en una única expresión.

- Los operandos lógicos son los elementos que son comparados o evaluados en una expresión lógica. Ellos son generalmente valores verdaderos o falsos, pero también pueden ser expresiones lógicas más complejas. En Python, los operandos lógicos son los valores True y False.

- Los operadores lógicos son ls símbolos o palabras clave que son usados ​​para combinar varias expresiones lógicas en una única expresión. En Python, los operadores lógicos son and, or y not, bien como las palabras clave if, elif e else.

Operadores lógicos más comunes

a    b  AND  OR  NOT
|0  |0  |0  |0  |1
|0  |1  |0  |1  |- 
|1  |0  |0  |1  |- 
|1  |1  |1  |1  |0

# Comandos de Control

Cuando trabajamos con bucles, podemos controlar el flujo de ejecución dentro del bloque de código, lo que nos permite manipular la ejecución de los bucles. continue y break son los comandos de control que podemos usar con los bucles for y while.

**continue** interrumpe la iteración actual del bucle y salta a la siguiente, es decir, regresa al inicio del código. Como ejemplo, aquí hay un código que cuenta del 1 al 5 con un bucle for:


```python
for i in range(1, 6):
    if i == 4:
        continue
    print(i)
```
Este código imprime todos los números del 1 al 5, excepto el 4. Cuando el valor de i es 4, continue salta a la siguiente iteración, omitiendo la instrucción print después de la condición en la iteración actual.

Por otro lado, break detiene por completo la ejecución del bucle, saliendo del bloque de código. Utilicemos el mismo ejemplo de conteo, pero esta vez con break:

```python
for i in range(1, 6):
    if i == 4:
        break
    print(i)
```

En este caso, el código imprime todos los números del 1 al 3. Cuando el valor de i es 4, break interrumpe por completo la ejecución del bucle y sale de él, ignorando cualquier otra iteración que esté dentro de la estructura.



# Para saber más: String - Una secuencia de caracteres

Como se ha visto en clases anteriores, una cadena es un tipo de dato que corresponde a datos de texto. Cuando creamos una cadena, estamos agrupando varios caracteres (números, letras e incluso símbolos), y cada uno de ellos tiene sus índices. Como ejemplo, creemos una cadena con el nombre "Python":

```python
lenguaje = 'Python'
```

Cada carácter de la cadena "lenguaje" se puede acceder mediante su índice, que comienza en 0 y va hasta la cantidad de caracteres de la cadena menos 1, incluyendo índices negativos. Podemos acceder a ellos de la misma manera que lo hacemos con las listas:

``` 
print(lenguaje[0], lenguaje[1], lenguaje[2], lenguaje[-3], lenguaje[-2], lenguaje[-1])
```
Salida: P y t h o n

Sin embargo, los índices solo se utilizan para acceder a los datos y no se puede cambiar el carácter presente en un índice específico mediante una simple asignación, como se hace con las listas. Por ejemplo, el código lenguaje[0] = 'p' generará un error en la compilación.

Con esto en mente, podríamos pensar que una cadena es una estructura de datos similar a una lista, ¿verdad? En realidad, no lo es. Una cadena es una secuencia de caracteres (letras, números, símbolos, etc.) representada por una sola variable. Por otro lado, una estructura de datos almacena una colección de elementos (que pueden ser de diferentes tipos) en una sola variable.

Sin embargo, es posible convertir una cadena en una lista mediante el método split(). Este método divide la cadena en una lista de cadenas, utilizando un delimitador especificado entre paréntesis. Este delimitador debe ser una cadena. Como ejemplo, convirtamos la cadena en una lista dividiéndola cada vez que aparezca el signo de interrogación "?":

```
pregunta = '¿Quién vino primero? ¿El huevo? ¿O fue la serpiente?'
lista_palabras = pregunta.split('?')
print(lista_palabras)
```
Salida: ['¿Quién vino primero', ' ¿El huevo', ' ¿O fue la serpiente', '']

El delimitador no aparece en la separación. Si no se define un delimitador, la cadena se separará por todos los espacios en blanco en el texto.

```
pregunta = '¿Quién vino primero? ¿El huevo? ¿O fue la serpiente?'
lista_palabras = pregunta.split()
print(lista_palabras)
``` 
Salida: ['¿Quién', 'vino', 'primero?', '¿El', 'huevo?', '¿O', 'fue', 'la', 'serpiente?']

Lo contrario también es posible, ya que podemos convertir una lista en una cadena mediante el método join(). Para usar esta función, debemos definir el carácter que se utilizará para unir los elementos de la lista y formar la cadena. Luego, usamos el método { join() pasando la lista como argumento. Veamos un ejemplo con una lista que contiene el resultado de algunas mezclas de colores primarios en pintura:

```
mezclas = ['Pinturas: rojo, azul y amarillo',
            'Verde: mezcla de azul y amarillo',
            'Naranja: mezcla de rojo y amarillo',
            'Morado: mezcla de rojo y azul']
unificador = '. '
cadena_mezclas = unificador.join(mezclas)
print(cadena_mezclas)
```   

Salida: 'Pinturas: rojo, azul y amarillo. Verde: mezcla de azul y amarillo. Naranja: mezcla de rojo y amarillo. Morado: mezcla de rojo y azul'

# **Para saber más: otras manipulaciones para las listas**

Hemos estudiado algunos métodos en clase, y además de esos, podemos utilizar otros para manipular listas en Python. Vamos a conocerlos y ver ejemplos de cómo se utilizan. En todos los casos, utilizaremos la siguiente lista llamada "razas_de_perros":

```
razas_de_perros = ['Labrador Retriever',
                   'Bulldog Francés',
                   'Pastor Alemán',
                   'Poodle']
```

El primer método es insert(), que permite insertar un elemento en una posición específica de la lista. La sintaxis es lista.insert(indice, elemento), donde "lista" es la lista que recibirá el nuevo elemento, "indice" es la posición donde se insertará el nuevo elemento y "elemento" es el nuevo elemento que se insertará.

```
razas_de_perros.insert(1, 'Golden Retriever')
razas_de_perros
```

Salida: ['Labrador Retriever', 'Golden Retriever', 'Bulldog Francés', 'Pastor Alemán', 'Poodle']

Siguiendo este enfoque, la estructura lista.insert(len(lista), elemento) es equivalente al uso del método append(), como vimos en el video anterior titulado "Manipulación de listas".

El método pop() elimina el elemento en una posición específica de la lista y lo devuelve como salida al ejecutar el método. Solo necesitamos especificar, entre paréntesis, el índice del elemento que deseamos eliminar, y se eliminará de la lista. Por lo tanto, eliminemos la raza "Golden Retriever" que agregamos en el método anterior.

```
razas_de_perros.pop(1)
```

Salida: 'Golden Retriever'

El método index() devuelve el índice de un elemento específico en la lista. Para hacerlo, especificamos el elemento entre paréntesis. Para encontrar el índice de la raza "Pastor Alemán" en la lista, hacemos lo siguiente:

```
razas_de_perros.index('Pastor Alemán')
```

Salida: 2

El método sort() ordena los elementos de la lista en orden ascendente o descendente. Si son palabras, el orden se basa en el orden alfabético o en el orden inverso. Para ordenar los valores, simplemente llamamos al método sort(), y la lista se organizará en orden. Para ordenar alfabéticamente la lista de razas de perros, podemos usar el siguiente código:

```
razas_de_perros.sort()
razas_de_perros
```

Salida: ['Bulldog Francés', 'Labrador Retriever', 'Pastor Alemán', 'Poodle']
