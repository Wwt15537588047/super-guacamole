# super-guacamole
C++
struct ListNode* ReverseList(struct ListNode* pHead ) {
    struct ListNode* cur=pHead;
    if(cur==NULL)
        return NULL;
    struct ListNode* cur_next=cur->next;
    while(cur_next)
    {
        struct ListNode* cur_next_next=cur_next->next;
        if(cur==pHead)
        {
            cur->next=NULL;
        }
        cur_next->next=cur;
        cur=cur_next;
        cur_next=cur_next_next;
    }
    return cur;
}
