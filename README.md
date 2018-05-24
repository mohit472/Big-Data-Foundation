# Big-Data-Foundation
# Big Data
Hey everyone this is a repository where I discuss Big Data technologies. It originally a rose out of my notes that I took while learning about various things.
# The Birth of Hadoop
Hadoop originates from the Google File System paper which was published in 2003 and the subsequent follow up paper "MapReduce: Simplified Data Processing on Large Clusters" published in December 2004. In 2006 the Hadoop subproject was created on the Apache Foundation website. The project was named after Doug Cutting, an engineer at Yahoo, son's toy elephant. #### Further Links/References [Hadoop on Wikipedia](https://en.wikipedia.org/wiki/Apache_Hadoop)
# Hadoop
Almost all modern big data systems in some way involve some aspect of Hadoop (or improvement of Hadoop). As such it seems most fitting to begin our discussion of big data here. The basic idea of Hadoop is to break large datasets up into small pieces and distribute them over large multi-node clusters for processing that runs concurrently. A very good repository that explains Hadoop in great detail is Hadoop Internals. However, I will attempt to go over its core parts.

# MapReduce
MapReduce is the processing part of Hadoop. Although newer systems like Spark and Flink have (for the most part) made MR itself obsolete, it is essential to understanding how they work as well.

# HDFS
"The Hadoop Distributed File System (HDFS) is a distributed file system designed to run on commodity hardware. It has many similarities with existing distributed file systems. However, the differences from other distributed file systems are significant. HDFS is highly fault-tolerant and is designed to be deployed on low-cost hardware. HDFS provides high throughput access to application data and is suitable for applications that have large data sets. HDFS relaxes a few POSIX requirements to enable streaming access to file system data. HDFS was originally built as infrastructure for the Apache Nutch web search engine project." - Apache Website Hadoop website

As the description states HDFS is bascially the distributed storage system of Hadoop. Unlike MR HDFS is still fairly relevant as neither Flink nor Spark replace HDFS and many companies still use it either for temporary storage or as a permanent data lake configuration.

# YARN
Apache Yarn is Hadoop's job manager.

# The Data Pipeline
Various use cases will differ however, most big data pipelines will have similar common features. For the most part they will follow the following form:
</br>
1.Data Collection</br>
2.Ingestion from a data source (this may also been called the extraction phase)</br>
3.Transformation/Computation</br>
4.(Not always but most of the time) storing data</br>
5.Serving the data to the user</br>

# Lambda Architecture
Lambda Architecture is having both a batch processing layer for your data and a realtime layer for your data. The realtime layer sacrifices accuracy for the sake of speed while the batch layer is perfectly accurate but slow. Periodically the batch layer updates the realtime layer. The goal of this model is to preserve overall data accurcay without scarificing speed.
