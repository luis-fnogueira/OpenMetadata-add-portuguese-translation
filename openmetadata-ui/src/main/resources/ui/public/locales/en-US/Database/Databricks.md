# Databricks

In this section, we provide guides and references to use the Databricks connector. You can view the full documentation for Databricks [here](https://docs.open-metadata.org/connectors/database/databricks).

## Requirements

To learn more about the Databricks Connection Details (`hostPort`,`token`, `http_path`) information visit these [docs](https://docs.open-metadata.org/connectors/database/databricks/troubleshooting).

$$note
we have tested it out with Databricks version 11.3LTS runtime version. (runtime version must be 9 and above)
$$

### Usage & Lineage

$$note
To get Query Usage and Lineage details, you need a Databricks Premium account, since we will be extracting this information from your SQL Warehouse's history API.
$$

You can find further information on the Databricks connector in the [docs](https://docs.open-metadata.org/connectors/database/databricks).

## Connection Details

$$section
### Scheme $(id="scheme")
SQLAlchemy driver scheme options. If you are unsure about this setting, you can use the default value.
$$

$$section
### Host Port $(id="hostPort")
Host and port of the Databricks service. This should be specified as a string in the format `hostname:port`. E.g., `adb-xyz.azuredatabricks.net:443`.
$$

$$section
### Token $(id="token")
Generated Token to connect to Databricks. E.g., `dapw488e89a7176f7eb39bbc718617891564`.
$$

$$section
### HTTP Path $(id="httpPath")
Databricks compute resources URL. E.g., `/sql/1.0/warehouses/xyz123`.
$$

$$section
### Catalog $(id="catalog")
Catalog of the data source. This is an optional parameter, if you would like to restrict the metadata reading to a single catalog. When left blank, OpenMetadata Ingestion attempts to scan all the catalogs. E.g., `hive_metastore`
$$

$$section
### Database Schema $(id="databaseSchema")
Schema of the data source. This is optional parameter, if you would like to restrict the metadata reading to a single schema. When left blank, OpenMetadata Ingestion attempts to scan all the schemas.
$$

$$section
### Connection Timeout $(id="connectionTimeout")
The maximum amount of time (in seconds) to wait for a successful connection to the data source. If the connection attempt takes longer than this timeout period, an error will be returned.

If your connection fails because your cluster has not had enough time to start, you can try updating this parameter with a bigger number.
$$

$$section
### Connection Options $(id="connectionOptions")
Additional connection options to build the URL that can be sent to service during the connection.
$$

$$section
### Connection Arguments $(id="connectionArguments")
Additional connection arguments such as security or protocol configs that can be sent to service during connection.
$$
