# hive-metastore

Docker image used to create a minimal unsecured hive metastore for teaching 
purposes. DO NOT use for production.

ENV variables:
 - METASTORE_DB_HOSTNAME - hostname used to ping metastore db during init
 - METASTORE_TYPE - type of metastore db (options: mysql, postgres) (default: mysql)
 