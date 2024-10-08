## *Most application today are data-intensive, as opposed to compute-intensive.*

In this chapter we will discuss about :

1. Reliablity: The system should keep on working correctly even after encountering software, hardware or human error.

2. Scalablity: If a system grows in terms of data, traffic or complexity there should be appropriate ways of dealing with it.

3. Maintainability: Over the time different people will work on the system, they should be able to work on it productively.


### Reliablity : 

By defination to be reliable means to be responsible of taking care of things one is supposed to.

So if terms of database systems,

    1. If an application performs the function it is supposed to,
    2. It can tolerate user making mistakes,
    3. It can perform good even in situations of high load,
    4. It make prevenet unauthorized access and abuse.

Then that system is called reliable (somewhat), basically if the system is working correctly even when the things go wrong then it is reliable.


Here the *things-that-can-go-wrong* can be termed as fault and a reliable system can also be called *fault-torlerant* or *resilient*.


Now deep-diving into the topic Reliablity

Data reliablity means that database perform consistently without causing any problems.

For data to be considered as reliable: 

    1. Data Integrity : Data is consistent 
    2. Data Saftely : Data is secure from any unauthorized access.
    3. Data recoverablity : Proper mechanisms are there in place in situations of data loss.

    should be ensured. 

*taken from*  [An Introduction to Database Reliability](https://www.bmc.com/blogs/database-reliability/)


#### Types of faults : 

##### 1. Hardware Faults : 
To deal with hardware fault we can add redundancy to each of the hardware component. By redundancy we mean storing the data in more than one place to deal with hardware faliures and keeping the operation active.

But nowadays the data volumes and application's compute demands have increased rapidly which have forced us to incorporate software fault-tolerant techniques in case of *loss of entire machine*.

##### 2. Software Faults :
Unlike the hardware faults which are very less likely to spread (i.e fault in one system's disk wouldn't affect any other system), software cause much more damage as these faults are corelated across the nodes.

Software bugs are very difficult to anticipate as they often lie dormant for a long time unless triggered.

Dealing with software faults is much more difficult task and consumes a lot of time.

    Some ways of dealing with software faults: 
    1. Thorough testing
    2. Process Isoloation
    3. Mointoring and analyzing system behavior in production.


##### 3. Human Error :
Humans can make errors is very obvious and we cant go around it as making error is a way of creating a good and reliable system. 

And reducing those errors is what I am learning.


### Scalabity :

If a system is working a reliable fashion now doesn't mean it would work in the same manner once load on the system is increased. One of the common reason for an application's downfall is it inablity to perform once the concurrent user increases, hence **Scalabilty** is very important aspect of designing a database.

*Scalability is the a system's ability to cope with the increased load.*.

Now lets talk what exactly load means : 

Load isn't a specific number but an umbrella term which may depend upon the context or scope of the project which depends on load parameter.
    It can be :

    1. Request per/sec to a web server.
    2. Ratio of read/write in a database.
    3. Number of active users in a chat room.
    4. Hit rate on a cache.
    5. OR SOMETHING ELSE...

Now lets describe what *performance* means:

Performance is the measure of how quickly and effectively a system operates. Caching, indexing, and query optimization are just a few of the performance-enhancing features that must be included in the architecture.

Performance in software architechture refers to responsiveness of a software system in deleviring its intended functionality, processing requests and providing smooth user experience. 


#### How to cope with increasing *LOAD* ?

On a very basic level there are two types of Scaling :

1. Vertical Scaling
2. Horizontal Scaling

##### Vertical Scaling:
Also know as up-scaling, here we increase the overall performance capacity of out system.
    It could be achived by:
    1. Upgrading the physical machine that's running our system.
    2. Migrating to a more capable machine to handle increased load.

##### Horizontal Scaling:
Also know as out-scaling, here we meet the desired need of the system by adding more number of machines (also known as nodes).
    It could be achieved by:
    1. Adding more number of machine to the environment for meeting the system requirements.

[Additinal Read](https://www.cockroachlabs.com/blog/vertical-scaling-vs-horizontal-scaling/)

In terms of database, it is common wisdom that, until forced to do so, database should be scaled vertically as adding multiple nodes and distributing the database on them can result in a lot of additional complexities.

