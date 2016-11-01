

# I've moved!
All future updates will be in the repository [https://github.com/Archethought/docker-jupyter-spark2](https://github.com/Archethought/docker-jupyter-spark2)


# docker-jupyter-spark2
Work sponsored by Archethought, http://www.archethought.com/

I could not find a dockerized jupyter notebook with Spark 2, 
so I merged Docker Stacks [pyspark-notebook](https://github.com/jupyter/docker-stacks/tree/master/pyspark-notebook) 
and [all-spark-notebook](https://github.com/jupyter/docker-stacks/tree/master/all-spark-notebook) with an update to Spark 2.0.0
 
 Build image with 
 ```
 $ docker build -t "all-spark-2:dockerfile" <path to dockerfile>
 ```
## Notes

### Container modifications

These are additions I've made to my container which may or may not be propagated to the image definition/Dockerfile, but am recording for tracking purposes.
Added to /usr/local/spark/conf:

 * core-site.xml
 * hdfs-site.xml
 * spark-env.xml, added HADOOP_CONF_DIR=$SPARK_HOME/conf
