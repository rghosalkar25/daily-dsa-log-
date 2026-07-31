Approach-Iterative: Maintain two pointers (left and right). Find the middle element. If the target is found, return its index. Otherwise, search the left or right half based on comparison.

Time: O(log n)
Space: O(1)

<!-- Python -->
def search(nums, target):
    left = 0
    right = len(nums) - 1

    while left <= right:
        mid = (left + right) // 2

        if nums[mid] == target:
            return mid
        elif nums[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1