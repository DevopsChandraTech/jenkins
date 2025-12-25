Agenda:
1.install 2 ec2 instances with 50GB t3.small
2.resize the partition home 20GB and root 10GB
3.install jenkins in master and install java for node because jenkins implementing using java
4.jenkins running on port number 8080 use master instance ip address and with 8080 port jenkins browse 
5.it is showing the key path take key and give the user details for sign-in
6.once logged in showing the dashboard of jenkins
7.we will give job to jenkins it is doing their job and give result as logs
8.here 2 type freestyle and pipeline
9.check pipeline syntax in google and try deploy the pipeline
10.we installed stageview plug-in
11.create route53 record for we access master in web so give public ip
12 create route53 record for node we access node in ec2 instance so give private ip
----
conditions:
    always: if pipeline success or fail it is running 
    success : if pipeline success then success message come into log
    failure : if pipeline failure then failure message come into log
pipeline 2 types:
1. declarative pipeline:
    before running the pipeline validate the total code of pipeline then execute pipeline
    not more secure,jenkins DSL Groovy
    if error occuer not executing the pipeline
2. scripted pipeline 
    running the pipeline without checking the code,if error occuer then stop the pipeline
    more secure and more control,Purely Groovy