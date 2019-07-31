# 面试题

## Python 函数调用的时候参数的传递方式是值传递还是引用传递？

Python 的参数传递有：位置参数、默认参数、可变参数、关键字参数。

函数的传值到底是值传递还是引用传递，要分情况：

* 不可变参数用值传递：

> 像整数和字符串这样的不可变对象，是通过拷贝进行传递的，因为你无论如何都不可能在原处改变 不可变对象。

* 可变参数是引用传递的：

> 比如像列表，字典这样的对象是通过引用传递、和 C 语言里面的用指针传递数组很相似，可变对象能在函数内部改变。

## 对缺省参数的理解？

> 缺省参数指在调用函数的时候没有传入参数的情况下，调用默认的参数，在调用函数的同时赋值时，所传入的参数会替代默认参数。

**args 是不定长参数**，他可以表示输入参数是不确定的，可以是任意多个。 __

**\*kwargs 是关键字参数**，赋值的时候是以键 = 值的方式，参数是可以任意多对

在定义函数的时候不确定会有多少参数会传入时，就可以使用两个参数。

## 为什么函数名字可以当做参数用?

Python 中一切皆对象，函数名是函数在内存中的空间，也是一个对象。

## Python 中 pass 语句的作用是什么？

在编写代码时只写框架思路，具体实现还未编写就可以用 pass 进行占位，使程序不报错，不会进 行任何操作。

## 有这样一段代码，print c 会输出什么，为什么？

```python
a = 10
b = 20
c = [a]
a = 15
```

答：10 对于字符串、数字，传递是相应的值。
