Approach-Two Pointers: Traverse both strings simultaneously, adding one character from each string alternately. If one string is longer, append its remaining characters at the end.

Time: O(n + m)
Space: O(n + m)

<!-- Python -->
def mergeAlternately(word1, word2):
    result = []
    i = 0

    while i < len(word1) and i < len(word2):
        result.append(word1[i])
        result.append(word2[i])
        i += 1

    result.extend(word1[i:])
    result.extend(word2[i:])

    return "".join(result)
