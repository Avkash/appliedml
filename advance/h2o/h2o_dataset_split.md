# Split Dataset in H2O #

Once data is loaded into H2O memory, as data scientist you may want to split it into various subsets of datasets so you can use them in various ways.

The most common methods of spliting dataset is following 2 ways:
- Type A - Most splits are design around 80/20 or 75/25 size where higher % is for training data and lower % is for validation.
  - Training dataset
  - Validation
- Type B - In this split user choose 80/10/10 or 70/15/15 where higher % is for training data and lower % is for validation.
  - Training 
  - Validation
  - Test Dataset
  
In the following example we will load the following dataset into H2O then split it into both types (A and B)
Dataset: https://s3.amazonaws.com/h2o-airlines-unpacked/allyears2k.csv (2000 Rows)  

## Spliting dataset in Spark/Scala ##
Importing required libraries and creating H2O Context:
```
import org.apache.spark.h2o._
val h2oContext = H2OContext.getOrCreate(sc)
```
Loading dataset from the local file system as below:
```
val airline_df = new H2OFrame(new File("/Users/avkashchauhan/Downloads/allyears2k.csv"))
airline_df.numRows
airline_df.numCols
```
Spliting dataset into 2 sets of training and validation sub datasets of 80/20 % distribution:
```
# Importing required libraries
import water.{Key, MRTask}
import _root_.hex.splitframe.ShuffleSplitFrame

val keys = Array[String]("train.hex", "valid.hex").map(Key.make[Frame](_))
val ratios = Array[Double](0.8, 0.2)
val frames = ShuffleSplitFrame.shuffleSplitFrame(airline_df, keys, ratios, 1234567689L)

val train = frames(0)
val valid = frames(1)
```
Spliting dataset into 3 sets of training, validation and test sub datasets of 70/15/15 % distribution:
```
import water.{Key, MRTask}
import _root_.hex.splitframe.ShuffleSplitFrame

val keys = Array[String]("train.hex", "valid.hex", "test.hex").map(Key.make[Frame](_))
val ratios = Array[Double](0.7, 0.15, 0.15)
val frames = ShuffleSplitFrame.shuffleSplitFrame(airline_df, keys, ratios, 1234567689L)

val train = frames(0)
val valid = frames(1)
val test = frames(2)
```
