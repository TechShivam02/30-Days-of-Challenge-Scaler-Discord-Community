
***Problem : 1255. Maximum Score Words Formed by Letters***

// https://leetcode.com/problems/maximum-score-words-formed-by-letters/



```
int maxScoreWords(vector<string>& words, vector<char>& letters, vector<int>& score) {
        vector<int> vec(26,0);
        
        for(auto i : letters){
            vec[i-'a']++;
        }
        
        int ans=0;
        int n=words.size();
        
        for(int i=1;i<(1<<n);i++){
            vector<int> cap(26,0);
            
            for(int j=0;j<(int)words.size();j++){
                
                if( (1 << j) & i ){
                    for(int k=0;k<(int)words[j].size();k++){
                        cap[words[j][k] - 'a']++;
                    }
                }
                
            }
            
            bool flag = true;
            
            for(int j=0;j<26;j++){
                if(cap[j] > vec[j]){
                    flag = false;   
                }
            }
            
            if(flag){
                int total = 0;
                
                for(int j=0;j<26;j++){
                    total += cap[j]*score[j];
                }
                
                ans = max(ans,total);
                
            }
        }
        
        
        return ans;
        
        
    }

```




***Here Below , ScreenShot of my Submission***

![day17](https://user-images.githubusercontent.com/109462762/195438312-21b4de15-6a3c-42f9-aaac-884d8de056c1.jpg)

