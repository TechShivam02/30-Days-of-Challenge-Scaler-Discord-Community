
***Problem : 1512. Number of Good Pairs  ***

// Problem Link : https://leetcode.com/problems/number-of-good-pairs/

```  int numIdenticalPairs(vector<int>& vec) {
        
        
        int n=vec.size();
        
        
        int count=0;
        
        for(int i=0;i<vec.size();i++){
        
            for(int j=i+1;j<n;j++){
            
                if(vec[i] == vec[j]){
                    count++;
                }
                
            }
            
            
        }
        
        
        return count;
        
        
    }

```




***Here Below , ScreenShot of my Submission***

