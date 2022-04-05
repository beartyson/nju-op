## The Missing Course of Your Computer Science Education（2021秋）

- 课程网站：http://jyywiki.cn/ICS/2021/

- teacher: 王慧妍@nju.edu.cn

- student: 刘培杰@liupj.top

#### 先修课

- [Linux 基本常识](https://linux.cn/article-6160-1.html)

- [Linux 入门教程](https://nju-projectn.github.io/ics-pa-gitbook/ics2021/linux.html)

- [The Missing Semester of Your CS Education](https://missing.csail.mit.edu/)

#### 什么是模拟器 ？

![image-20220405155243564](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220405155243564.png)

- 同理，模拟器也是一个程序，它的目标在于：

- 用软件模拟出计算机硬件的一些功能（eg：内存、cache、程序计数器、...），以支持在其上层执行其它程序

- 比如知名虚拟机软件 [virtualbox](https://www.virtualbox.org/) 和 [vmware](https://www.vmware.com/) 均是一个能够模拟出 pc 主机的软件，我们可以在模拟出的 pc 主机上运行其它操作系统

- 再比如 [NES Emulator](https://www.emulator-zone.com/doc.php/nes/)，是一款可以模拟出[红白机](https://baike.baidu.com/item/%E7%BA%A2%E7%99%BD%E6%9C%BA/4443886)的软件，我们可以在模拟出的红白机上运行各种经典 NES 游戏，比如魂斗罗、超级马里奥、...

#### 本课程的实验内容（`P`rogramming `A`ssignment）

- https://nju-projectn.github.io/ics-pa-gitbook/ics2021/

> 制作一个功能完备的简化模拟器 NEMU（NJU EMUlator）

![image-20220331233854027](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220331233854027.png)

#### Linux

![image-20220331234923555](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220331234923555.png)

#### 常见的命令行工具

![image-20220331235953382](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220331235953382.png)

#### > 重定向

![image-20220331235723557](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220331235723557.png)

#### UNIX 哲学

![image-20220401000153425](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220401000153425.png)

#### The Shell Scripting Language

```bash
#!/bin/sh

a=1
b=2

if [ $a != $b ]
  then
    echo "a is not equal to b"
fi

if [ $a > $b ]
  then
    echo "no"
fi
```
