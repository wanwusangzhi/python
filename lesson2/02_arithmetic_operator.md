## 算术运算符

* + 加
* - 减
* * 乘
* / 除
* % 取模（相除后的余数）
* ** 取幂（注意 ^ 并不执行该运算，你可能在其他语言中见过这种情形）
* // 相除后向下取整到最接近的整数

```
3**2 = 9
7//3 = 2
-11 // 3 = -4
```

## 科学记数法来定义很大的数字。

```
4.445e8 等于 4.445 * 10 ** 8，也就是 444500000.0
```

## 布尔型运算符、比较运算符和逻辑运算符
* 布尔数据类型存储的是值 True 或 False，通常分别表示为 1 或 0。

* 通常有 6 个比较运算符会获得布尔值：

* 比较运算符
| 	符号使用情况 |	布尔型	| 运算符	 	|
| 	5 < 3 	|	False	|	小于 		|
|	5 > 3	|  	True	|	大于 		|
|	3 <= 3	| 	True	| 	小于或等于	|
|	3 >= 5	| 	False	|	大于或等于	|
|	3 == 5	| 	False 	|	等于			|
|	3 != 5	|	True 	|	不等于		|

#### 你需要熟悉三个逻辑运算符：

|	逻辑使用情况	|	布尔型	| 	运算符	|
|	5 < 3 and 5 == 5	|	False	|	and - 检查提供的所有语句是否都为 True	|
|	5 < 3 or 5 == 5		|	True	|	or - 检查是否至少有一个语句为 True		|
|	not 5 < 3	|	True	|	not - 翻转布尔值		|

## 字符串
在 python 中，字符串的变量类型显示为 str。你可以使用双引号 " 或单引号 ' 定义字符串。如果你要创建的字符串包含其中一种引号
```
>>> first_word = 'Hello'
>>> second_word = 'There'
>>> print(first_word + second_word)

HelloThere

>>> print(first_word + ' ' + second_word)

Hello There

>>> print(first_word * 5)

HelloHelloHelloHelloHello

>>> print(len(first_word))

5
>>> first_word[0]

H

>>> first_word[1]

e
```

## 类型和类型转换
你到目前为止，已经见过四种数据类型：
* 整型
* 浮点型
* 布尔型
* 字符串

```
>>> print(type(4))
int
>>> print(type(3.7))
float
>>> print(type('this'))
str
>>> print(type(True))
bool
```


## 数据结构
Python 自带一些数据结构，在编程时会经常使用到，请看以下表格：

|	Data 	|	 Structure	|	Ordered		|	Mutable		|	Constructor	|	Example	|
|	int 	|	NA	|	NA	|	int()	|	5
|	float	|	NA	|	NA	|	float()	|	6.5
|	string	|	Yes	|	No	|	' ' or " " or str()	|	"this is a string"
|	bool	|	NA	|	NA	|	NA	|	True or False
|	list	|	Yes	|	Yes	|	[ ] or list()	|	[5, 'yes', 5.7]
|	tuple	|	Yes	|	No	|	( ) or tuple()	|	(5, 'yes', 5.7)
|	set 	|	No	|	Yes	|	{ } or set()	|	{5, 'yes', 5.7}
|	dictionary	|	No	|	Keys: No	|	{ } or dict()	|	{'Jun':75, 'Jul':89}