
***Problem : Killing Spree ***

// Problem Link : https://practice.geeksforgeeks.org/problems/killing-spree3020/1?page=1&difficulty[]=1&category[]=Divide%20and%20Conquer&sortBy=accuracy


```
long long int killinSpree(long long int n)
    
    {
    
        long long count=0;
        long long str=n;
        
            
            for(long long i=1;i<=n;i++){
                
                long long curr = i*i;
                
                if(str >= curr){
                    
                    str = str-curr;
                    count++;
                
                }
                
                else{
                    break;
                }
                
                
            }
            
         return count;
    
    }

```




***Here Below , ScreenShot of my Submission***

![day12](https://user-images.githubusercontent.com/109462762/194562604-81ff2dba-5712-4a40-9ce4-b02e8a771c3a.jpg)
