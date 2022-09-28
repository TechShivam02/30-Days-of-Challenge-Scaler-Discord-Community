
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

![day1](https://user-images.githubusercontent.com/109462762/192814846-a91d58be-f2cd-4ea3-93eb-9bfd208d6320.jpg)
