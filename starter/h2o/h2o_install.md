# H2O Installation #

H2O run on Linux, Windows and OSX environment and can be set to run either single node or in clustered mode i.e. running on multiple machine.

## Downloading H2O ##
 - #### Home of H2O Download ####
   - [https://www.h2o.ai/download/](https://www.h2o.ai/download/)
   - When in doubt select the "Latest Stable Release"
   - What is nightly build?
     - H2O automated build process build source code in nightly basis with the latest code pushed by the team, a very common open source practice. 
     - This is mostly untested code or mostly passed through automated code test run
     - Use at your own risk
 - #### Running on Windows/Linux/OSX: ####
   - Download H2O binaries on your machine
 - #### Downloading from R ####
   - Install H2O R Package on your R environment
     - CMD> install.packages("h2o", type="source", repos="URL_TO_THE_H2O_VERSION_R_DOWNLOAD")
 - #### Running from Python ####
   - Install H2O Python Package on your python environment
     - CMD> pip install URL_TO_THE_H2O_VERSION_R_DOWNLOAD

## H2O Install on Conda (Python) ##
  - Location of H2O Conda Packages
    - https://anaconda.org/h2oai/h2o/files
  - Install Command
    - $ conda install h2o 

### H2O Running into Single Node(Standalone Mode): ###
 - You just need to download h2o binaries and run as Java process. 
 - It is a 2 step process
   - Download the zip and unzip
   - Run it using Java runtime
     - Windows     : C:\h2o_unzip_folder> java -jar h2o.jar
     - Linux & OSX : $ java -jar h2o.jar
