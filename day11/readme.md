
***Problem : Power Of Numbers ***

// Problem Link : https://practice.geeksforgeeks.org/problems/power-of-numbers-1587115620/1?page=1&difficulty[]=0&category[]=Divide%20and%20Conquer&sortBy=accuracy

```

long long power(int N , int R)
    {

       if(R==1)

            return N;



        long long ans = power(N,R/2);

        if(R%2==0){   

            return (( ans%1000000007 * ans)%1000000007)%1000000007;
            
        }

        else{
            
        return ( N %1000000007 *  (( ans%1000000007 * ans)%1000000007)%1000000007 );
      
       }
       
       
        
    }



```




***Here Below , ScreenShot of my Submission***
