# PageRank-and-Topic-Modelling
Big Data Project utilizes two Scala classes which runs on Amazon EMR
Code packaged into a JAR file
Steps to Page Rank and Topic Modeling : 
1.	Upload the 480159016_T_ONTIME_REPORTING.csv file to AWS S3 bucket
2.	Upload the Sherlock.txt file to AWS S3 bucket
3.	Upload the project file created from intellij pagerank_topicmodeling_2.11-0.1.jar
4.	To run the PageRank/TopicModeling on the data, start AWS EMR cluster
5.	After the cluster is Ready, go to Steps  Add Step
6.	Select Step type as “Spark Application”
7.	For running the PageRank, we should specify 3 arguments
•	Enter “—class PageRank”
•	Select the options and choose jar “pagerank_topicmodeling_2.11-0.1.jar”
•	Argument 1 – Location of the Airport dataset 
s3://assignment2pagerank/480159016_T_ONTIME_REPORTING.csv
•	Argument 2 – Number of iterations
10
•	Argument 3 – Output file path
/FileStore/tables/output
8.	For running the TopicModeling, we should specify 2 arguments
•	Enter “—class TopicModeling”
•	Select the options and choose jar “pagerank_topicmodeling_2.11-0.1.jar”
•	Argument 1 – Location of the Text taken (we have taken Adventures of Sherlock Homes)
s3://assignmentpart2/Sherlock.txt
•	Argument 2– Output file path
/FileStore/tables/output
	(Note : https://assignmentpart2.s3.amazonaws.com/ - This is a file having links to all objects)
9.	Output files for Page Rank and Topic Modeling will be in AWS S3 bucket

10.	 Part 3 was done using data-bricks
•	Data Set used was – dogs and cats dataset from Kaggle
https://www.kaggle.com/chetankv/dogs-cats-images
 
11.	Link to code and output
•	https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/2116718655794530/3888587329200349/5576141171126174/latest.html
