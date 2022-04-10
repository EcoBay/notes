# Database Approach

Uses database to manage information, using a [database management system](database-management-system.md) for every application throughout the organization.

<div class="mermaid">
graph LR;
    A1([Order Filing System]) --> DBMS
    A2([Invoicing System]) --> DBMS
    A3([Payroll Systems]) --> DBMS
    DBMS <--> CD[(Central Database)]
</div>

## Elements of Database Approach

- [Enterprise Data Model](enterprise-data-model.md)
- [Enterprise Resource Planning](enterprise-resource-planning.md)
- [Relational Database](relational-database.md)
- [Database Application](database-application.md)

## Components of Database Environment

- [Computer-Aided Software Engineering (CASE)](computer-aided-software-engineering.md) Tools - used to design database application.
- [Repository](repository.md) - contains definition of programs.
- [Database](database.md) - contains occurrences of data.
- [DBMS](database-management-system.md) - provides access to the database and also the repository.
- [Application Programs](database-application.md) - used to create and maintain the database and provide information to users.
- [User Interface](user-interface.md) - provides user way to interact with the other components.
- Database Administrators - are persons who are responsible of designing database and for developing policies on how to interact with it.
- System Developers - are persons such as system analyst and programers who design new programs
- End-User - are persons who request, or interact with the DBMS.

<div class="mermaid">
graph TD;
    EU:([End users]) <--> DA[Database Application] & DBMS[Database Management System]
    DA <--> DBMS
    DBMS <--> DB[(Database)]
</div>

## Advantages and Disadvantages

These are the advantages and disadvantages of database approach compared to [traditional file processing](traditional-file-processing.md)

### Advantages

- Reducing data redundancy - it reduces duplication of data as it is stored in a single database
- Sharing data - sharing data is easier between application it is stored in one place where all application have access.
- More Information - as you could relate more data together you could gain more information.
- Data Integrity - database application provides constraints in place such as possible ranges of values to prevent invalid input data
- Data Consistency - provides consistency in the data such due to related nature of data
- Improved Data Security - provides different levels of authorization to every user only allowing limited set of actions for each.
- Enforcement of Standards - enforces necessary convention and standards for every data. _Related to data integrity_
- Economy of Scale - it is less costly to scale as information are separated to applications. They can be developed independent from each other.
- Balance of Conflicting Requirements - as decision will be based on the database as whole rather than individual entity.
- Increased Productivity - provides abstraction to low level file handling in easy to use functions.
- Improved Maintenance - as it application and database can be maintained independently without affecting each other.
- Increased Concurrency - as it can manage concurrent operations in the database.
- Improved backing and recovery services - as data are stored in single location backups are easier.

### Disadvantages

- Complexity - it is complex piece of software with a lot of feature and functionality
- Size - it consumes a lot of memory and disk space
- Cost of DBMS - a multi-user database is expensive to install and maintain
- Cost of Conversion - moving from **TFP** to database approach requires additional expenses on hardware and training.
- Performance - As database approach caters for many application, some application may run slower.
- High Impact of Failure - as database is centralized, failure in the database may halt operations in all applications dependent on it.
