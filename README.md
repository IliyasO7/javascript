#SQL

What is Sequelize and why it is used?

                SEQUELIZE is an OBJECT Relational mapping library , we want to work on the data not hte querry so sequelize is used!.

Why you are using MySql and why not NoSQL in the project?

    -It depends on the data if the data is going to be statis id not going to be dynamix or evovling w.r.t time than you should go fpr SQL.
    -When your data is going to be dynamic and evovling chaning or scaling that Nosql should be preferred.

What are views in MqSql?
                
                VIEWS Are ghraphical representaion of row and column inside a table.

How to connect sequelize to database?

         We can craete an instance of Sequelize using new keyword and pass the database configuration like database name,password,username,inside options we can specify dialect as thte type of database as post gre or               mysql and provide the host as local host or databse url.

What are joins ? Explain the different types of joins and their uses?
            
            joins are used to join 2 or more rows form different table based on the column

           > Inner join: Inner join return the records when there is a matching values in both the tables
                        SELECT table1.columnname, table2.columnname
                        from table1 
                        inner join table 2
                        on tabl1.columnname = table2.columnnmae

            > Left join : Left join return all therecords from the left table and the matching records from the right table

                        SELECT table1.columnname, table2.columnname
                        from table1 
                        left join table 2
                        on tabl1.columnname = table2.columnnmae


           >  Right join : right join return all the records from the right table and the matching records from the left table

                        SELECT table1.columnname, table2.columnname
                        from table1 
                        right join table 2
                        on tabl1.columnname = table2.columnnmae

            > FULL outer join : Return all the records if there is either match in both the table

                        SELECT table1.columnname, table2.columnname
                        from table1 
                        FULL OUTER JOIN table 2
                        on tabl1.columnname = table2.columnnmae

What are MySQL Triggers? Watch this video and explain it in your own words here.
        
        MYSQL TRIGGERS are named databses that are associated with the tables they get activated when certain events occur in that table


What is Sharding in SQL?
    
    Sharding i s a process of splitting data acrros multiple databses 
    There are 2 types of sharding one is ranged based sharding where we try to split  alarge dataset into chunks 
    lets say we have a data around 1-1000 so based on one particular key we try to split it in 1-100,1-200
    which can be userID

    the other way is hash based shared we try to hash a data set or  a key that is used to target a particular shard.
    crypto.hash("dataset")

 What is BLOB -> First watch this video and then go through 
        
    Blob stands for binary large object 
    it is used to store binary data like images and all.

    BLOB
    TINY BLOB
    MEDIUM BLOB
    Large BLOB

What are constraints in SQL? Explain 5 of them?
    
    Constriants are the rules that we specify durig creation of tables
    Like> 

        NOT NULL > the data which we are inserting should not be null
        UNIQUE > The data which we are inserting should be as unique as possible like useranme
        PRIMARY KEY> Its a combination of not null and unique if the data is a pk that means it a oarent table
        FOREIGN KEY> if a key is present as foreign key its a child table it prevents thte links from getting destroyed
        DEFAULT > Default keyword is used to set default values in a database like an example could be  status whcih is going to be active when ever the user will be created

What is a subquery? What are its various types?

                            A query inside a query is a subquery 2 select statements in  query 
                            it is used ot specificaly target rows in a table
                            EXAMPLE : 
                            for e.g we want to find out how many employess inside a dept earn more than avg salary in a dept.
                            there are 4 sub querries
                            SINGLE ROW SUBQUERRY
                            MULTI ROW SUB QUERRY
                            MULTI COLUMN CUBQUERRY
                            NESTED SUBQUERRY    

                                Select salary 
                                from Employee 
                                where salary =(
                                             select distinct salary 
                                             from employee 
                                             order by salary desc
                                             limit 1 offset 2
                                             ); 


What is the use of UNION keyword in SQL? Write an example query.
                                    
                                    UNION keyword is used to combine 2 rows from different table based on the column
                                    
                                    SELECT AGE FROM STUDENTS
                                    UNION 
                                    SELECT AGE FROM TEACHER;

What are Entities and Relationship (ER)?

    ER are the ghraphical representation of tables in terms of rows and columns ,so taht we can have data visulaisation and we can form relationships between the tables

What are the differents types of relationships which are there?

            ONE TO ONE  >>>>>> User and cart
            ONE TO MANY >>>>>>> USER and Products
            MANY TO MANY >>>>>> USER TO ORDERS or student and class 

What is normalisation of database?

    Its a process of arranging data in database
    so as to eliminate the inconsistency and inefficiency in a database
    effecitive utilisation of space and relations between tables

What are Delete, Truncate and DROP keywords?
    
    DDL > CREATE ALTER DROP TRUNCATE
    DML > SELECT INSERT DELETE UPDATE
    DELTE IS DML > delelete is used ot delete one or more rows or column from a table

    TRUNCATE AND DROP ARE DDL
    TRUNCATE IS USED TP drop the values inside the table but not the table
    DROP is used to drop/delte the entire table

    DROP TABLE tbale_name

What is Indexing? What is the advantage of indexing and what is the disadvantage?
        
        Index is a datastructure that is used to retieve the data from the database quicker
        it is used to order the unorderd table 
           
        SINGLE,COMPUND,HASHED INDEXING TEXT INDEIXNG
        CREATE INDEX indname ON column columnnmae

        CREATE INDEX indname
        On employe(columnnmae) 

IN OPERATOR 
           
             IN OPERATOR IS USED TO SPECIFY multiple values
              SELECT * from EMPLOYEE
              Where COUNTRY in ('INDIA','CHINA',"AUSTRALIA')

Between Opeartor
            
            BETWEEN IS USED OT SPECIFY RANGE OF VALUES

          SELECT * from PRODUCTS
          where price between 10 & 20;

How to write an SQL query to find students' names start with 'A'?
    
    SELECT * FROM STUDENTS WHERE NAME LIKE 'A%'


Write the SQL query to get the third maximum salary of an employee from a table named employees.You have to use OFFSET as other algos are not optimised. (Assume whatever you want to) - [Commonly asked Interview Question]
                                        
                                        SELECT * FROM EMPLOYEE 
                                        WHERE SALARY =(
                                        SELECT DISTINCT SALARY FROM EMPLOYEE 
                                        ORDER BY SALARY DESC
                                        LIMIT 1 OFFSET 2);

What is the ACID property in a database? Explain each one of them

                            ATOMICITY - a transaction  is considered as a  single unit
                            CONSISTENCY -  a transaction mainatians consistency in a database
                            ISOLATION - a transaction is isolated fromm all other transactions
                            DURABILITY - if  a transaction is commited the changes are supposed to be permanetn and will not be reverted

What is a deadlock in SQL?
    
    A deadlock is a condition where one resource tries to access the resource that is locked by the other.

    Is a blank space or zero the same as a NULL value?
    NULL MEANS UN AVAILABLE

What is the usage of the NVL() function?
    
    NVL is  a function that converts and expressoin to null for the value that we speicy;

What is SQL injection ? 
            
            Its a code injection technique that destroys our database , IT used in hacking

Write a Query to display the number of employees working in each region? 

                                    SELECT * FROM EMPLOYEE
                                    GROUP BY REGION

Write SQL query to fetch employee names having a salary greater than or equal to 20000 and less than or equal 10000
                  
                        SELECT empnmae from EMPLOYEE
                        Where salary >=10000 && salary <=20000

Given a table Employee having columns empName and empId, what will be the result of the SQL query below? select empName from Employee order by 2 asc;
                    
                    ORDER BY ATLEAST need 2 colums
                    so its  an invalid querry
        
How to delete a column in SQL? Please write the query.
                
                ALTER TABLE tablename DROP COLUMN column name;

How to find the nth highest salary in SQL?
                                         
                                                 SELECT DISTINCT SALARY FROM EMPLOYEE
                                                ORDER BY SALARY DESC
                                                LIMIT 1 OFFSET (n-1);

How to add a new column in SQL?

                                                ALTER TABLE TABLE NAME
                                                ADD COLUMN COLUMN NAME

Write a Query to display odd records from student table?
                        
                     //ALTERNATE AND ODD
                    SELECT * FROM STUDENT WHERE MOD(stud_id,2)=1;

TO FETCH EVEN

                    SLECT * FROM STUDENT WHERE MDO(stud_id,2)=0;
                    
Write a Query to display employee details belongs to ECE department?

        SELECT * FROM EMPLOYEE 
        WHERE DEPARTMENT=ECE

How do you return a hundred books starting from 105th? 
                       
                                SELECT * from Book
                                ORDER BY bookID DESC
                                LIMIT 100 OFFSET 104;

 How would you select all the users, whose email id and phone number is NULL?

                                SELECT * FROM USERS
                                WHERE EMAILID is NULL AND Phone is NUll;

Write an SQL query to fetch five max salaries from a table

                    SELECT DISTICT SALARY
                    FROM EMPLOYEE
                    ORDER BY SALALRY DESC
                    LIMIT 5;

How do you get the  second last id without the max function?

                        SELECT id 
                        FROM EMPLOYEE
                        ORDER BY id DESC
                        limit 1 OFFSET 1  
Write a query to find out the data between the age range of 25 to 35 from employee table?
               
                    SELECT * FROM EMPLOYEE
                    WHERE AGE >=25 AND AGE <=35

WRITE  A QUERY TO DISLAY EMAILID GIVE THE COUNT OF DUPLICATE DATA

    SELECT column1,column2, count(*)
    from TABLE
    GROUP BY COLUMNNMAE
    HAVNIG COUNT(*) > 1;
    

            
