#### Azure Cosmos DB Connector
Download uber jar  

Set spark config 

Hey presto!
```py
readConfig = {
  "Endpoint" : "host",
  "Masterkey" : "master_key",
  "Database" : "database_id",
  "preferredRegions" : "i.e. North Europe",
  "Collection" : "collection_name",
  "SamplingRatio" : "1.0",
  "schema_samplesize" : "1000",
  "query_pagesize" : "2147483647",
  "query_custom" : "SELECT TOP 10 * FROM c"
}

# read in the data
df = spark.read.format("com.microsoft.azure.cosmosdb.spark").options(**readConfig).load()
df.show(truncate=False)
```
