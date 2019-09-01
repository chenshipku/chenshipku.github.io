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

## 隧穿现象
量子隧穿可以发生的空间尺度是从飞米到毫米，其温度尺度也是从nK到百千万K。例如，约瑟夫森结中有宏观量子隧穿[PRL 95,010402](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.95.010402)，纳米磁分子中有量子隧穿，核聚变中存在量子隧穿，非序列双电离中也存在量子隧穿。

## 隧穿几率

### 静电场 & 氢原子基态
朗道早已在《量子力学》中用WKB近似方法给出了静电场下氢原子电子隧穿几率的表达式，现简述如下。

在静电场与库仑场复合场作用下，有

$$(\frac{1}{2}\Delta+I_p+\frac{1}{r}-\epsilon\cdot z)\Psi=0\ (I_p<0)$$

在抛物线坐标系下，

$$x=\sqrt{\xi\eta}cos\phi,\ y=\sqrt{\xi\eta}sin\phi,\ z=\frac{\xi-\eta}{2},\ r=\sqrt{x^2+y^2+z^2}$$

$$\xi=r+z,\ \eta=r-z,\ \phi=tan^{-1}(y/x)$$

$$\frac{4}{\xi+\eta}[\frac{\partial}{\partial\xi}(\xi\frac{\partial\Psi}{\partial\xi})+\frac{\partial}{\partial\eta}(\eta\frac{\partial\Psi}{\partial\eta})]+\frac{1}{\xi\eta}\frac{\partial^2\Psi}{\partial\phi^2}+[2I_p+\frac{4}{\xi+\eta}-\epsilon(\eta-\xi)]\Psi=0$$

将$$\Psi$$写成分离变量的形式$$\Psi=f_1(\xi)f_2(\eta)e^{im\phi}=\frac{\chi_1(\xi)}{\chi_2(\eta)}e^{im\phi}$$，就可以分离变量为

$$\frac{d^2{\chi_1}}{d\xi^2}+(\frac{I_p}{2}+\frac{\beta_1}{\xi}-\frac{m^2-1}{4\xi^2}-\frac{\epsilon}{4}\xi)\chi_1=0$$

$$\frac{d^2{\chi_2}}{d\eta^2}+(\frac{I_p}{2}+\frac{\beta_2}{\eta}-\frac{m^2-1}{4\eta^2}+\frac{\epsilon}{4}\eta)\chi_2=0$$

其中$$\beta_1+\beta_2=1$$,当电场强度$$\epsilon>0$$时向$$\eta$$方向隧穿；$$\epsilon<0$$时向$$\xi$$方向隧穿。

隧穿几率

$$w=\int_0^\infty \left|\Psi\right|^2v_z2\pi\rho d\rho$$

其中$$\rho=\sqrt{x^2+y^2}=\sqrt{\xi\eta},\ v_z\approx\sqrt{2(-\frac{1}{2}+\frac{1}{2}\epsilon\eta)}=\sqrt{\epsilon\eta-1}$$

对于基态氢原子，有$$I_p=-\frac{1}{2},\ m=0,\ \beta_1=\beta_2=\frac{1}{2}, \psi_{g.s.}=\frac{1}{\sqrt{\pi}}e^{-\frac{1}{2}(\xi+\eta)}$$

以$$\epsilon>0$$为例，在$$\eta$$方向隧穿。当$$\eta>\eta_0(1\ll\eta_0\ll\frac{1}{\epsilon})$$时，按照WKB近似，波函数是准经典的:

$$\chi=\frac{C}{\sqrt{p}}exp(i\int_{\eta_0}^\eta pd\eta+\frac{1}{4}i\pi)$$

其中$$p(\eta)=\sqrt{-\frac{1}{4}+\frac{1}{2\eta}+\frac{1}{4\eta^2}+\frac{\epsilon\eta}{4}}.$$

认为$$\eta<\eta_0$$时，波函数为基态波函数，根据连续条件($$\eta=\eta_0,\psi=\psi_{g.s.}$$)，可以得到系数C，于是有

$$\chi=(\frac{\eta_0\left| p_0\right|}{\pi p})^{\frac{1}{2}}exp(-\frac{\xi+\eta_0}{2}+i\int_{\eta_0}^\eta pd\eta+\frac{1}{4}i\pi)$$

$$\left|\chi\right|^2=\frac{\eta_0\left| p_0\right|}{\pi p}exp(-\xi-2\int_{\eta_0}^{\eta_1}\left| p\right|d\eta -\eta_0)$$

其中$$p(\eta_1)=0.$$

当$$\eta\gg 1$$时，

$$p\approx\frac{1}{2}\sqrt{\epsilon\eta-1},\ \left| p_0\right|\approx \frac{1}{2},\ \eta_1\approx\frac{1}{\epsilon}.$$

$$\left|\chi\right|^2=\frac{4}{\pi\epsilon\sqrt{\epsilon\eta-1}}exp(-\xi-\frac{2}{3\epsilon})$$

$$w=\int_0^\infty \left| \chi\right|^2\pi\sqrt{\epsilon\eta-1}d\xi=\frac{4}{\epsilon}exp(-\frac{2}{3\epsilon})$$

上式就是注明的静电场下氢原子电子隧穿几率公式，之后推导的公式在静电场加氢原子体系下应当回归到这个公式。

另外，上述推导过程还可以得到隧穿出口位置。以$$\eta$$方向隧穿为例，分离变量后有如下形式：

$$\frac{d^2\Psi}{dx^2}+2(\frac{I_p}{4}-U)$$

$$U(\eta)=-\frac{\beta_2}{2\eta}+\frac{m^2-1}{8\eta^2}-\frac{\epsilon}{8}\eta$$

沿隧穿方向根据$$\frac{I_p}{4}=U(\eta_0)$$可得$$\eta_0$$，垂直隧穿方向有$$\xi_0=0$$，抛物坐标系换到直角坐标系有

$$x=\frac{\xi\eta}cos\phi=0,\ y=\sqrt{\xi\eta}sin\phi=0,\ z=\frac{\xi-\eta}{2}=-\frac{\eta_0}{2}$$

即隧穿位置为$$(0,0,-\frac{\eta_0}{2})$$

### 静电场 & 氢原子任意束缚态
一般的，处于任意束缚态的电子隧穿几率为

$$w=C_{n^* l}^2E\frac{(2l+1)(l+\left|m\right|)}{2^{\left|m\right|}(\left|m\right|)!(l-\left|m\right|)!}(\frac{2\epsilon_0}{\epsilon})^{2n^* -\left|m\right|-1}exp(-\frac{2\epsilon_0}{3\epsilon})$$

以氢原子为例，基态时有$$E=\frac{1}{2},\ n^* =1,\ l=m=0,\ C_{n^* l}^2=\frac{2^{2n^* }}{n^* (n^* +l)!(n^* -l-1)!}=4$$

有$$w=\frac{4}{\epsilon}exp(-\frac{2}{3\epsilon})$$，回归到朗道隧穿几率公式。

### ADK隧穿几率
在$$n^* \gg l$$时，有$$C_{n^* l}=(\frac{2e}{n^* })^{n^* }\frac{1}{(2\pi n^* )^{1/2}}$$，带入上面的隧穿几率表达式即可得ADK隧穿几率表达式

$$w_{ADK}=\frac{\epsilon}{8\pi Z}(\frac{4eZ^3}{\epsilon n*^4})^{2n^* }(\frac{2Z^3}{\epsilon n*^3})^{-\left|m\right|}\frac{(2l+1)(l+\left|m\right|)}{2^{\left|m\right|}(\left|m\right|)!(l-\left|m\right|)!}exp(-\frac{2Z^3}{3n*^3\epsilon})$$

对于s态电子，有

$$w_{ADK_s}=\frac{\epsilon D^2}{8\pi Z}exp(-\frac{2(I_p)^{3/2}}{3\epsilon})$$

其中$$D=(\frac{4eZ^3}{\epsilon n*^4})^{n*},\ I_p=E=\frac{Z^2}{2n*^2}$$
### 绝热效应


### 分子隧穿几率
