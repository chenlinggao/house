算法

## 1. 算法基础

### 1.1. 模拟和高精度

#### 1.1.1. 单精度和高精度

* `单精度`：可以用内置的数据类型存储的整数
* `高精度`：用内置的数据类型已经存储不下了，要用数组来存储每个数位

#### 1.1.2. 大端序和小端序

* `大端序`：数字高位 对应 地址地位
* `小端序`：数字高位 对应 地址高位



<img src="https://staticcdn.boyuai.com/user-assets/5085/8wevpwJ5npySyrLpXoCyuP/%E5%A4%A7%E7%AB%AF%E5%BA%8F.jpg!jpg" alt="img" style="zoom:50%;" /> <img src="https://staticcdn.boyuai.com/user-assets/5085/y3d6nyDnNymbPEQDTVHpbQ/%E5%B0%8F%E7%AB%AF%E5%BA%8F.jpg!jpg" alt="img" style="zoom:50%;" />

#### 1.1.3. 高精度运算

##### 加法

```c++
// 高精度运算 -- 加法
#include <bits/stdc++.h>
#define N 110
using namespace std;
// 这里我们采用直接赋值的形式初始化，按照小端序的方式存储
// 所以这里加数a = 368， 加数b = 997，
// 感兴趣的话也可以按照之前介绍的方式改成手动输入
int a_digits[N] = {8, 6, 3}, a_len = 3;
int b_digits[N] = {7, 9, 9}, b_len = 3;
int ans_digits[N], ans_len;

int main() {
    // 1. 数位操作:     
    ans_len = max(a_len, b_len);  // 初始长度
    int k = 0;                    // 记录进位的变量
    for (int i = 0; i < ans_len; ++i) {
        // 假设a_len > b_len，这里需要保证b[b_len]到b[a_len - 1]的位置都是0，否则可能会出错。
        // TODO 请补全下述代码
        ans_digits[i] = a_digits[i] + b_digits[i] + k; // 相加计算
        k = ans_digits[i] / 10; // 更新进位
        ans_digits[i] %= 10;
    }
    
    // 2. 维护长度: 
    if (k) 
        // TODO 请补全下述代码
        ans_digits[ans_len++] = k ; // 最高位进位
    
    // 3. 输出    
    for (int i = ans_len - 1; i >= 0; --i) 
        cout << ans_digits[i];
    cout << endl;
    
    return 0;
}
```

##### 减法

```c++
// 高精度运算 - 减法
#include <bits/stdc++.h>
#define N 110
using namespace std;
// 同样，这里采用小端序存储
int a_digits[N] = {8, 6, 3, 2}, a_len = 4;
int b_digits[N] = {7, 9, 9},	b_len = 3;

int ans_digits[N], ans_len;
int main() {
    // 1. 数位操作
    // 我们依旧是从低位到高位开始逐位相减
    // 因为我们总假设a>=b，所以初始长度先设为a的长度
    // 考虑每一位，需要计算的部分是被减数的当前位，减去减数的当前位，再减去低位的借位
    // 如果上一步的计算得出当前位<0，那我们需要向高位借位，然后给当前位+10
    ans_len = a_len;	// 初始长度
    int k = 0;			// 维护借位
    for (int i = 0; i < ans_len; ++i) {
        ans_digits[i] = a_digits[i] - b_digits[i] - k;
        
        if (ans_digits[i] < 0) {
            k = 1;
            ans_digits[i] += 10;
        } else k = 0;	// 这里赋值成0很关键，而且容易遗漏
    }
    
    // 2. 维护长度
    // 想象一下，如果实际数字是1，但是长度记录是4的话，那么输出该数字结果将是0001，
    // 也就是出现了“前导0”，所以维护长度的目的是为了去掉前导0
    // 所以，我们用while循环实现这样的逻辑：只要最高位是0，我们就把位数缩小1位。
    // 但是需要注意，只有位数>1的时候才可以缩小，否则当保存的数字是0时，长度也会减为0.
    while (ans_len > 1 && !ans_digits[ans_len - 1]) // 只有长度大于1才可以去掉前导零
        --ans_len;
    
    // 3. 输出
    for (int i = ans_len - 1; i >= 0; --i) cout << ans_digits[i];
    cout << endl;
    return 0;    
}
```

##### 乘法

```c++
// 高精度运算 - c
#include <bits/stdc++.h>
#define N 110
using namespace std;
int a_digits[N] = {3, 2}, a_len = 2;
int b_digits[N] = {8, 6}, b_len = 2;
// int a_digits[N] = {0}, a_len = 1;
// int b_digits[N] = {9, 9}, b_len = 2;
int ans_digits[N * 2], ans_len;
int main() {
    // 1. 数位操作
    ans_len = a_len + b_len;		// 初始化长度
    for (int i = 0; i < ans_len; ++i) 
        ans_digits[i] = 0; 
    // 因为是不断累加的形式，所以要将范围内的元素初始化为0。
    
    for (int i = 0; i < a_len; ++i) 
        for (int j = 0; j < b_len; ++j)
            // TODO 请补全下述代码
            ans_digits[i + j] += a_digits[i] * b_digits[j];  // 乘法计算
    // ans的每一位更新都要使用累加的形式，这是因为对于ans的第k位，满足i + j == k的(i, j)很多，所以可能答案的第k位可能先后被更新很多次。
    
    // 2. 统一进位
    int k = 0;
    for (int i = 0; i < ans_len; ++i) {
        // TODO 请补全下述代码
        ans_digits[i] += k;
        k = ans_digits[i] / 10;
        ans_digits[i] %= 10; //
    }
    
    // 3. 维护长度
    while (ans_len > 1 && ans_digits[ans_len - 1] == 0) 
        --ans_len;
    
    // 4. 输出
    for (int i = ans_len - 1; i >= 0; --i) 
        cout << ans_digits[i];
    cout << endl;
    return 0;
}
```

###  1.2. 评估

#### 1.2.1. 算法评估角度

* 时间复杂度
  * CPU的**主频**，表示CPU每秒钟产生脉冲信号的次数（也就是每秒钟的时钟周期个数）。
  * 主频为`2.1GHz`的CPU，$1s$发出$2.1*10^9$次脉冲信号。每个时钟周期能完成1条指令，该计算机$1s$能完成$2.1*10^9$条指令
* 空间复杂度
  * 不同数据类型占据的字节大小不同，`int`是四个字节等

#### 1.2.2. 大O估计法

* 代码运行受到语种和运行环境的影响，速度也会受到影响
* 根据算法的最快增长项的系数来决定。因为评估算法的复杂度时都是用很大量的数据，增长慢的项往往可以忽略。



---

## 2. 枚举法

* 把所有可能都列举一遍



### 2.1. 子集枚举

* `01比特串法`

### 2.2. 排列枚举

* `next_permutation()`：将a数组中的元素重排成按照字典序顺序的下一个排列
* 
