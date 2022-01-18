# Módulo de administración

<font size = 4> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; La idea de este módulo es administrar la creación y edición de los bureaus y sus servicios 

## View principal <br/>
![admin-image1](./img/administration-1.png ':size=140%')

&nbsp;&nbsp;&nbsp; En esta pantalla se listan los bureaus con los siguientes datos:
	
* Nombre del bureau y su vendor #SAP 

* Fecha de expiración

* Owner

* Procurement Site

Además, un bureau tiene un *start date* y *servicios* linkeados a este.

&nbsp;&nbsp;&nbsp; Desde la misma pantalla, se puede editar cada bureau o agregar uno nuevo. Al crearlo, se deben agregar también los servicios que provee. Un bureau no es válido si no provee ningún servicio :cold_sweat:  

## Servicios llamados del back
&nbsp;&nbsp;&nbsp; Al **cargar** la view principal, hace un *GET* a */bureaus* para listarlos.

&nbsp;&nbsp;&nbsp; Al **eliminar un bureau**, llama al servicio que deshabilita con un *PUT* a */bureau/disable/:id*.

&nbsp;&nbsp;&nbsp; Al **tocar** el botón de edición de un bureau, debe listar sus servicios, por lo que llama mediante un *GET* a */bureau/services/:id*.

&nbsp;&nbsp;&nbsp; Al **agregar un servicio**, llama mediante un *POST* a */bureau/service*.

&nbsp;&nbsp;&nbsp; Al **eliminar** un servicio dentro de la pantalla de edición de un bureau, llama mediante *PUT* a */bureau/service/disable/:id*.
     
&nbsp;&nbsp;&nbsp; Finalmente, al **confirmar la edición** de un bureau, llama mediante *PUT* a */bureau*.

## Servicios <br/>

![admin-image-2](./img/administration-2.png ':size=80%')

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Los servicios cuentan con un nombre, un service link y precio. Ejemplo: un servicio que se llame *Verificar Identidad por DNI*, cuyo endpoint o service link sea *verifyDNI* y el precio *20 dólares*.
</font>
