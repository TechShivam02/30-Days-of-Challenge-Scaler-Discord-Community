
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
