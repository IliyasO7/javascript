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
  Block Scope : Two curly braces encoles together is a block scope.
                      { }
     Shadowing:
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
    
 11) Currying ?
Currying is a concept of using one function to create more function out of it for example.

     let multiply = function(x,y){
         return console.log(x*y);
       }

     let multiplyByTwo = multiply.bind(this,2);
     multiplyByTwo(3);

 This is what currying is using one function to create more functions out of it.

 
 
  

    
                    

            
  

         
         
      
      



 
