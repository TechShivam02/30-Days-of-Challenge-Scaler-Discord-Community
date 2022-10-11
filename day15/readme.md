
***Problem : Strong-Password ***

// https://www.hackerrank.com/challenges/strong-password/problem?isFullScreen=true



```

bool isSpeacialDigit(char ch){
    
    if( ch == '!' || ch == '@' || ch == '#' || ch == '$' || ch == '%' || ch == '^'
        ||  ch == '&' || ch == '*' || ch == '(' || ch == ')' ||  ch == '-' 
        ||  ch == '+' )
    
    {
        return true;
    }
    
    return false;
    
}


int minimumNumber(int n, string str) {
 
    bool isnum = false;
    
    bool issmall = false;
    bool islarge = false;
    
    bool isspecial = false;
    
    
    for(int i=0;i<str.length();i++){
        
        if(str[i] >='a' && str[i] <='z'){
            issmall = true;
        }
        
        else if(str[i] >='A' && str[i] <='Z'){
            islarge = true;
        }
        
        else if(isSpeacialDigit(str[i])){
            isspecial = true;
        }
        
        else{
            isnum = true;
        }
        
    }
    
    
    int count=0;
    
    if(!issmall){
        count++;
    }
    
    if(!islarge){
        count++;
    }
    
    if(!isspecial){
        count++;
    }
    
    if(!isnum){
        count++;
    }
    
    if(count + n >=6){
        return count;
    }
    
    return  6-n;
    
}



```




***Here Below , ScreenShot of my Submission***
![day15](https://user-images.githubusercontent.com/109462762/195154920-cde5c80e-c6ae-4190-9998-93c39940ca65.jpg)


