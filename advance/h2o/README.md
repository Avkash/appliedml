# appliedml with H2O for advance users #

## [1. Architecture]() ##
 - H2O for Java or Scala Developers
 - H2O in Docker
 - H2O API
  
## [2. Installation](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_install.md) ##
 - H2O as multiple node cluster
 - H2O on Hadoop
 - H2O on Spark
 - H2O in Docker

## [3. Starting H2O cluster](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_start.md) ##
 - In Cluster Mode
   - Multicast
   - Flatfile
 - Tips and Tricks
 
## [4. Starting H2O cluster in Hadoop](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_start_hadoop.md) ## 
 - Starting H2O in supported Hadoop distributions
   - Cloudera
   - Hortworks HDP
   - Mapr
   - Apache Hadoop
 - Starting H2O in EMR   
 - H2O Cluster Settings

## [5. Starting H2O cluster in Spark](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_start_spark.md) ## 
 - Starting H2O in Spark
   - Internal Model
     - Local Mode
     - Cluster or YARN mode
   - External Mode
 - Starting from Scala command line
 - Launching Cluster (deploy mode - client vs cluster)


## [6. H2O through pysparkling](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_pysparkling.md) ##
 - Installation
 - Connection spark cluster
 - pysparkling
   - GBM Example
   - DRF Sample
 
## [7. H2O through rsparkling](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_rsparkling.md) ##
 - Installation
 - Connection spark cluster
 - Analyzing Job and data
 - rsparkling
   - GBM Example
   - DRF Sample
 - Troubleshooting rsparkling projects

## [8. Accessing H2O library](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_access.md) ##
 - Connecting H2O from R/Python API
 - Scala with H2O
 - Difference between h2o.init() and h2o.connect()
 - Accessing H2O EC2 Instance from your OSX/Windows Machine
   
## [9. Data Ingest](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_data_ingest.md) ##
 - Supported Data Source
 - Ingesting data in H2O
   - Importing a File (Scala)
   - Importing Multiple Files (Scala)
   - Uploading a File (Scala)
 - [Ingest data from S3 & export to S3N/S3A](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_ingest_s3_general.md)
 - [Ingesting Data from S3 from Java API](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_ingest_s3_java.md)

## [10. Ingesting data from RDBS in Python and R](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_sql_ingest.md) ##
 - Supported Scenarios
 - Python API
 - R API

## [11. Create Test dataset with H2O of any size and and type](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_data_man_createframe.md) ##
 - Why test datasets?
 - FLOW
 - Python
 - R
 
 ## [12. Spliting dataset in H2O](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_dataset_split.md) ##
 - Why spliting datasets
 - H2O Dataframe split in Spark
 - H2O Dataframe split in Scala
 

## Tips and Tricks ##
  - [Converting pyspark.sql.dataframe.DataFrame to H2O Data Frame](https://github.com/Avkash/appliedml/blob/master/advance/h2o/spark/h2o_spark_df_conversion.md)
