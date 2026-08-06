Approach-Dynamic Programming: The number of ways to reach the current step is the sum of the ways to reach the previous two steps. Keep track of only the last two values to optimize space.

Time: O(n)
Space: O(1)

<!-- Python -->
def climbStairs(n):
    if n <= 2:
        return n

    first = 1
    second = 2

    for _ in range(3, n + 1):
        current = first + second
        first = second
        second = current

    return second