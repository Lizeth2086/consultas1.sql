# consultas1.sql

# CONSULTAS SQL

## Tabla usuario

![tabla usuario](img/tabla%20usuario.png "tabla usuario")

## COMANDO SELECT

1. Para visualizar toda la informacion que contiene la tabla `usuario`s se puede incluir con lainstruccion SELECT el caracter '*' o cada uno de los campos de la tabla

`select * from usuario`

![consulta 1](img/consulta1.png "consulta 1")

2. Visualizar solamente la identificación del usuario.

`select Identificacion from usuario`

![consulta 2](img/consulta2.png "consulta 2")

3. si se desea obtener los registros cuya identificacion sean mayoreso iguales a 150, se debe utulizar la clausula WHERE que espicifica las condiciones que deben reunir los registros que se van a seleccionar.

`SELECT * FROM usuario WHERE Identificación>=`150`

![consulta 3](img/consulta3.png "consulta 3")

4. si se desea obtener los registros cuyos los apellidos sean Vanegas o Cetina, se debe utilizar el operador IN que especifica los registros que se quieren visualizar de unatabla.

`SELECT apellidos FROM usuario WHERE apellidos IN ('Vanegas','Cetina')`

![consulta 4](img/consulta4.png "consulta 4")

O se puede utilizar el operador OR.

`SELECT apellidos FROM usuario WHERE apellidos='Vanegas' OR apellidos='Cetina'`

![consulta 4_2](img/consulta4_2.png "consulta 4_2")

5. si se desea obtener los registros cuya identificacion sea menor de '110' y la ciudad sea 'Cali', se debe utilizar el operador AND.

`SELECT * FROM usuario WHERE Identificacion<'110' AND ciudad_nac='Cali'`

![consulta 5](img/consulta5.png "consulta 5")

6. si se desea obtener los registros cuyos nombres empiecen por la letra 'A', se debe utilizar el operador LIKE que utiliza los patrones '%' todos y '_' (caracter).

`SELECT * FROM usuario WHERE nombre LIKE 'A%'`

![consulta 6](img/consulta6.png "consulta 6")

7. si desea obtener los registros cuyos nombres contengan la letra 'a'.
`SELECT * FROM usuario WHERE nombre LIKE '%a%'`

![consulta 7](img/consulta7.png "consulta 7")

8. si se desea obtener los registros donde la cuarta lletra del nombre sea una 'a'.

`SELECT * FROM usuario WHERE nombre LIKE '___a%'`

![consulta 8](img/consulta8.png "consulta 8")

9. si se desea obtener los registros cuya identificacio este entre el intervalo 110 y 150, se debe utilizar la clausula BETWEEN, que sirve para espicificar un intervalo de valores.

`SELECT * FROM usuario WHERE Identificación '110` AND '150'

![consulta 9](img/consulta9.png "consulta 9")




## COMANDO DELETE

10. Para eliminar solamente los registros suya identificacion sea mayor de 130.

`DELETE FROM usuario WHERE Identificación>'130'`

![consulta 10](img/consulta10.png "consulta 10")
![consulta 10_2](img/consulta10_2.png "consulta 10_2")


## COMANDO UPDATE

11. Para actualizar la ciudad de nacimiento de Cristian Vanegas, cuya Identificación es 114.

`UPDATE usuario SET ciudad nac = 'Manizales' WHERE Identificación='114'`

![consulta 11](img/consulta11.png "consulta 11")
![consulta 11_2](img/consulta11_2.png "consulta 11_2")


## INNER JOIN

Permite obtener datos de dos o mas tablas.Cuando se realiza la concatenacion de las tablas, no necesariamente se deben mostrar todos los datos de las tablas.

## Tabla pedidos

![Tabla pedidos](img/Tabla%20pedidos.png "Tabla pedidos")

12. Para visualizar los campos identificacion, nombre, apellidos de la tabla usuario y nropedido, fecha de compra, fecha de vencimiento y observacion de latabla pedidos, se debe realizar la siguiente instruccion SQL:

`SELECT usuario.Identificacion, usuario.nombre, usuario.apellidos, pedido.nropedido, pedidos.fechaCompra, pedidos.fechaVence, pedidos.observacion FROM usuario INNER JOIN pedidos ON usuario.Identificacion = pedidos.Identificacion`

![consulta 12](img/consulta12.png "consulta 12")

