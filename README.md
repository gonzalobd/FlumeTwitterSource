# FlumeTwitterSource
Fetch data from Twitter using flume. It will be sent to a Kafka topic and to a HDFS data warehouse.

# Requirements
We need to have installed hadoop to use their file system HDFS, and zookeeper and kafka with the topic created "twitter".

# Previous Steps
First we need to download the latest version of twitter4j in http://mvnrepository.com/artifact/org.twitter4j/twitter4j-stream
and move it to /usr/lib/flume-ng/lib. At our linux shell:

         > cd /tmp
         > mkdir flume
         > cd flume
         > git clone  https://github.com/cloudera/cdh-twitter-example.git
         > cd cdh-twitter-example
         > cd flume-sources
         > mvn package
         > cp flume-sources-1.0-SNAPSHOT.jar  /usr/lib/flume-ng/lib/
 
 After that we need to create the destination folder in HDFS. After installing and configuring hadoop:
 
          > start-all.sh
          > hadoop fs -mkdir /flume
          > hadoop fs -mkdir /flume/eventsTwitter
          > hadoop fs -chmod -R 777 /flume/
 
 And finally we have to start zookeeper and kafka services and create the topic "twitter".
 
# Runing
 
 Then we have to go to our flume directory copy our twitter.conf in /conf and run the following shell command:
 
 
