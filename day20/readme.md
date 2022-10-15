
***Problem : Merge Nodes in Between Zeros ***

// Problem Link : https://leetcode.com/problems/merge-nodes-in-between-zeros/

```

ListNode* mergeNodes(ListNode* head) {
     
        
        ListNode* temp = head;
        
        
        ListNode* prev = head;
        ListNode* nxt = head;
        
        
        int sum =0 ;
        
        int first=0;
        
        while(temp != NULL){
        
                if(first==0){
                    temp = temp->next;
                    first++;
                }
            
                else if(temp->val == 0 && sum!=0){
                    
                    nxt= temp;
                    
                    ListNode* newNode = new ListNode(sum);
                    
                    prev->next = newNode;
                    newNode->next = nxt;
                    
                    prev = nxt;
                    sum=0;
                    
                }
            
                else{
                    sum += temp->val;
                    temp = temp->next;
                }
            
        }
        
        
        
    
    ListNode* temp1 = head;   
    ListNode* temp2 = head;
        
        
        while(temp2 != NULL){
            temp2 = temp2->next;
            
            if(temp2!= NULL && temp2->val == 0){
                temp1 ->next = temp2->next;
                
                temp2 = temp1->next;
            }
            
            temp1 = temp1->next;
            
        }
        
        
        
        return head->next;
        
        
        
        
    }

```




***Here Below , ScreenShot of my Submission***

