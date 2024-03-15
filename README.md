# hive-metastore

Docker image used to create a minimal unsecured hive metastore for teaching 
purposes. 

> [!CAUTION]
> DO NOT use for production. 

Why? Because I haven't tested this image anywhere but in small local setups for demos and I like sleeping easy knowing that I've at least said this.

ENV variables:
 - METASTORE_DB_HOSTNAME - hostname used to ping metastore db during init
 - METASTORE_TYPE - type of metastore db (options: mysql, postgres) (default: mysql)
 - METASTORE_DB_PORT - port used for metastore db (options: 3306, 5432) (defaults: 3306 if type is mysql, 5432 if type is postgres)
 
