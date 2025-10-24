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

¹ Una expresión lógica es una declaración que puede ser evaluada como verdadera o falsa. Ella se compone por operandos lógicos² y por operadores lógicos³, que son usados ​​para combinar varias expresiones lógicas en una única expresión.

² Los operandos lógicos son los elementos que son comparados o evaluados en una expresión lógica. Ellos son generalmente valores verdaderos o falsos, pero también pueden ser expresiones lógicas más complejas. En Python, los operandos lógicos son los valores True y False.

³ Los operadores lógicos son ls símbolos o palabras clave que son usados ​​para combinar varias expresiones lógicas en una única expresión. En Python, los operadores lógicos son and, or y not, bien como las palabras clave if, elif e else.

Operadores lógicos más comunes

a    b  AND  OR  NOT
|0  |0  |0  |0  |1
|0  |1  |0  |1  |- 
|1  |0  |0  |1  |- 
|1  |1  |1  |1  |0

# Comandos de Control

Cuando trabajamos con bucles, podemos controlar el flujo de ejecución dentro del bloque de código, lo que nos permite manipular la ejecución de los bucles. continue y break son los comandos de control que podemos usar con los bucles for y while.

** continue ** interrumpe la iteración actual del bucle y salta a la siguiente, es decir, regresa al inicio del código. Como ejemplo, aquí hay un código que cuenta del 1 al 5 con un bucle for:


´´´python
for i in range(1, 6):
    if i == 4:
        continue
    print(i)
´´´
Este código imprime todos los números del 1 al 5, excepto el 4. Cuando el valor de i es 4, continue salta a la siguiente iteración, omitiendo la instrucción print después de la condición en la iteración actual.

Por otro lado, break detiene por completo la ejecución del bucle, saliendo del bloque de código. Utilicemos el mismo ejemplo de conteo, pero esta vez con break:

´´´python
for i in range(1, 6):
    if i == 4:
        break
    print(i)
´´´

En este caso, el código imprime todos los números del 1 al 3. Cuando el valor de i es 4, break interrumpe por completo la ejecución del bucle y sale de él, ignorando cualquier otra iteración que esté dentro de la estructura.


    


