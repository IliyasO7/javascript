# Javascript
Its All about javascript


1)What is javascript?


    Javascript is a single threaded synchronous language:
    a)single threaded means one line at a time and in a specific order.
     Everything in javascript happens inside an execution context,so whenever a program is run an execution context is created which has 2 components a memory component and a code component.
      inside the memory component the variables are registered with undefined as memory and in the code execution phase the actual value is being alloted to these variables.


2]What is an execution context?

                       Its the block where the javascript program is being run and executed(I mean compiled and adn interpreted)
                       Interpreteer - Interpretter scans the code.
                       Compiler: Compiles the code into binary code.

3] What is hoisting in javascript?

                                   When you try to access a varibale even before it has been alloted a memory that is hoisting.
                                   console.log(a); //undefined
                                   var a=7;
                                
                                Examples :

                                    a)
                                                    var a = 3;
                                                    function printName(name){
                                                      console.log(name)
                                                    }
                                                    printName("YAVTECH");
                                                    console.log(a)
                                                    
                                                    ANSWER: 
                                                    YAVTECH
                                                    3

                                    b)

                                                    printName("YAVTECH");
                                                    console.log(a);
                                                    var a = 3;
                                                    function printName(name){
                                                      console.log(name)
                                                    }
                                                    
                                                    ANSWER: 
                                                    YAVTECH
                                                    undefined

                                  c)

                                                  console.log(printName);
                                                  console.log(a);
                                                  var a = 3;
                                                  var printName = (name) => {
                                                    console.log(name)
                                                  }

                                                  ANSWER: 
                                                  undefined
                                                  undefined
4)Windows Object, this Keyword lexical scoping?

    When ever a program is run an execution context is created along with it a global object called windows and a this keyword is also ceatedand it referes to the object that is calling that function.

 5)What is lexical Scopipng?
 
           When a function is run an execution context is created the access to the local memory along with the reference to the parent is called as lexical scoping.

                                               a)     var a =7;
                                                    function fun(){
                                                      console.log(a)
                                                    }
                                                    ANSWER:
                                                    7 will be printed because it has access to the local memory as well as reference to the parent.
                                               b) function outerfunction() {
                                                                                console.log(a); 
                                                                                var a = 10;
                                                                                innerfunction();
                                                                                
                                                                                function innerfunction() {
                                                                                      console.log(a)
                                                                                      console.log(window.a);               
                                                                                      console.log(this.a)
                                                                                }      
                                                                          }                
                                                                                
                                                                                var a = 7;
                                                                                var b =3
                                                                                outerfunction();   
                                                                                
                                                                                ANSWER
                                                                                UNDEFINED
                                                                                10
                                                                                
  6)  LET,VAR,CONST

          var is attached to global space a var van be reinitialized again and again it is les strict that const ,

           a)  we can define a var with the same name and same identifier again and agian in the same scope.
                             var a=8;
                             var a=9;
                              NO ERROR
               
           b) A let can never be initialised again and agian with the same name and same identifier in the same scope
                                let a=7;
                                let a =8;
                            SYNTAX ERROR
      
          c) let and const are hoisted they are in temporal deadzone for the time being
          A const  once defined cannot be reinitailised again and again; it is very strict.

  7) SYNTAX<TYPE <REFERENCE ERRORS
         
                                                  Type error
                                                  const a=7;
                                                    a=8;
                        when you try to reinitialise a const with a  different value that is type error;

                                                SYNTAX ERROR
                                                 let a=9;
                                                 let a=10;
         
         
              >  syntax error when you try to reinintialise a let with the same name and same identifier again and again.

                                                Reference Error
                                                 console.log(z);
                   When you try to access a variable that is not in the scope that is a refernce error.


  8) Closures, Set Timeouts!
    Closure?

         A function bind together with a lexical scope is called as closure.
                                    function outerFunction(){
                                      var a=7;
                                      function innerFunction(){
                                            console.log(a)
                                        }
                                        innerFunction();
                                    }
                                    outerFunction();



  SETTIMEOUTS:
  a)

  
                                            console.log('a');
                                            console.log('b');
                                            setTimeout(()=> console.log('c'), 1000);
                                            setTimeout(()=> console.log('d'), 0);
                                            console.log('e');
                                          
                                            ANSWER:
                                                      a
                                                      b
                                                      e
                                                      d
                                                      c



9) DIFFERENCE IN ARRAY FOR EACH AND ARRAY.MAP
                                    
                                       FOR EACH > Array .forEach just traverser  over the array of elements it does not transform the elements of an array into a new array alltogether 
                                       var arr = [1,2,3,5]
                                       var newArr = arr.forEach((item, i ) => {
                                                  console.log(item + 'index' + i)
                                                  return item + i;
                                              })
                                              console.log(newArr)
                                              
                                              ANSWER
                                                        1index0
                                                        2index1
                                                        3index2
                                                        5index3
                                                        UNDEFINED
                                          MAP> Array.map transforms the array of elements into a new array altogether
                                          
                                       var arr = [1,2,3,5]
                                       var newArr = arr.forEach((item, i ) => {
                                                  console.log(item + 'index' + i)
                                                  return item + i;
                                              })
                                              console.log(newArr)
                                            ANSWER
                                            1INDEX0
                                            2INDEX1
                                            3INDEX2
                                            4INDEX3
                                            5INDEX4
                                            [ 1, 3, 5, 7, 9 ];


 10) Block Scope and Shadowing?

                                                     a)Block Scope : Two curly braces encoles together is a block scope.
                                                                        { }
                                                     b)Shadowing:
                                                       When you try to reinitialise a  variable again with a different value that is called a shadowing!
                                                  Example 1:     
                                                                         var a = 50;
                                                                                  {
                                                                                      var a =30;
                                                                                      let b = 20;
                                                                                      let c = 30;
                                                                                  }
                                                                        console.log(a) //30 var is attached to global space.
                                                  
                                                  Example2 :
                                                                            const a = 50;  same for let as well!
                                                                              {
                                                                              var a =30;
                                                                              let b = 20;
                                                                              let c = 30;
                                                                              }
                                                                             console.log(a)
                                                                             SYntax Error as var is attached to global space!
                                                  
                                                  Example 3:
                                                  var a = 50;
                                                            function fun(){
                                                                var a =30;
                                                                let b = 20;
                                                                let c = 30;
                                                            }
                                                        fun();
                                                        console.log(a) //50

  


  
10) CALL APLLY AND BIND
    
                Traditionally object used top have properties and method init , in javascript we can write objects seperately and methods seperatley and we can call apply and bind these methods on the object.
    
                                                        var obj={
                                                          val:1,
                                                        }
                                                        function addToThis(a,b,c){
                                                          return console.log(this.val + a+b+c);
                                                        }
                                                        var arr=[5,6,9]
                                                        
                                                          addToThis.call(obj,5);
                                                          addToThis.apply(obj,arr);
                                                          addToThis.bind(obj,arr);
    
 12) Currying ?
Currying is a concept of using one function to create more function out of it for example.

                                                       let multiply = function(x,y){
                                                           return console.log(x*y);
                                                         }
                                                  
                                                       let multiplyByTwo = multiply.bind(this,2);
                                                       multiplyByTwo(3);

 This is what currying is using one function to create more functions out of it.


 12)Advanced Closures?

                                                                                 function y(){
                                                                                 for(var i=1;i<6;i++){
                                                                                    function z(i){
                                                                                        setTimeout(() => console.log(i ), i * 1000)
                                                                                      }
                                                                                     z(i)
                                                                                   }
                                                                                   console.log('Done Coding')
                                                                                 }
                                                                                y();
                                            if it is var without a function it will refer to the same value of i at the end of the for loop.
                                            if its let a new copy of i will be sent each time.
                                            
  13) What is function statements?
      
                   When we give a name to a function with a keyword as function that is a function statement

                                                              function a(){

                                                                          }
15) What is function Expression?

                    When we assign a function to a varibales that is a function expression
    
                                                          var x = function a(){
         
                                                                }
16)what is the difference in both?

                  The difference is in hoisting, when you try to access x even before it has been initialised it gives undefined.
                 
                  difference is in hoisting during memory creation statement func is alloted a memory and func is assigned to a
                  but in case of express,it is alloted a memory of undefined as its a var and during memory asisgning it will give us an error type error.

 17) what is func delcaration ?

               When ever we use a function keyword to define any function that is a function statement or declarration.


 18)What is anonymous functions?

                                  A function without a name is called an anonymous function.
                                  function (){
                                  }

                                  
19) what is named function expression?
    
                                   When we assign a named function to a variable that is a function expression.
                                                var x = function x(){
                                                     console.log("FUNCTION EXPRESSION");
                                             }
                                            x();
    
20)Tricky Questions?

                                                       function fun1(a){
                                                             return (b) => { 
                                                             a = a + b;
                                                              console.log(a)    
                                                             }  
                                                        fun1(10)(30) // 40

                                                        INVALID ERROR SYNTAX
                                                         function fun1(a){
                                                          const fun2 = (b) => {
                                                          a = a + b
                                                          console.log(a)
                                                         })
                                                         fun1(10)(30)

21) THIS
    
                     When ever a program is run an execution context is creaated along with it a windows object and a this keyword is also created that referes to global space variables.
                     and in function this referes to the object that is calling that function.

22)Call back?

                      When we pass a function inside another function we call and execute it inside that function that is called as call back funciton.

                                                            var a=7;
                                                            function x(y){
                                                             console.log("X CALLED");
                                                             y()
                                                            };
                                                            
                                                            function y(){
                                                                console.log("Y CALLED");
                                                             }
                                                            x(y);  

 23)What is garbage collection . Why do we need to free up memory , any idea?
                          
                           a) When ever a variable is out of execution Scope it gets eligble for garbage collection
                           b) There is stack memory which stores static data like method and functions and then there is heap memmory which stores the objects that are referencing to these functions
                              and methods and there is an algorithm that is used for garbage collection that is called as mark and sweep algorithm in that the progam start from the root global space and tries to                                    accumulate these objects to free up space.
 
 
 24) QUEUE Queues are based on the FIFO principle    
 25) STACK Stacks are based on LIFO principle.

26)Starvation?

              Startvation is phenomenon when the events in event quesue do not get the opportunitity to get executed because of the event is th emicro task queue which generally have higher priority.


27) What is the use of spread operator?

                            Spread operator is used to copy the preexisting values of an object!

                                          const arr=["FOOTBALL","BASKET BALL"];
                                          const copiedArr = [...arr, "TENIS"];
                                          console.log(copiedArr);
    
29)Rest Operator  Rest Operator is used to merge the arguements into an array 
                                               
                                                let arr = function(x,y,z){
                                                      return[x,y,z]
                                                  }
                                                 console.log(arr(5,6,7));

30)Iterating over an object?

                                                         var studentobj = {
                                                         'yash': 26,
                                                         'vaibhav': 24,
                                                         'rajesh' : 25,
                                                         }

                                                        for(const key in studentobj){
                                                          console.log(`${key} in ${studentobj[key]}`);
                                                        }
                                                        
31)Object question find average?


                                                                          var persons = {
                                                                            
                                                                                        age1: 26,
                                                                                        age2: 24,
                                                                                        age3:29
                                                                          }
                                                                          
                                                                          var len = Object.keys(persons).length;
                                                                          
                                                                          var values = Object.values(persons);
                                                                          var sum=0;
                                                                          for(var i=0;i<values.length;i++){
                                                                            sum+=values[i]  
                                                                          }
                                                                          
                                                                          var avg = sum/len; 
                                                                          console.log(avg);

32)                  

                                                                                    setTimeout(()=>{
                                                                                    console.log("a");
                                                                                    },2000)
                                                                                    console.log("b");

                                                                                 Print A first and B Later.
                 1st Approach  is by Callback
                 
                                                                                        function x(y){
                                                                                          setTimeout(()=>{
                                                                                            console.log("a");
                                                                                            y();
                                                                                          },2000)
                                                                                        }
                                                                                        
                                                                                        function y(){
                                                                                          console.log("b");
                                                                                        }
                                                                                        x(y);

                 2nd Approach is by Promises
                 
                                                                    const res = function printA(){
                                                                      return new Promise((res,rej)=>{
                                                                         setTimeout(()=>{
                                                                                res("a");
                                                                          },2000)
                                                                      })
                                                                    } 
                                                                    
                                                                    res().then((msg)=>{
                                                                      console.log(msg)
                                                                       console.log("b");
                                                                    })
33) What is Process.nextTick;
 Difference between SetImmidiate and Process.nexttick

                           SetImmidiate will execeture at the end of the event loop.
                           Process.nextTick() will execute at the start of event loop. 

                                                     process.nextTick(()=>{
                                                      console.log('hey');
                                                    })
                                                    
                                                    setTimeout(function() {
                                                      console.log("HELLO")
                                                    }, 10);
    
                                                  // hey
                                                  // HELLO
         
                                                        
35) how can you check if a variable is an array?

                                                     Array.isArray() is function that is used of the Array class
                                                        var arr=[5,6,9];                
                                                        console.log(Array.isArray(arr));
                                                        //true

36)Output Questions

                                                        SetImmidiate (()=>{
                                                            console.log("first")
                                                        })
                                                        SetTimeout (()=>{
                                                            console.log("second")
                                                        })
                                                            console.log("third");
                                         ANSWER>>   THIRD
                                                    SECOND
                                                    FIRST
                                                    
37)What is difference between promise and call back?

    A) Call back >>>    i) Call back is function that is passed inside another function called and executed inside that function,it is used to amke the async world behave more like sync world.
                ii) The repetative passing of functions inside one another, creates calllback hell which is difficult to read and maintain that is the reason why we have promises,
                    to avoid call back hell and to handle errors.
                
     B)Promise>   i)A promise is like a real world object it either gets resolved or it gets rejected or it goes into the pending state;
          ii)A promise is used to avoid the call back hell and to make async world behave more like a synchronous programming
          iii)Using then and catch block we can handle errors 
          iv)The promise in return creates a promises hell its like a pyramid structure of then and catch block which is difficult to read and maintain so for that we have async and await.

                                                const a = new Promise((res,rej)=>{
                                                  res("PRINT A");
                                                })
                                                
                                                a.then((msg)=>{
                                                  console.log(msg)
                                                }).catch((err)=>{
                                                        console.log(err)}
                                                // PRINT A      
38)Difference in Array map,filter and Reduce?

                                                                           A) FILTER
                                                                    var arr = [5,6,9,10];
                                                                    var res = arr.filter(checkAge)
                                                                    function checkAge(x){
                                                                      return x>5;
                                                                    }
                                                                    console.log(res) 
                                                                    output>> 6,9,10

                                                                            B)MAP
                                                                    var arr = [5,6,9,10];

                                                                    var res = arr.map((item,i)=>{
                                                                      console.log(item + "INDEX"+ i)
                                                                      return item+ i;
                                                                    })
                                                                    
                                                                    console.log(res)
                                                                    OUTPUT>>
                                                                    5INDEX0
                                                                    6INDEX1
                                                                    9INDEX2
                                                                    10INDEX3
                                                                    [ 5, 7, 11, 13 ]

                                                                        C)Reduce
                                                                    Array.reduce is used to reduce the elements of an array into a new array altogether.
                                                                    var res =var arr = [1,2,3,4];
                                                                        var res = arr.reduce((sum,end)=>{
                                                                          return sum+=end;
                                                                        },0)
                                                                        console.log(res)
                                                                        OUTPUT> 10
39)How to find the length of an object

                                                                        var obj={
                                                                            val:1,
                                                                        }
                                                                        Object.keys(obj).length
                                                                        
40)What is the temporal dead zone?

        The time period between when the variable is defined and alloted a memory as undeifned and the actual initialization of the value to that varaible during the code execution phase that is called as 
        temporal dead zone.
        
41)Write a function to generate random number between 10 and 99?
        
        const res = Math.floor(Math.random(10,99)*100);
        console.log(res)

42) Difference between null and undefined??

                                               NULL>>        Null means unavailable does not exist
                                               Undefined>>   Undefined means,A memoory was alloted to a varable while in memory execution phase but not the actual value.
                                               Undeclared>>   when you try to access a variable that is not in the scope that is undeclared.
43)     Difference between ‘==’ and’ ===’ ?
        == it compares just the values not the datatype
        === it compares both value as well as datatype , identicallly similar

        console.log(null === undefined) //false
        console.log(null == undefined)  //true
    
44) OUTPUT QUESTIONS
    
                                                    const fun = () => arguments.length;
                                                    console.log(fun(1,2));
                                                  //  OUTPUT 5 arguement is a global object with a lentgh of 5

45)let str=”JavaScript=Node=Express”;  replace “=” with “.”

                                                     console.log(str.replaceAll('=','.');

46) str=”India” to "aidnI"

                                                            let a= '';              
                                                            for(let i =str.length-1; i>=0;i--){
                                                                a += str.charAt(i);
                                                            }
                                                            console.log(a);

47)Write a function to check if the given number "n" exists in the array.
If present remove the number from the array , return the remaining array excluding the number else print element not present.
        
                                                        let arr=[7,8,9,10];
                                                        let res = arr.filter(function(dig){
                                                          return dig!=7;
                                                        })
                                                        console.log(res);
48) Array.find()
    
                                                                 let arr = [5,6,7]
                                                                 let res = arr.find(funciton(x) {
                                                                        return x>6;
                                                                    }
                                                                    console.log(res); //7
                 Here, the arr.find() method in JavaScript returns the value of the first element in the array that satisfies the provided testing method

49) OUYTPUT QUESTIONS

                                                                                async function fun1(){
                                                                                        console.log('a');
                                                                                        console.log('b');
                                                                                        await setTimeout(() => console.log('c'), 1000)
                                                                                        await setTimeout(() => console.log('d'), 0)
                                                                                        console.log('e');
                                                                                }
                                                                                fun1();
                                                               OUTPUT
                                                                a,b,e,d,c
                                               PRINTING IT IN RIGHT ORDER
   
                                                               async function fun1(){
                                                                                    console.log('a');
                                                                                    console.log('b');
                                                                                    const res3 = await printC();
                                                                                    console.log(res3)
                                                                                    const res4 = await printD();
                                                                                    console.log(res4)
                                                                                    console.log('e');
                                                                            }
                                                        
                                                                        function printC(){
                                                                          return new Promise((res,rej)=>{
                                                                            setTimeout(() =>  res('c'), 1000)
                                                                          })
                                                                        }
                                                                        
                                                                        function printD(){
                                                                          return new Promise((res,rej)=>{
                                                                            setTimeout(() =>  res('d'), 0)
                                                                          })
                                                                        } 
                                                                        fun1()


50) What are generator function in javascript ? How are they different from normal function?

                A generator function is used to pause and resume a program using next and yeild
 
                    function *generatorFunction(){
                          console.log('HEY');
                          yield 100;
      
                          console.log("HELLO THERE")
                          yield 200;
                        }
                        
                        const gen = generatorFunction();
                        gen.next();
                        gen.next();
    
51) What is an IIFE (Immediately Invoked function expression)? Can you give an example?
    
        when a funciton is defined and called right after its has been defined that is IIFE?

                                                                  (()=>{
                                                                        console.log("HELLO")
                                                                    }();

52) Explain the different ways of creating object in javascript? Explain all the 3 ways.

                    i) 1 way is by class and constructors
                                class Student{
                                        constructor(name){
                                            this.name=name;
                                        }
                                    }
                                    const obj1 = new Strudent("ILIYAS");

                    ii) 2nd way is my key value pairs?
                                const obj={
                                        age:1
                                    }
                
                    iii)3rd is by Object Prortype method
                                    const personProtoType = {
                                                    greet(){
                                                            console.log("HELLO")
                                                        }       
                                                 }
                                    const carl = Object.create(personProtoType)
                                            carl.greet()// HELLO
                            ProtoTypes are the mechanisms by which one object tries to inherit the properties of another object.
    
53)What is object chaining in javascript? Can you create functions to explain object chaining better?

                    Using output of function as an input to another is called as object chaining.

                                                    const obj = function(){
                                                     this.i=0;
                                                      this.add = function(i){
                                                         this.i+=i;
                                                         return this;
                                                      }  
                                                      this.subtract = function(i){
                                                         this.i-=i;
                                                         return this;
                                                      } 
                                                      this.print = function(){
                                                        return this.i;
                                                      }
                                                    }
                                                    
                                                    var x = new obj();
                                                    console.log(x.add(5).subtract(3).print())
                                                    //2
                                                                    
                                                           
54) What is the main difference between fat arrow function and normal function?

                                                                 const person ={
                                                                  constructor(n){
                                                                    this.name=n
                                                                  }
                                                                  
                                                                  regFunction(){
                                                                    setTimeout(function(){
                                                                      console.log(this.name)
                                                                    },1000);
                                                                  }
                                                                  
                                                                  arrowFunction(){
                                                                    setTimeout(()=>{
                                                                      console.log(this.name)
                                                                    },1000)
                                                                  }
                                                                }
                                                                
                                                                var obj = new person("ILIYAS");
                                                                obj.regFunction(); //undefined
                                                                obj.arrowFunction(); //ILIYAS


                                                                //OTHER APPROACH
                                                                    let person={
                                                                      name:"ILIYAS",
                                                                      af:()=>{
                                                                        console.log(this.name);
                                                                      },
                                                                      
                                                                      rf(){
                                                                        console.log(this.name);
                                                                      }
                                                                    }
                                                                    person.rf();
                                                                    person.af();
    
55)What are the advantages of Axios vs other competitors( like fetch, http, got etc)? Why is axios so widely used?

                        Axios has interceptors to modify request and responses and we dont have to explicitly convert the responses into json format it does it automatically as in fetch.
                        
                                    
56) What is NaN property in JavaScript?

                                                                        NAN means Not a Number it can be character String but not a number.
    
58) Explain pass by value and pass by reference? Give code example of how you would pass by reference in javascript?
    
                In pass by value the values that are passed inside the function hold new copy of values altogether they do not change the actual variables in the global scope.

                                                            var a=7;
                                                            var b=8;
                                                            
                                                            function passByValue(a,b){
                                                              let temp=a;
                                                              a=b;
                                                              b=temp;
                                                              
                                                              console.log(a +'<<<a & b is>>>'+b);
                                                            }
                                                            passByValue(a,b)
                                                            console.log("value of a and b" );
                                                            console.log(a,b)
    
            IN PASS BY REFERENCE WE actually pass the address of these variables and not the copy so any change insdie these function will change the actual values outside those function as well.

    59)What is memoization in javascript?

    Its a form of caching,
    Ability of function to remember the reference to the vairables/attributes is called as memoisation.

                                              function salutation() {
                                                let name = 'Aayush'
                                                    function greet() {
                                                        console.log(`Hello ${name}!`);
                                                    }
                                                    return greet;
                                                }
                                                let wish = salutation();
                                                wish();
    60) What is coercion ?
    
                                                        Implicit conversion of one data type to another is called as coercion.
                                                        const a = 'iliyas'+5;
                                                            OUTPUT>> iliyas5
    61)what is wrapper Object?
                                                                    let str='hello'
                                                                    str.toUpperCase()
                                                                    
                                                    whenever you try to access a property of a string str, JavaScript coerces the string value to an object,
                                                    by new String(str). This object is called a wrapper object.
                                                   // optional >> It inherits all string methods, and is used to resolve the property reference.
     
    














                                                        

                                                                    



 
