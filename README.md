# javascript
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
                                                                          









 
 
  

    
                    

            
  

         
         
      
      



 
