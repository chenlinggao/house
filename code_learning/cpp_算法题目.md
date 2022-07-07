## 

### 最大子序列和

### 1. 暴力解

```c++
/*
	用起点和终点来确认一个子序列，这样我们就可以用两层的嵌套循环，枚举出所有的子序列
	O(N^3)
*/
int maxSubsequenceSum(int a[], int size, int &start, int &end) {
    int maxSum = 0;
    // 枚举起点 i
    for (int i = 0; i < size; i++ ) {
        // 枚举终点 j
        for( int j = i; j < size; j++ ) {
            int thisSum = 0; 
            // 计算i到j的子序列和
            for( int k = i; k <= j; k++ )     thisSum += a[ k ];
            // 如果是最大的，存下这个子序列的起点和终点以及最大的和
            if( thisSum > maxSum ) {
                maxSum = thisSum;
                start = i;   end = j;
            }
        }
    }
    return maxSum;
}
```

### 2. 枚举

```c++
/*
	在枚举的时候，ii 到 j+1j+1 这个子序列的和，没必要再用一个for循环，可以直接在 ii 到 jj 这个子序列的和上再加1个数，省略到最里层的循环。
	O(N^2)
*/
int maxSubsequenceSum(int a[], int size,  int &start, int &end) {
    int maxSum = 0;
    for (int i = 0; i < size; i++ ) {
        int thisSum = 0; 
        for( int j = i;  j < size; j++ ) {
            // 直接在之前的计算结果上加上一个数，就能得到i到j的子序列和
            thisSum += a[ j ];
            if( thisSum > maxSum )   {
                maxSum = thisSum;
                start = i;   end = j
            }
        }
    }
    return maxSum;
}
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
int maxSum(int a[ ],  int left,  int right , int &start, int &end) {
    int maxLeft, maxRight, center;
    int leftSum = 0, rightSum = 0;           
    int maxLeftTmp = 0,  maxRightTmp = 0;     
    int startL , startR,  endL,  endR;             
    
    // 递归的终止条件
    if (left == right) {                    
        start = end = left;
        return a[left] > 0 ? a[left] : 0;
    }
    
    center = (left + right) / 2;  
    // 递归地计算整个位于前半部的最大连续子序列
    maxLeft = maxSum(a,  left,  center,  startL,  endL); 
    // 递归地计算整个位于后半部的最大连续子序列
    maxRight = maxSum(a, center + 1,  right,  startR,  endR); 
    
    
    // 从中间往左扫描
    start = center;
    for (i = center; i >= left; --i) {
        leftSum += a[i];
        if (leftSum > maxLeftTmp) {
            maxLeftTmp = leftSum;
            start = i;      
        }     
    }
    // 从中间往右扫描
    end = center + 1;
    for (i = center + 1; i <= right; ++i) {
        rightSum += a[i];
        if (rightSum > maxRightTmp) {
            maxRightTmp = rightSum;
            end = i;    
        }  
    }
    
    
    // 计算从前半部开始在后半部结束的最大连续子序列的和
    // 选择三个值中的最大值
    if (maxLeft > maxRight ) 
        if (maxLeft > maxLeftTmp + maxRightTmp)  {
            start = startL;
            end = endL;
            return  maxLeft;
        }
        else return maxLeftTmp + maxRightTmp;
    else
        if (maxRight > maxLeftTmp + maxRightTmp)  {
            start = startR;
            end = endR;
            return maxRight;
        }
        else return maxLeftTmp + maxRightTmp;
}
```

#### 在枚举法上改进

```c++
/*
	现象：和为负的子序列不可能是最大连续子序列的开始部分
    结论：当检测出一个负的子序列时，可以让start直接增加到j+1
    O(N)
*/
int maxSubsequenceSum(int a[], int size, int &start, int &end) {  
    // starttmp用于保存前面的最优方案
    int maxSum, starttmp, thisSum; 
    start = end = maxSum = starttmp = thisSum = 0; 
    for( int j = 0; j < size ; ++j ) {
        thisSum += a[j];
        if ( thisSum <= 0 ) {              
            thisSum = 0; 
            starttmp = j+1;
        } else if (thisSum > maxSum )  {   
            maxSum = thisSum; 
            start = starttmp;
            end = j;   
        }
    } 
    return maxSum;
}
```

