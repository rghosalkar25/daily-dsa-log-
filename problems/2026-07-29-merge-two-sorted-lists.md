Approach-Two Pointers: Use a temporary dummy node to easily build the new list without dealing with empty head edge cases. Compare the current nodes of both lists, link the smaller value to your merged list tail, and advance that list's pointer.

Time: O(n + m)
Space: O(1)

<!-- Python -->
Definition for singly-linked list.
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

def mergeTwoLists(list1: Optional[ListNode], list2: Optional[ListNode]) -> Optional[ListNode]:
    dummy = ListNode()
    tail = dummy
    
    while list1 and list2:
        if list1.val < list2.val:
            tail.next = list1
            list1 = list1.next
        else:
            tail.next = list2
            list2 = list2.next
        tail = tail.next
        
    tail.next = list1 if list1 else list2
    return dummy.next

Notes
Key insight: Using a dummy head pointer eliminates complex null-checking when initializing the merged list. Once one list runs empty, you can instantly attach the entire remainder of the other list in O(1) time without looping further.


