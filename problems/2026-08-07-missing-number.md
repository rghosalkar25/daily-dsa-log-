Approach-Mathematical Formula: Calculate the expected sum of numbers from 0 to n using the formula n × (n + 1) / 2. Subtract the actual sum of the array to find the missing number.

Time: O(n)
Space: O(1)

<!-- Python -->
def missingNumber(nums):
    n = len(nums)
    expected_sum = n * (n + 1) // 2
    actual_sum = sum(nums)

    return expected_sum - actual_sum