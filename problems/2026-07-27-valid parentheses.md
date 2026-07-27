Approach:Use a stack. Push opening brackets. On a closing bracket, check if the top of the stack matches its pair — if yes, pop; if no (or stack is empty), it's invalid. String is valid if the stack is empty at the end.

Time: O(n)
Space: O(n)

<!--python -->
def isValid(s: str) -> bool:
    stack = []
    pairs = {')': '(', ']': '[', '}': '{'}
    
    for char in s:
        if char in pairs.values():
            stack.append(char)
        elif char in pairs:
            if not stack or stack.pop() != pairs[char]:
                return False
        else:
            return False
    
    return not stack