# 25. Reverse Nodes in k-Group

**Difficulty:** Hard  
**Topics:** Linked List, Recursion  
**LeetCode Link:** https://leetcode.com/problems/reverse-nodes-in-k-group

## Problem Statement

Given the `head` of a linked list, reverse the nodes of the list `k` at a time, and return the modified list.

If the number of nodes is not a multiple of `k` then left-out nodes, in the end, should remain as is.

You may **not alter the values** in the list's nodes, only nodes themselves may be changed.

### Example 1:
```
Input: head = [1,2,3,4,5], k = 2
Output: [2,1,4,3,5]
```

### Example 2:
```
Input: head = [1,2,3,4,5], k = 3
Output: [3,2,1,4,5]
```

### Constraints:
- The number of nodes in the list is `n`
- `1 <= k <= n <= 5000`
- `0 <= Node.val <= 1000`

## Approach

**Algorithm:** Iterative Reversal with Grouping
- Find the end of each k-group
- Reverse that k-group
- Connect to next group
- Repeat until end of list

**Time Complexity:** O(n) - Single pass with reversals
**Space Complexity:** O(1) - Only pointers used

## Solutions

### Java
```java
class Solution {
    public ListNode reverseKGroup(ListNode head, int k) {
        // Check if there are at least k nodes
        ListNode check = head;
        for (int i = 0; i < k; i++) {
            if (check == null) return head;
            check = check.next;
        }
        
        // Reverse first k nodes
        ListNode prev = null;
        ListNode curr = head;
        for (int i = 0; i < k; i++) {
            ListNode next = curr.next;
            curr.next = prev;
            prev = curr;
            curr = next;
        }
        
        // Recursively reverse remaining groups
        head.next = reverseKGroup(curr, k);
        return prev;
    }
}
```

### Python
```python
class Solution:
    def reverseKGroup(self, head: Optional[ListNode], k: int) -> Optional[ListNode]:
        # Check if there are at least k nodes
        check = head
        for i in range(k):
            if not check:
                return head
            check = check.next
        
        # Reverse first k nodes
        prev = None
        curr = head
        for i in range(k):
            next_node = curr.next
            curr.next = prev
            prev = curr
            curr = next_node
        
        # Recursively reverse remaining groups
        head.next = self.reverseKGroup(curr, k)
        return prev
```
