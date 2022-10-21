
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

![day26](https://user-images.githubusercontent.com/109462762/197229183-27453270-6841-4e44-bd01-3dd00a566bd8.jpg)

