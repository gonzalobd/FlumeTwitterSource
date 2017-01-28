# FlumeTwitterSource
Fetch data from Twitter using flume. It will be sent to a Kafka topic and to a HDFS data warehouse.
# Previous Steps
First we need to download the latest version of twitter4j in http://mvnrepository.com/artifact/org.twitter4j/twitter4j-stream
and move it to /usr/lib/flume-ng/lib:

         cd /tmp
         mkdir flume
         cd flume
         git clone  https://github.com/cloudera/cdh-twitter-example.git
         cd cdh-twitter-example
         cd flume-sources
         mvn package
         cp flume-sources-1.0-SNAPSHOT.jar  /usr/lib/flume-ng/lib/
 
 # Runing.
 
 Then we have to go to our flume directory copy our twitter.conf in /conf and run the following shell command:
 
 
