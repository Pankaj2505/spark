---
layout: post
title:  "History of Big data"
date:   2022-01-31 09:04:08 +0530
categories: spark
permalink: /:categories/:title
---


# History of Big-Data

> as data volumn incresed , the power of storage and processing also increased.
- Task associated with data
    - Data caputure and ingestion
    - Data Storage and Management
    - Data Processing and Transformation
    - Data Access and retrival



- Data caputure and ingestion
    - __data collection is gonna increase every day__ 
    - google search engine was reading each webpage, and capturing some data from it,
    - caputuring how many users ad how often they are visiting.
    - there is 5 property of data
        - volumn,
            - reading thousand of petabyte
        - variety,
            - what type of data we are reading (text, audio, vedio, binary, numerical)
        - velocity,
            - how often we are reading the data
        - verasity,
            - how much noise is in data
        - value
            - how much valuable your data is.
    - IOT devices (device with sensor) they create peta bytes of data every year.
- Data Storage and Management
    - we uses various data base to store and manage data
        - Boyes and cott, they came with an idea of relational database (store data in table)
            - orcle,
            - sql server
            - postgres
            - My SQL
    - but as data volumn increased relation database started failing , as they are not desinged for petabytes level of data
        - Google (larry page,Jeff Dean) came with an idea of distributed system
            - Hadoop
            - Map Reduce
            - Spark
            - Mongo DB
        > __Every Tool has its own objective__
- Data Processing and Transformation
    - compute heavy task
        - super computer system
        - weather forcasting need to compute on many algortihm, here we do lot of optmization computing
        - Deep learning(lots of computation is needed even for small dataset)
        - Super computer are desinged for parallel processing . for example 4 core, can do 4 task parallely ,so supercomputer has 100 cores or more.
        - two framework are popular for parallel processing
            - MPI(1970)
            - PVM(1980-1990)
    - data heavy task
        - Big data system
        - (joining, grouping, count) these are data heavy task
        - Traditional relation database sytem(before 2000)
            - core idea: hardisk and ram is not cheap 
                - that's why we uses normalization to minimize the amount of data storage
                - wait time is ok for query execution
                - Database is hosted in single server, which may have many core for computation, but still there used to be a wait time invlolve in query execution.
        -  Distributed storage system(Map Reduce)(2000)
            - Core idea: Hard disk is cheap,RAM is expensive,  computation and low latency application is important
                - Hadoop has designed HDFS(hadoop distributed file system) is the implemantation of map reduce
                - hive is facebook implemantation of map reduce,this is a engine which convert sql query to map reduce queries
                - pig desgined by yahoo, this is a engine which convert sql query to map reduce queries
            - they have used a rack made by 10+ motherbored, each mother has its own harddisk, ram, cooling fan, processor(cpu)
            - all these motherbord is connected using lan
            - now we are storing the data across multiple harddisk( distributing the storage accross multiple harddisk)
            - Scalable (as we can add more motherbord)
            - Map Reduce, is a framework which helps to process through distributed storage.
                - File system 
                    - its a orchastration software which, given a large data, distribute it data accross multiple storage.
                - compute cordination system
                    - given a task,  orchastration software, which used to pull data from various HDD, and do the task.
              
            - Hadoop used to stores intermediatory data to disk, as ram is expensive. so computation is very expensive.
            
            
        - SPARK(2012)
            - core idea : RAM is cheaper, harddisk is super cheap , low latency application is must
            - now all the intermediatory data is stored in RAM.
            - Spark is superset of Map- Reduce, intermediatory data is sotred in RAM, if its too much , then in harddisk
            - pyspark is the language to work with spark
                
        
        - GPU(2017)
            - Graphics processing unit
            - it sits beside CPU, and process all the graphics (game graphichs, video processing)
            - deep learning on large dataset is both copute heavy and data heavy task
     
        - CLOUD computing
    
- Data Access and retrival


```python

```
