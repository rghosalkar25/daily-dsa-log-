Approach-Two Pointers: Maintain a pointer for the position of the next non-zero element. Traverse the array, moving each non-zero value forward. After all non-zero elements are placed, fill the remaining positions with zeros.

Time: O(n)
Space: O(1)

<!-- Python -->
def moveZeroes(nums):
    index = 0

    for i in range(len(nums)):
        if nums[i] != 0:
            nums[index] = nums[i]
            index += 1

    while index < len(nums):
        nums[index] = 0
        index += 1