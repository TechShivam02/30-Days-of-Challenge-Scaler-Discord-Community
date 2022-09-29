
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


![day1](https://user-images.githubusercontent.com/109462762/193086678-b963af49-7cd5-4d30-91a5-7c74cea49a50.jpg)