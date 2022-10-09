
***Problem : Xor Palindrome ***

// https://www.codechef.com/submit/XOR_PAL?tab=statement



```

#include <iostream>
using namespace std;

void solve(int left , int right , string str , int &count)
{
    while(left < right){
        if(str[left] != str[right]){
            count++;
        }
        
        left++;
        right--;
    }
    
    
    
}
int main() {
    
    int t;
    cin>>t;
    
    while(t--){
        int n;
        cin>>n;
        
        string str;
        cin>>str;
        
        int count=0;
        solve(0 , n-1 , str , count);
        
        cout<<(count+1)/2<<endl;
        
    }
	return 0;
}


```




***Here Below , ScreenShot of my Submission***
