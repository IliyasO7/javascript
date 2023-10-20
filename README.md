Insertion sort

                                        
                                        var arr=[1,2,4,3,6];
                                        for(let i=1;i<arr.length;i++){
                                          var j=i-1;
                                          var temp=arr[i];
                                                              
                                          while(j>=0 && temp<arr[j]){
                                            temp = arr[j+1];
                                            arr[j+1]=arr[j];
                                            arr[j]=temp;
                                            j=j-1;
                                            
                                          }
                                          arr[j+1]=temp
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

