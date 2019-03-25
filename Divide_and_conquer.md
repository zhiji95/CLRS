# Divide and conquer

## 1. Maximum Subarray Problem 

find a mid

entirely in the subarray A[*low* : *mid*􏰀], so that *low* 􏰎 <= i <= 􏰎 j <= 􏰎 *mid*,
entirelyinthesubarrayA[*mid*+1::*high*]􏰀,so that *mid*<i 􏰎j 􏰎*high*,or
crossing the midpoint, so that *low* 􏰎 <= i <=  􏰎 *mid* <= j <=  􏰎 *high*.

```python
def maxSubArray(self, nums: List[int]) -> int:
        dp = [-float("inf")] * (len(nums)+1)
        for i in range(len(nums)):
            dp[i+1] = max(nums[i], dp[i]+nums[i])
        return max(dp)
```



## 2. Strassen's algorothm for matrix multiplication

1. Divide matrices A, B and output matrix C into  n/2􏰒 X n/2 submatrices. 
2.  Create 10 n/2􏰒 X n/2 matrices, 



## 3. Substitution method for solving recurrences

1. Guess the form of solution
2. Use mathematical induction to find the constants and show that the solution works.



## 4. Recursion-tree method for solving recurrences

## 5. Master method for solving recurrences

**1. Master theorem**

Let a 􏰃 1 and b > 1 be constants, let f(n) be a function, and let T(n) be defined
on the nonnegative integers by the recurrence:

T(n) = aT(n/b)+f(n)

1. $f(n) = O(n^{log_b{a-\epsilon}})$ : $T(n) = \Theta(n^{log_b{a-\epsilon}})$
2. $f(n) = \Theta(n^{log_b{a}})$: $T(n) = \Theta(n^{log_b{a-\epsilon}}lg{n})$
3. $f(n) = \Omega(n^{log_b{a+\epsilon}})$, and if af(n/b) <= cf(n) for c < 1: $T(n) = \Theta(f(n))$

 We compare f(n) with $n^{log_b{a}}$ , larger one dominants.

In first case, f(n) must be asymptotically smaller by a factor of $n^\epsilon$.

