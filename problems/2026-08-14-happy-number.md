Approach-Hash Set: Repeatedly replace the number with the sum of the squares of its digits. Use a set to track previously seen numbers. If the number becomes 1, it is a happy number. If a number repeats, a cycle exists, so it is not a happy number.

Time: O(log n)
Space: O(log n)

<!-- Python -->
def isHappy(n):
    seen = set()

    while n != 1 and n not in seen:
        seen.add(n)
        total = 0

        while n > 0:
            digit = n % 10
            total += digit * digit
            n //= 10

        n = total

    return n == 1