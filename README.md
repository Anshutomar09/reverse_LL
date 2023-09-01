# reverse_LL

class Solution {
public:
    ListNode* reverseList(ListNode* head) {
        ListNode*slow=head;
        
        ListNode*prev=NULL;
        
        if(head==NULL || head->next==NULL)
     {
         return head;
     }
        
        while(slow->next!=NULL and slow!=NULL){
             ListNode*temp=slow->next;
            slow->next=prev;
           prev= slow;
            slow=temp;
             
        }
        slow->next=prev;
       
        return slow;
    }
};
