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
