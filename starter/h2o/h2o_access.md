# Accessing H2O Library #

Before you would want to access H2O you would need to make sure you have installed H2O properly. The link below will help you install in your desired environment:
 - [H2O Installation](https://github.com/Avkash/appliedml/blob/master/starter/h2o/h2o_install.md)

There are 2 key API to connect with H2O cluster from R or Python interface:
```
h2o.init()
h2o.connect()
```
Note: 
  - If no IP address and PORT is give, default IP as localhost and defult port 54321 will be used.
  - You can use h2o.init() and h2o.connect() to connect any H2O instance started locally, Hadoop, YARN etc. API does not distinguish how H2O cluster was started. 

## List of parameters for h2o.init() ##
- url: Full URL of the server to connect to. (This can be used instead of ip + port + https.)
- ip: The ip address (or host name) of the server where H2O is running.
- port: Port number that H2O service is listening to.
- https: Set to True to connect via https:// instead of http://.
- insecure: When using https, setting this to True will disable SSL certificates verification.
- username: The username to log in with when using basic authentication.
- password: The password to log in with when using basic authentication.
- cookies: Cookie (or list of) to add to each request.
- proxy: The proxy server address.
- start_h2o: If False, do not attempt to start an H2O server when a connection to an existing one failed.
- nthreads: “Number of threads” option when launching a new H2O server.
- ice_root: The directory for temporary files for the new H2O server.
- enable_assertions: Enable assertions in Java for the new H2O server.
- max_mem_size: Maximum memory to use for the new H2O server.
- min_mem_size: Minimum memory to use for the new H2O server.
- strict_version_check: If True, an error will be raised if the client and server versions don’t match.

## Web Frontend (FLOW) ##
You can access H2O from FLOW by 
 https://IP_ADDRESS:PORT

The default port for H2O is 54321 so you can access H2O from FLOW 
![](https://github.com/Avkash/mldl/blob/master/images/flow-ui.png?raw=true)


## Python ##
You can connect to H2O from Python as below:
```
import h2o
h2o.init(ip = "ip_address_of_h2o_instance", port = NNNNN)
```


## R ##
You can connect to H2O from R as below:
```
library(h2o)
h2o.init(ip = "ip_address_of_h2o_instance", port = NNNNN)
```

## Connecting H2O from R/Python API ##
First of all you must have H2O cluster version same as your R/Python API version so you can use H2O functions correctly however sometimes you may want to connect a little different H2O cluster from R/Python API. You can pass string_version_check with false in any of the H2O API to conenct with H2O with different version.
### R ###
```
h2o.init(string_version_check = False)
```
### Python ###
```
h2o.init(string_version_check = False)
```
Note: If you try to connect an H2O cluster which large version different you will get lots of error so its best to avoid using string_version_check parameter so make sure both H2O cluster and API have same version. 

