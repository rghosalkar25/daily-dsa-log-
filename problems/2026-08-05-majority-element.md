Approach-Boyer-Moore Voting: Maintain a candidate and a count. If the count becomes zero, choose the current element as the new candidate. Increase the count for the same element and decrease it for different elements. The remaining candidate is the majority element.

Time: O(n)
Space: O(1)

<!-- Python -->
def majorityElement(nums):
    count = 0
    candidate = None

    for num in nums:
        if count == 0:
            candidate = num

        if num == candidate:
            count += 1
        else:
            count -= 1

    return candidate