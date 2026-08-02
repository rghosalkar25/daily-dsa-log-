Approach-Hash Map: Count the frequency of each character in the first string and compare it with the frequency of characters in the second string. If both frequency maps are equal, the strings are anagrams.

Time: O(n)
Space: O(n)

<!-- Python -->
def isAnagram(s, t):
    if len(s) != len(t):
        return False

    count = {}

    for ch in s:
        count[ch] = count.get(ch, 0) + 1

    for ch in t:
        if ch not in count:
            return False
        count[ch] -= 1
        if count[ch] < 0:
            return False

    return True