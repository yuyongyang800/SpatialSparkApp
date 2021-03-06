SpatialSparkApp
===============

## Introduction

This repository will be used as a codebase for our efforts to realize spatio-temporal queries on top of Spark-Streaming. 

## Requirements
You need to have sbt 0.13x installed. More information about [sbt] (http://www.scala-sbt.org/0.13/tutorial/Setup.html) 

## Building 

To build a single jar for Spark cluster submission.

	$ sbt assembly

## Eclipse integration

You need [ScalaIDE](http://scala-ide.org/) Eclipse plugin. 

The project template is configured with the eclipse project generator plug-in so that Eclipse can be used as an IDE. To generate the required files for Eclipse, run:

	$ sbt eclipse

Then, do 
	File -> Import ... -> Existing Projects into workspace 

### Notes

If the dependencies change, you need to run again:

	$ sbt eclipse 

and refresh your project directory from the Project Explorer.

## Kafka as Source and Sink for Queries

If you want to mimic a full stream processing cycle, where you have the following pipleline:

	Input streams --> Processing --> Output streams 

Instead of the following:

	Input streams --> Processing --> Output Console 

You can use Kafka as a source and as a sink. The example application is at 
	
	queries.Kafka

Obviously, you need Kafka deployed. Check out their website [http://kafka.apache.org/](http://kafka.apache.org/). 

