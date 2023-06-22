
# Run pyspark 

docker run -it apache/spark-py /opt/spark/bin/pyspark

docker run -it --rm -p 8888:8888 jupyter/all-spark-notebook
-- code in

https://spark.apache.org/docs/latest/api/python/index.html

https://spark.apache.org/docs/latest/api/python/getting_started/quickstart_df.html

https://spark.apache.org/docs/3.2.0/api/python/getting_started/quickstart_ps.html



https://spark.apache.org/docs/latest/api/python/getting_started/quickstart_connect.html



# some pyspark scripts 

## Dataframe 
https://spark.apache.org/docs/latest/api/python/getting_started/quickstart_df.html

import pandas as pd
from pyspark.sql.functions import pandas_udf


# spark  jupyter 

https://github.com/jupyter/docker-stacks



# usefull 

- install pandas from ipython
import pip
pip.main(['install', 'pandas'])
import importlib
importlib.reload(pandas)




# Links
https://hub.docker.com/r/apache/spark

https://hub.docker.com/r/jupyter/pyspark-notebook

https://jingwen-z.github.io/learning-pyspark-with-docker/

https://hub.docker.com/r/apache/spark-py

https://spark.apache.org/docs/latest/api/python/getting_started/quickstart_df.html

https://hub.docker.com/r/jupyter/all-spark-notebook/
