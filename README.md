FIND MINIMUM IN AN ARRAY
                 
                                        console.log("FIND Minimum in an array");
                                        
                                        //find min in array
                                        var arr=[5, 4, 7, 2, 6]
                                        
                                        
                                        for(var i=0;i<arr.length-1;i++){
                                          var min=arr[i];
                                          var swap=0;
                                          
                                          if(min<arr[i+1]){
                                            swap=arr[i+1];
                                            arr[i+1]=arr[i];
                                            arr[i]=swap;
                                          }else{
                                            min=arr[i+1]
                                          }
                                          
                                        }

                                              console.log(min)

FIND MAX IN AN ARRAY:

                                      //find max in array
                                      var arr=[5, 4, 7, 2, 6]
                                      
                                      for(var i=0;i<arr.length-1;i++){
                                        var max = arr[i];
                                        var swap=0;
                                        if(max>arr[i+1]){
                                          swap = arr[i+1];
                                          arr[i+1]=arr[i];
                                          arr[i]=swap;
                                        }else{
                                          max =arr[i+1];
                                        }
                                      }
                                      console.log(max)

"STORE PRIME NUMBERS IN AN ARRAY";

                                    //store prime no.s in  ARRAY
                                            var arr=[];
                                            var n=5;
                                            var counter=0;
                                            var x=2;
                                            while(counter<n){
                                              var flag=true;
                                              
                                              for(i=2;i<x;i++){
                                                if((x%i)==0){
                                                  flag=false;
                                                  break
                                                }
                                                
                                              }
                                              if(flag){
                                                arr[counter]=i;
                                                counter++;
                                              }
                                              x++;
                                              
                                            }
                    
                                console.log(arr)

CALCUALTE THE SUM OF PRIME NUMBER IN THE ARRAY
                                                
                                                  
                                                  var arr = [1,2,3,5,7,91,8];
                                                  var sum=0;
                                                  for(var i=0;i<arr.length;i++){
                                                    if(arr[i]>1){
                                                      var flag =true
                                                    }
                                                    
                                                    for(var j=2;j<i;j++){
                                                      if(arr[i]%j ==0){
                                                        flag=false;
                                                        break;
                                                      }
                                                    }
                                                    
                                                    if(flag){
                                                      console.log(arr[i])
                                                      sum+=arr[i]
                                                    }
                                                  }
                                                  
                                                  console.log(sum)
SUB ARRAY

                                                          console.log("SUB ARRAYS");
                                                          
                                                          var arr = [1,2,3,4,5]
                                                          
                                                          for(var i=0;i<arr.length;i++){
                                                            for(var j=i;j<arr.length;j++){
                                                              var str='';
                                                              for(var k=i;k<=j;k++){
                                                                  str+=arr[k]
                                                                  console.log(str)
                                                              }
                                                              console.log(' ')
                                                            }
                                                          }

//MAX SUM IN SUBSARRAY

                                                var arr = [5,2,-4,-5, 3,-1,2,3,1]
                                                var max=0;
                                                for(var i=0;i<arr.length;i++){
                                                  for(var j=i;j<arr.length;j++){
                                                    var sum=0;
                                                    for(var k=i;k<=j;k++){
                                                        sum+=arr[k]
                                                        //
                                                    }
                                                    if(sum>max){
                                                      max=sum;
                                                    }
                                                  }
                                                }
                                                console.log(max)
RUNNING SUM 

                                                          //RUNNING SUM in
                                                          
                                                          var arr = [1,2,3,4];
                                                          var num=[];//anotehr array to store the running sum;
                                                          for(var i=0;i<arr.length;i++){
                                                            var sum=0;
                                                            for(var j=0;j<=i;j++){
                                                              sum+=arr[j]
                                                            }
                                                            num[i]=sum;
                                                          }
                                                          console.log(num)
Insertion sort

                                        
                                     
                                                    var arr = [1,4,5,6,9,10];
                                                         //     j=1 temp=4 because array starts with 1 element
                                                    for(var i=1;i<arr.length;i++){
                                                      var j=i-1;
                                                      var temp=arr[i];
                                                      while(j>=0 && temp<arr[j]){
                                                        var swap = arr[j+1];
                                                        arr[j+1]=arr[j];
                                                        arr[j]=swap;
                                                        j--;
                                                      }  
                                                      arr[j+1]=temp;
                                                      
                                                    }
                                                    
                                                    console.log(arr)

Selection Sort


                                                        var arr=[1,2,4,3,6];
                                                for(var i=0;i<arr.length-1;i++){
                                                  var temp = arr[i];
                                                  var index=i
                                                  for(var j=i+1;j<arr.length;j++){
                                                    if(temp<arr[j]){
                                                      temp=arr[j];
                                                      index=j;
                                                    }
                                                  }
                                                  var swap=arr[i];
                                                  arr[i]=arr[index];
                                                  arr[index]=swap;
                                                }
                                                
                                                console.log(arr)

Bubble Sort

                                var ar=[5,9,3,4,]
                                        for(var i=0;i<arr.length-1;i++){
                                          for(var j=0;j<arr.length-1;j++){
                                                var max = arr[j];
                                                if(max<arr[j+1]){
                                                  var swap = arr[j+1]
                                                  arr[j+1]=arr[j];
                                                  arr[j]=swap
                                                }else{
                                                  max = arr[j+1];
                                                }   
                                              }
                                        }
                                            console.log(arr)


SUM OF ODD LENGTH SUB ARRAYS

                                           for(int i=0;i<arr.length;i++)
                                           {
                                               for(int j=i;j<arr.length;j++)
                                               {
                                                   
                                                   for(int k=i;k<=j;k++)
                                                   {
                                                       if((j-i+1)%2!=0){
                                                       sum =sum + arr[k];
                                                       }
                                                   }
                                               }
                                               
                                           }
                                                return sum;
                                                    
                                        }
                                }

MAX SUM IN 2D array
                                    
                                    var accounts = [[1,2,3],[5,6,9]];
                                    var max=0;
                                    for(var i=0;i<accounts.length;i++){
                                      var sum=0;
                                      for(var j=0;j<accounts[i].length;j++){
                                        sum=sum+accounts[i][j];
                                      }
                                      if(sum>max){
                                        max=sum;
                                      }
                                    }
                                    
                                    console.log(max)

