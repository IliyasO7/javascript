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



Count the maximum words 

                                          var sentences = ["alice and bob love leetcode", "i think so too", "this is great thanks very much"]
                                          var maxCount = 0;
                                          for(var i=0;i<sentences.length;i++){
                                            var count=1;
                                            for(var j=0;j<sentences[i].length;j++){
                                              if(sentences[i][j] == ' '){
                                                count++;
                                              }
                                            }
                                            if(count>maxCount){
                                              maxCount=count;
                                            }
                                          }
                                          console.log(maxCount)

"TIME COMPLETXITY"
1)

                                                var a=0
                                                for(var i=0;i<N;i++){
                                                  for(var j=N;j>i;j--){
                                                    a+=j;
                                                  }
                                                }
                                                
                                                What will be the time Complexity - Choose the correct Option
                                                
                                                O(N*N)
                                                
                                                A) O(N^2)  <<<<<<<<<<
                                                
                                                B) O(N)
                                                
                                                C) O(N Log N)
                                                
                                                D) O(Log N)
2)

                                                            var a=0
                                                           for(var i=n/2;i<=n;i++){
                                                             for(var j=2;j>i;j=j*2){
                                                                      a+=j;
                                                                      }
                                                                  }  
                                                               O(nlogn)
                                              What will be the time Complexity - Choose the correct Options
              
                                                                          A) O(N^2)
                                                                          B) O(N)
                                                                          C) O(N Log N)
                                                                          D) O(Log N)

3)   

                                              f1(n) = 2^n
                                              f2(n) = n^(3/2)
                                              f3(n) = nLogn
                                              f4(n) = n^(Logn)
     
                                           f3,f2,f1,f4 increasing order



   BINARY SEARCH
TIME COMPLETXITY : O(log n)
Best case  O (1)

Given an array of integers nums which is sorted in ascending order, and an integer target, write a function to search target in nums. If target exists, then return its index. Otherwise, return -1.
You must write an algorithm with O(log n) runtime complexity.

      i)                                 nums = [-1,0,3,5,9,12], target = 9
 
                                       var search = function(nums, target) {
                                          var l=0;
                                          var h=nums.length-1;
                                      
                                          while(l<h){
                                              var mid = Math.floor((l+h)/2); // important
                                              if(target == nums[mid]){
                                                  return mid;
                                              }
                                      
                                              if(target < nums[mid]){
                                                  h=mid-1;
                                              }else{
                                                  l=mid+1;
                                              }
                                          }
                                          return -1;    
                                      };
      ii)

      A peak element is an element that is strictly greater than its neighbors.
                        Given a 0-indexed integer array nums, find a peak element, and return its index. If the array contains multiple peaks, return the index to any of the peaks.
                        You may imagine that nums[-1] = nums[n] = -∞. In other words, an element is always considered to be strictly greater than a neighbor that is outside the array.
                        You must write an algorithm that runs in O(log n) time
                        Example 1
                        Input: nums = [1,2,3,1]
                        Output: 2
                        Explanation: 3 is a peak element and your function should return the index number 2.


                        //Find The Peak Element
                              var nums = [1,2,3,1]
                              var l=0;
                              var h=nums.length-1; 
                              while(l<h){
                                var mid = Math.floor((l+h)/2);
                                if(nums[mid]>nums[mid+1]){
                                  h=mid
                                }else{
                                  l=mid+1;
                                }
                              }
                              console.log(nums[l])
iii)   Search in Rotated Sorted Array

          First check if the peft array is sorted then try to find the target in the left sorted array adn then in the right note
          while(l<=h) >>> nums[l]<=nums[mid]
        
                          var search = function(nums, target) {
                          var l=0;
                          var h=nums.length-1;
                            while(l<=h){
                                var mid = Math.floor((l+h)/2);
                                if(target == nums[mid]){
                                    return mid;
                                }
                                if(nums[l] <= nums[mid]){
                                    //left array is sroted
                                    if(nums[l] <= target && target < nums[mid]){
                                        h=mid-1;
                                    }else{
                                        l=mid+1;
                                    }
                                }else{
                                    if(target <= nums[h] && target>nums[mid] ){
                                        l=mid+1;
                                    }else{
                                        h=mid+1;
                                    }
                                }
                            }
                            return -1;      
                        };

TWO SUM 
Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
You may assume that each input would have exactly one solution, and you may not use the same element twice.
You can return the answer in any order.
Example 1:
Input: nums = [2,7,11,15], target = 9
Output: [0,1]

Explanation: Because nums[0] + nums[1] == 9, we return [0, 1].

                              var twoSum = function(nums, target) {
                                  let map = new Map();
                                  let arr=[];
                              
                                  for(var i=0;i<nums.length;i++){
                              
                                      if(map.has(target-nums[i])){
                                          arr[0]=i;
                                          arr[1]= map.get(target-nums[i])
                                          return arr;
                                      }else{
                                          map.set(nums[i],i)
                                      }
                                  }
                              
                                  
                              };


HASHMAP :                        
LUCKY INTEGER IN AN ARRAY
  
                                              var findLucky = function(arr) {
                                            
                                                let map = new Map();
                                            
                                                for(var i=0;i<arr.length;i++){
                                                    if(map.has(arr[i])){
                                                        map.set(arr[i], map.get(arr[i])+1 )
                                                    }else{
                                                        map.set(arr[i],1)
                                                    }
                                                }
                                                let maxKey=-1;
                                                for(var j=0;j<arr.length;j++){
                                                    if(arr[j] === map.get(arr[j]) && maxKey <map.get(arr[j])){
                                                        maxKey=arr[j]
                                                    }
                                                }
                                                return maxKey;
                                            
                                                
                                            };

JEWELS AND STONES:

You're given strings jewels representing the types of stones that are jewels, and stones representing the stones you have. Each character in stones is a type of stone you have. You want to know how many of the stones you have are also jewels.
Letters are case sensitive, so "a" is considered a different type of stone from "A".
Example 1:

Input: jewels = "aA", stones = "aAAbbbb"

Output: 3
                                                  
                                                  var jewels = "aA";
                                                  var stones = "aAAbbbb";
                                                  
                                                  let map = new Map();
                                                  
                                                  for(var i=0;i<jewels.length;i++){
                                                      map.set(jewels.charAt(i),i)
                                                  }
                                                  
                                                  var count=0;
                                                  for(var j=0;j<stones.length;j++){
                                                    if(map.has(stones.charAt(j))){
                                                      count++;
                                                    }
                                                  }
                                                  console.log(count)




STACKS:


    MIN STACKS

    class MinStack {  
      Stack<Integer> stack = new Stack<>();
      Stack<Integer> min_value = new Stack<>();    
  
       /* public MinStack() {
          
          
      }
    */
    
    public void push(int val) {
        if(min_value.isEmpty() || val<= min_value.peek())
        {
            min_value.push(val);
        }
        
        stack.push(val);
    }
    
    public void pop() {
        
        if(stack.peek().equals(min_value.peek()))
        {
            min_value.pop();
        }
        
        stack.pop();
    }
    
    public int top() {
        return stack.peek();
    }
    
    public int getMin() {
        return min_value.peek();
    }
}

Valid parenthesis:

    Stack<Character> st = new Stack<>();
        for(int i=0;i<s.length();i++)
        {
            if(s.charAt(i) == '('|| s.charAt(i) == '{' || s.charAt(i) == '[')
            {
                st.push(s.charAt(i));
            }
            else if (!st.isEmpty() && s.charAt(i) == ')' && st.peek().equals('('))
            {
                st.pop();
            }
            else if (!st.isEmpty() && s.charAt(i) == '}' && st.peek().equals('{'))
            {
                st.pop();
            }
            else if (!st.isEmpty() && s.charAt(i) == ']' && st.peek().equals('['))
            {
                st.pop();
            }
            else 
                return false;
        }
        if(st.isEmpty())
        {
            return true;
        }
        else 
            return false;
    }
}


Validate Stack Sequence:

            int j=0;
                  int n = pushed.length;
                  Stack<Integer> st = new Stack();
                for(int i=0;i<n;i++)
                {
                    st.push(pushed[i]);
                    while(!st.isEmpty() && st.peek()==popped[j])
                    {
                        st.pop();
                        ++j;
                    }
                }
                return j==n;
            }
      }
                  
