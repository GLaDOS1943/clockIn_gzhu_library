# 广州大学GZHU图书馆自动预约座位

## 免责申明

本项目仅做免费的学术交流使用。仅适用于周末天天去图书馆的同学。

## 更新日志

增加新功能：使用pushplus 推送加 微信公众号推送打卡成功与否的消息

## 简介

1. 脚本使用Github Actions实现广州大学GZHU图书馆自动预约座位
2. 使用此脚本需要设置三个Repository secret：XUHAO、MIMA和SEATNO它们的值分别对应你的学号，密码，座位号（1-358）
3. 脚本会在每天早上6点半自动运行，预约次日的座位
4. （可选功能）使用pushplus 推送加 微信公众号推送打卡成功与否的消息 [设置方法](#推送预定成功与否的消息（可选功能）)

## 使用教程

1. 首先把该项目Fork一份（在网页右上角，点Fork前记得顺便**点个Star**哦~）
2. 然后点击如下图所示的地方，也就是你的账号名。

---
![1](./assets/1.png)

---
然后就来到下面这个界面

---
![2](./assets/2.png)

---
请按上图操作，先点Repositories，然后找到自己刚刚Fork的项目，点击。

这样就进入到了你自己Fork的项目，如下图

---
![3](./assets/3.png)

---
按上图中操作

1. 先点Settings按钮
2. 然后点Secrets按钮
3. 之后再点击Secrets的下拉菜单中的Actions，进入Actions secrets界面。

接着继续按下图操作

---
![4](./assets/4.png)

---
上图圈起来的是需要创建的三个Secrets，点击New repository secret进入创建界面，如下图

---
![5](./assets/5.png)

---

- 要创建的第一个Secret的Name为XUHAO，注意XUHAO要大写
- Value是你自己的学号
- 全部输入完成后点击图中圈起来的绿色按钮Add secrect来创建

---

- 接下来是第二个要创建的Secret，Name是MIMA，注意MIMA要大写。
- Value是你自己的密码
- 全部输入完成后点击图中圈起来的绿色按钮Add secrect来创建
---

- 接下来是第三个要创建的Secret，Name是SEATNO，注意SEATNO要大写。
- Value是你自己想预约的座位号（1-358）
- 全部输入完成后点击图中圈起来的绿色按钮Add secrect来创建

继续操作

---
![6](./assets/6.png)

---
如上图先点击Settings按钮左边的Actions按钮,再点击绿色按钮，进入下图界面

---
![7](./assets/7.png)

---
如上图

1. 点击箭头1处蓝色的地方（上图中使用其他人的项目做演示）
2. 点击2处箭头Enable workflow

至此，全部配置完毕，自动预约已经激活了

## 推送预定成功与否的消息（可选功能）

### pushplus 推送加 微信公众号

- 创建一个Repository secret，Name是PUSHPLUS，注意PUSHPLUS要大写。
- Value是pushplus 推送加 的token

## FAQ

### Q: 如果脚本运行失败怎么办？

1. 如果你是第一次运行脚本，请先检查学号密码座位是否输入错误
2. 其它时候大多是因为校园网网络服务问题，可以尝试重新运行脚本

## 特别鸣谢
本项目参考了[广州大学自动打卡](https://github.com/LihaoLikeOrangeJuice/clock-in-gzhu)

感谢作者的开源，本项目也是在此基础上修改而来。
