# API-REST

## **💡 Sobre este repositorio**

Este repositorio contiene una API de tipo REST (Representational State Transfer) usada para gestionar la base de datos de un contexto universitario.  
Esta API fue solicitada en un proyecto de mi universidad. Puedes mirar condiciones e indicaciones en el documento:  
`Proyecto-contextoUniversitario.pdf`.

---

</br>

## **🔍 ¿Cómo funciona?**

Las API (Application Programming Interface) son usadas para permitir la comunicación entre máquinas o software.
Estas las puedes encontrar tanto en páginas web como en aplicaciones, por ejemplo:
La API de **Google Maps** nos permite usar los mapas de Google desde nuestra página/aplicación

</br>

Existen varios tipos de APIs, así como las de tipo: **Rest, Soap, Web Socket, Webhook, etc...**
Sin embargo, hablaremos de las de tipo **Rest**, generalmente usadas en aplicaciones web con microservicios como lo son los sistemas E-commerce. Este tipo de API se caracteriza por usar unicamente **metodos HTTP** los cuales son:

-`GET`: Para obtener recursos.
-`POST`: Para crear nuevos recursos.
-`PUT`: Para actualizar recursos existentes.
-`DELETE`: Para eliminar recursos.

>⚠️ _Antes de continuar, esta API fue creada con Typescript y frameworks como Node.js, Express.js, etc..., recuerda que en el directorio `dist` se encuentran los archivos JS que Typescript se encargó de traducir para que nuestro navegador los tomará_

---

</br>

## **⚙️ Src**

En este directorio encontrarás:

-`models`: Definimos la estructura apropiada de cada entidad para que un registro pueda guardarse correctamente en la base de datos.
-`controllers`: Definimos las acciones posibles para cada entidad (_Recordemos que al ser REST, usaremos unicamente metodos HTTP_).
-`routes`: Definimos las rutas para acceder, agregar, actualizar y eliminar registros de cada entidad.

---

</br>

## **🗂️db.ts & app.ts🚀**

En `db.ts` creamos la conexión con la base de datos dando las credenciales solicitadas para una base de datos MySQL, por ejemplo:
Con *host: process.env.DB_HOST* indicamos que el host de la base de datos se encuentra en una variable *DB_HOST* del archivo *.env*
>⚠️ _Notese que el archivo *.env* no se encuentra en el repositorio, esto debido a que allí se encuentran nuestras credenciales para realizar una conexión con la base de datos_

Y finalmente, en `app.ts` importaremos: 

-La constante *db* del archivo `db.ts` para hacer uso de ella
-Los routers que creamos (los cuales usan los controllers que utilizan los models), lo que nos permite acceder y hacer uso del directorio `src`
-frameworks que usaremos con sus respectivos directorios.

con esto aseguramos tener todo en nuestra app, la cual es la que se va a usar inicialmente en el momento de hacer peticiones por un cliente.