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