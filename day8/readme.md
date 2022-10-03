
***Problem : Big Sorting (Hacker Rank) ***

// Problem Link : https://www.hackerrank.com/challenges/big-sorting/problem

```

bool compare(string str1 , string str2){
    
    if(str1.length() != str2.length()){
        
        return str1.size() < str2.size();
       
    }
    
    else{
        return str1<str2;
    }
}


vector<string> bigSorting(vector<string> vec) {

    sort(vec.begin(),vec.end() , compare);
    
    return vec;
    
}
```


