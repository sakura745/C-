### 1.语句基础
表达式加分号。

复合语句：由大括号组成，无需在结尾加分号，形成独立的域（明确变量的生存周期）

顺序和非顺序语句

最基本的非顺序语句是`goto`

### 2.分支语句
#### if
包含分支是一整条语句，多条`if else`嵌套，可实现多重分支。`if ... else if ...`是嵌套出来的。

`constexpr if`可以优化程序，在编辑期进行分支，而非运行期

if还可以带初始化语句

#### switch
条件为可以隐式转换为整形或枚举类型的变量，可以包含初始化语句

`case/default`标签

### 3.循环语句
#### while
while中不包含初始化语句

#### do while
循环结尾要有分号，同样不包含初始化。

#### for
可在初始化中包含多个声明，但需要确保每个声明类型相同。如`int a, b;`

`int a, double b;`这种语句非法。而且，`int* p ,q;`表示q为非指针，容易引起误解。`int* p, *q;`为指针。

除了for中初始化，不建议将多个声明一起初始化。

for的条件可为空

#### range-for
语法糖，编译器会自动将该range-for转为for循环。详见c++ insights

只读元素时，可使用左值引用；写元素时，建议使用万能引用

#### break，continue
前者是终止循环，后者是跳过循环体剩余部分，执行下一次循环。（不适用于多重循环）

可使用goto跳转于多重循环

### 4.达夫设备
将switch和循环相结合。