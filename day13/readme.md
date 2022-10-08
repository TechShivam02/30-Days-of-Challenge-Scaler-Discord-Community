
***Problem : Binary Matrix with at most K 1s***

// https://practice.geeksforgeeks.org/problems/largest-square-in-a-binary-matrix-with-at-most-k-1s-for-multiple-queries/1?page=1&difficulty[]=1&category[]=Divide%20and%20Conquer&sortBy=difficulty


```

vector<int> largestSquare(vector<vector<int>> matt, int r, int c, int K, int Q, int q_i[], int q_j[]) {
    
        int dp[r][c];
        
        memset(dp , 0 , sizeof(dp));
        
        
        dp[0][0] = matt[0][0];
        
        
    
        for(int i=1;i<r;i++){
            dp[i][0] = dp[i-1][0] + matt[i][0];
        }
        
        
        for(int i=1;i<c;i++){
            dp[0][i] = dp[0][i-1] + matt[0][i];
        }
         
        
        for(int i=1;i<r;i++){
            
            for(int j =1;j<c;j++){
            
                dp[i][j] = matt[i][j] + dp[i-1][j] +  dp[i][j-1] - dp[i-1][j-1];
                
            }
        }
        
        
        vector<int> ansVec;
        
        
        for(int i=0;i<Q;i++){
            
            int m = q_i[i];
            int n = q_j[i];
            
            
            int minDist = min(min(m,n) , min(r-m-1 , c-n-1));
            
            
            int l=0;
            int r=minDist;
            
            int ans=-1;
            
            while(l <=r){
                
                int mid = (l+r)/2;
                
                    int fir1 = m-mid;
                    int fir2 = m+mid;
                    
                    int sec1 = n-mid;
                    int sec2 = n+mid;
                    
                
                int count = dp[fir2][sec2];
                
                if(fir1 > 0){
                    count -= dp[fir1-1][sec2];
                }
                
                if(sec1 > 0){
                    count -= dp[fir2][sec1-1];
                }
                
                if(fir1 > 0 && sec1 > 0){
                    count += dp[fir1-1][sec1-1];
                }
                
                
                
                
                if(count <= K){
                    ans = 2*mid+1;
                    l = mid+1;
                }
                
                else{
                    r=mid-1;
                }
            }
            
            
            if(ans == -1){
                ans=0;
            
            }
            
             
             ansVec.push_back(ans);
            
          
            
        }
        
        
        return ansVec;
        
        
        
    }

```




***Here Below , ScreenShot of my Submission***

![day13](https://user-images.githubusercontent.com/109462762/194721039-29e6dd28-e3eb-4531-82e3-0bea1f079a06.jpg)
