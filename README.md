# 📚 Catálogo de Libros 

Una aplicación de consola desarrollada en **Java** con **Spring Boot** que permite gestionar un catálogo de libros consumiendo la API de Gutendex y almacenando la información en una base de datos PostgreSQL.

## 🚀 Características

- **Búsqueda de libros** por título utilizando la API de Gutendex
- **Gestión de autores** con información de nacimiento y fallecimiento
- **Filtrado por idiomas** (Español, Inglés, Francés, Portugués)
- **Consultas avanzadas** para autores vivos en años específicos
- **Persistencia de datos** con PostgreSQL y JPA
- **Interfaz de consola** interactiva

## 🛠️ Tecnologías Utilizadas

- **Java 17**
- **Spring Boot 3.2.0**
- **Spring Data JPA**
- **PostgreSQL**
- **Jackson** (para parsing JSON)
- **Maven** (gestión de dependencias)
- **HttpClient** (consumo de API REST)

## 📋 Prerrequisitos

Antes de ejecutar el proyecto, asegúrate de tener instalado:

- ☑️ Java 17 o superior
- ☑️ Maven 3.6+
- ☑️ PostgreSQL 12+
- ☑️ IntelliJ IDEA (recomendado)

## ⚙️ Configuración del Proyecto

### 1. Clonar el Proyecto

```bash
# Si tienes Git configurado
git clone <tu-repositorio>
cd literatura

# O crear manualmente la estructura de carpetas
mkdir -p src/main/java/com/alura/literatura
mkdir -p src/main/resources
```

### 2. Configurar PostgreSQL

```sql
-- Conectarse a PostgreSQL y crear la base de datos
CREATE DATABASE catalogo_libros;

-- Verificar la creación
\l
```

### 3. Configurar application.properties

Crea el archivo `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/catalogo_libros
spring.datasource.username=postgres
spring.datasource.password=TU_PASSWORD_AQUI
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect
```

> ⚠️ **Importante**: Cambia `TU_PASSWORD_AQUI` por tu contraseña real de PostgreSQL



## 🚀 Ejecutar la Aplicación

### Opción 1: Desde IntelliJ IDEA
1. Importa el proyecto como proyecto Maven
2. Espera a que se descarguen las dependencias
3. Ejecuta la clase `LiteraturaApplication.java`

### Opción 2: Desde la terminal
```bash
# En la raíz del proyecto
mvn clean install
mvn spring-boot:run
```

### Opción 3: Como JAR ejecutable
```bash
mvn clean package
java -jar target/literatura-0.0.1-SNAPSHOT.jar
```

## 📱 Uso de la Aplicación

![91](https://github.com/user-attachments/assets/2dbaf8ef-207f-47ed-970b-0b32df903bdf)

![92](https://github.com/user-attachments/assets/d90fa78b-7f3a-43a9-99f9-9acecb90d1e3)

![93](https://github.com/user-attachments/assets/49d1b968-5f71-42a0-9f8e-0db91c9688b3)

![94](https://github.com/user-attachments/assets/6630b600-8835-49f0-9a7c-cbc9408cbf03)

![95](https://github.com/user-attachments/assets/8f53f623-e9ee-485e-ab85-0f9db632214d)


## 🔧 API Externa

El proyecto consume la **API de Gutendex**:
- **URL Base**: `https://gutendex.com/books/`
- **Búsqueda**: `https://gutendex.com/books/?search=TITULO`
- **Documentación**: [gutendex.com](https://gutendex.com/)



## 📝 Licencia

Este proyecto fue desarrollado como parte del curso de Alura y es de uso educativo.

## 👨‍💻 Autor

A.B.
