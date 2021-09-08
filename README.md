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
    
## References
- [Tutorial](https://www.youtube.com/watch?v=WPAKj0ygul0&list=PL8LikImwls6IM8Ks9CvpnU4UbcBCJUd3C&index=1&ab_channel=SivaReddy)
- [Setting Ojdbc Jar in local mvn repo](https://mkyong.com/maven/how-to-add-oracle-jdbc-driver-in-your-maven-local-repository/)
