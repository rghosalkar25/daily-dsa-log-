Approach-Prefix and Suffix Products: Calculate the product of all elements before each index using a prefix pass. Then multiply it with the product of all elements after each index using a suffix pass.

Time: O(n)
Space: O(1)

<!-- Python -->
def productExceptSelf(nums):
    n = len(nums)
    result = [1] * n

    prefix = 1
    for i in range(n):
        result[i] = prefix
        prefix *= nums[i]

    suffix = 1
    for i in range(n - 1, -1, -1):
        result[i] *= suffix
        suffix *= nums[i]

    return result