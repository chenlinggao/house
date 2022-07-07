# 背景

## 存储方式

1. 顺序存储：数组，可以通过下标找到
2. 链接存储：单链表，用指针显式地指出元素之间的关系
3. 哈需存储：用存储位置表示元素之间的关系
4. 索引存储：索引区和数据区

# 数据结构

## 顺序结构

###  基本模板类：线性表

* 抽象类

```c++
template <class elemType>
class list {
  public: 
     // 清除
     virtual void clear() = 0;
     // 长度
     virtual int length() const = 0;
     // 插入
     virtual void insert(int i, const elemType &x) = 0; 
     // 删除
     virtual void remove(int i) = 0;
     // 搜索
     virtual int search(const elemType &x) const = 0;
     // 访问
     virtual elemType visit(int i) const = 0;
     // 遍历
     virtual void traverse() const = 0;
     // 析构
     virtual ~list() {};
};
```

* 线性表的抽象类定义虚析构函数
  * 虚析构函数是为了解决父类指针指向子类对象时，释放子类对象的资源时，释放不完全，造成的内存泄漏问题。
* 基本操作
  - **创建**空的线性表
  - **清除**所有元素
  - 求线性表的**长度**
  - 在第i个位置**插入**一个元素
  - **删除**第i个位置的元素
  - **搜索**某个元素在线性表中是否出现
  - **访问**线性表的第i个元素
  - **遍历**线性表

### 1. 顺序表

* 顺序表比较适合**静态的**、**经常做线性访问**的线性表
  * ![image-20220707163444005](imgs/image-20220707163444005.png)
* 顺序表类模板

```c++
template <class elemType>
class seqList: public list<elemType> { 
private:
    elemType *data;
    int currentLength;
    int maxSize;
    void doubleSpace();	// 为了解决插入元素时，数组容量不够的问题
public:
    seqList( int initSize = 10 );
    // 析构函数：还掉动态空间
    ~seqList( )  {  delete [] data;  }
    // 清空数组元素：只要把表长设为0
    void clear( )  {   currentLength = 0;   }
    // 数组长度：只需要返回这个私有成员变量currentLength
    int length( ) const  {   return currentLength;   }
    void insert( int i, const elemType &x); 
    void remove( int i );  
    int search( const elemType &x ) const ;
    // 访问数组元素：返回下标为i的数组元素
    elemType visit( int i) const { return data[i]  ; }
    void traverse( ) const ;
};
```

#### 构造函数

```c++
template <class elemType>
seqList<elemType>::seqList(int initSize) {
    data = new elemType[initSize]; 
    maxSize = initSize; 
    currentLength = 0;
} 
```

#### search

```c++
```

#### traverse

```c++
```

#### insert(i, x)

```c++
```

#### doubleSpace

```c++
```

#### remove(i)

```c++
```




### 2. 单链表



### 3. 双链表

# 算法题

