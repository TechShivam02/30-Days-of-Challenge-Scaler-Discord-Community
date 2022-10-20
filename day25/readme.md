
***Problem : 132-pattern ***

// Problem Link :https://leetcode.com/problems/132-pattern/

```  bool find132pattern(vector<int>& nums) {
        
        
        int m = INT_MIN;
        
        stack<int> st;
        
        for( int i = nums.size()-1; i >= 0; i -- ){
            
            if( nums[i] < m ) return true;
            
            else {
                
                while( !st.empty() && nums[i] > st.top() ){ 
                    m = st.top();
                    st.pop(); 
                }
                
                
                st.push(nums[i]);
                
            }
            
        }
        
        
        return false;
        
        
    }

```




***Here Below , ScreenShot of my Submission***
