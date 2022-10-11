
***Problem : Print Anagrams Together ***

// https://practice.geeksforgeeks.org/problems/print-anagrams-together/1?page=1&difficulty[]=1&category[]=Strings&sortBy=difficulty



```
vector<vector<string> > Anagrams(vector<string>& vec) {
    
        vector< vector<string> > ans;
        map< string , vector<string > > mp;
        
        
        int n = vec.size();
        
        for(int i=0;i<n;i++){
            
            string str = vec[i];
            sort(str.begin() , str.end());
            mp[str].push_back(vec[i]);
            
        }
        
        map< string , vector<string>  > :: iterator itr;
        
    
        for (itr = mp.begin(); itr != mp.end(); ++itr) {
           ans.push_back(itr->second);
        }
    
    
      return ans;
    
        
    }


```




***Here Below , ScreenShot of my Submission***
