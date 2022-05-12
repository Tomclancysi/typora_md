---
layout: post
title:remote sensor with ai
---



![image-20211201140927356](pics/image-20211201140927356.png)

![image-20211201140843556](pics/image-20211201140843556.png)

- ![image-20211201141307368](pics/image-20211201141307368.png)

- ![image-20211201141423879](pics/image-20211201141423879.png)

- ![image-20211201141604288](pics/image-20211201141604288.png)

智能解译 重要目标的识别

- ![image-20211201141719385](pics/image-20211201141719385.png)
  - 空间分辨率提高后，解析更方便

- ![image-20211201141842472](pics/image-20211201141842472.png)
  - 十年工作的挑战

- ![image-20211201141907040](pics/image-20211201141907040.png)

- ## 挑战一 旋转不变性

![image-20211201142023438](pics/image-20211201142023438.png)

- ## 挑战二 不是简单的aabb包围框

![image-20211201142126214](pics/image-20211201142126214.png)

- ## 挑战三  无监督学习 不能精细标注

- ![image-20211201142245744](pics/image-20211201142245744.png)

- ## 挑战四 小样本

- ![image-20211201142347344](pics/image-20211201142347344.png)

- ## 挑战五 视角单一

- ![image-20211201142449840](pics/image-20211201142449840.png)

# 解决方案

## 挑战1 旋转

![image-20211201142636392](pics/image-20211201142636392.png)

![image-20211201142910911](pics/image-20211201142910911.png)

## 挑战2 旋转候选框

![image-20211201142945094](pics/image-20211201142945094.png)

![image-20211201143144935](pics/image-20211201143144935.png)

![image-20211201143249949](pics/image-20211201143249949.png)

![image-20211201143313266](pics/image-20211201143313266.png)

## 挑战3 弱监督

![image-20211201143422316](pics/image-20211201143422316.png)

![image-20211201143542153](pics/image-20211201143542153.png)

## 挑战4 小样本

![image-20211201143645960](pics/image-20211201143645960.png)

![image-20211201143722580](pics/image-20211201143722580.png)

![image-20211201143825372](pics/image-20211201143825372.png)

![image-20211201143914337](pics/image-20211201143914337.png)

## 挑战4 视角太少

![image-20211201144012957](pics/image-20211201144012957.png)

# 十年的感悟 和 展望

![image-20211201144207774](pics/image-20211201144207774.png)

![image-20211201144354117](pics/image-20211201144354117.png)

## 小目标检测识别

![image-20211201144501429](pics/image-20211201144501429.png)

**不同来源的数据结合起来，迁移学习** 在大数据量里炼丹用到小数据量

![image-20211201144608181](pics/image-20211201144608181.png)

![image-20211201144648072](pics/image-20211201144648072.png)
