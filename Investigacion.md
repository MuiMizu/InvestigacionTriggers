# Investigacion Triggers Fabian Lorenzo

1-¿Qué es un Trigger?
Un Trigger es un objeto de base de datos que se ejecuta automáticamente cuando ocurre un evento específico como puede ser INSERT, UPDATE o DELETE en una tabla o vista.

2-¿Para que sirve un Trigger?
Se pueden crear para enviar notificaciones cuando pasa algo en la base de datos, y con esto automatizar proccesos dentro de esta.

3-¿Cuándo se puede usar un Trigger?
En cualquier momento siempre y cuando los anteriores eventos mencionados esten involucrados.

4-Estructura de un Trigger
Su nombre
Momento de activacion
Evento que lo activa
Tabla sobre el que se ejecutara
Cuerpo general del trigger

5-Tipos de Trigger
Hay 2 tipos de tipos de trigger, Depende de el evento o el momento
Depende del momento existen BEFORE, AFTHER o INSTEAD OF
Depende del evento, INSERT, DELETE o UPDATE

6-¿Cuándo ejecuta su accion un Trigger?
Luego de que el evento para el que fue creado a la hora de activarse, sea llamado
Este sera llamada automaticamente si todo esta bien definido

7-Ejemplo de un Trigger
CREATE TRIGGER TR_EvitarEliminadoEmpleados
ON Empleados
INSTEAD OF DELETE
AS
BEGIN
    PRINT 'No se permite eliminar empleados directamente.';
END;

8-Trigger Marketing
Se refiere a una accion automatizada que ocurre cuando el usuario interactua con algo en la aplicacion, pagina etc
El ejemplo mas comun puede ser cuando pones un objeto en plataformas de ventas online, y en unas semanas te notifican (Primer trigger) que ese objeto que tu añadiste a tu canaste
se encuentra en oferta por tiempo limitado (Segundo Trigger)

9-¿Cómo hacer un Trigger?
Usando la estructura anteriormente dada, siguiendola correctamente nos deberia quedar algo parecido a ejemplo del la pregunta 7

10-Caracteristicas de un Trigger
-Automatizacion
-Notificacion
-Depende de un evento previo a su activacion

11-Desventajas de un Trigger
-Pueden afectar el rendimiento si no se diseñan bien.
-En algunos servidores pequeños, pueden dar problemas de depuracion
-Si estan mal diseñados pueden colizionar con otros triggers con acciones parecidas.

12-Sustituto de los trigguer en otras bases de datos.
PostgreSQL:	Rules, Event Triggers
SQL Server:	Procedimientos almacenados
Firebase:	Cloud Functions
