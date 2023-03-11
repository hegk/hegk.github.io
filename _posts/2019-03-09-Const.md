---
layout: post
title: const简析
date: 2019-03-09 12:00:00.000000000 +08:00
---

这个const，在各个位置上的的修饰作用真的是一直傻傻分不清，整理一下

#### const含义：

只要一个变量前用const来修饰，意味着该变量里的数据只能被访问，不允许被修改，产生静态作用，在一定程度上提高程序的安全性和可靠性。
规则：const离谁近，谁就不能被修改；

	const修饰的数据类型是常类型，常类型的变量或者对象的值是不能被修改的；
	const修饰一个变量时，一定要给这个变量初始化，若不初始化，在后面也不能初始化。

#### const作用：

	·可以用来定义const常量，具有不可变性，且被const修饰的东西，都受到强制保护，可以预防其它代码无意识的进行修改； 
	·使编译器保护那些不希望被修改的参数，防止无意代码的修改，减少bug；
	·便于类型检查，避免模糊意义的数字出现，同宏定义一样可以做到一变皆变，方便进行参数的调整修改
	·可以节省内存空间提升效率
	
	
#### const的使用分析：

##### · const在前面
>const int nValue； //int是const

>const char *pContent; //char是const, pContent可变

>const char* const pContent; //pContent和*pContent都是const

##### · const在后面，与上面的声明对等

>int const nValue; //nValue是const

>char const * pContent; //*pContent是const, pContent可变

>char* const pContent; //pContent是const,*pContent可变

>char const* const pContent; //pContent和*pContent都是const

##### 分析：

	1、const只修饰其后的变量，至于const放在类型前还是类型后并没有区别。如：const int a和int const a都是修饰a为const。注意*不是一种类型，如果*pType之前是某类型，那么pType是指向该类型的指针

	1、const在*前面就表示const作用于p所指向的量，此时p所指向的是个常量。

	2、const在*后面，表示p本身是常量，但是p指向的不一定是常量

