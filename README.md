# NerutiDemo (Backend) - Sentiment Analysis Map Visualisation (SAMV)
>   by Neruti Developers

This application(SAMV) is only for demo purpose and has no real real-world application due to the missing of some components in the natural language processing pipelines such as:

  - Word Standardization 
  - Language Detection
  - Model is pretrained using Stanford Sentiment Treebank
  - Lemmatization
  - Removing not usable symbols 

# Version

  - 12 April 2017 - The first version pushed - 1.0


# Bugs
As this is the so called "part-time" project/simple demo for Neruti Developers and we do not spend too much focusing on fixing the bugs as it would divert our direction. These are the bugs：
  - Stopping Twitter Stream, SparkSession is not really working
  - We can only open one instance/tab to query for one thing only at one time because sharing of Twitter application key/OAuth Key, this can be fixed by allowing user to submit their own OAuth key in frontend and every submission of query will call TwitterUtil again
  - If geographical area of the user is not available, problem comes
  - User need to refresh the backend and frontend often if they want to change query
  - Cannot catch errors in the frontend when the backend has closed connection
  - Using Spark core instead of Spark Streaming 

### Installation of Backend

SAMV requires few things to run and it uses Play Framework as our backend technology (API).
1.  [Java+Scala](https://www.scala-lang.org/download/) 
2.  [sbt](http://www.scala-sbt.org/) 
3.  [RabbitMQ](https://www.rabbitmq.com/download.html) 
4.  [Redis](https://redis.io/) 
5.  [Spark](http://spark.apache.org/) 

The demo is tested on ***Ubuntu 16.04*** Platform。 We do not guarantee Windows can return the same result as installation of the server stuff like redis,rabbitmq and spark will be issues as well.

Clone/ Fork this repo and get started

You will need to go to app>twitter>TwitterIngestion to use your Twitter OAuthToken and Credential

```sh
$ cd nrt-demo-backend
$ sbt run
```

Run the frontend until Spark Session is finished initializing.
You can monitor the MQ and Spark at its monitoring port, refer to Uncle Google/contributors if unclear.

### Frontend
Please visit [SAMV FrontEnd Repo](https://github.com/neruti-developers/neruti-demo-frontend) for more.


### Contributor List
*Austin Goh*  - austin@neruti.com 

---
***Disclaimer*** *We do not guaranteed that it will be maintained well as this repo is just opened for sharing*

Enjoy, 
*Austin (zhao yang)*
