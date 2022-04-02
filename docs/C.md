#### 知识铺垫

- https://liupj.top/dev-c-on-linux/

#### 预编译（`#include`、`#define`、`#if`、`#else`、`#endif`、`#`、`##`、`#ifdef`、...）

- #include 就是一种「复制粘贴」～

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
#if aa == bb
	printf("Yes\n"); // 这里输出了 ！这是因为：预编译时，这里的变量 aa 和 bb 无需声明即可使用，初始值都是空，因此二者相等
#else
	printf("No\n");
#endif
}
```
