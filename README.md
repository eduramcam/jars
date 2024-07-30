
  # Even driven example with kafka consumer  📝  
  Project 
  
  ## Get Started 🚀  
  Prerequisitos.
   
  [Kafka](https://downloads.apache.org/kafka/3.7.1/kafka_2.13-3.7.1.tgz) <br>
  [Redis DB](https://github.com/tporadowski/redis/releases)<br>
  [Maria DB](https://mariadb.org/download/?t=mariadb&p=mariadb&r=11.4.2&os=windows&cpu=x86_64&pkg=msi&mirror=bharat)<br>
  [IntelliJ IDEA](https://www.jetbrains.com/es-es/idea/)<br>
  [Heidi SQL](https://www.heidisql.com/?place=lnklblWebpage)<br>
  [Maven](https://maven.apache.org/download.cgi)<br>
  [Java](https://www.oracle.com/mx/java/technologies/downloads/)<br>


  ## Prebuilt Components/Templates 🔥  
  <b><i>1. Instalacion de base de datos Maria DB.</i></b>
  * DB: MySQL
  * Usuario: root
  * Usuario: admin
  <br/>
  <b><i>2. Heidi SQL y creacion de base de datos </i></b>
  * Realizar la conexion a la base de MySQL
  * Generar una base de datos llamada <b>shipping_order</b>
  * Generar una entidad de base de datos con el scipt <b>shipping_order_entity</b> script <b>shipping_order_entity.txt</b>
  <br/>
  <b><i>3. Compilar componentes</i></b>
  * Descomprimir el archivo <b>crm-extension-deployment.zip</b>
  * Pegar el contenido del zip en la ruta <b>".m2\repository\com\comviva\pacs"</b>
  * Descomprimir el contenido de <b>kafka_2.13-3.7.1.tgz</b> en la ruta <b>C:\kafka</b>
  * Descomprimir el contenido de <b>Redis-x64-5.0.14.1</b> en la ruta <b>C:\redis</b>
  
  * Ir a la carpeta <b>C:\redis</b> y Ejecutar <b>redis-server</b>
  * En linea de comandos abrir dos ventanas <b>(cmd)</b> ir a la carpeta  <b>C:\kafka</b> y Ejecutar los siguientes comandos 
    * bin\windows\zookeeper-server-start.bat config\zookeeper.properties
    * bin\windows\kafka-server-start.bat config\server.properties
  * Descomprimir el contenido de los 3 en una carpeta donde estara el codigo. <b>(tmf700.zip/shipping-order-impl.zip/audit-file-writer.zip)</b>
    * Abrir el proyecto <b>tmf700</b> desde <b>IntelliJ</b> ejecutar los comandos maven clean & install
    * Abrir el proyecto <b>shipping-order-impl</b> desde <b>IntelliJ</b> ejecutar los comandos maven clean & install
    * Abrir el proyecto <b>audit-file-writer</b> desde <b>IntelliJ</b> ejecutar los comandos maven clean & install
     
  ## Test  ✨  
  1. Compilar y levantar el proyecto <b>shipping-order-impl</b> y <b>audit-file-writer</b>
  2. Ingresar a la url http://localhost:8083/q/dev-ui
  3. Enviar una peticion GET  http://localhost:8089/api/v1/shippingOrders?placeFrom.id=888
  4. Engiar una peticion POST http://localhost:8089/api/v1/shippingOrders con el json <b>request_post.txt</b> 
  
