# Federico Olivieri DTS-03 PI03


## Reporte de calidad y detalle de los datos

- Accedi a la base de datos de FTX a traves de su api.
- Solamente ingeste las 10 criptomonedas elegidas.
### Dividi en 2 las consultas a la api
- Precios Historicos
- Precios Actuales

#### Precios Historicos
Realice una consulta para cada criptomoneda utilizando una solicitud similar a esta:

#### "https://ftx.com/api/markets/MATIC/USD/candles?resolution=86400&&start_time=0"

 Accedi a "/markets" para solicitar la info necesaria, a eso le agregue la criptomoneda a la cual queria acceder como por ejemplo "/MATIC/USD", le agregue "candles?resolution=86400" esto lo que hace es separar la informacion por dia (86400 son los segundos que tiene un dia), y por ultimo "start_time=0" que hace que me devuelva la informacion desde el segundo 0.

Una vez que ingeste las 10 criptomonedas realice lo siguiente:
- Agregue una columna id a cada tabla.
- Unifique las 10 tablas en una.
- Dropie las columnas que no necesitaba.
Me quede con las columnas
- Precio de cierre
- Precio mas alto
- Precio mas bajo
- Precio de apertura
- Fecha
- Volumen de transacciones

#### Precios Actuales

Accedi a los info actualizada utilizando una solicitud para cada criptomneda similar a esta:

#### "https://ftx.com/api/markets/MATIC/USD"

- Cree un id correspondiente a cada criptomoneda
- Unifique todo en una tabla
- Agregue la columna nombre
- Dropie las columnas que no necesitaba.
Me quede con las columnas
- Nombre
- Precio
- Precio mas alto en las ultimas 24hs
- Precio mas bajo en las ultimas 24hs
- Volumen de transaccion

### Datos utilizados en el dashboard
- Precio promedio actual (Precio mas bajo + mas alto) / 2
- Precio actual
- Volumen de transaccion ultimas 24h
- Varianza de precio de cada criptomoneda aplicando la funcion de Power BI
- Precio mas alto
- Precio mas bajo
