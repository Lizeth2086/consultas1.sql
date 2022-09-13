# consultas1.sql

#CONSULTAS SQL

![tabla usuario](img/tabla%20usuario.png "tabla usuario")

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