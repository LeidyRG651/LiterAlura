LibroGestor 📚
Creado como parte del Desafío de Gestión de Libros, en colaboración con Alura Latam y Oracle dentro del programa ONE, este proyecto se centra en ofrecer una solución integral para organizar y explorar tu colección literaria.

Descripción del Proyecto 📝
LibroGestor es una aplicación de gestión de libros escrita en Java, diseñada para facilitar a los usuarios la búsqueda y el manejo de libros y autores. La herramienta se conecta a una API externa para enriquecer la información disponible, mientras que utiliza una base de datos local para almacenar los datos necesarios de manera eficiente.

Tecnologías Empleadas 💻
Java: Lenguaje de programación principal.
API Externa: Integración con Gutendex para acceder a información sobre una vasta cantidad de libros y autores.
Spring Framework: Para facilitar la inyección de dependencias y el acceso a la base de datos.
Base de Datos: Utilización de sistemas como H2 o MySQL para el almacenamiento de datos persistentes.
Control de Versiones: Implementación de Git y GitHub para el seguimiento de cambios y la colaboración en equipo.
Entorno de Desarrollo: Utilización de IntelliJ IDEA para la codificación, depuración y ejecución de la aplicación.
Funcionalidades Destacadas 🧩
Archivo Principal: Main.java
El núcleo de la aplicación donde los usuarios pueden interactuar a través de un menú en la consola. Entre sus principales características se incluyen:

Buscar libros por título.
Buscar autores por nombre.
Listar todos los libros en la base de datos.
Listar todos los autores registrados.
Filtrar autores vivos en un año específico.
Listar libros disponibles en diferentes idiomas.
Acceder a estadísticas sobre los libros.
Mostrar los 10 libros más descargados.
Listar autores nacidos o fallecidos en un año determinado.
Clase ApiConsumer.java
Encargada de manejar las consultas a la API externa, facilitando la obtención de información sobre libros y autores.

Clase DataConverter.java
Transforma los datos obtenidos de la API para su uso interno dentro de la aplicación.

Interfaz AuthorRepository.java
Define las operaciones de base de datos relacionadas con los autores, asegurando un acceso eficiente a la información.

Modelado de Datos y Entidades 🗃️
La aplicación utiliza varias clases modelo para representar las entidades clave del dominio, como libros y autores, que están mapeadas a las tablas de la base de datos mediante JPA (Java Persistence API).

Clase Author.java
Representa a los autores en la base de datos y contiene atributos fundamentales como el nombre, la fecha de nacimiento y una lista de libros relacionados.

Atributos Clave:
id: Identificador único.
nombre: Nombre del autor.
fechaDeNacimiento: Año en que nació.
fechaDeFallecimiento: Año de fallecimiento (puede ser nulo si el autor está vivo).
libros: Colección de libros escritos por el autor.
Clase ResponseData.java
Usada para mapear la respuesta JSON de la API, conteniendo información como el número total de resultados y la lista de libros.

Atributos Clave:
total: Cantidad total de resultados disponibles.
libros: Lista de objetos que representan los libros.
Clase BookData.java
Define la estructura de un libro como es recibido de la API, incluyendo título, autores, idiomas y el número de descargas.

Atributos Clave:
titulo: El título del libro.
autores: Lista de autores asociados.
idiomas: Idiomas en los que el libro está disponible.
numeroDeDescargas: Total de descargas registradas.
Mapeo de Entidades con JPA
Se emplean anotaciones específicas de JPA para mapear las clases a las tablas de la base de datos:

@Entity: Marca una clase como entidad de JPA.
@Table: Define la tabla asociada en la base de datos.
@Id: Especifica el campo clave primaria.
@GeneratedValue: Define cómo se generan los valores de la clave primaria.
@Column: Asocia un campo a una columna específica de la tabla.
@OneToMany: Define relaciones entre entidades.
Estas anotaciones permiten que las clases modelo se conviertan en entidades persistentes, facilitando la interacción con la base de datos a través de los repositorios y servicios.

Guía de Uso 🚀
Clonación: Clona el repositorio en tu computadora local.
Apertura del Proyecto: Abre el proyecto en IntelliJ IDEA o en cualquier IDE de tu elección.
Configuración de la Base de Datos: Ajusta la conexión en el archivo de configuración correspondiente.
Ejecución: Corre la clase Main.java para iniciar la aplicación.
Interacción: Sigue las indicaciones en pantalla para explorar libros, autores y consultar estadísticas.
