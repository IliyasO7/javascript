#OOPS

 OBJECT ORIENTED PORGRAMMING is a programming technique that revolves around 
 4 pillars of oops like inheritance,encapsualtion , abstraction and polymorphism
 which lets you create the object that you want to create and the methods to handle
 those object.


  Inheritance: 
                       
                       Inheritance is the property of one class to inherit the property of another class

                       //Inheritance

                            class Car{
                              constructor(name,model){
                                this.name=name;
                                this.model=model
                              }
                              
                              getInfo(){
                                return console.log(this.name + " is the  name and the model is "+ this.model);
                              }
                            }
                            
                            class Model extends Car{
                              constructor(name,model){
                                super(name);
                                this.model=model
                              }
                            }
                            
                            
                            let my_car = new Model("BWM","MODEL1");
                            my_car.getInfo()
    
Encapulation: 

                                                Encapsulation is binding the data with functions

                                        class person{
                                          name 
                                          
                                          setName(name){
                                            this.name=name
                                          }
                                          
                                          getName(){
                                            return console.log(this.name)
                                          }
                                        }
                                        
                                        
                                        var p1 = new person();
                                        p1.setName("ILIYAS");
                                        p1.getName()

Polymorphism :
                                     
                                     Polymorphism means ability to have more than one form is polymorphism
                                     
                                     class First{
                                     add(){
                                         console.log("ADDING")
                                         }
                                    }

                                    class Second{
                                        add(x,y){
                                            console.log(x+y)
                                            }
                                        }

                                    var f1 = new First()
                                    var s1 =new Second()
                                    f1.add()
                                    s1.add(5,6)

ABSTRACTION 
                                    
                                    Abstraction is hiding the detaills

                            class Person{
                                constructor(fn,ln){
                                    this.firstname=fn;
                                    this.lastname=ln
                                    }

                                    getDetails(){
                                        console.log(this.firstname,this.lastname)
                                    }
                                }
                                    
                                         
    
    
