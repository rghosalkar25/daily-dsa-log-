Approach-Hash Map: Use a sorted version of each wprd as a key. Words with the same sorted characters are anagrams, so store them together in a hash map.

Time: O(n * k log k)
Space: O(n * k)

<!-- Python -->
def groupAnagrams(strs):
    groups = {}

    for word in strs:
        key = ''.join(sorted(word))

        if key not in groups:
        group[key] = []

        groups[key].append(word)

    return list(groups.values())