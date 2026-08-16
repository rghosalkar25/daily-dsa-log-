Approach-Sliding Window: Maintain a window using two pointers and a set of characters. Expand the right pointer and remove characters from the left whenever a duplicate is found. Keep track of the maximum window length.

Time: O(n)
Space: O(n)

<!-- Python -->
def lengthOfLongestSubstring(s):
    seen = set()
    left = 0
    max_length = 0

    for right in range(len(s)):
        while s[right] in seen:
            seen.remove(s[left])
            left += 1

        seen.add(s[right])
        max_length = max(max_length, right - left + 1)

    return max_length