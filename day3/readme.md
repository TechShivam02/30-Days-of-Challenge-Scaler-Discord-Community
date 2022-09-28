
***Problem : 1828. Queries on Number of Points Inside a Circle***

// Problem Link : https://leetcode.com/problems/queries-on-number-of-points-inside-a-circle/

```

#include<cmath>
class Solution {
public:
    vector<int> countPoints(vector<vector<int>>& points, vector<vector<int>>& queries) {
        
        vector<int> vec;
      
        
        for(int i=0;i<queries.size() ;i++){
            
            
            int oldlow = queries[i][0];
            int oldhigh = queries[i][1];
            
            int rad = queries[i][2];
            
            int count=0;
            
            for(int j=0;j<points.size() ; j++){
                
                int newlow  = points[j][0];
                int newhigh = points[j][1];
                
                
  double dist = sqrt( ( (newlow - oldlow)*(newlow - oldlow) )   +  ( (newhigh - oldhigh)*(newhigh - oldhigh)) );
                
                if(dist <= rad){
                    count++;
                }
                
            }
            
            
            vec.push_back(count);
            
        }
        
        return vec;
    }
};
```


***Here Below , ScreenShot of my Submission***


![day3](https://user-images.githubusercontent.com/109462762/192811981-e54711cc-3fda-4197-b643-ed5179740cf7.jpg)
