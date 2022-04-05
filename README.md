## The Missing Course of Your Computer Science Education（2021秋）

- 课程网站：http://jyywiki.cn/ICS/2021/

- teacher: 

  - 王慧妍 why@nju.edu.cn
  - 蒋炎岩 jyy@nju.edu.cn
  - 欧先飞 ouxianfei@smail.nju.edu.cn
  - 屈道涵 whuqdh@126.com

- student: 

  - 刘培杰 lpj@liupj.top

#### 理论课（我还没学完 ！！！）

- 见：[中国大学MOOC](https://www.icourse163.org/)

- 搜索关键词「计算机系统基础、南京大学、袁春风」

#### Linux 入门知识

- [Linux 基本常识](https://linux.cn/article-6160-1.html)

- [Linux 入门教程](https://nju-projectn.github.io/ics-pa-gitbook/ics2021/linux.html)

#### 国外课程（我还没学完 ！！！）

- [The Missing Semester of Your CS Education](https://missing.csail.mit.edu/)

#### 什么是模拟器 ？

![image-20220405155243564](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220405155243564.png)

- 同理，模拟器也是一个程序，它的目标在于：

- 用软件模拟出计算机硬件的一些功能（eg：内存、cache、程序计数器、...），以支持在其上层执行其它程序

- 比如知名虚拟机软件 [virtualbox](https://www.virtualbox.org/) 和 [vmware](https://www.vmware.com/) 均是能够模拟出 pc 主机的软件，我们可以在模拟出的 pc 主机上运行其它操作系统

- 再比如 [NES Emulator](https://www.emulator-zone.com/doc.php/nes/)，是一款可以模拟出[红白机](https://baike.baidu.com/item/%E7%BA%A2%E7%99%BD%E6%9C%BA/4443886)的软件，我们可以在模拟出的红白机上运行各种经典 NES 游戏，比如魂斗罗、超级马里奥、...

#### 本课程的终极目标

- 并不只是让你完成实验（做一个模拟器）

- 更重要的是

  - 让你理解「一个程序在被一步步地（预处理、编译、汇编、链接、执行、完成）的整个过程中，计算机究竟都做了什么」

  - 让计算机执行程序的过程，在我们的眼中不再是黑盒

#### 本课程的实验内容（`P`rogramming `A`ssignment）

- https://nju-projectn.github.io/ics-pa-gitbook/ics2021/

> 制作一个功能完备但简化了的模拟器 NEMU（NJU EMUlator）

- PA1：简易调试器、加法器

- PA2：程序执行

- PA3：cache 与 存储管理

- PA4：异常 与 I/O

#### 小结

![image-20220331233854027](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220331233854027.png)

#### DO NOT ASK

- 安装XXX错了怎么办 ？

- Segmentation Fault 怎么办 ？

#### 另外

- 如果你感觉本实验异常困难，那么其实你需要加强 C/C++ 编程的训练

- 越是独立完成，受到的训练就越好
