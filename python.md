一、注释

```python
# This is a comment
```



二、变量

**global**：在函数内部创建全局变量



三、数据类型

| 类型       | 名称                       |
| ---------- | -------------------------- |
| 文本类型   | str                        |
| 数值类型   | int,float,complex          |
| 序列类型   | list,tuple,range           |
| 映射类型   | dict                       |
| 集合类型   | set,frozenset              |
| 布尔类型   | bool                       |
| 二进制类型 | bytes,bytearray,memoryview |

**type()**：获取数据类型。

**类型名(数据)**：指定数据类型。如x = str("hello world")。



四、数字

int-整型,float-浮点型,complex-复数。

**random模块**：

```python
import random
        
// 初始化随机数生成器
random.seed(a=None,version=2)
        
// 返回start到stop的随机选择元素
random.randrange(start,stop[,step])
        
// 返回a到b之间的随机整数，相当于randrange(a, b+1)
random.randint(a,b)
        
// 从非空序列seq返回一个随机元素
random.choice(seq)
        
// 从*population*中选择替换，返回大小为k的元素列表
// population-集群，weights-相对权重，cum_weights-累加权重，k-选取次数
random.choices(population,weights=None,*,cum_weights=None,k=1)

// 将序列x随机打乱位置
random.shuffle(x[,random])

// 从总体序列或集合中选择的唯一元素的k长度列表，用于无重复的随机抽样
random.sample(population,k)
        
// 返回[0.0, 1.0)范围内的下一个随机浮点数
random.random()
      
// 返回一个随机浮点数N
random.uniform(a,b)

// 返回不同分布的随机数(size=)
// 返回一个随机浮点数N，使得low<=N<=high并在这些边界之间使用指定的mode
random.triangular(low,high,mode)

// Beta分布
random.betavariate(alpha,beta)
      
// 指数分布
random.expovariate(lambd)
            
// Gamma分布
random.gammavariate(alpha,beta)
            
// 高斯分布
random.gauss(mu,sigma)
            
// 对数正态分布
random.lognormvariate(mu,sigma)
            
// 正态分布
random.normalvariate(mu,sigma)
            
// von Mises分布
random.vonmisesvariate(mu,kappa)
            
// 帕累托分布
random.paretovariate(alpha)
            
// 威布尔分布
random.weibullvariate(alpha,beta)
```



五、字符串

```python
// 赋值
a = "hello"

// 多行字符串
a = """Python is a widely used general-purpose, high level programming language. 
It was initially designed by Guido van Rossum in 1991 
and developed by Python Software Foundation. 
It was mainly developed for emphasis on code readability, 
and its syntax allows programmers to express concepts in fewer lines of code."""
或
a = '''Python is a widely used general-purpose, high level programming language. 
It was initially designed by Guido van Rossum in 1991 
and developed by Python Software Foundation. 
It was mainly developed for emphasis on code readability, 
and its syntax allows programmers to express concepts in fewer lines of code.'''

// 访问字符串元素
a[1]

// 切片
b[2:5]

// 负索引，末尾计数
b[-5,-2]

// 字符串长度
len(a)

// 删除开头和结尾的空白字符
a.strip()

// 返回小写字符串
a.lower()

// 返回大写字符串
a.upper()

// 字符串替换
a.replace("b","c")

// 字符串拆分
a.split(",")

// 检查子串是否存在
txt = "abcde"
x = "a" in txt
print(x)

// 检查子串是否不存在
x = "a" not in txt
print(x)

// 串联字符串
a = "hello"
b = "world"
c = a + b

// 字符串格式化
a = "hello{}".format("world")
b = "hello{0}{1}".format("nancy","jim")
```

更多字符串操作：

| 方法                              | 描述                                                         |
| --------------------------------- | ------------------------------------------------------------ |
| capitalize()                      | 把首字符转换为大写。                                         |
| casefold()                        | 把字符串转换为小写。                                         |
| center(length,character)          | 返回居中的字符串，length规定返回字符串的长度，character填补两侧缺失的字符。 |
| count(value,start,end)            | 返回指定值在字符串中出现的次数。                             |
| encode(encoding=,errors=)         | 返回字符串的编码版本。                                       |
| endswith(value,start,end)         | 判断字符串是否以指定值结尾。                                 |
| expandtabs(tabsize)               | 设置字符串的tab尺寸。                                        |
| find(value,start,end)             | 返回字符串中指定值的位置。失败时返回-1。                     |
| format(value1,value2...)          | 格式化字符串中的指定值。                                     |
| format_map(mapping)               | 格式化字符串中的指定值，mapping为字典对象。                  |
| index(value,start,end)            | 返回字符串中指定值的位置。失败时引发异常。                   |
| isalnum()                         | 判断是否所有字符都是字母数字。                               |
| isalpha()                         | 判断是否所有字符都在字符表中。                               |
| isdemical()                       | 判断是否所有字符都是小数。                                   |
| isdigit()                         | 判断是否所有字符都是数字。                                   |
| isidentifier()                    | 判断字符串是否为标识符。                                     |
| islower()                         | 判断是否所有字符都为小写。                                   |
| isnumeric()                       | 判断是否所有字符都是数。                                     |
| isprintable()                     | 判断是否所有字符都是可打印的。                               |
| isspace()                         | 判断是否所有字符都是空白字符。                               |
| istitle()                         | 判断字符串是否遵循标题规则。                                 |
| issupper()                        | 判断是否所有字符都是大写。                                   |
| join(iterable)                    | 把可迭代对象的元素连接到字符串的末尾。                       |
| ljust(length,character)           | 字符串左对齐。                                               |
| lower()                           | 字符串转换为小写。                                           |
| lstrip(characters)                | 删除字符串左边的空白字符或指定字符。                         |
| maketrans(intab,outtab)           | 返回经过转换表转换后的字符。                                 |
| partition(value)                  | 返回字符串被子串划分的三部分。                               |
| replace(oldvalue,newvalue, count) | 返回替换后的字符串                                           |
| rfind(value, start, end)          | 查找指定值的最后一次出现位置。                               |
| rindex(value, start, end)         | 查找指定值的最后一次出现位置。                               |
| rjust(length, character)          | 字符串右对齐。                                               |
| rpartition(value)                 | 搜索指定字符串的最后一次出现，并将该字符串拆分为包含三个元素的元组。 |
| rsplit(separator, max)            | 在指定的分隔符处拆分字符串，并返回列表。                     |
| rstrip(characters)                | 删除字符串右边的空白字符或指定字符。                         |
| split(separator, max)             | 在指定的分隔符处拆分字符串，并返回列表。                     |
| splitlines(keeplinebreaks)        | 在换行符处拆分字符串并返回列表。                             |
| startswith(value, start, end)     | 判断字符串是否以某一字符开始。                               |
| strip(characters)                 | 删除字符串两边的空白字符或指定字符。                         |
| swapcase()                        | 大小写转换。                                                 |
| title()                           | 把每个单词的首字符转换为大写。                               |
| translate()                       | 返回被maketrans(intab,outtab)转换后的字符串。                |
| upper()                           | 把字符串转换为大写。                                         |
| zfill()                           | 字符串开头填充指定数量的0。                                  |













