***Problem : 1502. Can Make Arithmetic Progression From Sequence ***

// Problem Link :https://leetcode.com/problems/can-make-arithmetic-progression-from-sequence/

```
class Solution {
public:
    bool canMakeArithmeticProgression(vector<int>& vec) {
        
        
        sort(vec.begin() , vec.end());
        
        int diff;
        
        if(vec.size() >=2){
            diff = vec[1]-vec[0];
        }
        
        for(int i=1;i<vec.size()-1 ;i++){
            
            int newDiff  = vec[i+1] - vec[i];
            
            if(newDiff != diff)
            {
                return false;
            }            
            
            
        }
        
        return true;
    }
};

```


***Here Below , ScreenShot of my Submission***

![day2](https://user-images.githubusercontent.com/109462762/192814997-50ba40fa-1cb8-4308-bb7e-44da1eec18ff.jpg)

