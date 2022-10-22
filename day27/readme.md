
***Problem : 1346. Check If N and Its Double Exist  ***

// Problem Link :  https://lnkd.in/dDNTaGnP

```  

    bool checkIfExist(vector<int>& vec) {
        
        int n = vec.size();
        
        
        for(int i=0;i<n;i++){
            
            for(int j=0;j<n;j++){
        
                    if(i != j && vec[i] == 2*vec[j]){
                        return true;
                    }
                
            }
        }
        
        
        return false;
        
        
        
    }
```




***Here Below , ScreenShot of my Submission***

![day27](https://user-images.githubusercontent.com/109462762/197340168-6d97c21d-6cfb-4d03-9164-e10087290408.jpg)
