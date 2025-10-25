# Para saber más: listas en diccionarios

Podemos asociar estructuras de datos a otras estructuras de datos, como ocurre cuando tenemos listas dentro de diccionarios. En este caso, las listas pueden ser almacenadas en los valores de un diccionario de tal manera que cada clave puede tener una lista asociada a ella. Esto es útil cuando necesitamos almacenar varios valores relacionados con una sola clave. Por ejemplo, podemos construir un conjunto de datos de una tienda que contenga una clave con los nombres de cada producto y otra clave con los precios correspondientes, como se muestra en el código a continuación:
```
tienda = {'nombres': ['televisión', 'celular', 'notebook', 'geladeira', 'estufa'],
          'precios': [2000, 1500, 3500, 4000, 1500]}
```
Para acceder a los valores, podemos utilizar una estructura de bucles for:
```
for clave, elementos in tienda.items():
  print(f'Clave: {clave}\nElementos:')
  for dato in elementos:
    print(dato)
``` 

El primer bucle, el más externo, recorre los elementos dentro del diccionario (claves y elementos). Sabiendo que los elementos son listas, podemos acceder a los datos de las listas con otro bucle anidado que se encuentra dentro del primer bucle. El bucle más interno recorre los elementos de cada lista uno a uno e imprime los valores dentro de ellas.

Además, podemos realizar operaciones comunes en las listas, como agregar, eliminar o contar elementos en la lista asociada a una clave del diccionario. Puedes copiar los códigos anteriores y ejecutarlos en Colab para verificar la salida.

#  Para saber más: funciones incorporadas

Durante las clases, trabajamos directamente con varias funciones incorporadas que son predefinidas y están disponibles por defecto en Python. Estas funciones trabajan como herramientas útiles para llevar a cabo tareas comunes, como conversiones de tipos, operaciones matemáticas, manipulación de cadenas y más, sin necesidad de escribir código adicional.

Algunas de las funciones incorporadas que ya conocemos son: print(), input(), len(), int(), str(), float(), range(), chr(), etc. Pero hay otras además de estas que también son muy útiles, como: sum(), help() y dir(). ¿Las conocemos?

sum()

La función sum() permite sumar los elementos de una secuencia o estructura de datos. En el siguiente ejemplo, vamos a sumar los precios de productos:

```
precios = [100.0, 400.0, 200.0]
suma = sum(precios)
suma
```
Salida: 700.0

help()

La función help() se utiliza para acceder a la documentación de funciones, métodos y otros elementos de Python. Muestra información en inglés sobre la funcionalidad, sintaxis y uso de un objeto específico. Para usar esta función, simplemente pasa el elemento deseado entre paréntesis. Por ejemplo, vamos a verificar la documentación de la función print():
```
help(print)
``` 
Salida:

```
Help on built-in function print in module builtins:
print(...)
    print(value, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
    
    Prints the values to a stream, or to sys.stdout by default.
    Optional keyword arguments:
    file:  a file-like object (stream); defaults to the current sys.stdout.
    sep:   string inserted between values, default a space.
    end:   string appended after the last value, default a newline.
    flush: whether to forcibly flush the stream.
```
dir()

Por último, la función dir() se utiliza para mostrar una lista de atributos y métodos asociados a un elemento. Por ejemplo, vamos a descubrir todos los atributos y métodos de una lista:
``` 
lista = [1,2,3]
dir(lista)
```
Salida:
```
['__add__', '__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
```
Es útil conocer varias funciones incorporadas y cómo funcionan, ya que ayudan mucho en la creación de código. Para obtener más información sobre las funciones, puedes consultar la documentación de Python.
**https://docs.python.org/3/library/functions.html"
