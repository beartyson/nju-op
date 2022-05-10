
> 此书为听课笔记。

#### 注意

- 越是**独立完成**，受到的训练就越好

- 禁用百度，禁用中文 => Add `127.0.0.1 www.baidu.com`

  - For Unix => /etc/hosts
  - For Windows => C:\Windows\System32\drivers\etc\hosts

- 拥抱开源社区
  - [github](https://github.com/), [awesome-of-github](https://github.com/search?q=awesome)
  - [stackoverflow](https://stackoverflow.com/)
  - ...

- 如果你感觉本实验异常困难，那么其实你需要加强编程的训练（eg：C/C++）

#### 实验进度

- [x] PA0：一些预备知识和准备工作
- [ ] PA1：简易调试器、加法器
- [ ] PA2：程序执行
- [ ] PA3：cache 与 存储管理
- [ ] PA4：异常 与 I/O

#### 资源

- [课程网站](http://jyywiki.cn/ICS/2021/)
- [实验内容（Programming Assignment）](https://nju-projectn.github.io/ics-pa-gitbook/ics2021/)
- [前导理论课 | MOOC（计算机系统基础、南京大学、袁春风）](https://www.icourse163.org/)
- [精彩工具课 | The Missing Semester of Your CS Education](https://missing.csail.mit.edu/)

#### 本课程的终极目标

- 通过制作一个功能完备但简化了的模拟器 NEMU（NJU EMUlator），让你理解「一个程序在被一步步地（预处理、编译、汇编、链接、执行、完成）的整个过程中，计算机究竟都做了什么」

- 让计算机执行程序的过程，在我们的眼中不再是黑盒

![image-20220510122321626](https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220510122321626.png)

#### 什么是模拟器 ？

- 支付宝是一个程序，它的目标在于：用软件模拟出 ATM 机的功能（eg：存款、取款、转帐、汇款、...）

  <img src="https://aliyun-oss-lpj.oss-cn-qingdao.aliyuncs.com/images/by-picgo/image-20220405190312821.png" width=400 />

- 同理，模拟器也是一个程序，它的目标在于：用软件模拟出计算机硬件的一些功能（eg：内存、cache、程序计数器、...），以支持在其上层执行其它程序

  - 比如知名虚拟机软件 [virtualbox](https://www.virtualbox.org/) 和 [vmware](https://www.vmware.com/) 均是能够模拟出 pc 主机的软件，我们可以在模拟出的 pc 主机上运行其它操作系统

  - 再比如 [NES Emulator](https://www.emulator-zone.com/doc.php/nes/)，是一款可以模拟出[红白机](https://baike.baidu.com/item/%E7%BA%A2%E7%99%BD%E6%9C%BA/4443886)的软件，我们可以在模拟出的红白机上运行各种[经典 NES 游戏](https://github.com/Brannua/nes-games)，比如魂斗罗、超级马里奥（Mario）、...
