# Intuition
The problem involves removing nodes from a linked list that have a greater value node anywhere to their right. This can be approached more efficiently by working backwards, allowing us to identify the maximum value in the list and retain only nodes that are greater than or equal to the maximum encountered so far.

# Approach
1. Reverse the linked list: By reversing the list, we can start processing it from the end to the beginning, which makes it easier to keep track of the maximum value seen so far.
2. Iterate through the reversed list: As we traverse the reversed list, we keep track of the current maximum value seen so far. If a node's value is greater than or equal to the current maximum, we retain the node in the list and update the current maximum. Otherwise, we skip the node.
3. Reverse the list back: After removing the necessary nodes, we reverse the list again to restore its original order.
4. Return the new head: Return the new head of the list, which is now filtered based on the condition provided in the problem.

# Complexity
- Time complexity:
The algorithm involves reversing the linked list twice, and iterating through the linked list once. Each of these operations takes linear time in relation to the length of the list, resulting in a time complexity of O(n).
- Space complexity:
The algorithm uses a constant amount of extra space to hold pointers for reversing the list and keeping track of the current maximum value. Therefore, the space complexity is O(1).
