## 破解学习笔记

> 逆向工程、反汇编入门摸索记录

------

## 警告

- 本笔记仅用于学习研究之用，不得用于任何商业用途，尤其不得把学习所得用于违法犯罪用途！！
- 请认真学习、并遵守当地的法律法规（如《[计算机软件保护条例](http://www.people.cn/zixun/flfgk/item/dwjjf/falv/7/7-2-03.html)》、《[网络安全法](http://www.cac.gov.cn/2016-11/07/c_1119867116.htm)》），勿以身试法！！
- 若触犯法律法规，由此产生的后果由违法者自行负责，本人不承担任何法律责任！！

> 所有献身于安全事业的同学、应以成为遵纪守法的白帽子为傲，为守护一方净土而努力！！


## 前言

因为这门技能的特殊性问题，导致存在各种主观和客观不可描述的原因，使得鄙人在学习破解的路上并没有师傅领进门，过程磕磕碰碰：找不到（浅显易懂的）教程、找不到破解工具（知其名而不知其所用）、找不到练习软件（被黑被格盘），等等都是常有的事。

故作此笔记，把学习过程中挖到的课程、工具、练习题记录在案，以方便日后自己查阅、或他人借鉴。

本笔记均是基于 WinXP-x64 平台进行记录，不必担心教程过时的问题，因为入门主要学习破解思路，先把简单的学会，待有基础积累后，再向 Win7/8/10 等安全系数更高的系统挑战，新手大忌就是贪多不烂。


## 注意

学习破解时，必须在虚拟机下操作，主要原因有二：

- 避免 Windows 平台的 ASLR 基地址随机化问题，使得实操与教程讲解的地址会不一致，造成新手迷惑
- 某些软件有反汇编能力，为了给破解者惩罚，可能会对其电脑进行投毒、甚至对数据进行破坏，必须慎之！

> 关于虚拟机环境搭建，可详见 [此处](vm/)


## 目录导航

```
.
├── vagrant ............... 虚拟机环境构建脚本
│   ├── README.md
│   └── Vagrantfile
├── tools ................. 破解工具集（均基于 WinXP）
│   ├── 01_detect ......... 侦壳工具
│   ├── 02_debugger ....... 调试工具（动态分析）
│   ├── 03_disassembler ... 反编译工具（静态分析）
│   ├── 04_unpacker ....... 脱壳工具
│   ├── 05_patcher ........ 补丁工具
│   ├── 06_packer ......... 加壳工具
│   ├── 07_crptography .... 密码算法相关工具
│   ├── 08_dongle ......... 加密狗相关工具
│   ├── 09_editor ......... 程序资源编辑、文本操作相关工具
│   ├── 10_petool ......... PE 文件逆向相关工具
│   ├── 11_android ........ Android 程序逆向相关工具
│   ├── 12_.net ........... .Net 程序逆向相关工具
│   ├── 13_mac_osx ........ Mac OSX 程序逆向相关工具
│   └── 99_other .......... 其他工具
├── course ................ 破解学习课程
├── training .............. 破解训练题、挑战赛赛题
├── Q&A.md ................ 新手入门百问
└── README.md ............. 本仓库说明
```


> [>> 新手入门百问](Q&A.md)
