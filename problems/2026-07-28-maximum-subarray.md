Approach-Kadane's Algorithm: track the best subarray sum ending at the current index (current_sum) and the best sum seen overall (max_sum). At each element, decide whether to extend the previous subarray or start fresh from the current element — whichever gives a larger sum.

Time: O(n)
Space: O(1)

<!-- python -->
def maxSubArray(nums: list[int]) -> int:
    current_sum = max_sum = nums[0]
    
    for num in nums[1:]:
        current_sum = max(num, current_sum + num)
        max_sum = max(max_sum, current_sum)
    
    return max_sum

Notes
Key insight: if current_sum ever goes negative, it's better to drop it and start fresh from the next element rather than carry a negative sum forward. Works with negative numbers in the array too — just make sure nums isn't empty before running.