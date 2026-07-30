Approach-Iterative: Use three pointers (prev, curr, next) to reverse the list in place. Update the current node's next pointer to point backward, then advance all pointers forward.

Time: O(n)
Space: O(1)

<!-- Python -->
Definition for singly-linked list.
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

def reverseList(head: Optional[ListNode]) -> Optional[ListNode]:
    prev = None
    curr = head
    
    while curr:
        next_node = curr.next
        curr.next = prev
        prev = curr
        curr = next_node
        
    return prev
