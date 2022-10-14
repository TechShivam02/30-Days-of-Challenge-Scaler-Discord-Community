
***Problem : Compare two linked lists  ***

// Problem Link : https://www.hackerrank.com/challenges/compare-two-linked-lists/problem

```


bool compare_lists(SinglyLinkedListNode* head1, SinglyLinkedListNode* head2) {

    while(head1!= NULL && head2!=NULL){
        if(head1->data != head2->data){
            return false;
        }
        
        head1 = head1->next;
        head2 = head2->next;
    }
    
    if(head1== NULL && head2== NULL)
    {
        return true;
    }
    
    return false;

}


```




***Here Below , ScreenShot of my Submission***
![day19](https://user-images.githubusercontent.com/109462762/195870036-f5fdda61-1eea-4103-8f20-b548eac58f68.jpg)

