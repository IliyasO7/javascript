# NO-SQL
GO THROUGH THIS AFTER THIS REPO:
 
https://github.com/Devinterview-io/mongodb-interview-questions

What does NoSQL mean?
        
        No sql means Not only structured query language
        
What is the advantage of using NOSQL over SQL according to you? OR
What are some of the advantages of MongoDB? 
       >> Flexible
       >> Scalable
       >> Insertion and Retrival is fast
       >> support automatic sharding
       
What format does NoSql store data in?
        
        JSON format to be specific BSON format

Can we form relations in NOSql? When should we do that? Explain with examples

    Yes, we can embed the data from one collection to another collection which is called referring in No-SQl

What is the type of _id? What is so special about it?
   
    Its a Alphanumeric unique string that is used to uniquely identify the document inisde a collection
    Its a 4 BYTE TIME STAMP
          5 BYTE RANDOM VALUE
          3 BYTE INCREMENTAL COUNTER

When will you use SQL and when will you use NOSql. Explain with example.
      
        It depends on the data if the data is static its not going to vary or change i will choose SQL
        if the Data is dynamic and its scaling w.r.t thatn we should go for nosql

What is a ODM ?

    ODM stands for Object Documenting Mapping Library
    Like mongoose we want to work on the data and not the query so ODM's are used.    

What is populate used for?
       
        Populate is used to sow the details of the objectId or the document that is embeded from another collection to the current collection
What is select used for?
    
    Select is used to sellect certain fields from the document

What is a Document in MongoDB?       
            
            Its a data that is stored in KEY VALUE PAIR inside a collection inside a document
What are Databases in MongoDB?        
        
        They are collection inside which we have document i key value pairs
 
 How do you Scale up MongoDB to handle millions of users? (This can impress interviewers)
        
        >> 1 way is HS i.e adding up the server 
        >> sharding : sharding is the process of splitting data accross multiple databases
          we have 2 type of sharing one is range based sharindg and the other is hash based sharding
          Range based: Suppose you have a large amount of data lets say from 1-1000 we try to split this data into smal parts as in 1-100,100-200 based on 1 key whcih is called a s shardkey whcih can be Userid
          to target one partilcualr shard/database

          Hash based: 
          In hash based shard we try to create a hash on a shard key that is used to uniquely identifiy a shard and that is used to target the database
          On top of that we can apply indexes.

Indexing
    
    Its a data structure whcih is used tp insert and retrieve the data faster
    Its used to order the unordered table

    Type of Indexing 
        Single Indexing
        Compond
        Hashed 
        Text
        
    userSchema.createIndex({"FIELDNNAME"})
if array 
    
     productSchema.createIndex({"FIELDNAME.element});

What does replica set mean in Mongodb?
    
    Its a group of mongodb instances that hold the same data set

    So basically while writing or inserting there is a primary/MASTER node that writes the data and the then we have secondary nodes that retrieves the data from the primary ndoe
    and if the primary node fails the secodnary nodes choose a primary node amonsgt themselves


Virtuals ? 
Virtuals are the funciton that are used to access the properties of schemas?
                                            
                                            userSchema.virtuals("usernmae.full").get(function(){
                                                return console.log(this.name.first + " " + this.name.last)
                                            }).set(fucntion(value){
                                                var fullName = value.split(" ")
                                                this.name.first = fullName[0];
                                                this.name.last = fullName[1];
                                            }
                                                

🔹 22. Does Mongodb Support Foreign Key Constraints?
        
        NO it does not support fk constraint


What is cluster in monogdb
    
    Its a group of nodes that works together and  is used to maintian the consistency,scalability and availabiltioy in a databse

when should u normalise a database
    
    to eliminate inconsistency,

What is the storage engine used
Wired tiger

    compression of data
    concurrency control
    locking of documents

          
