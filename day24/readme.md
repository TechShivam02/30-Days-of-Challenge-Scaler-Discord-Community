
***Problem : Simple-text-editor***

// Problem Link : https://www.hackerrank.com/challenges/simple-text-editor/problem?isFullScreen=true

``` 
int main() {
    string str = "";
    
    int opr;
    cin >> opr;
    
    vector<string> vec;
    
    for(int i = 0; i < opr; i++){
        
        string s, ss;
        
        cin >> s; 
        
        if(s != "4") cin >> ss;
        
        if(s == "1"){
            vec.push_back(str);
            str += ss;
        }
        else if( s == "2"){
            vec.push_back(str);
            str.erase(str.end() - stoi(ss), str.end());
        }
        
        else if(s == "3"){ cout << str[stoi(ss)-1] << endl; }
        
        else {
            str = vec.back();
            vec.pop_back();
        }
        
        
    }
    
    return 0;
}

```




***Here Below , ScreenShot of my Submission***
