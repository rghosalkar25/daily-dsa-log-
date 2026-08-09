Approach-Hash Map: Count the frequency of each character in the first string. Traverse the second string and decrease the count. The character that is not found or whose count becomes negative is the extra character.

Time: O(n)
Space: O(n)

<!-- Python -->
def findTheDifference(s, t):
    count = {}

    for ch in s:
        count[ch] = count.get(ch, 0) + 1

    for ch in t:
        if ch not in count or count[ch] == 0:
            return ch
        count[ch] -= 1