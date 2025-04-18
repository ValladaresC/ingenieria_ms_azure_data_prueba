# ingenieria_ms_azure_data_prueba

### Imagen resumen de servicios de Azure usados en la ejecución del proyecto:

![image](https://github.com/user-attachments/assets/738f1ed3-8ec0-408c-a5a3-62de0db51e89)

### Se realizó una ingesta de datos de prueba desde una base de datos Azure SQL hacia un Azure Data Lake Storage, automatizado mediante un pipeline realizado en Azure Data Factory y aplicando políticas de seguridad mediante Azure Key Vaults. 

### Los archivos migrados como .csv al Azure Data Lake Storage son cargados y procesados en Azure Databricks (Lakehouse) para posteriormente obtener un Dashboard (Lakeview) dentro de este último servicio.

### Por último fue generado un notebook que es procesado mediante un pipeline de Databricks DataFlow y las conexiones establecidas con el Azure Data Lake Storage cumplen con políticas de seguridad con Azure Key Vault.

### La siguiente imagen muestra el proceso o secuencia del proyecto mediante un índice de contenido:

![image](https://github.com/user-attachments/assets/dcb07e14-4da3-4eb2-95de-6b4a2788fabd)

