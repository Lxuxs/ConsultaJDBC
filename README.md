# JDBC: Java Database Connectivity

### ¿Qué es JDBC y cuáles son sus componentes?


**JDBC** (Java Database Connectivity) es una API estándar de Java que permite a las aplicaciones interactuar con bases de datos relacionales. Proporciona una interfaz para enviar consultas, realizar actualizaciones y administrar conexiones entre una aplicación Java y la base de datos.

## Componentes de JDBC

JDBC consta de varios elementos clave que permiten su funcionalidad:

**1.Driver JDBC**

    -Es un controlador que traduce las solicitudes de la aplicación Java al lenguaje de la base de datos.

    -Tipos de drivers:

  **Tipo 1**: Driver puente JDBC-ODBC.
       
  **Tipo 2**: Driver de API nativa.
       
  **Tipo 3**: Driver puente de red.
       
  **Tipo 4**: Driver directo (Thin Driver).

**2. DriverManager**

    -Administra los drivers registrados y facilita el establecimiento de conexiones.

    -Proporciona el método getConnection() para obtener una conexión a la base de datos.

    -Es el encargado de seleccionar el driver adecuado para interactuar con la base de datos.

**3. Connection**

    -Representa una conexión activa con la base de datos.
     
    -Es el punto de entrada para ejecutar sentencias SQL y manejar transacciones.
    
    -Métodos clave:
   
         *createStatement(): Crea un objeto Statement.
         
         *prepareStatement(): Crea un objeto PreparedStatement.
         
         *setAutoCommit(boolean autoCommit): Controla las transacciones.




  **4. Statement**
     -Es una interfaz que permite ejecutar consultas SQL y obtener resultados.
     
     -Tipos:

  **Statement**: Para ejecutar consultas simples.
     
 **PreparedStatement**: Para consultas SQL precompiladas con parámetros.

 **CallableStatement**: Para ejecutar procedimientos almacenados.


**5. ResultSet**
    -Es el conjunto de resultados devueltos por una consulta SQL.
    -Permite iterar por los datos fila por fila.
    -Métodos clave:
         *next(): Avanza a la siguiente fila.
         
         *getInt(String columnLabel), getString(String columnLabel): Obtiene datos de una columna.

**6. SQLException**
    -Es la excepción que se lanza cuando ocurre un error al interactuar con la base de datos.
    
    -Métodos importantes:
    
            *getMessage(): Proporciona un mensaje detallado del error.
            
            *getErrorCode(): Devuelve el código de error del proveedor de la base de datos.

### Documente 2 librerías de Scala que permitan conectarse a una base de datos relacional. En una tabla resuma sus diferencias.

# Conexión a Bases de Datos Relacionales en Scala

En Scala, dos de las principales bibliotecas utilizadas para interactuar con bases de datos relacionales son Slick y Doobie. Ambas permiten manejar bases de datos mediante el uso de la API JDBC, pero ofrecen enfoques diferentes para lograrlo.

## 1.Slick (Scala Language-Integrated Connection Kit

  **Descripción:**

     Slick es una biblioteca ORM funcional que traduce consultas Scala a SQL, permitiendo trabajar de forma declarativa y tipada con bases de datos. Es ideal para quienes 
     prefieren un enfoque más abstracto y orientado a objetos.

  **Características principales:**

      -Consultas SQL generadas automáticamente desde código Scala.
   
      -Validación tipada en tiempo de compilación.
   
     -Soporte para múltiples bases de datos como PostgreSQL, MySQL, SQLite, entre otras.
   
     -Compatible con programación asincrónica utilizando Future.

## 2. Doobie

  **Descripción:**
  
      Doobie es una biblioteca funcional pura que permite trabajar directamente con SQL, sin la capa de abstracción de un ORM. Está diseñada para ser altamente flexible y se 
      integra perfectamente con el ecosistema funcional de Scala (Cats, ZIO).
      
  **Características principales:**
        -Consultas SQL escritas directamente.
        -Validación tipada de consultas SQL en tiempo de compilación.
        
        -Manejo explícito de transacciones y alto control sobre las operaciones.
        
        -Compatible con asincronía mediante Cats Effect o ZIO.

 ## Tabla

 ![image](https://github.com/user-attachments/assets/4c0d2400-1478-4832-8618-e56e5baca25d)






       



     


