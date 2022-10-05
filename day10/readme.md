
***Problem : 2033. Minimum Operations to Make a Uni-Value Grid ***

// Problem Link : https://leetcode.com/problems/minimum-operations-to-make-a-uni-value-grid/

```


class Solution {
    
public:
    
    
    int minOperations(vector<vector<int>>& grid, int x) {
        
        vector<int> vec;
        
        for(int i=0; i<grid.size(); i++) {
            for(int j=0; j<grid[0].size(); j++){
                vec.push_back(grid[i][j]);
            }
        }
        
        sort(vec.begin(), vec.end());
        
        
        int k = vec[vec.size() / 2];
        int ans = 0;

        for(int i : vec) {
            
            if(abs(i - k) % x) {
                return -1;
            }
            
            ans += abs(i - k);
        }
        
        return ans / x;
    }
    
};


```




***Here Below , ScreenShot of my Submission***
![day10](https://user-images.githubusercontent.com/109462762/194116898-73723e02-5845-4a9a-b4ab-4c8ec218b39c.jpg)
