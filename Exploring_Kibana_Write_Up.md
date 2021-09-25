## Activity File: Exploring Kibana

* You are a DevOps professional and have set up monitoring for one of your web servers. You are collecting all sorts of web log data and it is your job to review the data regularly to make sure everything is running smoothly. 

* Today, you notice something strange in the logs and you want to take a closer look.

* Your task: Explore the web server logs to see if there's anything unusual. Specifically, you will:

:warning: **Heads Up**: These sample logs are specific to the time you view them. As such, your answers will be different from the answers provided in the solution file. 

---

### Instructions

1. Add the sample web log data to Kibana.

2. Answer the following questions:

    - In the last 7 days, how many unique visitors were located in India?
      - 228
    - In the last 24 hours, of the visitors from China, how many were using Mac OSX?
      - 11
    - In the last 2 days, what percentage of visitors received 404 errors? How about 503 errors?
      - 404 Errors - 23
      - 503 Errors - 17
    - In the last 7 days, what country produced the majority of the traffic on the website?
      - China produced the most traffic at 20.5%
    - Of the traffic that's coming from that country, what time of day had the highest amount of activity?
      - 10:00 
    - List all the types of downloaded files that have been identified for the last 7 days, along with a short description of each file type (use Google if you aren't sure about a particular file type).
      - css - files that describe how HTML elements are displayed on the screen
      - deb - Debian Software Package file, used to retrieve and install .deb archives associated with a package
      - gz - a compressed archive file, created by GNU zip compression algorithm
      - rpm - Red Hat Package Manager file used to store and install packages on Linux operating systems
      - zip - compressed file using DEFLATE algorithm

3. Now that you have a feel for the data, Let's dive a bit deeper. Look at the chart that shows Unique Visitors Vs. Average Bytes.
     - Locate the time frame in the last 7 days with the most amount of bytes (activity).
     - In your own words, is there anything that seems potentially strange about this activity?
       - There were an average of 15,709 bytes downloaded by one unique user at 20:57. This does seem odd and may point us in the direction of someone downloading or uploading a large amount of information. 
     
4. Filter the data by this event.
     - What is the timestamp for this event?
       - 20:57
     - What kind of file was downloaded?
       - An .rpm file was downloaded
     - From what country did this activity originate?
       - India
     - What HTTP response codes were encountered by this visitor?
       - 200 which indicates the request has succeeded
     
5. Switch to the Kibana Discover page to see more details about this activity.
     - What is the source IP address of this activity?
       - 35.143.166.159
     - What are the geo coordinates of this activity?
       -  43.34121, -73.6103075 which is The Flloyd Bennet Memorial Airport in New York
     - What OS was the source machine running?
       - Windows 8
     - What is the full URL that was accessed?
       - https://www.elastic.co/downloads/
     - From what website did the visitor's traffic originate?
       - elastic.co
     
6. Finish your investigation with a short overview of your insights. 

     - What do you think the user was doing?
       - It looks like they are experimenting with a sample Kibana dataset.
     - Was the file they downloaded malicious? If not, what is the file used for?
       - They Downloaded a Kibana sample data log so probably not Malicious activity. 
     - Is there anything that seems suspicious about this activity?
       - It is odd that the geo.coordinates gave an airport as a source location of where this file is being downloaded. The IP address is also one that is maped to Florida. So the source and destination IPs are odd because they say this originated in India and was headed for China
     - Is any of the traffic you inspected potentially outside of compliance guidlines?
       - It is strange to see a Florida IP that is claiming to be in India. Its also strange to see that the geo-coordintaes are in New York

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  