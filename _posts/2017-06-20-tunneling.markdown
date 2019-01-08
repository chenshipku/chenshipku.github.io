---
layout:     post
title:      "tunneling"
subtitle:   ""
date:       2017-06-20 11:30:00
author:     "陈实"
header-img: "img/in-post/tbi.PNG"
catalog: true
tags:
    -   NSDI
---

&emsp;&emsp;在我之前的印象中，量子隧穿只能发生在微观体系中得到观测，而实际上，量子隧穿可以发生的空间尺度是从飞米到毫米，其温度尺度也是从nK到百千万K。举几个例子，约瑟夫森结中有宏观量子隧穿[PRL 95,010402](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.95.010402)，纳米磁分子中有量子隧穿，核聚变中存在量子隧穿，非序列双电离中也存在量子隧穿。

&emsp;&emsp;每条电离轨道的权重如何确定直接决定了最终的模拟结果。这里介绍下几种不同情况下轨道权重如何确定。

&emsp;&emsp;最简单的是对RII机制主导的NSDI模拟。这种情况下，第一个电子先电离 ，电离后的初始位置(0,0,z)由隧穿理论得到，初始速度为$$(v_p\cos\theta,v_p\sin\theta,0)$$，按理说$$v_p$$应当从0到无穷都有可能，但由于$$v_p$$太大时，隧穿几率太小，所以模拟时只考虑$$v_p\in(0,1)$$。之后隧穿电离与具有确定能量的内层电子（由微正则分布生成）就遵循牛顿定律进行演化。权重W等于第一个电子的纵向速度分布$$w_0$$乘上它的隧穿几率$$w_1$$。

&emsp;&emsp;对于阈下区域，RESI机制主导的NSDI过程，还需要考虑第二个电子的隧穿[PRA 64,043412](https://link.aps.org/doi/10.1103/PhysRevA.64.043412)。当电子到达反转点时，即dz/dt=0(实际处理可限定一个范围，如-0.01到0.01）,$$E\cdot z<0$$,它将具有一定几率穿过势垒。由WKB近似可给出隧穿几率为：

  $$P_{tun}=exp[-2\sqrt{2}\int_{z_i^{in}}^{z_i^{out}}\sqrt{V(z_i)-V(z_i^{in})}dz_i]$$

  其中$$z_i^{in},z_i^{out}$$是方程

  $$V(z_i)=-2/\big |z_i\big |+z_i\epsilon(t)=-2/\big|z_i^{in}\big|+z_i^{in}\epsilon(t)$$

  的两个根(忽略了电子电子之间的库仑作用)，且有

  $$\big|z_i^{in}\big|<\big|\sqrt{2/\epsilon}\big|<\big|z_i^{out}\big|$$

很容易得到，

$$\epsilon>0$$时，$$z_i^{out}=\frac{2}{\epsilon\cdot z_i^{in}}$$;

$$\epsilon<0$$时,$$z_i^{out}=-\frac{2}{\epsilon\cdot z_i^{in}}$$.

下图是隧穿几率随隧穿入口位置的变化曲线，可见隧穿位置靠近核时，势垒过深，隧穿几率可忽略不计。随着隧穿入口向势垒顶端靠近，隧穿几率迅速增加。由此，我在想，高激发态电子的隧穿几率应该是要比低激发态电子的隧穿几率要高得多（高激发态的-2/z小，z大，隧穿几率大）。
![](http://orq05s7wy.bkt.clouddn.com/e2tunnel.PNG)

以上是隧穿电离情况，若是激光场场强足够大，会由隧穿电离转为越势电离。
![](http://orq05s7wy.bkt.clouddn.com/threeionization.PNG)
在
