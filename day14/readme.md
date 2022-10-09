
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

![day14](https://user-images.githubusercontent.com/109462762/194757418-29e1b597-57d1-4df0-8975-e1f6f69c68e8.jpg)

