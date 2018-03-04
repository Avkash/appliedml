# H2O Data Ingest #

### [Supported Data Source](#supporteddatasources) ###
H2O supports the following data source natively:
- Local File System
- Web based files hosted on https/https
- S3 (Supports both s3 and s3n)
- HDFS 
- JDBC (SQL source connected with JDBC driver 0.42 or higher )

H2O also supports the following data sources with some external libraries:
- Google Cloud Store Object Store files system using Google’s cloud storage connector (gcs-connector-latest-hadoop2.jar)
- IBM Swift Object Storage using IBM HDFS Driver (hadoop-openstack.jar)
- Alluxio data storage source using Alluxio client library (alluxio-core-client-*-jar-with-dependencies.jar)

### [Ingesting data in H2O](#IngestingDataInH2O) ###
Scala
```   
val h2oContext = H2OContext.getOrCreate(sc)
import h2oContext._
import h2oContext.implicits._
import java.io.File
val prostateData = new H2OFrame(new File("/Users/avkashchauhan/src/github.com/h2oai/sparkling-water/examples/smalldata/prostate.csv"))
```

### [Importing Multiple Files](#ImportingMultipleFiles) ###
#### Scala ####
You just need to Scala/Java support file filter to select the files from the folder and then create an H2O Dataframe.
```
val h2oContext = H2OContext.getOrCreate(sc)
import h2oContext._
import h2oContext.implicits._
import java.io.File
val prostateData = new H2OFrame(new File("/Users/avkashchauhan/learn/customers/prostate_*.csv"))
##-----------
NEED AN EXAMPLE
##------------
```

### [Uploading a File](#UploadingFileInH2O) ###

#### Scala ####
You can use Scala/Java API to read files from local file system and then create H2O frame in memory.


