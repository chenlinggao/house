

# 数组

| 类型 | 题目       | 难度 |
| :--: | ---------- | :--: |
| 数组 | 两数之和、 | 简单 |
|      | 两数相加   | 中等 |
|      |            | 困难 |
|      |            |      |



## 1. 两数之和

### 1. 暴力解

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        for i, ni in enumerate(nums):
            for j, nj in enumerate(nums[i+1:]):
                if (ni + nj == target):
                    return [i, j]
		return []
```



### 2. hash table

```python
# 返回的是索引值
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        hashtable = {};
        for idx, num in enumerate(nums):
			if target - num in hashtable:
                return [hashtable[target-num], i]
            hashtable[nums[i]] = i		# 记录值的索引
        return []
```

## 2. 两数相加

```python
class Solution:
    def addTwoNumbers(self, l1: ListNode, l2: ListNode) -> ListNode:

        # 初始化个位节点，先不做进位
        newPoint = ListNode(l1.val + l2.val)

        # rt用来作为最后return的节点，tp用来遍历节点
        rt, tp = newPoint, newPoint

        # l1,l2只要后面还有节点，就继续往后遍历；或者新链表还需要继续往后进位
        while (l1 and (l1.next != None)) or (l2 and (l2.next != None)) or (tp.val > 9):
            l1, l2 = l1.next if l1 else l1, l2.next if l2 else l2
            tmpsum = (l1.val if l1 else 0) + (l2.val if l2 else 0)
            # 计算新链表下个节点的值（当前节点的进位+当前l1 l2的值之和），先不做进位
            tp.next = ListNode(tp.val//10 + tmpsum)
            # 新链表当前节点的值取个位
            tp.val %= 10
            # 新链表往后遍历一个节点
            tp = tp.next
        return rt 						# 返回的是一个头节点
```

## 3. 最大子序列和

### 1. 暴力解

```c++
/*
	用起点和终点来确认一个子序列，这样我们就可以用两层的嵌套循环，枚举出所有的子序列
	O(N^3)
*/

```

### 2. 枚举

```c++
/*
	在枚举的时候，ii 到 j+1j+1 这个子序列的和，没必要再用一个for循环，可以直接在 ii 到 jj 这个子序列的和上再加1个数，省略到最里层的循环。
	O(N^2)
*/

```

### 3. 分治法

```c++
/*
	分成不同的情况来解决：
      * 情况1：最大和子序列位于前半部，可递归计算
      * 情况2：最大和子序列位于后半部，可递归计算
      * 情况3：最大和子序列从前半部开始但在后半部结束
          - 从两半部分的边界开始
          - 通过从右到左的扫描来找到左半段的最长序列
          - 从左到右的扫描找到右半段的最长序列
          - 把这两个子序列组合起来，形成跨越分割边界的最大连续子序列
    O(NlogN)
*/

```

#### 4. 在枚举法上改进

```c++
/*
	现象：和为负的子序列不可能是最大连续子序列的开始部分
    结论：当检测出一个负的子序列时，可以让start直接增加到j+1
    O(N)
*/

```



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

### ==总结==：

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



