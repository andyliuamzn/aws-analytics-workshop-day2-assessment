Tasks you need to complete on this learn to hire session.
If you cannot complete all task, provide the details where did you stuck and how did you investigate the issue.
And what is next you will try in this situation, the more details the better.

"The majority of the exercises can be completed using the "Dev Tool" in Opensearch Dashboard but not all.
---
#### 1. Set up a public-based OpenSearch 2.17 cluster (Choose just 1 m5.large data node without dedicated master node while optimizing cost).
* You can refer to this AWS Doc https://docs.aws.amazon.com/opensearch-service/latest/developerguide/vpc.html
* No need to provide any relevant details.

#### 2. Set up an index template with 3 primary shards and 2 replicas. Use the appropriate command to check the current index settings. Record the command in your answer.
* Provide the query you use to setup the index settings.
* Screenshot of the index settings

#### 3. Using the data file amazon.book.json, process the dataset (attachment: amazon.books.json) and upload it to your cluster. 
* You can use curl, Logstash, or any programming language to process the file and send it to the Elasticsearch cluster you created.
* Details of how you process the data, what issues have you encountered in your work?

#### 4. Create visualizations and a dashboard. Create two simple visualizations, and then create one dashboard that incorporates the visualizations you've created.
* The screenshot of the dashboard you created and each of settings.
  
#### 5. Using the "opensearch_dashboards_sample_data_flights" dataset, write an Elasticsearch query to find out how many flights have delays.
* The query you use to find out the total of flight delay
