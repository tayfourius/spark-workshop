## What You Will Learn (aka Goals)

The goal of the workshop is to give you a practical introduction to Apache Spark and how to use Spark's Scala API (developer) and infrastructure (administrator, devops) effectively.

The workshop uses the code-first approach in which the modules start with enough knowledge to get you going fairly well and (after 10 minutes or so) move to using the concepts outlined in examples. It comes with many practical sessions that should meet expectations of software engineers, administrators, devops, and other technical roles like system architects or technical leads.

It simply provides participants with practical skills to leverage the features of Apache Spark with Scala (the programming language).

## Outcomes

Participants will be able to:

* Develop Spark applications using Scala API
* Use Spark in local mode as well as Spark Standalone clusters
* How to install Spark development and runtime environments
* How to build processing pipelines using Spark's RDD and abstractions above in Spark SQL (DataFrames), Spark Streaming (DStreams), and Spark MLlib (Pipeline API).
* The internals of Spark and execution model

## Agenda

The programming language to use during the course is [Scala](http://www.scala-lang.org/). There is a one-day "crash course" to the language during the workshop. It is optional for skilled Scala developers who are familiar with the fundamentals of Scala.

### Scala (one-day crash course)

This module aims at introducing Scala and the tools, i.e. sbt and Scala REPL, to complete the other Spark modules.

This module covers:

* Scala REPL
* Literals and Values
* Basic Types (Numerics, Strings)
* More Advanced Types (Tuples, Options)
* Expressions and Conditions
* Methods and Functions
* Scala Collection API and Common Collection Types
  * Seqs, Lists, Sets, Maps
* Command-line Applications
* Packages
* Case Classes, Objects, and Traits
* Pattern Matching

### Spark Core

1. Installing Spark and My First Spark Application (using spark-shell)
  1. Exercise: Word Counter = Counting words in README.md
1. Using Spark’s Core APIs in Scala - Transformations and Actions
  1. Exercise: Key-value pair operators
1. Building, Deploying and Monitoring Spark Applications (using sbt, spark-submit, and web UI)
  1. Exercise: A Complete Development Cycle of Spark Application
1. Processing Structured Data using RDDs
  1. Traditional / Old-Fashioned Approach
  1. Exercise: Accessing Data in Apache Cassandra
1. Monitoring Spark Applications using web UI
  1. Jobs, Stages, Tasks, and Shuffling
  1. Caching and Storage Tab
  1. Exercise: Monitoring using web UI
1. Clustering Spark and Spark Standalone
  1. Exercise: Setting up Spark Standalone
  1. Exercise: Deploying Applications using spark-submit (`--master` and `--deploy-mode`)
1. Tuning Spark Infrastructure
  1. Exercise: Configuring CPU and Memory for Master and Executors
  1. Exercise: Observing Shuffling using `groupByKey`

### Spark SQL

1. Spark SQL and DataFrames
  1. Exercise: Creating DataFrames
      * `toDF`
      * `SQLContext.createDataFrame` and Explicit Schema using `StructType`
  1. Exercise: Manipulating data from CSV using DataFrames
      * `SQLContext.read`
      * `count`
1. DataFrames and Query DSL
  1. Exercise: Using Query DSL to select columns
  1. Exercise: `withColumn`
1. functions object
  1. Exercise: Manipulating DataFrames using functions
    * `withColumn`
1. Spark SQL and Datasets
  1. Exercise: Loading data from CSV and JSON
1. Caching
  1. Exercise: Measuring Query Times using web UI
1. Aggregating
  1. Exercise: Compute Aggregates using `mapGroups`
    * Word Count using Datasets
1. Accessing Structured Data using JDBC
  1. Modern / New-Age Approach
  1. Exercise: Reading Data from and Writing to MySQL
1. User-Defined Functions (UDFs)
  1. Exercise: Using UDFs to create new DataFrames

### Spark Streaming

1. Spark Streaming
  1. Exercise ConstantInputDStream in motion in Standalone Streaming Application
1. Input DStreams (with and without Receivers)
  1. Exercise: Processing Files Using File Receiver
    * Word Count
  1. Exercise: Using Socket Receiver
  1. Exercise: Processing `vmstat` Using Apache Kafka
1. Monitoring Streaming Applications using web UI (Streaming tab)
  1. Exercise: Monitoring and Tuning Streaming Applications
    * "Sleeping on Purpose" in `map` to slow down processing
1. Spark Streaming and Checkpointing (for fault tolerance and exactly-once delivery)
  1. Exercise: Start StreamingContext from Checkpoint
1. State Management in Spark Streaming (Stateful Operators)
  1. Exercise: Use `mapWithState` for stateful computation
1. Spark Streaming and Windowed Operators
  1. Exercise: ???

### Spark MLlib

1. ML Pipelines

### Extras

1. Exercise: Stream Processing using Spark Streaming and Spark SQL.

## Requirements

* Training classes are best for groups up to 12 participants.
* Some experience of software development using modern programming language (Scala, Java, Python, C, Ruby, JavaScript) is recommended. The workshop introduces only enough Scala to develop Spark applications using Scala API.
* Participants have decent computers, preferably with Linux/Mac OS operating systems
  * There are issues with running Spark on Windows (mostly with Spark SQL / Hive)
* Participants have to download the following packages to their computers before the class:
  * [spark-1.6.0-bin-hadoop2.6.tgz](http://www.apache.org/dyn/closer.lua/spark/spark-1.6.0/spark-1.6.0-bin-hadoop2.6.tgz)
  * [sbt-0.13.11.zip](https://dl.bintray.com/sbt/native-packages/sbt/0.13.11/sbt-0.13.11.zip)
  * sbt-assembly plugin
  * [IntelliJ IDEA Community Edition 15.0.4](https://www.jetbrains.com/idea/download/) (or equivalent development environment)
    * Install [Scala plugin](https://plugins.jetbrains.com/plugin/?id=1347)
  * [kafka_2.11-0.9.0.1.tgz](https://www.apache.org/dyn/closer.cgi?path=/kafka/0.9.0.1/kafka_2.11-0.9.0.1.tgz)
  * [H2 Database Engine](http://www.h2database.com/html/main.html) - download [zip file with Version 1.4.191 for All Platforms](http://www.h2database.com/h2-2016-01-21.zip)
  * [apache-cassandra-3.4-bin.tar.gz](http://www.apache.org/dyn/closer.lua/cassandra/3.4/apache-cassandra-3.4-bin.tar.gz)
  * [Cassandra Spark Connector 1.6.0-M1](http://spark-packages.org/package/datastax/spark-cassandra-connector) by executing the following command: `$SPARK_HOME/bin/spark-shell --packages datastax:spark-cassandra-connector:1.6.0-M1-s_2.10`
  * (optional) Apache MySQL and MySQL JDBC Driver