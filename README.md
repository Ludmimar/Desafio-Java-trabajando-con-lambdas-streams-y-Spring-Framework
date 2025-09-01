# 📚 Explorador de Libros – Gutendex API

Aplicación en **Java** que consume la API pública **Gutendex** para explorar el catálogo de libros de *Project Gutenberg*.  

---

## 🚀 Funcionalidades principales
- 🔗 Conexión a una **API REST** usando `HttpClient` (Java 11+).  
- 📦 Conversión de datos **JSON → objetos Java** con **Jackson**.  
- 📊 Listado del **Top 10 de libros más descargados**.  
- 🔍 Búsqueda de libros por título ingresado por el usuario.  
- 📈 Generación de estadísticas: máximo, mínimo, promedio y cantidad de descargas.  

---

## 🛠 Habilidades demostradas
- Consumo de **APIs REST en Java**.  
- Manejo de **JSON y mapeo a objetos** (`record`, `@JsonIgnoreProperties`).  
- Uso de **Streams, Optional y Collectors** para procesamiento de datos.  
- Interacción con el usuario vía **consola**.  
- Buenas prácticas: separación en **capas service y model**.  

---

## 🧩 Principales clases
- **Clase Principal**  
  - Orquesta el programa.  
  - Descarga la info desde la API Gutendex.  
  - Convierte JSON a objetos Java.  
  - Muestra resultados y gestiona interacción con el usuario.  

- **Datos**  
  - Representa un autor (nombre, año de nacimiento).  
  - Ignora datos irrelevantes con `@JsonIgnoreProperties`.  

- **DatosLibros**  
  - Representa un libro (título, autores, idiomas, descargas).  
  - Clase clave para manejar la información.  

- **ConsumoAPI**  
  - Hace las llamadas HTTP con `HttpClient`.  
  - Devuelve la respuesta en formato JSON (String).  

- **IConvierteDatos**  
  - Interfaz genérica para convertir JSON → objetos Java.  

---

## ⚙️ Tecnologías utilizadas
- ☕ **Java 11+** → lenguaje de programación principal  
- 🌐 **Gutendex API** → catálogo de libros de Project Gutenberg  
- 📦 **Jackson** → deserialización de JSON a objetos Java  
- 🔗 **HttpClient** → consumo de la API REST  
- 🧮 **Java Streams & Collectors** → procesamiento de datos  
- 🔑 **Optional** → manejo seguro de valores nulos  

---

## 🛠 Stack resumido
`Java · HttpClient · Gutendex API · Jackson · Streams · Optional · Collectors`

---

## 📷 Flujo de la aplicación (opcional)
```mermaid
flowchart TD
    A[Usuario] -->|Ingresa búsqueda o pide Top 10| B[Clase Principal]
    B --> C[ConsumoAPI - HttpClient]
    C --> D[Gutendex API]
    D --> C
    C --> E[Jackson - Convierte JSON a objetos]
    E --> F[DatosLibros / Datos Autor]
    F --> G[Procesamiento con Streams & Collectors]
    G --> A[Resultados en consola]

