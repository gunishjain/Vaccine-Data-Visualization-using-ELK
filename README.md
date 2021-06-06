# Vaccine-Data-Visualization-using-ELK

This Project is Created for ElasticSearch Hackathon organized by Code for Cause
Main Task was to create any project using Elastic Product.
So I used ElasticSearch, Logstash and Kibana to visualize COVID-19 Vaccine Related Dataset.

The Dataset was taken from Kaggle: https://www.kaggle.com/harveenchadha/india-covid19-vaccination-data

# Steps Involved in Creation of The Project

1. Ubuntu ec2 instance was launched and accessed by SSH.
2. JDK, python packages was installed for running ELK stack.
3. **ElasticSearch , Logstash and Kibana** was installed in the ubuntu instance.
4. For accessing Kibana dashboard , I installed Nginx also so that anyone can access the dashboard.
5. Elasticsearh YAML file was configured to Open the Ports and necessary networks.
6. Kibana was also configured so that it connects with elasticsearch.
7. Nginx configuration file in _/etc/nginx/sites-available/default_ was created and ec2 instance IP was given so that it connects with the localhost of Kibana.
8. For using CSV dataset files, logstash required **custom logstash pipeline** which should be created under _/etc/logstash/conf.d_ 
9. Logstash PipeLine file  requires 3 main things:

   **I. Input**
   
   **II. Filter**
   
   **III. Output**
 
10. Pipeline file was created and then Index was created in Kibana.
11. Different tools were then used to Visualize the Data.

PipeLine File : https://github.com/gunishjain/Vaccine-Data-Visualization-using-ELK/blob/master/vaccine-registration.conf

Nginx Configuration with Kibana: https://github.com/gunishjain/Vaccine-Data-Visualization-using-ELK/blob/master/Nginx%20Kibana%20Config.txt

**Images and Configuration files are stored in the repo**

# External References/Resources

https://burnhamforensics.com/2019/02/06/how-to-install-and-configure-nginx-for-kibana/
https://cloudaffaire.com/how-to-create-a-pipeline-in-logstash/
https://coralogix.com/blog/logstash-csv-import-parse-your-data-hands-on-examples/
