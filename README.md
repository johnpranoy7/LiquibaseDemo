# LiquibaseDemo with Oracle DB
You will need a DB(Oracle in this example). Place its dependency in pom.xml (here ojdbc8.jar) along with liquibase maven plugin

## Commands
First Clean the Project then execute 

    mvn clean
    mvn liquibase:update
 
 To generate SQL File and review with your DBA/Leads before executing 
 
    mvn liquibase:updateSQL

 To delete all Tables
    
    mvn liquibase:dropAll
    
 To generate SQL for the Existing Database (trying to setup Liquibase for database which is already in use)
 Note: This will not generate ChangeSets for Stored Procedures, Functions and Triggers
    
    mvn liquibase:generateChangeLog
    
## Useful DB Queries

    //If execution fails in between need to run this query to remove Lock
    UPDATE DATABASECHANGELOGLOCK SET LOCKED=0, LOCKGRANTED=null, LOCKEDBY=null where ID=1;
    
    //For Validation Error on Modified ChangeSet
    update databasechangelog set md5sum=null where id=1; 
    
## References
- [Tutorial](https://www.youtube.com/watch?v=WPAKj0ygul0&list=PL8LikImwls6IM8Ks9CvpnU4UbcBCJUd3C&index=1&ab_channel=SivaReddy)
- [Setting Ojdbc Jar in local mvn repo](https://mkyong.com/maven/how-to-add-oracle-jdbc-driver-in-your-maven-local-repository/)
