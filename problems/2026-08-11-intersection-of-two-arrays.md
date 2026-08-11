Approach-Hash Set: Store the elements of the first array in a set. Traverse the second array and add common elements to the result set to avoid duplicates.

Time: O(n + m)
Space: O(n)

<!-- Python -->
def intersection(nums1, nums2):
    set1 = set(nums1)
    result = set()

    for num in nums2:
        if num in set1:
            result.add(num)

    return list(result)