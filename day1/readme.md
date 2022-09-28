
***Problem : 1920. Build Array from Permutation ***

// Problem Link : https://leetcode.com/problems/build-array-from-permutation/

```class Solution {
public:
    
    vector<int> buildArray(vector<int>& nums) {
        
        
        vector<int> vec(nums.size());
        
        for(int i=0;i<nums.size();i++){
            vec[i] = nums[nums[i]];
        }
        
        return vec;
        
    }
};

```


***Here Below , ScreenShot of my Submission***

