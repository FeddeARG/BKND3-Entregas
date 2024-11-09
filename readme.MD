Para testear la primer pre entrega:

Para ejecutar:

Colocar en la terminal node src/app.js



Para verificar funcionamiento: 

POSTMAN: 

Para generar mascotas simuladas:

GET http://localhost:8080/api/mocks/mockingpets?num=100


Para generar usuarios simulados:

GET http://localhost:8080/api/mocks/mockingusers?num=50


Para insertar datos simulados en la base de datos:

POST http://localhost:8080/api/mocks/generateData

En el cuerpo de la solicitud (Body), seleccionamos RAW y formato JSON:

{
    "users": 10,
    "pets": 20
}