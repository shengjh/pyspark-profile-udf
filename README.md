# pyspark-profile-udf. Add simple udf profiler for pyspark.

* Requirements
  1. flameprof
  ```python
  pip install flameprof
  ```

* How to use
  1. Rename this project to pyspark
  2. Compress this project to pyspark.zip, and move it to
    $SPARK_HOME/python/lib
  3. Enable pyspark profile in your application code, and set the
     profile dump path
  ```python
  spark_session = SparkSession \
        .builder \
        .appName("Python Arrow-in-Spark profile") \
        .config("spark.python.profile", "true") \
        .config("spark.python.profile.dump", profile_dump_path)
        .getOrCreate()
    ```

