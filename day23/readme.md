
***Problem : 20. Valid Parentheses ***

// Problem Link : https://leetcode.com/problems/valid-parentheses/

``` 
class Solution {
public:
    
    
    char giveOpp(char ch){
        if(ch == ')'){
            return '(';
        }
        
        else if(ch == ']'){
            return '[';
        }
        return '{';
    }
    
    
    bool isValid(string str) {
        
        
        stack<char> stk;
        
        for(int i=0;i<str.length();i++){
        
                if(str[i] == '(' || str[i] == '{' || str[i] == '[' ){
                    stk.push(str[i]);
                }
            
                else{
                    
                    char ch = giveOpp(str[i]);
                    
                    if(!stk.empty() && stk.top() == ch){
                        stk.pop();
                    }
                    
                    else{
                        stk.push(str[i]);
                    }
                    
                }
            
        }
        
        if(stk.empty()){
            return true;
        }
        
        return false;
        
    }
};

```




***Here Below , ScreenShot of my Submission***
