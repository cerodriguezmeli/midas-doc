# Levantar localmente

## Levantar bureaus cost api

<font size = 4> &nbsp;&nbsp;&nbsp; Para obtener el back, que está en Java: </font>

> <font size = 4> fury get bureaus-cost-api </font>

<font size = 4> &nbsp;&nbsp;&nbsp; Desde IntelliJ IDEA:</font>

![admin-image-2](./img/backend-local-1.png ':size=80%')

> <font size = 4> Ir a Environment -> Environment Variables -> Edit environment variables </font>

<font size = 4> Y agregar una a una las variables de entorno </font>

![admin-image-2](./img/backend-local-2.png ':size=100%')

<font size = 4>  También se puede sin entrar al edit desde la pantalla de Environment modificar el string:
SCOPE=local;LOCAL_DB_HOST=proxysql.master.meliseginf.com:6612;LOCAL_DB_NAME=bu reaudb;LOCAL_DB_USER=usuario;LOCAL_DB_PASS=pass con tu usuario y password de la base de datos. </font>

## Levantar midas

<font size = 4>&nbsp;&nbsp;&nbsp; Para el frontend en Nordic: </font>

> <font size = 4> fury get midas </font>
