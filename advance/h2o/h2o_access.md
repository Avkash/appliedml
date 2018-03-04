# Accessing H2O Library #

Before you would want to access H2O you would need to make sure you have installed H2O properly. The link below will help you install in your desired environment:
 - [H2O Installation](https://github.com/Avkash/appliedml/blob/master/advance/h2o/h2o_install.md)

There are 2 key API to connect with H2O cluster from R or Python interface:
```
h2o.init()
h2o.connect()
```
Note: 
  - If no IP address and PORT is give, default IP as localhost and defult port 54321 will be used.
  - You can use h2o.init() and h2o.connect() to connect any H2O instance started locally, Hadoop, YARN etc. API does not distinguish how H2O cluster was started. 
  
### Difference between h2o.init() and h2o.connect() ###
 - ### h2o.init() ###
  - API will check first to see if H2O to running at default IP address and port
  - If H2O is running, then API will connect to running H2O instance
  - If H2O is not running, then API will try to start H2O on given IP address (Only apply to local IP Address/Localhost)
  - H2O cluser will not be started if startH2O parameter is set to FALSE (R)/ start = False/True for Python. 
 - ### h2o.connect() ###
  - This option is use to connect with an H2O instance which is already running and available on an IP/PORT
  - You must provide IP and PORT with the parameter. 
  

## Scala ## 
You would be using Sparkling Water package with Spark to use with Scala. Once you have Sparkling Water prompt you can start the sparking shell as below:
```
 $ bin/sparklink-shell
```
Once sparkling shell is available from scala, you get the H2O context as below:
```
scala> import org.apache.spark.h2o._
import org.apache.spark.h2o._

scala> val hc = H2OContext.getOrCreate(spark)
......
......
Sparkling Water Context:
 * H2O name: sparkling-water-avkashchauhan_local-1509317501071
 * cluster size: 1
 * list of used nodes:
  (executorId, host, port)
  ------------------------
  (driver,10.0.0.46,54321)
  ------------------------

  Open H2O Flow in browser: http://10.0.0.46:54321 (CMD + click in Mac OSX)
```
After that you just connect to H2O from FLOW, R or Python, either way you want to. 

## Accessing H2O EC2 Instance from your OSX/Windows Machine ##
- Setup H2O in EC2 instance. It can be a single machine running H2O or a cluster of machine running H2O cluster
- You need to make sure EC2 instance has security configuration opens IP address and port 54321/54323 (or other PORT configured to run H2O) so you can access from your windows or OSX machine
- At your OSX/Windows machine start R/Python
- Load H2O library
```
## R
library(h2o)
## Python
import h2o
```
- Initalize H2O 
```
## R/python
h2o.init(ip="ip address of EC2 istance where H2O is running", port = PORT_VALUE)
```
- Validate the H2O cluster details
```
## R
h2o.clusterStatus()
## Python
h2o.cluster_status()
```

