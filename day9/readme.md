
***Problem : The Full Counting Sort ***

// Problem Link : https://www.hackerrank.com/challenges/countingsort4/problem

```

void countSort(vector<vector<string>> arr) {

    map<int , vector<string> > mp;
    
    for(int i=0 ; i< (arr.size()/2) ; i++){
        arr[i][1] = "-";
    }
    
    for(int i=0 ; i< arr.size() ; i++){
        mp[stoi( arr[i][0] )].push_back((arr[i][1]));
        
    }
    
    for(auto pair : mp){
        for(auto s : pair.second){
            cout<<s<<" ";
        }
    }
    
    cout<<endl;
    
    
    
}

```




***Here Below , ScreenShot of my Submission***
![day9](https://user-images.githubusercontent.com/109462762/194116814-83c033fa-00e3-4098-be78-0fd5fdbdb3dc.jpg)
