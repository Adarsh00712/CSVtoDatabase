
# Java Sync Service
***
## Task
Create a Java service that syncs data from CSV to MySQL. It consists of two parts.

Part 1: You will be given a CSV file that should keep updating over the time. You have to right a Java program that adds few rows of data in the CSV File.

Part 2: You have to populate the MySQL table with the data present in CSV. Your service should run in every 2 mins and check for any new data in CSV.

## Skills
***
Java,DBMS on MYSQL,MS Office..

## Technologies
***
* [IntelliJ Idea Community Edition](https://www.jetbrains.com/idea/download/?fromIDE=#section=windows): Version 2022.1.1
* [JDK](https://download.oracle.com/java/18/latest/jdk-18_windows-x64_bin.msi): Version  18.0.1.1 
* [MYSQL](https://dev.mysql.com/downloads/mysql/) Version 8.0.29
* [Github](https://github.com/) Version 5.10.3

## Installation
***


Steps to install Intellij IDEA plugin from IDE:

* Open the Settings dialog.

* In the left-hand pane, select Plugins.

* On the Plugins page that opens in the right-hand part of the dialog, click the Install MAVEN and Githuib Plugins.

### Creating a java Project
***
* File -> New Project.
* Choose 'Java'.
* Choose the project location and java sdk
* Finish

### Maven project using maven-plugin
***
* File -> New Project

* Choose Maven
* Choose the  java sdk then Enter project Name, location.
* Finish
### Dependecies
***
* Adding dependecies of mysql-connector and opencsv in POM.XML file

```bash
  <dependencies>
        <!-- https://mvnrepository.com/artifact/mysql/mysql-connector-java -->

        <dependency>
            <groupId>mysql</groupId>
            <artifactId>mysql-connector-java</artifactId>
            <version>8.0.29</version>

        </dependency>

        <!-- https://mavenlibs.com/maven/dependency/com.opencsv/opencsv -->
        <dependency>
            <groupId>com.opencsv</groupId>
            <artifactId>opencsv</artifactId>
            <version>5.6</version>
        </dependency>
```
### Execution 
***
* After Creating project named CSVtoDatabase and adding dependecies to POM.XML I have created a two java package which are csvtodatabase and parts.
* In csvtodatabase package I have created a java class named CSVConsume.java and Write a java code to Sync data from given CSV file to database and run the code Successfully.
### Result
![CSVtoDatabase](https://user-images.githubusercontent.com/105857305/174337400-45219b6f-79b2-4dd2-9e99-3ba95a91665c.png)
![CSVtoDatabase Proof](https://user-images.githubusercontent.com/105857305/174337800-5e0ce8e4-7568-49e2-887b-98e06e4161e9.png)

* For part 1 I have created java class Part1.java in package named parts and Write code  that adds few rows of data in the CSV File and run the code by adding 3 rows data to CSV file Successfully.
### Result
![Part1](https://user-images.githubusercontent.com/105857305/174338375-8df85e9b-71fd-4abf-93d4-95fc0a7d27dc.png)

![Part1 Result Proof](https://user-images.githubusercontent.com/105857305/174338019-e26addc7-58c3-4a0d-9a28-3431a191e63b.png)

* For part 2 I have created a java class Part2.java in package named parts and Write a code which run the service in every 2 minutes and check for new data. For adding the new csv file data to database I have use the Section of code from CSV.Consume.java class firstly by Truncate the table which avoid the rewriting the same data into the database. All this section of code run inside run() method by using Runnable interface. After that by using ScheduledExecutorService object (scheduler is created using the Executors.newScheduledThreadPool(int corePoolSize) method)  for running the code after every 2 Minutes with 0 initial delay I use scheduleAtFixedRate() method.
### Result 
![Part2](https://user-images.githubusercontent.com/105857305/174338768-86de3ee9-df0a-4ba5-b008-4581cf9b72f0.png)

### Support
***
For Support email adarshdwivedi2@gmail.com

### License
***
Apache License 2.0




