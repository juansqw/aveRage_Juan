# Vectores, Matrices y Data Frames
R almacena información en diferentes tipos de objetos. En esta ocasión estaremos viendo 3 tipos de los más frecuentes: vectores, matrices y data frames.

## Vectores
Los vectores son la forma más simple de almacenamiento de datos. Se caracterizan por almacenar un tipo de datos (lógico, enteros, decimales [doubles], caracteres, complejos, entre otros). Podemos crear un vector utilizando la funcion c().

```
# Lógico
c(TRUE, FALSE, TRUE)

# Entero (integer)
c(1L, 2L, 3L)

# Decimal (double)
c(1.2, 2.05, 3.5)

# Caracteres (characters)
c("banana", "manzana", "mango")

# Error intencional
c(TRUE, 1L, 1.2, "banana")
```

En la última linea del código anterior tenemos un error, esto se debe a que los vectores solamente pueden contener elementos del mismo tipo. En este caso intentamos crear un vector con un elemento lógico, entero, decimal y un caracter, respectivamente.

Podemos crear un vector y luego acceder a cada uno de sus elementos utilizando la posición del elemento que necesitemos. Otra forma de acceder es utilizando operadores lógicos. Esto lo logramos utilizando el nombre del vector seguido de [ ] y dentro colocamos la seleccion correspondiente.

```
# Crea vector numérico que contiene los números del 10 al 20
nums <- c(10:20)
nums

# Selecciona elementos por posiciones
nums[3]

# Selecciona varios elementos por posicion
nums[c(2,5)]

# Selecciona todos los elementos con excepcion de los especificados
nums[-3]

nums[-c(2,5)]

# Selecciones con operadores lógicos

# Mayor o igual que / menor o igual que
nums[nums >= 13]
nums[nums <= 13]

```

Podemos combinar dos vectores del mismo tipo utilizando la misma funcion c()

```
frutas <- c("banana", "manzana", "mango")
vegetales <- c("espinaca", "brocoli", "zanahoria")
lista_compras <- c(frutas, vegetales)
lista_compras
```

Utilizando vectores podemos realizar diferentes operaciones aritméticas, siempre teniendo en consideración que la longitud de los vectores debe ser la misma.

```
# Vectores
x <- c(1:5)
y <- c(6:10)

# Suma y resta
x + y
x - y

# Multiplicación y división
x * y
x / y

```



## Matrices

## Data Frames
