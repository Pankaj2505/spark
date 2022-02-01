---
layout: post
title:  "Introduction to spark"
date:   2022-02-01 09:04:08 +0530
categories: spark
permalink: /:categories/:title
---

# Introduction to Spark

#### AS data is growing because of IOT and internet companies. so challanges related to data.
- Data collection and Ingestion 
- data storage and management
- Data processing and transformation
- Data Access and Retrieval

#### Solution to challange
- Hadoop has implemented GFs(Google file system ) with HDFS  to store large data into distributed system
    - hdfs is highliy scalable , you can add as many cluster to it as data size grows
- Map Reduce solved the compute capacity, by implementing a distributed computation framework over hdfs.
    - it break the computing process to smaller task,
    - use cluster of computer to process individual task 
    - lastly combine the outcome of each task to produce consolidated result

- Other projects based on google file system and google map reduce similarly like hadoop created a mapping system, which will convert user friendly code to map reduce code.
    - Hadoop(opensource) data efficient and not compute efficient as processing data used to stored in hard disk.
    - pig (yahoo) similar to sql
    - hive(facebook) closer to sql
    - apache spark(open source) closer to programming language like python and jave
        - apache spark has many API's to work with hadoop filesystm and mapreduce 
        - spark sql
        - spark streaming
        - MLlib(Machine learning)
        - graphX (Graph API)


# Background to Distributed computing

#### Hadoop vs Datawarehouse
- Before Hadoop how do we handle large data ?
    - Data warehouses like tera data and exa data
    - we create pipelines to gets data from oltp system and brought them in datawarehouse

- why big data is better than DW
    - Horizontal Scalability 
        - simply by adding hardware we can grow the system
    - low Capital cost
        - we can add low cost storage cluster 
        - we can add low cost srevers for processing
        
#### Hadoop (onprimise solution) vs cloud 
- Datalake is the cloud version of hadoop
- data lake has below capabilities 
    - ingestion : data capture and ingestion(integration)
    - store : data storage and management
    - process : data process and transformation
    - consume : data access and retrieval
- in data lake is a repository where we keep raw/unprocessed data,  and sometimes processed data also 
- marketplayer 
    - ingestion : data capture and ingestion(integration)
        - tool which brings data from source system to Datalake
            - informatica
            - talend
            - DW using (pipeline)
        
        - properties
            - its a raw data
            - which we will not change
    
    - store : data storage and management
        - hadoop(onprimises)
        - amazon s3
        - azure blob
        - google cloud
      
        - properties
            - highly scalable
            - highly available
            - low cost
    
    - process : data process and transformation
      - all computaion happens
          - intital data quality check 
          - transformation and preperation of data
          - corelating
          - aggegating
          - Analyzing (extraction of busniness insight)
          - Applying machine learning model
      - to do computin at large scale , process layer broke into two part
          - data processing framwork
              - it allows us to design and develop distributed compuating application
              - ex- apache spark
          - orchestration
              - it is responsible for the formation of cluster
              - managing resources
                  - scaling up
                  - scaling down
              - ex: kunernetes, hadoop yarn, apache mesos
              
    - consume : data access and retrieval
        - putting data for real life process
            - data scitist might want to access dat from lake
            - application and dashboard
            - jdbc /odbc framework
            - rest api dashborad
- chanllanges with data lake
    - security and access control
    - scheduling and workflow mangement
    - data catalog and meta data
    - data life cycle and governance
    - operation and monitoring
            
     

# Spark Archietecture
#### What
   - Spark Ecosystem has two layer
       - Spark next top most layer (Set of DSL, Libraries, API)
           - spark sql framework
           - streaming
           - ML lib
           - Graph X
       - Spark core (Runs on cluster of server to provide distributed system)
           - Spark Core API's
               - Scala
               - Java
               - Python 
               - R
           - Distributed computing engine(Spark Engine)
              
           - Cluster Manager
                - __Spark does not manage cluster, it just give you a framework to work with HDFS and MAPreduce embedded cluster so we need a cluster manager__
               - Resource manger or content orchastrator
               - commonly we use hadoop YARN, as Spark runs on Hadoop paltform
               - we have kubernetes and apache mesos
           - Distributed Storage
               - __Spark does not come with inbuilt storage system. it allows to process data which is stored in variety of storage__
               - commonly use storage HDFS, blob, S3, google cloud storage, casandra system
   
#### More on SPARK architecture   
- __Apache Spark does not provide storage and  cluster managment__
- spark compute engine manage the processing part
    - it breaks the process into smallar task
    - Scheduling those task to cluster for parallel processing
    - Providing data to these task
    - managing and monitoring the task
    - provide intolrance in case of process failure
    - interacting with storage manager and cluster manager
    - cosolidate the output of each task 
- Spark Core API's
    - its a programming interface layer which offers core API's in 4 language
        - Scala
        - python 
        - java
        - R
    - using these API's we used to write data processing logic but these API's are little tricky
        - they are hard to learn as new syntax for common work
        - lacks performance optimization features
- Spark External API's
    - Set of API'S, Packages, Libraries
    - developed over Spark core APIs, that mean internally these API's will use Spark CORE API's
    - Spark Libraries
        - Spark SQL
        - Spark Data frame and data set (Fucntional programming technique)(data crunching )
        - Streaming(allow process countinous Data 
        - MLlib( to process ML and DL problem
        - GraphX
        
####  Why Spark 
- Abstraction
    - abstarct the fact that you are coding on a program to execute on cluster of computer , it gives a feel that we are working on database, python dataframe
    - all complixity like distributed storage, parallel processing, computation is abstracted away
- Unified Platform
    - here we can do batch processing , stream processing, structured and semi structured data processing, graph processing, ML &DL code processing at single platform
- Ease of use 
    - use ready to use libraries,Alogorithm, and integration with other tool
    - code are shorter , simple
        

        




```python

```
