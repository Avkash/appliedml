# Starting H2O Cluster #

## Starting H2O locally ##
 - ### Running on Windows/Linux/OSX: ###
   - Run > java -jar h2o.jar
 - ### Running from R ###
   - Load Binaries
     - CMD> library(h2o)
   - Initialize H2O
     - CMD> h2o.init()     
 - ### Running from Python ###
   - Load Binaries
     - CMD> import h2o
   - Initialize H2O
     - CMD> h2o.init()   
     
## Access H2O locally from FLOW ##
 - When H2O is running on a machine or cluser of machines and you know the IP Address you can access H2O from any machine inside the web browser
 - You must have full network access from your machine to the machine where H2O is running (either locally or remotely)
