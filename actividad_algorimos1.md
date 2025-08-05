#Ejercicios

##Ejercicio 3
- Realice un algoritmo para determinar cuánto se debe pagar por equis cantidad de Lápices considerando que si son 1000 o más el costo es de $85 cada uno; de lo contrario, el precio es de $90. Represéntelo con el pseudocódigo y el diagrama de flujo.

|Variables| Tipo| Comentario|
|---------|-----|-----------|
|Lápices | Entrada| Cantidad de Lápices|
|Precio | Salida| Precio total de Lápices|
|85,90 | Contantes| No cambian|

## Pseudocódigo

```
Inicio
Leer Lápices
si Lápices>=1000:
    valor_unidad = 85
Si no 
    valor_unidad = 90
Fin Si
Precio = Lápices * valor_unidad
Escribir "El valor total es:", Precio
Fin

```

![alt text] (diagrama1.PNG)

4.  Un almacén de ropa tiene una promoción: por compras superiores a $250 000 se les aplicará un descuento de 15%, de caso contrario, sólo se aplicará un 8% de descuento. Realice un algoritmo para determinar el precio final que debe pagar una persona por comprar en dicho almacén y de cuánto es el descuento que obtendrá. Represéntelo mediante el pseudocódigo y el diagrama de flujo.

## Análisis

|Variables| Tipo| Comentario|
|---------|-----|-----------|
|Totalcompra| Entrada|Valor bruto de la compra |
|Preciofinal| Salida | precio a pagar con el descuento aplicado|
|descuento | salida| |Descuento según el valor de la compra |
|15% / 8% / $250000 |constantes|descuentos que se pueden aplicar, valor de referencia|

## Pseudocódigo

```
Inicio
Leer totalcompra
si totalcompra <250000:
  descuento=totalcompra*0.15
si no
  descuento=totalcompra*0.08
Fin si
preciofinal=totalcompra-descuento
Escribir "Valor a pagar:" , preciofinal, ". Se hizo n descuento de", 
descuento
Fin

```

5. El director de una escuela está organizando un viaje de estudios, y requiere determinar cuánto debe cobrar a cada alumno y cuánto debe pagar a la compañía de viajes por el servicio. La forma de cobrar es la siguiente: si son 100 alumnos o más, el costo por cada alumno es de $65.00; de 50 a 99 alumnos, el costo es de $70.00, de 30 a 49, de $95.00, y si son menos de 30, el costo de la renta del autobús es de $4000.00, sin importar el número de alumnos.

## Análisis
|Variables| Tipo| Comentario|
|---------|-----|-----------|
|Alumno| Entrada|Cantidad de alumnos |
|costoalumnos| Salida | precio a pagar de los alumnos|
|costototal| salida| |Costo a pagar de los alumnos y autobus |
|alumnos >= 100 / 50 <= alumnos < 100 / 30 <= alumnos <50 / alumnos <30 / $4000 |constantes|rango de alumnos|

## Pseudocódigo

```
Inicio
Leer alumnos
Si alumnos >= 100:
  costoalumno=65.00
  costototal:= costoalumno*alumno
    Si no:
     Si 50 <= alumnos <100
     costoalumno=70.00
     costototal= costoalumno*alumno
       Si no:
         Si 30 <= alumnos <50
         costoalumno=95.00
         costototal= costoalumno*alumnos
         Si no:
         Si alumnos <30
          costototal=4000
          costoalumno=costototal/alumno
          Fin si
    Fin si
Fin si
Escribir "Costo total:", cotoalumno
Fin

 ```
 




