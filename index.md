# This is my first heading.
## This is h2 heading.
![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)
```python
class Solution:
    def maxProfit(self, prices: List[int]) -> int:
        n = len(prices)
        @cache
        def dfs(i: int, hold: bool) -> int:
            if i < 0:
                return -inf if hold else 0
            if hold:
                return max(dfs(i - 1, False) - prices[i], dfs(i - 1, True))
            return max(dfs(i - 1, False), dfs(i - 1, True) + prices[i])
        return dfs(n - 1, False)
```
- [x] Done
- [ ] This is a task list


