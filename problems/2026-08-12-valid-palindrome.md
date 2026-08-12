Approach-Two Pointers: Use one pointer at the beginning and another at the end of the string. Skip non-alphanumeric characters and compare the remaining characters in a case-insensitive manner. If all matching characters are equal, the string is a palindrome.

Time: O(n)
Space: O(1)

<!-- Python -->
def isPalindrome(s):
    left = 0
    right = len(s) - 1

    while left < right:
        while left < right and not s[left].isalnum():
            left += 1
        while left < right and not s[right].isalnum():
            right -= 1

        if s[left].lower() != s[right].lower():
            return False

        left += 1
        right -= 1

    return True