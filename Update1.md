Project Update 1
Boyuan Sun

In order to develop a logging system for our album store application, for now, I have started investigation of the technical stack. 
1.	What kind of database to use: 
MySQL or some time series database. After investigation, AWS supports AWS Timeseries and InfluxDB. And InfluxDB has similarities with SQL, with the advantage of being a time series database. So InfluxDB is probably what I will use to store the log. Also, it seems to have the integration with Grafana. 
2.	What is the schema that InfluxDB support: leaned measurement, tag, value, stream of tables etc. concepts of InfluxDB.
3.	How to collect Log information:
After investigation, there are mainly 2 ways to collect log information. One is to make the server send information to InfluxDB. The other one is to use a collector. Within the option of using a collector, there are two options too. One is to develop an API that the server will send information through. Or the server just write to a file and the collector reads the file.
Having a collector reads a file probably has the minimal impact on performance of the main task. So, I investigated the tools I will need, Java Logback and Fluent Bit. 
