mongodb-bench
=============

A simple command line tool for benchmarking MongoDB performance

This tool takes its inspiration from the famous Apache Bench tool, which is has been used for years to benchmark Apache Web server installations.
The intentions is to have a simple utility which allows you to quickly see if your MongoDB performance is in the right ball park and you haven't
done an accidental misconfiguration (like not set your ulimits high enough, or set your /data/db directory to some naff little disk)

Building mongodb-bench
----------------------

mongodb-bench is written in Java (version 1.6) using Maven (version 3)

THe following steps assume you have Java 1.6 and Maven 3 installed and configured

1.  Pull down the project

    git clone https://github.com/bishi3000/mongodb-bench.git

2.  Inside the mongodb-bench directory, type:

    mvn clean compile assembly:single

This will now create a single jar file in the mongodb-bench/target directory called "mongodb-benchmark-<version>-jar-with-dependencies.jar"

All the projects libraries will be included in this jar file

Runnuning mongodb-bench
-----------------------

To run mongodb-bench, run the following command:

    java -jar mongodb-benchmark-1.0-SNAPSHOT-jar-with-dependencies.jar

This should present the usage and options output.

By default mongodb-bench will attempt to connect to a mongodb instance running on 'localhost' on the default port '27017'

These default can be overriden with the -h and -p arguments.

