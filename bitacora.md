TABLE 1
┌─────────┬────┬──────────────┬─────────┬───────────────────────┬────────────┬──────────┬────────┐
│ (index) │ id │ fecha        │ cliente │ producto              │ ciudad     │ cantidad │ precio │
├─────────┼────┼──────────────┼─────────┼───────────────────────┼────────────┼──────────┼────────┤
│ 0       │ 1  │ '2026-09-01' │ 'C01'   │ 'Origen Huila 500 g'  │ 'Medellín' │ 2        │ 42000  │
│ 1       │ 2  │ '2026-09-01' │ 'C02'   │ 'Origen Nariño 250 g' │ 'Bogotá'   │ 1        │ 26000  │
│ 2       │ 3  │ '2026-09-02' │ 'C03'   │ 'Prensa francesa'     │ 'Cali'     │ 1        │ 95000  │
│ 3       │ 4  │ '2026-09-02' │ 'C01'   │ 'Origen Huila 500 g'  │ 'Medellín' │ 1        │ 42000  │
│ 4       │ 5  │ '2026-09-03' │ 'C04'   │ 'Origen Sierra 500 g' │ 'medellín' │ 3        │ 45000  │
│ 5       │ 6  │ '2026-09-03' │ 'C05'   │ 'Origen Nariño 250 g' │ 'Bogotá'   │ 2        │ 26000  │
│ 6       │ 7  │ '2026-09-04' │ 'C02'   │ 'Molino manual'       │ 'Bogotá'   │ 1        │ 120000 │
│ 7       │ 8  │ '2026-09-04' │ 'C06'   │ 'Origen Huila 500 g'  │ 'Cali'     │ 0        │ 42000  │
│ 8       │ 9  │ '2026-09-05' │ 'C03'   │ 'Origen Sierra 500 g' │ 'Cali'     │ 2        │ 45000  │
│ 9       │ 10 │ '2026-09-05' │ 'C07'   │ 'Origen Huila 500 g'  │ 'Pereira'  │ 4        │ 42000  │
│ 10      │ 11 │ '2026-09-06' │ 'C01'   │ 'Prensa francesa'     │ 'Medellín' │ 1        │ 95000  │
│ 11      │ 12 │ '2026-09-06' │ 'C08'   │ 'Origen Nariño 250 g' │ 'Bogotá'   │ 3        │ 26000  │
└─────────┴────┴──────────────┴─────────┴───────────────────────┴────────────┴──────────┴────────┘

Errors found:
- For "Ciudades", Medellín City has 2 different input ways, one with upppercase and other with lowercase: Medellín and medellín. 
- For "Cantidades", 'Origen Huila 500 g' has 0 units, that could be an inconvienient when proccesing math operations. 
- For "cliente", C01,C02, and C03 there are more than 1 input aisgned to their ID. C01 (ID 1,4, and 11),C02 (IDs 2 and 7), and C03 (IDs 3 and 9)
- For "producto" index 2 , 6 and 10 has asigned values which doe snot match with the main topic for this category (which is the coffe orgin and not the Type of preparation)

------------------------------------------------------------------------------------------------
PROBLEM                                       //       ACTION
------------------------------------------------------------------------------------------------
vENTA 8 CON CANTIDAD 0                              No contar en el ticket
Ciudades con espacios y miusculas                   Normalizar antes de comparar
clientes con compras repetidas                      es valido, asignar valores S5 y S6
Diccionario de datos                                Propiedad ~ tipo ~ significado


------------------------------------------------------------------------------------------------
DICCIONARIO DE DATOS
------------------------------------------------------------------------------------------------

DATO                PROPIEDAD               TIPO                SIGNIFICADO                         

id                                          entero              Muestra el numero identificador unico de cada usuario
fecha                                       Fecha               Muestra la fehca en la que se realizo la compra
cliente                                     String              Muestra el nombre del cliente
producto                                    string              Muestra el nombre del producto en cada compra
ciudad                                      string              Muestra la ciudad en donde se realizo la compra
cantidad                                    entero              Muestra la cantidad de que se ha comprado de cierto producto    