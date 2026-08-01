Approach-Iterative: Traverse the array once while keeping track of the minimum price seen so far. At each step, calculate the profit by selling at the current price and update the maximum profit.

Time: O(n)
Space: O(1)

<!-- Python -->
def maxProfit(prices):
    min_price = float('inf')
    max_profit = 0

    for price in prices:
        if price < min_price:
            min_price = price
        else:
            max_profit = max(max_profit, price - min_price)

    return max_profit