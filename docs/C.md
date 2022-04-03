#### 知识铺垫

- https://liupj.top/dev-c-on-linux/

#### 深入了解预编译过程中的「复制粘贴」

![image-20220402093422109](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220402093422109.png)

- 以下代码有什么区别 ？

```c
#include <stdio.h>
#include "stdio.h"

使用 gcc 编译时，添加 --verbose 编译选项，会发现二者默认搜索的路径不一样

#include "..." 搜索从这里开始：
#include <...> 搜索从这里开始：
  /usr/lib/gcc/x86_64-pc-linux-gnu/11.2.0/include
  /usr/local/include
  /usr/lib/gcc/x86_64-pc-linux-gnu/11.2.0/include-fixed
  /usr/include
搜索列表结束。
```

- --verbose 查看编译日志的方法真的很有用 ！

![image-20220402161801154](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220402161801154.png)

- 以下代码会输出什么 ？为什么 ？

```c
#include <stdio.h>

int main() {
#if aa == bb				// 预编译时，这里的变量 aa 和 bb 无需声明即可使用，初始值都为空，因此二者确实相等
	printf("Yes\n");	// 因此这里会输出 ！
#else
	printf("No\n");
#endif
}
```

- 以下代码会输出什么 ？为什么 ？

```c
#include <stdio.h>

int main() {
#ifdef __x86_64__
	printf("__x86_64__\n");	// gcc curFile.c				&& ./a.out => 输出本行
#else
	printf("X86\n");				// gcc curFile.c -m32		&& ./a.out => 输出本行
#endif
}
```

- 知乎问题：如何搞垮一个 OJ ？

```c
#define TEN(X) X X X X X X X X X X
#define A "aaaaaaaaaa"
#define B TEN(A)
#define C TEN(B)
#define D TEN(C)
#define E TEN(D)
#define F TEN(E)
#define G TEN(F)
int main() {
	puts(G);
}
```

- 某些 Online Judge 平台不允许用户调用系统的 API，有没有什么 hack 的方法躲过 OJ 的关键字检测 ？

```c
#define A sys ## tem // ## 可以将其左右两侧的字符串连接起来
int main() {
	A("echo Hello\n");
}
```

- 如何毁掉一个身边的同学 ？

```c
#define true (__LINE__ % 2 != 0)

#include <stdio.h>

int main() {
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
  if (true) printf("%d\n", __LINE__);
}
```

#### 妙用 -E 编译选项

> 这种难以用肉眼进行宏展开的源代码，可以用 -E 选项帮助我们进行宏展开

![image-20220403101039458](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220403101039458.png)

#### 加深理解

- 宏展开，通过「复制/粘贴」改变代码的形态

- 反复粘贴，直到没有宏可以展开为止

- X-macros

```c
#define PRINT(x) puts("Hello, " #x "!");
#define NAMES(A) \
	A(Tom) A(Jerry) A(Tyke) A(Spike)

int main() {
	NAMES(PRINT);
}
```

> 类似这种（封装 & 复用）的思想在实际编码工作中很常用 ！

#### 元编程

- 类似上述利用宏定义宏展开编写源代码，配合预编译的方式也叫元编程（meta-programming）

	- gcc 的预处理器也可以处理汇编代码

	- c++ 中的模板元编程、Rust 中的 macros、...

- 优点

	1. 提供更为灵活的用法（X-macros）

	2. 接近自然语言的写法

- 缺点

	破坏代码的可读性，在代码分析和补全方面增加困难度

```c
#define L (
int main L) { puts L "Hello" ); }
```

