Approach-Hash Set: Traverse the array while storing each element in a set. If an element is already present in the set, a duplicate exists. Otherwise, add it to the set and continue.

Time: O(n)
Space: O(n)

<!-- Python -->
def containsDuplicate(nums):
    seen = set()

    for num in nums:
        if num in seen:
            return True
        seen.add(num)

    return False