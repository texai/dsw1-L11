# Desarrollo de Servicios Web 1

## Semana 1

- Presentación personal (xp pro, lenguajes, empresas)
- Presentación del curso
- Encuesta: Intro (conocimientos: Java, Spring o Spring Boot, HTML, git, Maven, Docker)
- Participación: ¿Que es un web service?, Ejemplos
- Guía Idat: Tema 1 - Arquitectura y Estándares / Sub Tema 1.1 ¿Qué es Web Services?
- SOAP vs Rest
- Guía Idat: Tema 1 - Arquitectura y Estándares / Sub Tema 1.2 Tipos de Web Services
- Intro: Request & Response (diagrama)
- Intro: Chrome DevTools
- Demo git
- Software Requerido:
  - Java JDK 17
    - <https://www.oracle.com/java/technologies/downloads/#jdk17-windows>
  - VS Code
    - <https://code.visualstudio.com/download>
  - VS Code ext: Rest Client
    - <https://marketplace.visualstudio.com/items?itemName=humao.rest-client>
  - VS Code ext: Extension Pack for Java
    - <https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack>
  - VS Code ext: Maven for Java
    - <https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-maven>
  - git
    - <https://git-scm.com/downloads>
- Creación de cuenta en GitHub.com
  - Link entre VS code y github:
    - Crear un directorio vacío
    - Abrir ese directorio con VS code
    - Ir a sección "source control" en vs code (barra de íconos lateral)
    - Clic en "Publish to github", seguir los pasos
  - Guia Guthub en consola: <https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account>

## Semana 2

- Guia Sprint: <https://spring.io/guides/gs/producing-web-service/>
- Guía Idat: Tema 2 - Servicios SOAP / Sub Tema 2.1 Primero llegó SOAP, luego REST
- [Github] Creción de Repo de clase: cursos-idat/dsw1-{id}
- Github key config
  - Demo
  - Ejercicios git: {repo}/alumnos/A123456-Ernesto-Anaya/correo.txt
- Diagrama de secuencia de mensajes: Requests y Responses
  - Diagrama de secuencia de mensajes: Caso Búsqueda y Asientos Redbus.pe
  - Tarea: Diagrama de secuencia de mensajes de caso a elección del alumno
- Guía Idat: Tema 2 - Servicios SOAP / Sub Tema 2.2 JAX/WS: (is Deprecated)
- Tarea: "Hola {nombre}" usando SOAP web service
  - Resolución
- Guia Sprint: <https://spring.io/guides/gs/consuming-web-service/>

## Semana 3

- Repaso ws soap paises
- Consumiento un servicio Soap
- EC1 EJ1: traductor de día del español al inglés
- Resolución del ejercicio del examen

## Semana 4

- Guia MySQL https://spring.io/guides/gs/accessing-data-mysql/
- EC1 EJ2: Implementar CRUD completo a entidad

## Semana 5
- Guia Rest: https://spring.io/guides/gs/rest-service/
- Ejecución de aplicación:
  - `mvnw clean package`
  - `java -jar target/*.jar`  
- Docker, Dockerfile, docker-compose
- render.com
  - simple rest
  - pg db
- Practica:
  - Ejecutar la [guia Rest](https://spring.io/guides/gs/rest-service/) y desplegarla en [render](https://render.com) 
  - Referencia: [Repo Desplegable en Render](https://github.com/texai/render-rest-saludo-L11)
  - Pasos:
    - Crear el proyecyo java https://start.spring.io/
    - Implementarlo segun la guía (CRTL-C CTRL-V de 2 archivos)
    - Dejar de ignorar el directorio target
    - Crear archivo Dockerfile (segun referencia)
    - mvnw clean package
    - Crear servicio web en render, vinculando su repositorio
    - Hacer pruebas: /saludo?name=Idat
- Partica (+5 en EC2 participacion)
  - Desplegar en render la implementación de la guia https://spring.io/guides/gs/accessing-data-mysql/ pero para Postrge
  - Referencia: Aplicacion desplegable en render: https://github.com/texai/render-rest-saludo-L11
  - Referencia: Aplicacion desplegable en render (con PG BD) https://github.com/texai/render-rest-saludo
  - Entregable: URL .onrender.com y URL del Repo
  - Tests:
    - GET url.onrender.com/saludo
    - GET url.onrender.com/saludo?name=Peru
    - GET url.onrender.com/demo/all
    - POST url.onrender.com/demo/add
   
## Semana 6

- GitHub CodeSpaces
  - Entorno de desarrollo cloud, nos evita configurar un entorno de desarrollo local, con posibles conflictos entre diferentes versiones de Java
  - 60 horas gratis al mes
  - Detalles: https://github.com/features/codespaces
  - Reporte de uso de Github CodeSpaces: https://github.com/settings/billing
  - Alternativa a Github Codespaces: https://gitpod.io/
  - Práctica CodeSpaces:
    - Crear un nuevo repo en Github (con un archivo README) https://github.com/new
    - Abrir el repositorio con CodeSpaces
      - Desde el repositorio
        - Clic al botón verde "Code"
        - Clic a la pestaña CodeSpaces
        - Clic al botón verde "Open in CodeSpace"
      - Otra manera de abrir nuestro repo en CodeSpaces: https://github.com/codespaces/new
    -  Crear un nuevo proyecto Java con la dependencia Spring Web: https://start.spring.io/
    -  Pasar los archivos generados hacia CodeSpaces
    -  Crear un nuevo Controller.java según ejemplo: https://github.com/texai/hola-codespaces-L11/blob/main/src/main/java/com/example/holacodespacesL11/Controller.java
    -  Instalar las extensiones: "Extension Pack for Java" y "Rest Client"
    -  Abrir el archivo Application.java
    -  Click en Run and Debug
    -  Hacer público el puerto (pestaña al costao de Terminal)
  - Práctica CodeSpaces + Render
    - Escribir un Dockerfile: https://github.com/texai/render-rest-saludo/blob/main/Dockerfile
    - Abrir el archivo .gitignore y borrar la linea que pone `target/`
    - Abrir el terminal y ejecutar el comando: `chmod +x mvnw`
    - Luego el comando: `./mvnw clean package`
    - [Source Control] Realizar el commit (Botón: Commit) y luego push (Botón: Sync Changes)
    - Crear una app web render
    - Vincular al repositorio
    - Probar ...onrender.com
  - Práctica CodeSpaces + Render + PostgreSQL
    - Referencia: https://github.com/texai/idat-dsw1-accessing-data-mysql [*]
    - Agregar dependencias al archivo pom.xml (JPA, postgresql) [*]
    - Añadir un nuevo controlador ApiController.java [*]
    - Añadir clases: User.java y UserRepository.java [*]
    - En Render.com crear la BD PostgreSQL
    - Configurar archivo application.properties con los datos de conexion de la BD PostgreSQL
    - Luego ejecutar el comando: `./mvnw clean package`
    - Realizar commit y push (Sync)
    - Instalar en el VS code de CodeSpaces la extensión: Rest Client
    - Escribir archivo reqs.http
      - GET ...onrender.com/                    -> codigo y nombre
      - GET ...onrender.com/api/usuario/all     -> []
      - POST ...onrender.com/api/usuario/add {} -> "Saved!"
      - GET ...onrender.com/api/usuario/all     -> [{id:1...}]
    - Probar ...onrender.com/
  
## Semana 7

  - Evaluación Contínua 2
    - Crear un nuevo repositorio
    - Abrir con CodeSpace
    - Creamos un nuevo proyecto de Java: https://start.spring.io/
      - Project: Maven
      - Packaging: JAR
      - Java version: 17
      - Dependendencies:
        - Spring Web
        - Spring Data JPA
        - PostgreSQL Driver
    - Instalar Estos plugins:
      - Extension Pack for Java
      - Rest Client
    - En Explorer > Java Projects > clic en "Import Projects"
    - Crear los archivos, segun referencia: https://github.com/texai/idat-dsw1-accessing-data-mysql
      - Curso.java
      - CursoRepository.java
      - MainController.java
      - application.properties
    - Para desplegar en render
      - Crear archivo Dockerfile
      - Eliminar "target/" del archivo .gitignore
      - Ejecutar el comando `chmod +x mvnw`
      - Ejecutar el comando `./mvnw clean package`
      - Nos aseguramos que exista y esté versionado nuestro archivo `target/*.jar`
      - Comiteamos todo, syncronizamos todo (commit & push)
      - Desplegamos en render

## Semana 8

  - Rest Resource
    - Eliminar los controladores
    - Agregar una nueva dependencia a nuestro archivo pom.xml
    ```xml
    <dependency>
	    <groupId>org.springframework.boot</groupId>
	    <artifactId>spring-boot-starter-data-rest</artifactId>
    </dependency>
    ```
    - Modificar nuestro archivo Repository, asi:
    ```java
	package com.example.demo;
	
	import org.springframework.data.repository.CrudRepository;
	import org.springframework.data.repository.PagingAndSortingRepository;
	import org.springframework.data.repository.query.Param;
	import org.springframework.data.rest.core.annotation.RepositoryRestResource;
	import java.util.List;
	
	@RepositoryRestResource(collectionResourceRel = "cursos", path = "cursos")
	public interface CursoRepository extends PagingAndSortingRepository<Curso, Integer>,CrudRepository<Curso, Integer> {
	    
	    List<Curso> findByNombre(@Param("nombre") String nombre);
	
	}
    
    ```
    - Agregar de la misma manera las clases Carrera.java (Entidad) y CarreraRepository.java (Repository)
    - Vincular Curso.java con Carrera.java
        - Un Curso tiene una Carrera
          ```java
          // Curso.java
          @ManyToOne(cascade = CascadeType.ALL)
          @JoinColumn(name = "id_carrera")
          private Carrera carrera;
          
          public Carrera getCarrera() {
              return carrera;
          }
          public void setCarrera(Carrera carrera) {
              this.carrera = carrera;
          }
          ```

        - Una Carrera tiene muchos Cursos
          ```java
          // Carrera.java
          @OneToMany(targetEntity = Curso.class, mappedBy = "carrera")
          @OrderBy("nombre ASC")
          private Set<Curso> cursos = new HashSet<Curso>();
	
          public Set<Curso> getCursos() {
            return cursos;
          }
          public void setCursos(Set<Curso> cursos) {
            this.cursos = cursos;
          }
          ```
    - Instalar extension cliente de postgresql: Database Client
      - Asignar un id_carrera a los cursos
    - Realizar Pruebas

## Semana 9

  - [Guía](https://spring.io/guides/tutorials/react-and-spring-data-rest/)
  - Para construir el paquete (built, bundle) de nuestra app de frontend:
    - ignorar node_modules: Agregar una nueva linea con el texto `node_modules` en el archivo `.gitignore`
    - instalar dependencias de node: `npm i`
    - Para ejecutar webpack desde versiones de node superiores a la 16: `export NODE_OPTIONS=--openssl-legacy-provider`
    - Ejecutamos webpack para que empquete nuestra aplicación de frontend segun la configuración declarada en el archivo webpack.config.js `./node_modules/webpack-cli/bin/cli.js`

## Semana 10

- Evaluación COntínua 3

## Semana 11

- Revisión: FrontEnd
- Práctica:
  - Tomando como base un repositorio ya con BackEnd y FrontEnd funcionando: https://github.com/texai/semana9-app-cliente-react-L11
  - Implementar su propia entidad, con al menos 3 atributos (campos)
    - clase Entidad
    - interface Repository
    - Database Loader
    - Modificar app.js
    - reqs.http

## Semana 14

  - Evaluación Final
    - BackEnd
      - Construir 1 servicio web para 2 entidades (CrudRepository, PagingAndSortingRepository)
      - Controlador adicionales
    - FrontEnd
      - Vista de tabla de datos, con datos cargados, usando ReactJS
      - Formulario para crear y editar.

