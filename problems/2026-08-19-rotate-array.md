Approach-Reversal: Reverse the entire array, then reverse the first k elements and the remaining elements. This rotates the array to the right by k positions.

Time: O(n)
Space: O(1)

<!-- Python -->
def rotate(nums, k):
    n = len(nums)
    k %= n

    nums.reverse()
    nums[:k] = reversed(nums[:k])
    nums[k:] = reversed(nums[k:])