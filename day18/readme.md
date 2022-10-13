
***Problem : Delete node in Doubly Linked List***

// https://lnkd.in/d6CQs2iT



```
    
    Node* deleteNode(Node *head, int pos)
    {
        
        if(pos == 1){
            Node* temp = head;
            head = head->next;
            
            delete temp;
            
            return head;
        }
        
        Node* temp= head;
        pos = pos-1;
        
        
        while(pos--){
            temp = temp->next;
        }


        if(temp->next == NULL){
            Node* copy = temp;
            temp->prev->next = NULL;
            delete copy;
            
            return head;
        }        
        
        
        Node* copy = temp;
        
        temp->next->prev = temp->prev;
        temp->prev->next = temp->next;
        
        delete copy;
        
        return head;
        
        
        
        
        
    }

```




***Here Below , ScreenShot of my Submission***
![day18](https://user-images.githubusercontent.com/109462762/195546727-5f9f9721-e253-471c-8f3f-cc454234db8b.jpg)

