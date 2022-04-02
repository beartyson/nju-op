#### 知识铺垫

- https://liupj.top/dev-c-on-linux/

#### 预编译（`#include`、`#define`、`#`、`##`、`#ifdef`、...）

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

