
***Problem : 4. Median of Two Sorted Arrays***

// Problem Link : https://leetcode.com/problems/median-of-two-sorted-arrays/

```class Solution {
public:
    double findMedianSortedArrays(vector<int>& vec1, vector<int>& vec2) {
        
    int m=vec1.size();
    int n=vec2.size();
    
    vector<int> ans;
    
        int i=0;
        int j=0;

        while(i<m && j<n){
            if(vec1[i] < vec2[j]){
                ans.push_back(vec1[i]);
                i++;
            }

            else{
                ans.push_back(vec2[j]);
                j++;
            }
        }

        while(i<m){
                ans.push_back(vec1[i]);
                i++;
            
        }

        while(j<n){
                ans.push_back(vec2[j]);
                j++;
        }





    int st=0;
    int end=ans.size()-1;


    int first;
    int second;

    while(st<=end){

        first=ans[st];
        second=ans[end];
        
        st++;
        end--;

    }


    double ansReturn = double(first+second)/2;

    return ansReturn;





        
    }
};

```


***Here Below , ScreenShot of my Submission***

