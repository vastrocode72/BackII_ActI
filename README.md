# Actividad: Desarrollo de API RESTful con Spring Boot y Prisma.io

**Estudiante:** Víctor Alejandro Berrío Rivera
**Institución:** CESDE  
**Materia:** Desarrollo de Backend II  

---

## 1. Introducción
Este proyecto consiste en el diseño y despliegue de una **API RESTful** construida con **Spring Boot 3.4.3**. La aplicación gestiona un modelo de datos de estudiantes y utiliza **Prisma.io** como proveedor de base de datos **PostgreSQL** en la nube, garantizando persistencia y escalabilidad.



## 2. Instancia de Base de Datos en Prisma.io
Se ha creado y configurado una instancia de base de datos relacional en la plataforma Prisma.io.


---<img width="1166" height="162" alt="Captura de pantalla 2026-03-11 203235" src="https://github.com/user-attachments/assets/45e52e09-cdbc-4f42-b0ac-60462ad2bc6a" />

---

## 3. Configuración de la Base de Datos
La conexión se estableció mediante el protocolo seguro de PostgreSQL. Los parámetros de configuración aseguran que la comunicación esté cifrada mediante SSL.

**URL de conexión utilizada:** `postgresql://db.prisma.io:5432/postgres?sslmode=require`
---

## 4. Log de Inicio de Spring Boot
Evidencia del arranque exitoso de la aplicación. En el log se observa la inicialización de **Hibernate** y la exposición de los endpoints en el puerto **8080**.


<img width="869" height="303" alt="Captura de pantalla 2026-03-11 203617" src="https://github.com/user-attachments/assets/37eec0cf-4050-412b-a56c-8c6ecb8a71ef" />

---

## 5. Evidencia de Pruebas de la API (CRUD)
Se utilizaron las herramientas de **Postman** para interactuar con la API base en la ruta `/api/students`. A continuación, se detallan los resultados:

### A. POST: Crear Estudiantes
Se realizaron 3 peticiones exitosas para registrar nuevos estudiantes en la base de datos de Prisma.
<img width="767" height="574" alt="Captura de pantalla 2026-03-11 201135" src="https://github.com/user-attachments/assets/b45f071b-6acf-47e6-81d1-bb599a55340a" />

<img width="783" height="599" alt="Captura de pantalla 2026-03-11 200948" src="https://github.com/user-attachments/assets/72f826e2-584c-4da2-94de-583bab0ae03c" />
<img width="766" height="618" alt="Captura de pantalla 2026-03-11 201412" src="https://github.com/user-attachments/assets/25347113-6530-40e1-ac89-79e7b21fee6c" />

### B. GET ALL: Listar Estudiantes
Consulta general para verificar que los datos creados se persisten correctamente en la nube.
<img width="767" height="626" alt="Captura de pantalla 2026-03-11 201430" src="https://github.com/user-attachments/assets/3b4a96c8-e860-4525-9336-2adafc78d827" />



### C. GET by ID: Obtener por ID
Búsqueda específica de un estudiante utilizando su identificador único autogenerado.
<img width="762" height="418" alt="Captura de pantalla 2026-03-11 201453" src="https://github.com/user-attachments/assets/752d9d91-e76f-42d0-89dc-1299f6cbf677" />


### D. GET by Email: Obtener por Correo
<img width="769" height="510" alt="Captura de pantalla 2026-03-11 201518" src="https://github.com/user-attachments/assets/ec13e5f2-a86c-4b5e-9c23-ffcde3c94202" />


### E. PUT: Actualizar Información
Modificación de los campos `firstName` y `phone` de un registro existente.

<img width="761" height="581" alt="Captura de pantalla 2026-03-11 201603" src="https://github.com/user-attachments/assets/94241eb3-eb12-4b56-a613-665e0d316b7e" />


### F. DELETE: Eliminar Estudiante
Validación de la eliminación física de un registro en la base de datos.

<img width="756" height="457" alt="Captura de pantalla 2026-03-11 201624" src="https://github.com/user-attachments/assets/31927ca5-6800-4a3a-aca4-929fdb60c42b" />


---

## 6. Ejecución de Pruebas Unitarias y de Integración
Se ejecutó el comando `./mvnw test` para validar la integridad del código. Las pruebas internas del proyecto finalizaron con éxito.

* **Tests run:** 1
* **Failures:** 0
* **Errors:** 0
* **Build Status:** SUCCESS

<img width="836" height="207" alt="Captura de pantalla 2026-03-11 202259" src="https://github.com/user-attachments/assets/f7c6710a-9b54-40ec-9331-30130d9e8879" />


---

## 7. Conclusiones
La integración de **Spring Boot** con **Prisma.io** permite un ciclo de desarrollo ágil, separando la lógica de negocio de la gestión de la infraestructura de datos. Se validó correctamente el funcionamiento de todos los métodos HTTP, asegurando que la API cumple con los estándares RESTful requeridos.
