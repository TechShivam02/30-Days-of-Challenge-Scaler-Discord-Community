
***Problem : 147 Insertion Sort List ***

// Problem Link : https://leetcode.com/problems/insertion-sort-list/

```
class Solution {
public:
    ListNode* insertionSortList(ListNode* head) {
        
        ListNode* dummy = new ListNode(1000);
        
        ListNode* temp = NULL;
        
        
        while(head){
            
            ListNode* next = head->next;
            temp = dummy;
            
            while(temp->next && temp->next->val < head->val){
                temp = temp->next;
            }
            
            
            head->next = temp->next;
            temp->next = head;
            
            head=next;
            
        }
        
        return dummy->next;
        
        
        
        
    }
};

```




***Here Below , ScreenShot of my Submission***

