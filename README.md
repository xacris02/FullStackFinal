# FullStackFinal
Descripción del contexto o dominio del proyecto:
El proyecto corresponde al sistema SaludPlus. Es un software diseñado para mejorar la gestión de la información de los pacientes y la organización de citas médicas. El dominio del proyecto exige que tanto pacientes como médicos cuenten con una cuenta pre-registrada. Una de las características principales de la lógica de negocio es que el sistema no debe contener datos nulos ni duplicados. A nivel funcional, el sistema permite registrar, modificar e iniciar sesión como cliente. Además, permite la gestión de la agenda, otorgando la capacidad de agendar y eliminar horas médicas.  
Nombres de los/las estudiantes:
El equipo de desarrollo computinx está compuesto por los siguientes integrantes:  

Alvaro Chirinos: Desarrollador Back End.  
Gonzalo Sandoval: Desarrollador Front End.  
Jose Tapia: QA y DevOps.  
Vicente Valdivia: Project Manager y Analista Funcional.  

Listado de microservicios implementados:
El alcance de la arquitectura base está conformado por la integración de dos microservicios principales que interactúan de forma sincronizada:  
API Registrar Cliente (Administrador de Clientes): Microservicio encargado de gestionar el registro y guardado de nuevos clientes. Gestiona también la búsqueda de clientes específicos, la actualización de perfiles existentes y la eliminación de registros en el sistema.  
API Registrar Cita (Administrador de Citas): Microservicio dedicado a agendar horas médicas y eliminarlas (registrar, modificar y eliminar citas para clientes ya registrados en el sistema).  
Rutas principales del Gateway:
1. GET /api/v1/clientes/{id} 
2. POST /api/v1/clientes 
3. PUT /api/v1/clientes/{id}
4. DELETE /api/v1/clientes/{id} 
5. POST /api/v1/citas 
6. PUT /api/v1/citas/{id}
7. DELETE /api/v1/citas/{id}

Instrucciones:
Empezamos configurando Laragon ya que este configura MySQL/MariaDB en el puerto 3306. Para cambiarlo al puerto 3309, sigue estos pasos:
Paso a paso en Laragon:
1. Detén los servicios: Abre la interfaz de Laragon y asegúrate de que todos los servicios estén detenidos.
2. Accede a las preferencias: Haz clic en el ícono del engranaje (Configuración/Preferences) en la esquina superior derecha de la ventana de Laragon.
Cambia el puerto:
3. Dirígete a la pestaña Servicios y Puertos.
4. En la sección de MySQL/MariaDB, busca la casilla del puerto (que debería decir 3306) y cámbiala a 3309.
5. Cierra la ventana de configuración.
6. Inicia los servicios: Haz clic en "Iniciar Todo". Si el puerto 3309 está libre, MySQL arrancará sin problemas.

En tu IDEE;
1. Preparación del Entorno (Visual Studio Code)
Asegúrar de tener instalado el Extension Pack for Java y el Spring Boot Extension Pack.
Abre tu IDE y carga la carpeta de la API de Clientes. Cada api se debe abrir en ventanas distintas

3. Verificar los Puertos
Antes de ejecutar, revisa el archivo application.properties de cada proyecto.
Confirma que la API de Clientes y la API de Citas tengan puertos distintos asignados (por ejemplo, server.port=8081 y server.port=8082) para evitar choques al correr ambas simultáneamente.

4. Ejecutar la API de Clientes.
En el explorador de archivos del IDE hasta encontrar la clase principal.
Abre el archivo. Justo encima del método, verás que aparecen unos pequeños botones de acción rápida que dicen "Run" o "Debug".
Haz clic en Run.
Se abrirá la terminal integrada en la parte inferior mostrando los logs de Spring Boot.

6. Ejecutar la API de Citas
Abre una nueva ventana del IDE y carga la carpeta de la API de Citas.
Hace lo mismo: busca la clase principal (ej. CitaApplication.java) y haz clic en el botón Run sobre el método main.
De esta manera, tendrás ambas APIs operando.
