# Taller de repaso de algoritmos

1. ## **Verificación de peso de despegue**
    
    En una pista de pruebas de aeronaves, el sistema debe verificar si el peso total de la aeronave, incluyendo combustible y carga, supera el límite máximo permitido para el despegue. Dependiendo del resultado, el sistema deberá indicar si la aeronave está lista para despegar o si debe reducir carga o combustible.

    ### Análisis

| Variable | Tipo de Variable | Comentario |
|----------|------------------|------------|
| Peso_aeronave | Entrada | Esta variable será ingresada por el usuario, la cuál indicará el peso de la aeronave **en vacío.** |
| Peso_carga | Entrada | Esta variable será ingresada por el usuario, la cuál indicará el peso de la carga dentro de la aeronave. Este valor incluye el peso de la cabina (pilotos, tripulación y pasajeros) y la carga paga (maletas o mercancía).
| Peso_combustible | Entrada | Esta variable será ingresada por el usuario, la cuál indicará el peso del combustible cargado en la aeronave para el vuelo.
| Peso_lim | Entrada | Esta variable será ingresada por el usuario, la cuál indica cuál es el peso límite de despegue de la aeronave en cuestión.
| Peso_total | Salida | Esta variable indicará cuál es el peso total de la aeronave. A partir de este valor se determinará si la aeronave está lista para despegar, o si supera el límite de peso permitido. |
| Diferencia_pesos | Salida | Esta variable mostrará la diferencia de pesos entre el peso límite y el peso de la aeronave.

### Pseudocódigo

```
Inicio
Escribir "Ingresar el peso de la aeronave vacía [kg]"
Leer Peso_aeronave
Escribir "Ingresar peso de la carga en la aeronave [kg]"
Leer Peso_carga
Escribir "Ingresar el peso cargado a la aeronave [kg]"
Leer Peso_combustible
Escribir "Ingresar el peso límite para el despegue"
Leer Peso_lim
Peso_total = Peso_aeronave + Peso_carga + peso_combustible 
Diferencia_pesos= Peso_lim - Peso_total
Si Peso_total > Peso_lim:
   Diferencia_pesos = Diferencia_pesos * (-1)
   Escribir: "La aeronave no está lista para despegar. Necesita reducir" Diferencia_pesos "kg"
   Si no 
   Escribir: "La aeronave está lista para despegar"
Fin si
Fin
```


2. ## **Control de temperatura del motor**
    
    Durante una inspección de rutina, se mide la temperatura de un motor de turbina. Si la temperatura es mayor a un valor crítico, se debe indicar "Peligro: sobrecalentamiento". Si está dentro del rango seguro, indicar "Operación normal". Si es demasiado baja, indicar "Motor frío – Calentar antes de operar".

    ## Ánalisis
| Variable | Tipo de Variable | Comentario |
|----------|------------------|------------|
|T_motor|Entrada | Es el valor ingresado por el usuario, la cual indicará la temperatura en la turbina|
|T_min |Entrada | Es el valor de temperatura mínima segura para el funcionamiento |
|T_max |Entrada | Es el valor de temperatura en el que se considera crítico |
|Estado_motor |Salida | Indica el estado del motor, y dará la indicación |

## Pseudocódigo

```
Inicio
Escribir: "Ingresar la temperatura registrada [°C]"
Leer T_motor
Escribir: "Ingrese la temperatura minima segura [°C]"
Leer T_min
Escribir: "Ingrese la temperatura máxima segura [°C]"
Leer T_max
Si T_motor > T_max:
  Esribir: "Peligro: sobrecalentamiento"
   si no
     Si T_motor < T_min:
     Escribir: "Motor frío - Calentar antes de operar"
      Si no 
       Escribir: "Operación normal"
       Fin si
    Fin si
Fin
```
# Con bucles

1. **Registro de altitudes de vuelo**
    
    Un sistema debe registrar la altitud de vuelo cada 10 minutos durante una hora y mostrar todas las mediciones al final.

## Análisis
| Variable | Tipo de Variable | Comentario |
|----------|------------------|------------|
|Altitud | Entrada| 
|i| Controlador|
|Dato |


## Pseudocódigo

```
Inicio
Definir altitud[6] 
Para i = 1 hasta i = 6
 Escribir: "Ingrese la altitud"
 Leer altitud
 Altitud[i] = Dato
 i = i + 1
 Fin para

 Escribir: "Registro de altitudes durante una hora:"
 Para i = 1 hasta i = 6
 Escribir: "Minuto" i*[10] ":" Dato 
 Fin para
Fin
```

2. **Control de combustible en pruebas**
    
    Durante un ensayo en banco de un motor a reacción, se mide el nivel de combustible cada minuto y se detiene el registro cuando el combustible baja del 10%. Mostrar el tiempo total de operación antes de llegar a ese punto.

## Ánalisis

| Variable | Tipo de Variable | Comentario |
|----------|------------------|------------|
|N_combustible|Entrada |Valor ingresado por el usuario que indica el nivel de combustible por minuto|
|Tiempo |Salida |Tiempo total de operación |
| i |Control |Indicador de ciclos |





## Pseudocódigo 

```
Inicio
Tiempo = 0
Escribir: "Ingrese el nivel de combustible [%]"
Leer N_combustible
 Si N_combustible >= 10  Entonces
 Tiempo = Tiempo + 1
 Fin si
Hasta que N_combustible < 10
Escribir: "Tiempo total de operación", Tiempo, "minutos"
Fin 

