# ingenieria_ms_azure_data_prueba

### Resumen de servicios de Azure usados en la ejecución del proyecto:

![image](https://github.com/user-attachments/assets/e7c60e5c-5c69-43be-b863-49aa07ed17c6)

### Se realizó una ingesta de datos de prueba desde una base de datos Azure SQL hacia un Azure Data Lake Storage, automatizado mediante un pipeline realizado en Azure Data Factory y aplicando políticas de seguridad mediante Azure Key Vaults. 

### Los archivos migrados como .csv al Azure Data Lake Storage son cargados y procesados en Azure Databricks (Lakehouse) para posteriormente obtener un Dashboard (Lakeview) dentro de este último servicio.

### Por último fue generado un notebook que es procesado mediante un pipeline de Databricks DataFlow y las conexiones establecidas con el Azure Data Lake Storage cumplen con políticas de seguridad con Azure Key Vault.

### La siguiente imagen muestra el proceso o secuencia del proyecto mediante un índice de contenido:

![image](https://github.com/user-attachments/assets/d427b371-387f-44f9-9353-4cc2a52b90b3)

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

### Imagen 08 y 09. Creación del dataset proveniente de la base de datos en Azure sql

### Sin parámetros para que pueda recorrer todas las tablas de la base de datos.

<p align="center">
  <img src="https://github.com/user-attachments/assets/4b9d4440-b1d8-481c-8a3d-85426cdbe50b">
</p>

### Con parámetros para que obtenga los nombres de las tablas de la base de datos.

<p align="center">
  <img src="https://github.com/user-attachments/assets/0db946d8-ce17-4895-86b5-5b2e2bd3525b">
</p>

### Imagen 10. Carga del dataset generado en ADLS

<p align="center">
  <img src="https://github.com/user-attachments/assets/09c5d4ac-67e5-4f64-8bc1-1dfc1a64483f">
</p>

### Imagen 11. Creación del pipeline, pip-sql-a-adls-csv

<p align="center">
  <img src="https://github.com/user-attachments/assets/f8ac56a5-b991-4522-94fe-ee979659c598">
</p>

### Explicación gráfica del pipeline en Azure Data Factory

<p align="center">
  <img src="https://github.com/user-attachments/assets/3825e2fe-9eb4-43c9-bcfa-8e700282fd8d">
</p>

> [!NOTE]
> El linked service lksv_asql_01 tiene establecido la base de datos Azure SQL a la cual debe conectarse. Como opción, pudo haberse establecido como parámetro .

### Imagen 12. Creación del Azure Data Lake Storage, adlseu2dsrpd01cv

<p align="center">
  <img src="https://github.com/user-attachments/assets/feac3961-425e-47b0-bf51-3de3552f5489">
</p>

### Imagen 13 y 14. Creación del contenedor 'data' y directorio 'archivoscsv'

<p align="center">
  <img src="https://github.com/user-attachments/assets/6d8c4565-f73f-46fe-a174-fb357ad3f49c">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/67541c1f-503d-48dc-b135-3b2b08a4b987">
</p>

### Imagen 15 y 16. Carga de los archivos .csv mediante ejecución del pipeline

<p align="center">
  <img src="https://github.com/user-attachments/assets/d97b5374-22cd-4017-b9a1-f3c42b586b51">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/bac2c368-c268-4b72-b917-77eb4d8bb1e9">
</p>

### Imagen 17 y 18. Creación del Databricks dataflow, pipeline-lakehouse-cv, para ejecutar el notebook Conect_Read_Load_ADLS_DBricks, que lleva los archivos .csv en el ADSL hacia Databricks

<p align="center">
  <img src="https://github.com/user-attachments/assets/4410b545-321b-4a0c-9de4-8574829b8211">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/1913f3c9-9f97-4ea1-bd2b-2cd20316b16d">
</p>

> [!NOTE]
> El archivo Conect_Read_Load_ADLS_DBricks.dbc se encuentra en los descargables de este proyecto

### Imagen 19 y 20. El pipeline incluye trigger y notificación mediante e-mail

<p align="center">
  <img src="https://github.com/user-attachments/assets/8e5ea5e0-cc23-4f2a-8cfd-a293e6157a55">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/e95ff026-da03-4948-8ac6-8b5f820d7f8e">
</p>

### Imagen 21. Creación del Cluster, carlos valladares's Cluster 14.3LTS

<p align="center">
  <img src="https://github.com/user-attachments/assets/f79bff1f-be0b-4e07-9fa9-93403453fa31">
</p>

### Imagen 22. Creación de la carpeta poryecto en Workspace y notebook Conect_Read_Load_ADLS_DBricks

<p align="center">
  <img src="https://github.com/user-attachments/assets/0e233dcf-e075-45a5-858e-91c8551fdb94">
</p>

### Imagen 23. Ejecución del notebook mediante el pipeline (dataflow) y generación de tabla delta (delta_notas_estudiantes)

<p align="center">
  <img src="https://github.com/user-attachments/assets/806937ab-56ed-4d98-aad9-9efafe626022">
</p>

### Imagen 24. Uso de tabla delta para generación del dashboard (lakeview)

<p align="center">
  <img src="https://github.com/user-attachments/assets/f59ba1b7-1a95-4693-8896-aadc32645a3e">
</p>

### Imagen 25. Generación de nuevo conjunto de datos con sql query (Total_Estudiantes) para conocer aprobados y reprobados en los diferentes cursos.

<p align="center">
  <img src="https://github.com/user-attachments/assets/ecc80251-f223-463c-868e-3ca1617579a3">
</p>

### Imagen 26 y 27. Creación de KPI's. graficas y tablas para el Dashboard

<p align="center">
  <img src="https://github.com/user-attachments/assets/a51afbed-992d-434c-871d-c8e6b1fd786e">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/9038dc20-4df0-4e04-a591-69ab730033d6">
</p>











