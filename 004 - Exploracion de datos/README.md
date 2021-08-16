# Exploración de Datos
Una vez importada la data, procedemos a examinar el resultado. Esto es un paso importante, puesto que de la data dependen los resultados de nuestro análisis. Es por esto que, antes de continuar, debemos revisar la data.

Este proceso podemos dividirlo en dos fases: en la primera estaremos enfocados en identificar los valores perdidos de la base de datos y en la segunda identificaremos los valores atípicos, es decir, valores fuera de lo común.

## Identificando Valores Perdidos
Los valores perdidos pueden ser provocados por diferentes razones, pero la conclusión es la misma: no existe ese valor. Para ilustrar esta situación estaremos utilizando la base de datos de "Employee Selection Data". Esta base recopila información (su nivel de IQ, una medida de bienestar laboral y otra de desempeño laboral luego de 6 meses) de 20 empleados. Algunas de estas informaciones han sido intencionalmente eliminadas para fines ilustrativos.

```
library(mice)
data("employee")

# Descripción de la base de datos
?employee
```

Hay diferentes formas de examinar de manera general una base de datos. Primero podemos revisar la dimensión de la misma, es decir, revisar cuantas variables y observaciones tiene la base de datos. Si necesitamos más información, podemos revisar los nombres de las variables y el tipo de variable. También podemos observar *n* número de observaciones al inicio, al final o de manera aleatoria.Para esto podemos utilizar el siguiente código.

```
# Dimensión de la base
dim(employee)

# Nombres y tipo de variables
str(employee)

# n primeras observaciones
head(employee, n = 6)

# n últimas observaciones
tail(employee, n = 6)

# n observaciones aleatorias
employee[sample(1:nrow(employee), size = 6),]
```

De entrada podemos ver que hay algunas observaciones que tienen valores perdidos en "jobperf". 
