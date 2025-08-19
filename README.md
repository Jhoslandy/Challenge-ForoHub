# 🌐 ForoHub - Plataforma de Foros Educativos 📚

✨ **ForoHub** es una plataforma dinámica y segura, desarrollada con **Spring Boot**, que revoluciona la interacción en foros educativos. Con un enfoque en la eficiencia y la experiencia del usuario, facilita la creación y gestión de debates, temas, cursos y respuestas. La planificación y seguimiento de este proyecto se llevaron a cabo utilizando **Trello** para la gestión de tareas y **Notion** para la documentación integral. ✨

---

## 🚀 Descripción y Características

-   🔐 **Gestión de Usuarios**:
    -   Sistema de autenticación robusto con **JWT**, que garantiza seguridad y acceso diferenciado por roles (administrador y usuario).

-   📝 **Gestión de Foros**:
    -   Capacidad para crear, visualizar, editar y responder a temas en diversas categorías, promoviendo la colaboración.

-   📘 **Gestión de Cursos**:
    -   Asociación directa de temas con cursos, facilitando la organización del contenido educativo y su búsqueda.

-   📄 **Documentación de la API**:
    -   Exploración y testeo de la API sin esfuerzo a través de **Swagger** (SpringDoc OpenAPI), lo que facilita el desarrollo y la integración.

---

## 🏗️ Arquitectura del Sistema

El proyecto sigue una arquitectura modular y escalable, dividida en capas para una clara separación de responsabilidades:
-   💻 **Capa de Presentación (API)**: Maneja las solicitudes REST y la seguridad de los puntos finales.
-   ⚙️ **Capa de Lógica de Negocio (Dominio)**: Contiene la lógica central del negocio, como entidades, servicios y repositorios.
-   🗄️ **Capa de Persistencia (Infraestructura)**: Se encarga de la interacción con la base de datos, el manejo de errores y configuraciones de seguridad.

---

## ⚙️ Tecnologías Utilizadas

-   🧑‍💻 **Lenguaje**: Java 21
-   🌱 **Framework**: Spring Boot
-   🗃️ **Base de Datos**: MySQL
-   📜 **Documentación**: SpringDoc OpenAPI (Swagger)
-   🔒 **Seguridad**: JWT, OAuth

---

## 🛠️ Configuración e Instalación

### **Prerrequisitos**
-   JDK 21
-   Maven
-   MySQL

### **Pasos de Instalación**

1.  **Clonar el repositorio**:
    ```bash
    git clone [https://github.com/usuario/tu-proyecto.git](https://github.com/usuario/tu-proyecto.git)
    cd tu-proyecto
    ```

2.  **Configurar la base de datos**:
    -   Crea una base de datos en MySQL.
    -   Actualiza las credenciales en el archivo `application.properties`:
        ```properties
        spring.datasource.url=jdbc:mysql://localhost:3306/nombre_base_datos
        spring.datasource.username=tu_usuario
        spring.datasource.password=tu_contraseña
        ```

3.  **Compilar y ejecutar la aplicación**:
    ```bash
    mvn clean install
    mvn spring-boot:run
    ```

4.  **Acceder a la documentación de la API**:
    🌐 [Swagger UI](http://localhost:8080/swagger-ui.html)

---

## 🔗 Endpoints Principales

| **Método** | **Endpoint** | **Descripción** | **Ejemplo de Cuerpo (JSON)** |
|:---|:---|:---|:---|
| `POST` | `/auth/login` | Autenticación de usuario. | `{ "username": "admin", "password": "1234" }` |
| `GET` | `/users` | Obtiene la lista de usuarios. | - |
| `GET` | `/topics` | Lista todos los temas de foros. | - |
| `POST` | `/topics` | Crea un nuevo tema en un foro. | `{ "title": "Nuevo Tema", "message": "Texto" }` |

---

## 📂 Estructura del Proyecto

```plaintext
forohub/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com.desafio.forohub/
│   │   │       ├── controller/
│   │   │       ├── domain/
│   │   │       │   ├── curso/
│   │   │       │   ├── respuesta/
│   │   │       │   ├── topico/
│   │   │       │   └── usuario/
│   │   │       ├── infra/
│   │   │       │   ├── errors/
│   │   │       │   ├── security/
│   │   │       │   ├── service/
│   │   │       │   └── springdoc/
│   │   │       └── ForohubApplication.java
│   │   └── resources/
│   │       ├── db.migration/
│   │       ├── static/
│   │       ├── templates/
│   │       └── application.properties
├── test/
```



---

## 📈 Avance del Proyecto

### Funcionalidades Completadas
- ✅ Autenticación de usuarios.
- ✅ Creación y gestión de temas en foros.
- ✅ Asociación de cursos con temas.

### Próximas Funcionalidades
- ⏱️ Sistema de notificaciones.
- 📊 Estadísticas de uso y participación.

---

## 🤝 Contribución

¡Tu ayuda es invaluable! Si deseas contribuir, sigue estos sencillos pasos:

1.  Haz un `fork` del repositorio.
2.  Crea una nueva rama para tus cambios:
    ```bash
    git checkout -b feature/nueva-funcionalidad
    ```
3.  Realiza tus cambios y haz un `commit`:
    ```bash
    git commit -m "feat: Añadida nueva funcionalidad"
    ```
4.  Sube tus cambios a tu `fork`:
    ```bash
    git push origin feature/nueva-funcionalidad
    ```
5.  Abre un `pull request` en el repositorio principal.

---

## 📜 Licencia

Este proyecto está liberado bajo la **Licencia MIT**. Para más detalles, consulta el archivo `LICENSE`.

---

© Derechos reservados por **Jose Aruquipa** @2025.
