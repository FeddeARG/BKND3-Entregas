Primera Pre Entrega Backend3:

- Crear un router llamado mocks.router.js que funcione bajo la ruta base /api/mocks.

- Mover el endpoint “/mockingpets” (Desarrollado en el primer Desafío Entregable) dentro de este router.

- Crear un módulo de Mocking para generar usuarios de acuerdo a un parámetro numérico. Dichos usuarios generados deberán tener las siguientes características:
    En “password” debe tener la contraseña “coder123” encriptada.
    “role” puede variar entre “user” y “admin”.
    “pets” debe ir como array vacío.

- Dentro del router mocks.router.js, utilizar este módulo en un endpoint GET llamado “/mockingusers”, y generar 50 usuarios con el mismo formato que entregaría una petición de Mongo.

- Dentro del router mocks.router.js, desarrollar un endpoint POST llamado /generateData que reciba los parámetros numéricos “users” y “pets” para generar e insertar en la base de datos la cantidad de registros indicados.

- Comprobar dichos registros insertados mediante los servicios GET de users y pets

- Link al repositorio de Github con el proyecto completo, sin la carpeta de Node_modules.




Para testear la primer pre entrega:

Para ejecutar:

Colocar en la terminal npm start app.js



Para verificar funcionamiento: 

POSTMAN: 

+++ Para generar mascotas simuladas:

GET http://localhost:8080/api/mocks/mockingpets?num=100

![Imagen mocking 100 pets](./src/public/img/Mock100Pets.png)


+++ Para generar usuarios simulados:

GET http://localhost:8080/api/mocks/mockingusers?num=50

![Imagen mocking 50 users](./src/public/img/Mock50Users.png)


+++ Para insertar datos simulados en la base de datos:

POST http://localhost:8080/api/mocks/generateData

En el cuerpo de la solicitud (Body), seleccionamos RAW y formato JSON:

{
    "users": 10,
    "pets": 20
}

![Imagen getData POSTMAN](./src/public/img/PostGetDataPostman.png)


+++ Corroboración MongoDB :

20 Pets: 

![Imagen 20 pets creados MongoDB](./src/public/img/Mongo20Pets.png)


10 Users: 

![Imagen mocking 100 pets](./src/public/img/Mongo10Users.png)




+++ Ssc Postman método GET de users y pets.

Users: 

![Imagen mocking 100 pets](./src/public/img/GetPostman10Users.png.png)

Pets: 

![Imagen mocking 100 pets](./src/public/img/GetPostman20Pets.png)