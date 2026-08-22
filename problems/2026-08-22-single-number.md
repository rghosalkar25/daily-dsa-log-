Approach-XOR: XOR all the elements in the array. Since a number XOR itself becomes 0 and XOR with 0 remains unchanged, the number that appears only once will remain.

Time: O(n)
Space: O(1)

<!-- Python -->
def singleNumber(nums):
    result = 0

    for num in nums:
        result ^= num

    return result