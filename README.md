# ingenieria_ms_azure_data_prueba

### Resumen de servicios de Azure usados en la ejecución del proyecto:

![image](https://github.com/user-attachments/assets/738f1ed3-8ec0-408c-a5a3-62de0db51e89)

### Se realizó una ingesta de datos de prueba desde una base de datos Azure SQL hacia un Azure Data Lake Storage, automatizado mediante un pipeline realizado en Azure Data Factory y aplicando políticas de seguridad mediante Azure Key Vaults. 

### Los archivos migrados como .csv al Azure Data Lake Storage son cargados y procesados en Azure Databricks (Lakehouse) para posteriormente obtener un Dashboard (Lakeview) dentro de este último servicio.

### Por último fue generado un notebook que es procesado mediante un pipeline de Databricks DataFlow y las conexiones establecidas con el Azure Data Lake Storage cumplen con políticas de seguridad con Azure Key Vault.

### La siguiente imagen muestra el proceso o secuencia del proyecto mediante un índice de contenido:

![image](https://github.com/user-attachments/assets/dcb07e14-4da3-4eb2-95de-6b4a2788fabd)

### Imagen 01. Servicios de Azure para el proyecto

<p align="center">
  <img src="https://github.com/user-attachments/assets/cb0ba538-5e8f-42e4-bfb6-e966b7103762">
</p>

### Imagen 02. Creación de servidor SQL, azuresqlservercvalladares

<p align="center">
  <img src="https://github.com/user-attachments/assets/91300236-8757-46eb-ab81-351e504981ae">
</p>

### Imagen 03. Creación de base de datos Azure SQL, databcvalladares

<p align="center">
  <img src="https://github.com/user-attachments/assets/e602ca93-55dd-41bb-8ffd-c9be47c54159">
</p>

### Imagen 04. Creación de tablas (Alumnos, Cursos y Notas) e inserción de datos

<p align="center">
  <img src="https://github.com/user-attachments/assets/49ef03c9-fccc-4682-b1a9-563e3615107d">
</p>

> [!NOTE]
> EL código SQL para creación de tablas e inserción de datos se encuetran en el archivo insert_data_azure_sql.txt

### Imagen 05 y 06. Seguridad establecida medienta key vaults para conexion con Azure SQL y ADLS

<p align="center">
  <img src="https://github.com/user-attachments/assets/af5f4670-96a6-4fa5-9aab-f6195367ba35">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/7d78eeac-2b41-4be1-8534-ec3a4aae5461">
</p>

### Imagen 07. Creación de linked services para key vault, azure sql y azure data lake storage (ADLS)

<p align="center">
  <img src="https://github.com/user-attachments/assets/c2e9fac8-3119-4957-9b85-4ed72f963611">
</p>

### Imagen 08 y 09. Creación del data sets proveniente de la base de datos en Azure sql

### Sin parámetros para que pueda recorrer todas las tablas de la base de datos.

<p align="center">
  <img src="https://github.com/user-attachments/assets/4b9d4440-b1d8-481c-8a3d-85426cdbe50b">
</p>

### Con parámetros para que obtenga los nombres de las tablas de la base de datos.

<p align="center">
  <img src="https://github.com/user-attachments/assets/0db946d8-ce17-4895-86b5-5b2e2bd3525b">
</p>

### Imagen 10. Carga del data ser generado en ADLS

<p align="center">
  <img src="https://github.com/user-attachments/assets/09c5d4ac-67e5-4f64-8bc1-1dfc1a64483f">
</p>

### Imagen 11. 


