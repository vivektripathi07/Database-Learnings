*Most application today are data-intensive, as opposed to compute-intensive.*

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

*taken from ~* [An Introduction to Database Reliability](https://www.bmc.com/blogs/database-reliability/)


#### Types of faults : 

##### 1. Hardware Faults : 
To deal with hardware fault we can add redundancy to each of the hardware component. By redundancy we mean storing the data in more than one place to deal with hardware faliures and keeping the operation active.

But nowadays the data volumes and application's compute demands have increased rapidly which have forced us to incorporate _software fault-tolerant_ techniques in case of *loss of entire machine*.





