## 定义函数
```

def cylinder_volume(height, radius):
    pi = 3.14159
    return height * pi * radius ** 2

```
函数头部
我们从函数头部开始，即函数定义的第一行。

函数头部始终以关键字 def 开始，表示这是函数定义。
然后是函数名称（在此例中是 cylinder_volume，因为函数名是要一个单词，所以需要用_进行连接），遵循的是和变量一样的命名规范。你可以在本页面下方回顾下命名规范。
名称之后是括号，其中可能包括用英文逗号分隔的参数（在此例中是 height 和 radius）。形参（或实参）是当函数被调用时作为输入传入的值，用在函数主体中。如果函数没有参数，这些括号留空。
头部始终以英文冒号 : 结束。
函数主体
函数的剩余部分包含在主题中，也就是函数完成操作的部分。

函数主体是在头部行之后缩进的代码。在此例中是定义 π 和返回体积的两行代码。
在此主体中，我们可以引用参数并定义新的变量，这些变量只能在这些缩进代码行内使用。
主体将经常包括 return 语句，用于当函数被调用时返回输出值。return 语句包括关键字 return，然后是经过评估以获得函数输出值的表达式。如果没有 return 语句，函数直接返回 None（例如内置 print() 函数）。
函数的命名规范
函数名称遵守和变量一样的命名规范。

仅在函数名称中使用普通字母、数字和下划线。不能有空格，需要以字母或下划线开头。
不能使用在 Python 中具有重要作用的保留字或内置标识符，我们将在这门课程中学习这方面的知识。要了解 python 保留字列表，请参阅此处。
尝试使用可以帮助读者了解函数作用的描述性名称。
## 变量作用域
变量作用域是指可以在程序的哪个部分引用或使用某个变量。

在函数中使用变量时，务必要考虑作用域。如果变量是在函数内创建的，则只能在该函数内使用该变量。你无法从该函数外面访问该变量。

#### This will result in an error
```
def some_function():
    word = "hello"

print(word)
```
这意味着你可以为在不同函数内使用的不同变量使用相同的名称。

#### This works fine
```
def some_function():
    word = "hello"

def another_function():
    word = "goodbye"
```
像这样在函数之外定义的变量依然可以在函数内访问。

#### This works fine
```
word = "hello"

def some_function():
    print(word)

print(word)
```
注意，我们可以在此函数内以及函数外输出 word。作用域对理解信息在用 Python 和任何编程语言编写的程序中的传递方式来说很关键。

关于变量作用域的更多信息
在编程时，你经常会发现相似的想法不断出现。你将使用变量进行计数、迭代和累积要返回的值。为了编写容易读懂的代码，你会发现你需要对相似的想法使用相似的名称。一旦你将多段代码放到一起（例如，一个脚本中有多个函数或函数调用），你可能需要为两个不同的概念使用相同的名称。

幸运的是，你不需要不断想出新的名称。可以为对象重复使用相同的名称，只要它们位于不同的作用域即可。

良好实践：建议将变量定义在所需的最小作用域内。虽然函数_可以_引用在更大的作用域内定义的变量，但是通常不建议这么做，因为如果程序有很多变量，你可能不知道你定义了什么变量。

## 文档
文档使代码更容易理解和使用。函数尤其容易理解，因为它们通常使用文档字符串，简称 docstrings。文档字符串是一种注释，用于解释函数的作用以及使用方式。下面是一个包含文档字符串的人口密度函数。
```
def population_density(population, land_area):
    """Calculate the population density of an area. """
    return population / land_area
 ```

文档字符串用三个引号引起来，第一行简要解释了函数的作用。如果你觉得信息已经足够了，可以在文档字符串中只提供这么多的信息；一行文档字符串完全可接受，如上述示例所示。

```
def population_density(population, land_area):
    """Calculate the population density of an area.

    INPUT:
    population: int. The population of that area
    land_area: int or float. This function is unit-agnostic, if you pass in values in terms
    of square km or square miles the function will return a density in those units.

    OUTPUT: 
    population_density: population / land_area. The population density of a particular area.
    """
    return population / land_area
```
如果你觉得需要更长的句子来解释函数，可以在一行摘要后面添加更多信息。在上述示例中，可以看出我们对函数的参数进行了解释，描述了每个参数的作用和类型。我们经常还会对函数输出进行说明。

文档字符串的每个部分都是可选的。但是，提供文档字符串是一个良好的编程习惯。你可以在此处详细了解文档字符串惯例。

## Lambda 与 Map

```

map() 是一个高阶内置函数，接受函数和可迭代对象作为输入，并返回一个将该函数应用到可迭代对象的每个元素的迭代器。下面的代码使用 map() 计算 numbers 中每个列表的均值，并创建列表 averages。测试运行这段代码，看看结果如何。

通过将 mean 函数替换为在 map() 的调用中定义的 lambda 表达式，重写这段代码，使代码更简练。

numbers = [
              [34, 63, 88, 71, 29],
              [90, 78, 51, 27, 45],
              [63, 37, 85, 46, 22],
              [51, 22, 34, 11, 18]
           ]

def mean(num_list):
    return sum(num_list) / len(num_list)

averages = list(map(mean, numbers))
print(averages)


练习解决方案：Lambda 与 Map
numbers = [
              [34, 63, 88, 71, 29],
              [90, 78, 51, 27, 45],
              [63, 37, 85, 46, 22],
              [51, 22, 34, 11, 18]
           ]

averages = list(map(lambda x: sum(x) / len(x), numbers))
print(averages) // [57.0, 58.2, 50.6, 27.2]


练习解决方案：Lambda 与 Filter
cities = ["New York City", "Los Angeles", "Chicago", "Mountain View", "Denver", "Boston"]

short_cities = list(filter(lambda x: len(x) < 10, cities))
print(short_cities) // ['Chicago', 'Denver', 'Boston']


练习解决方案：实现 my_enumerate
lessons = ["Why Python Programming", "Data Types and Operators", "Control Flow", "Functions", "Scripting"]

def my_enumerate(iterable, start=0):
    count = start
    for element in iterable:
        yield count, element
        count += 1

for i, lesson in my_enumerate(lessons, 1):
    print("Lesson {}: {}".format(i, lesson))

输出：   
Lesson 1: Why Python Programming
Lesson 2: Data Types and Operators
Lesson 3: Control Flow
Lesson 4: Functions
Lesson 5: Scripting


练习解决方案：Chunker
def chunker(iterable, size):
    """Yield successive chunks from iterable of length size."""
    for i in range(0, len(iterable), size):
        yield iterable[i:i + size]

for chunk in chunker(range(25), 4):
    print(list(chunk))

输出：
[0, 1, 2, 3]
[4, 5, 6, 7]
[8, 9, 10, 11]
[12, 13, 14, 15]
[16, 17, 18, 19]
[20, 21, 22, 23]
[24]
```












