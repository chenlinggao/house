# 剑指offer

## 栈和队列

### 1. 用两个栈实现一个队列

```python
class CQueue:
    def __init(self):
        self.stack_in = []
        self.stack_out = []

    def appendTail(self, value:int):
        self.stack_in.append(value)
    
    def deleteHead(self):
        if not self.stack_out:
            if not self.stack_in:
                return -1
            else:
                self.stack_out.append(self.stack_in.pop())
        return self.stack_out.pop()
```



## 动态规划

### ==\**总结**==：

#### 1. 将问题总结为状态转移方程

### 1. 斐波那契数列

```python
"""
写一个函数，输入 n ，求斐波那契（Fibonacci）数列的第 n 项（即 F(N)）。斐波那契数列的定义如下：
F(0) = 0,   F(1) = 1
F(N) = F(N - 1) + F(N - 2), 其中 N > 1.
斐波那契数列由 0 和 1 开始，之后的斐波那契数就是由之前的两数相加而得出。
答案需要取模 1e9+7（1000000007），如计算初始结果为：1000000008，请返回 1。
"""
# 有问题
def fib(n: int):
    a, b = 0, 0
    for _ in range(n):
        a = b
        b = a+b
    return a % (1e9+7)

class Solution:
    def fib(self, n: int) -> int:
        MOD = 10 ** 9 + 7
        if n < 2:
            return n
        p, q, r = 0, 0, 1
        for i in range(2, n + 1):
            p = q
            q = r
            r = (p + q) % MOD
        return r
```

### 2. 青蛙跳台问题

```python
"""一只青蛙一次可以跳上1级台阶，也可以跳上2级台阶。求该青蛙跳上一个 n 级的台阶总共有多少种跳法。"""

# 斐波那契数列解法
"""
	在只剩下0个台阶时，f(0)=1; 在只剩下1个台阶时，f(1)=1
	最终将上述问题转换成斐波那契数列问题
"""
def numWays(n: int):
    dp = [1, 1]
    for i in range(2, n+1):
        dp.append(dp[i-2]+dp[i-1])
    return dp[-1] % 1000000007
```

## 查找

### ==\**总结**==：

#### 1. 二叉查找



### 1. 返回旋转数组中最小的数字

```python
"""把一个数组最开始的若干个元素搬到数组的末尾，我们称之为数组的旋转。

给你一个可能存在 重复 元素值的数组 numbers ，它原来是一个升序排列的数组，并按上述情形进行了一次旋转。请返回旋转数组的最小元素。例如，数组 [3,4,5,1,2] 为 [1,2,3,4,5] 的一次旋转，该数组的最小值为1。  """

# 分治策略
def minArray(numbers: list) -> int:
    low, high = 0, len(numbers)-1
    while low < high:
        pivot = low + (high - low) // 2
        if numbers[pivot] > numbers[high]:
            high = pivot
        elif numbers[pivot] < numbers[high]:
            low = pivot + 1
       	else:
            high -= 1
    return numbers[low]
```



