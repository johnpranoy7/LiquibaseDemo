# LiquibaseDemo
## Commmands
First Clean the Project then execute 

    mvn clean
    mvn liquibase:update
 
 To generate SQL File and review with your DBA/Leads before executing 
 
    mvn liquibase:updateSQL

To delete all Tables
mvn liquibase:dropAll
