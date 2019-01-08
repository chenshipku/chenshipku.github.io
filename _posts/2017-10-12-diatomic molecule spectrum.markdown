---
layout:     post
title:      "双原子分子的振动和转动光谱"
subtitle:   ""
date:       2017-10-12 22:00:00
author:     "陈实"
header-img: ""
catalog: true
tags:
    - AMO
---

# 电子能

假设原子核和电子是质点，忽略自旋-轨道相互作用，则多原子分子的哈密顿量为：

$$\hat{H}=-\frac{\hbar^2}{2m}\sum_i \nabla_i^2-\frac{\hbar^2}{2}\sum_\alpha\frac{1}{m_\alpha}\nabla_\alpha^2+\sum_\alpha\sum_{\beta>\alpha}\frac{Z_\alpha Z_\beta e^2}{r_{\alpha \beta}}-\sum_\alpha\sum_{i}\frac{Z_\alpha e^2}{r_{i\alpha}}+\sum_i\sum_{i>j}\frac{e^2}{r_{ij}}$$

依次为电子动能，核动能，核间静电排斥能，核-电子静电吸引能，电子间静电排斥能。这个哈密顿量太麻烦，解不了。所以先采取波恩-奥本海默近似，即把核看成是固定不动，略去核的动能项，并且核的排斥能是常数，不影响电子波函数。于是便可得到纯电子的哈密顿量：

 $$\hat{H_e}=-\frac{\hbar^2}{2m}\sum_i \nabla_i^2-\sum_\alpha\sum_{i}\frac{Z_\alpha e^2}{r_{i\alpha}}+\sum_i\sum_{i>j}\frac{e^2}{r_{ij}}$$

 相应的薛定谔方程为

 $$\hat{H_e}\Psi_e=E_e\Psi_e$$

 其中$$E_e$$为纯电子能量，总能量还要加上核排斥能$$U=E_e+V_N$$。
 最简单的例子是氢分子离子$$H_2^+$$,有

 $$\hat{H_e}=-\frac{\hbar^2}{2m}\sum\nabla^2-\frac{e^2}{r_1}-\frac{e^2}{r_2}$$   

 $$V_N=\frac{e^2}{R}$$

 假定分子轨道由原子轨道线性组合得到(LCAO-MO)

 $$\Psi_e=C_1\Psi_1+C_2\Psi_2$$

 $$\Psi_1=\sqrt{\frac{1}{\pi a^3}}e^{-r_1/a}$$

 $$\Psi_2=\sqrt{\frac{1}{\pi a^3}}e^{-r_2/a}$$

 $$U=\frac{<\Psi_e|\hat{H_e}+V_N|\Psi_e>}{<\Psi_e|\Psi_e>}$$

 由变分原理$$\frac{\partial U}{\partial C_1}=0,\frac{\partial U}{\partial C_1}=0$$可得

 $$\Psi_e^1=\frac{\Psi_1+\Psi_2}{\sqrt{2+2S_{12}}};U^1=\frac{H_{11}+H_{12}}{1+S_{12}}$$

 $$\Psi_e^2=\frac{\Psi_1-\Psi_2}{\sqrt{2-2S_{12}}};U^2=\frac{H_{11}-H_{12}}{1-S_{12}}$$

 其中$$S_{12}=<\Phi_1|\Phi_2>;H_{11}=<\Psi_1|\hat{H_e}+V_N|\Psi_1>;H_{12}=<\Psi_1|\hat{H_e}+V_N|\Psi_2>$$
 前者在两质子之间也有电子波函数分布，是稳定存在的共价键；后者两质子之间的电子分布很少，两质子互相排斥，是不稳定的态。另外需要注意，我们这样得到的势能函数U只依赖于核间距R。

# 双原子分子作为刚性转子
考虑最简单的刚性转子模型，核间距为定值，分子的势能是常数，所以仅需考虑两个原子的动能项。可以通过坐标变换转化为单体问题，即用质心坐标和相对坐标代替两个原子各自的坐标。于是哈密顿量可写为$$\hat{H}=\hat{H_M}+\hat{H_\mu}$$,$$\hat{H_M}=\frac{\hat{P_M}}{2M}$$代表整个分子的平动，取分子质心为坐标原点，则可不用考虑该项，只是把平动能从总能量中减去，不影响转动波函数。$$\hat{H_\mu}=\frac{\hat{P_\mu^2}}{2\mu}$$代表分子转动，式中折合质量$$\mu=\frac{m_am_b}{m_a+m_b}=-\frac{\hbar^2}{2\mu}\nabla^2$$。

分子质心坐标系下用球坐标表示的拉普拉斯算符为：

$$\nabla^2=\frac{\partial^2}{\partial R^2}+\frac{2}{R}\frac{\partial}{\partial R}+\frac{1}{R^2}ctag\theta\frac{\partial}{\partial \theta}+\frac{1}{R^2\sin^2\theta}\frac{\partial^2}{\partial \psi^2}$$

对刚性转子，R=d=const,所以哈密顿量为

$$\hat{H}=-\frac{\hbar^2}{2\mu d^2}[\frac{1}{\sin\theta^2}\frac{\partial}{\partial\theta}(\sin\theta\frac{\partial}{\partial \theta})+\frac{1}{\sin^2\theta}\frac{\partial^2}{\partial\psi^2}]=\frac{1}{2\mu d^2}\hat{L}^2$$

其中$$\hat{L}$$ 为角动量算符，实际上可以利用$$H=\frac{L^2}{2I}$$（I为转动惯量）直接写出哈密顿量的表达式。$$\hat{L}^2$$的本征函数是球谐函数，用J代表分子的转动角动量量子数，M代表磁量子数，则有：

$$\frac{1}{2\mu d^2}\hat{L}^2Y_J^M(\theta,\psi)=\frac{1}{2\mu d^2}J(J+1) \hbar^2 Y_J^M(\theta,\psi)$$

$$E=\frac{J(J+1)\hbar^2}{2\mu d^2}=J(J+1)\hbar B\ \ (J=0,1,2,...,M=0,\pm1,...,\pm J)$$

其中转动常数$$B=\frac{\hbar}{8\pi^2I}$$。

转子的本征函数有一些规律，如J=M时是$$\theta=90^\circ$$的八字形，M=0时是$$\theta=0^\circ$$的八字形。

# 双原子分子作为振动转子
实际情况中，原子间距R是变化的，分子势能项$$U(R)$$也不是常数，需要考虑。下面我们就考虑小振动情况下的振动转子模型。同上，采用质心坐标系，除去平动项，有：

$$[-\frac{\hbar^2}{2\mu}\nabla^2+U(R)]\Psi_N=E\Psi_N$$

对核运动波函数进行径向角向分离变量$$\Psi_N=F(R)Y_J^M(\theta,\psi)$$,可得

$$[-\frac{\hbar^2}{2\mu}(\frac{\partial^2}{\partial R^2}+\frac{2}{R}\frac{\partial}{\partial R})+\frac{\hbar^2}{2\mu R^2}J(J+1)+U(R)]F(R)=EF(R)$$

作变换

$$G(R)=R\cdot F(R)$$

并将U在平衡位置$$R_e$$附近展开（小振动）

$$U(R)=U(R_e)+\frac{1}{2}k_eq^2$$

$$\frac{1}{(q+R_e)^2}=\frac{1}{R_e^2}$$

其中$$q=R-R_e,k_e=U^"(R_e)$$，可得

$$-\frac{\hbar^2}{2\mu}G^"(q)+[\frac{J(J+1)\hbar^2}{2\mu R_e^2}+U(R_e)+\frac{1}{2}k_eq^2-E]G(q)=0$$

$$-\frac{\hbar^2}{2\mu}G^"(q)+[\frac{1}{2}k_eq^2-W]G(q)=0$$

其本征波函数

$$G_\nu(q)=(\frac{\alpha}{\pi})^{1/4}\frac{1}{(2^\nu \nu !)^{1/2}}H_\nu(\alpha^{1/2}q)e^{-1/2\alpha q^2}$$

$$H_\nu$$为厄米多项式，$$\alpha=\frac{4\pi^2\nu_e\mu}{h}$$

本征值（振动能量）为

$$W=(\nu+1/2)h\nu_e$$

总结一下，核的运动波函数

$$\Psi_N=\frac{G_\nu(q)}{R}\cdot Y_J^M(\theta,\psi)$$

除平动能之外的分子能量

$$E=U(R_e)+(\nu+1/2)h\nu_e+J(J+1)\hbar B_e$$

对于氢分子基态，$$U_e=-31.9eV,h\nu_e=0.5eV,\hbar B_e=8\times 10^{-3}eV$$,分别对应可见光谱/紫外光谱，红外光谱，微波谱。

# 定态微扰法修正能量

上一节中，由于采用小振动模型，对$$U(R),\frac{1}{(q+R_e)^2}$$做了近似，可用定态微扰法对能量进行修正。微扰算符

$$\hat{H}'=aq+bq^2+cq^3+dq^4$$

$$a=-\frac{2J(J+1)hB_e}{R_e}$$

$$b=-\frac{3J(J+1)hB_e}{R_e^2}$$

$$c=\frac{1}{6}U^{'"}(R_e)$$

$$d=\frac{1}{24}U^{""}(R_e)$$

处理过程不写了，在教材上能找到，最后可以得到双原子分子除平动能以外的总能量：

$$E=U(R_e)+h\nu_e(\nu+\frac{1}{2})+hB_eJ(J+1)-h\nu_e\chi_e(\nu+\frac{1}{2})^2-h\alpha_e(\nu+\frac{1}{2})J(J+1)-h\bar{D_e}J^2(J+1)^2+hY_{00}$$

第一项是平衡电子能$$U(R_e)=E_e(R_e)+\frac{Z_aZ_be^2}{R_e}$$

第二项是振动能

第三项是转动能

第四项是振动能级的非谐性效应，是U偏离谐振子势能（抛物线）的结果，$$\nu_e\chi_e$$被称为非谐性系数，大部分情况下该系数为正，降低了振动能级，且随$$\nu$$增加而增加，使得振动能级的间隔越来越小，能级越来越密。

$$\nu_e\chi_e=\frac{B_e^2R_e^4}{4h\nu_e^2}[\frac{10B_eR_e^2[U^{'"}(R_e)]^2}{3h\nu_e}-U^{""}(R_e)]$$

第五项是转动振动的相互作用，$$\alpha_e$$被称为振动-转动耦合常数。

$$\alpha_e=-\frac{2B_e^2}{\nu_e}[\frac{2B_eR_e^3U^{'"}(R_e)}{h\nu_e^2}+3]$$

第六项是离心畸变，转动加快时(J变大)，离心作用使核间距变大，有效转动惯量变大，转动能级比刚性转子降低。但此项很小。

$$\bar{D_e}=\frac{4B_e^3}{\nu_e^2}$$

最后一项是常数项。

$$Y_{00}=\frac{B_e^2R_e^4}{16h\nu_e^2}[U^{""}(R_e)-\frac{4B_eR_e^2[U^{'"}(R_e)]^2}{9h\nu_e^2}]$$
