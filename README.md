
# ELK-based Analysis of Mozilla Build System Logs

## Introduction

In this project, we aim to analyze the logs generated by the Mozilla Build System and load them into Elasticsearch using Logstash.

Once the logs are loaded into Elasticsearch, we will use Kibana to visualize and analyze the data. Kibana is an open-source analytics and visualization platform designed to work with Elasticsearch. With Kibana, we can create interactive dashboards and visualizations to explore the data and gain insights.

![proejct](https://github.com/aym0ane/LogsAnalysiswithELK/blob/main/imgs/proejct.JPG)

Overall, this project aims to provide a comprehensive analysis of the Mozilla Build System logs, with the goal of improving the build process and identifying areas for optimization.

### Here is an overview of our proejct : 
![](https://github.com/aym0ane/LogsAnalysiswithELK/blob/main/imgs/project%20overview.JPG)
## Data Preparation 

The data preparation phase of this project involved transforming the raw text log files into a more structured and usable format. This was achieved by writing a Python script that parsed the log files line by line, extracted the relevant information, and transformed it into a JSON format that could be easily loaded into ElasticSearch. 

The script utilized regular expressions to identify key data points such as the start and end times of each step or block, the name of each step or block, the arguments passed to each step or block, and the duration of each step or block. Once the log data was transformed into JSON format, it was loaded into ElasticSearch using Logstash.

 #### Code in  : data(logs) Preparation.ipynb 

![log transformation function ]()

This allowed for more efficient storage and retrieval of the log data, as well as enabling more advanced analysis and visualization using Kibana. 

#### logs structure after the transformation  : 
![logs after transformation ]()

The data preparation phase was critical in ensuring that the log data was properly structured and formatted for analysis, and laid the foundation for the subsequent phases of the project.


## Configuration of filebeat and  Logstash


configurations

## Mapping in Elasticsearch

Using  Elasticsearch as our database, we needed to create a mapping that would define the structure of our documents. The mapping outlines the fields and their types, which allows Elasticsearch to index and search the data more efficiently.

In our case, we created a mapping that included various fields, such as "@timestamp," which is a reserved field in Elasticsearch that stores the timestamp of each log event, and "@version," which represents the version of the log. We also included fields like "host," "log," "errno," and "file," each of which is defined with its own data type and properties. By creating this mapping, we were able to ensure that the data would be stored accurately and efficiently in Elasticsearch, allowing us to easily search and analyze the data with Kibana.


### Visualization with Kibana

After loading the Mozilla build logs into Elasticsearch, we can visualize the data using Kibana. Kibana provides various options for creating visualizations such as bar charts, line charts, pie charts, and more. We can use Kibana to create visualizations of the Mozilla build logs to better understand the data and draw insights.



## Conclusion

In conclusion, the Mozilla Build System Logs Analysis using Elk project aimed to provide insights and valuable information from the Mozilla build logs. Through the use of Logstash, Elasticsearch, and Kibana, we were able to transform the raw log data into a structured and searchable format. The project involved data preparation, configuring Filebeat and Logstash, mapping the data in Elasticsearch, and creating visualizations in Kibana. With this project, we were able to successfully analyze the build logs and identify issues that could potentially impact the overall build process. The project demonstrated the power and flexibility of the ELK stack in transforming large amounts of unstructured data into actionable insights.

