
***Problem : Reversing the equation***

// Problem Link : https://lnkd.in/dMw3WAbg

``` string reverseEqn (string str)
        {
            int n=str.length();
            
            stack<string> stk;
            string temp="";
            
            
            for(int i=0;i<str.length();i++){
                
                if(str[i] == '+' || str[i] == '-' || str[i] == '*' ||  str[i] == '/'  ){
                    
                    stk.push(temp);
                    temp="";
                    
                        string m ="";
                        char ch = str[i];
                        
                        m+=ch;
                        
                       stk.push(m);
                
                }
                    
                else{
                    temp+=str[i];
                    
                }
                
            }
            
            if(temp.length() >0){
                stk.push(temp);
            }
            
            
            string final="";
            
            while(!stk.empty()){
                final += stk.top();
                stk.pop();
            }
            
            
            return final;
            
            
               
        }

```




***Here Below , ScreenShot of my Submission***
![day22](https://user-images.githubusercontent.com/109462762/196200214-0acd7ea2-8c7a-4e9e-8943-4453ed6554a5.jpg)

