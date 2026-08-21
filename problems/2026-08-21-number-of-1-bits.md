Approach-Bit Manipulation: Repeatedly use n & (n - 1) to remove the lowest set bit. Count how many times this operation can be performed until n becomes zero.

Time: O(k), where k is the number of 1 bits
Space: O(1)

<!-- Python -->
def hammingWeight(n):
    count = 0

    while n:
        n = n & (n - 1)
        count += 1

    return count