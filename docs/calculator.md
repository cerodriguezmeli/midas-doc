# Calculadora de costos

## View principal <br/>
![admin-image1](./img/calculator-1.png ':size=130%')


&nbsp;&nbsp;&nbsp; <font size = 4> La idea de esta view es tener una calculadora del costo que puede tener en una aplicación implementar llamadas a servicios de un bureau. Para ello, se deberan seleccionar un solo bureau pero podrían ser múltiples servicios de este, cada uno con la frecuencia a ser utilizada. 

&nbsp;&nbsp;&nbsp; Por ejemplo, dado el bureau llamado *New Bureau with service en BRL*, se selecciona sólamente el servicio llamado *brasil service*, el cual será utilizado para *40 usuarios*, *2 requests por usuario* y de forma *diaria*.

&nbsp;&nbsp;&nbsp; Además, tiene dos tipos de uso:

* Campaign: Se calculará cuánto cuesta llamar a los servicios con las frecuencias elegidas dentro del rango de fechas seleccionada, realizando un promedio para el costo diario, semanal y mensual en caso de que corresponda, es decir, que el rango de fechas abarque al menos un dia, al menos una semana, al menos un mes, etc. 
* Daily: Es igual que el caso anterior solo que se calcula un promedio de lo que costaría por dia, por semana, por mes y por año, siendo el total, al igual que el caso anterior, el costo dentro del rango de fechas seleccionadas. 


## Servicios llamados del back
&nbsp;&nbsp;&nbsp; Al **cargar** la view principal, hace un *GET* a */bureaus* para listarlos.

&nbsp;&nbsp;&nbsp; Al **seleccionar un bureau**, lista los servicios de este con un *GET* a */bureau/services/:id*.  

&nbsp;&nbsp;&nbsp; Al **clickear calculate**, llama al servicio */calculator* mediante un *POST*, encargado de hacer los calculos dentro del rango de fechas seleccionado.

</font>