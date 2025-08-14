# EJERCICIOS DE BUCLES:
**Integrantes de grupo**:
- Evelyn Roldán Rendón
- David Piedrahita Valencia
- Sebastián Pulgarín Castrillón

### Ejercicio con condicionales:
1. **Verificación de peso de despegue.**
   
    En una pista de pruebas de aeronaves, el sistema debe verificar si el peso total de la aeronave, incluyendo combustible y carga, supera el límite máximo permitido para el despegue. Dependiendo del resultado, el sistema deberá indicar si la aeronave está lista para despegar o si debe reducir carga o combustible
 
**Análisis.**
 
| Variable | Tipo de Variable | Comentario |
|----------|------------------|------------|
| P_V_A | Entrada | Esta variable será ingresada por el usuario, la cuál indicará el peso de la aeronave **en vacío.** |
| P_CA_A | Entrada | Esta variable será ingresada por el usuario, la cuál indicará el peso de la carga dentro de la aeronave. Este valor incluye el peso de la cabina (pilotos, tripulación y pasajeros) y la carga paga (maletas o mercancía).
| P_CO_A | Entrada | Esta variable será ingresada por el usuario, la cuál indicará el peso del combustible cargado en la aeronave para el vuelo.
| P_LIM_D | Entrada | Esta variable será ingresada por el usuario, la cuál indica cuál es el peso límite de despegue de la aeronave en cuestión.
| P_TOT_A | Salida | Esta variable indicará cuál es el peso total de la aeronave. A partir de este valor se determinará si la aeronave está lista para despegar, o si supera el límite de peso permitido. |
| D_P_A | Salida | Esta variable mostrará la diferencia de pesos entre el peso límite y el peso de la aeronave.
 
***Nota:** Se pedirá ingresar todos los pesos en unidad de kilogramos para manejar el mismo sistema*
 
**Pseudocódigo.**
```
INICIO
Escribir "Ingrese el peso en vacío de la aeronave [Kg]"
Leer P_V_A
Escribir "Ingrese el peso de la carga en la aeronave [Kg]"
Leer P_CA_A
Escribir "Ingrese el peso del combustible cargado [Kg]"
Leer P_CO_A
Escribir "Ingrese el peso límite de despegue de la aeronave [Kg]"
Leer P_LIM_D
P_TOT_A = P_V_A + P_CA_A + P_CO_A
D_P_A = P_LIM_D - P_TOT_A
Si P_TOT_A > P_LIM_D:
    D_P_A = D_P_A * (-1)
    Escribir "La aeronave no puede despegar. Debe reducir", D_P_A, "[Kg]"
Si no:
    Escribir: "La aeronave puede despegar, aún puede almacenar", D_P_A, "[KG]"
Fin Si
FIN
```

2. **Registro de altitudes de vuelo**
    
    Un sistema debe registrar la altitud de vuelo cada 10 minutos durante una hora y mostrar todas las mediciones al final.
#### Solución
 
|Variable|Tipo|Definición|
|--------|----|----------|
|Altitud|Arreglo|Guarda las altitudes de vuelo registradas en cada intervalo de 10 minutos (6 valores).|
|i|#Entero|Contador utilizado para recorrer los índices del arreglo Altura durante la lectura y la impresión de datos.|
|dato|Entrada|Altitud registrada en determinado momento.|
 
```
Inicio
Definir Altitud[6] como arreglo numérico
Para i = 1 hasta i = 6
  Escribir "Ingrese la altitud"
  leer dato
  Altitud[i] = dato
  i = i + 1
FinPara
Escribir "Las altitudes registradas son:"
Para i = 1 hasta i = 6
  Escribir "Minuto ", i*10, ": ", Altitud[i]
  i = i + 1
FinPara
Fin
```

2. **Control de temperatura en cabina**
    
    Un sistema mide cada 5 minutos la temperatura en cabina durante una hora. Si en algún momento se detecta una temperatura mayor a 27°C o menor a 18°C, debe indicar que se active el sistema de climatización.

 #### Solución
 
|Variable|Tipo|Definición|
|--------|----|----------|
|i|Contador|Usado para determinar el avance del ciclo para|
|Temp|Entrada|Registra la Temperatura de la aeronave|
 
```
Inicio
i = 1
Para i = 1 hasta i = 12
  Escribir "ingrese temperatura"
  leer Temp
  Si 27 > Temp > 18:
    Escribir "Todo ok"
    Si no:
      Escribir "Activar climatización"
  FinSi
  i = i + 1
FinPara
Fin      
```