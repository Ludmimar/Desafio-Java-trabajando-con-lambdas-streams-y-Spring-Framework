# Desafio-Java-trabajando-con-lambdas-streams-y-Spring-Framework

Proyecto: Explorador de Libros – Gutendex API
Aplicación en Java que consume la API pública Gutendex para explorar el catálogo de libros de Project Gutenberg.

🔹 Funcionalidades principales:
Conexión a una API REST usando HttpClient.
Conversión de datos JSON a objetos Java con Jackson.
Listado del Top 10 de libros más descargados.
Búsqueda de libros por título ingresado por el usuario.
Generación de estadísticas (máximo, mínimo, promedio y cantidad de descargas).

🔹 Habilidades demostradas:
Consumo de APIs REST en Java.
Manejo de JSON y mapeo a objetos (record).
Uso de Streams, Optional y Collectors en Java.
Interacción con el usuario vía consola.
Aplicación de buenas prácticas (separación en capas service y model).

Clase Principal
Es la clase que orquesta todo el programa.
Usa la API pública de Gutendex (un catálogo de libros de Project Gutenberg).
Descarga información en JSON, la convierte en objetos Java, la muestra y permite interactuar con el usuario.

Funcionalidades:
Mostrar el JSON completo que devuelve la API.
Convertir ese JSON a objetos (Datos, DatosLibros, DatosAutor).
Listar el Top 10 de libros más descargados.
Permitir buscar un libro por título.
Calcular estadísticas sobre las descargas (promedio, máximo, mínimo, cantidad de registros evaluados).

Clase Datos
Representa a un autor.
Tiene nombre y año de nacimiento.
Se ignoran otros datos extra que la API podría traer (@JsonIgnoreProperties).

Clase DatosLibros
Representa un libro de la API.
Tiene título, lista de autores, idiomas y número de descargas.
Es la clase clave para manejar la información de cada libro.

Clase ConsumoAPI
Se encarga de hacer la llamada HTTP a la API Gutendex.
Usa HttpClient (Java 11+).
Devuelve la respuesta como un String JSON.

Interfaz IConvierteDatos
Define un contrato genérico para convertir JSON → objeto Java.
