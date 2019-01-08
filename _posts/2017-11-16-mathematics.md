---
layout:     post
title:      "数学基础"
subtitle:   ""
date:       2017-11-16 11:00:00
author:     "陈实"
header-img: ""
catalog: true
tags:
    - 基础知识
---

# 矢量运算
## 矢量多重积和混合积
$$A\cdot(B\times C)=C\cdot(A\times B)=B\cdot(C\times A)$$

$$A\times(B\times C)=B\cdot (A\cdot C)-C\cdot (A\cdot B)$$

$$(A\times B)\cdot(C\times D)=(A\cdot C)(B\cdot D)-(A\cdot D)(B\cdot C)$$

$$A\times[B\times(C\times D)]=B[A\cdot(C\times D)]-(C\times D)(A\cdot B)$$

证明：

$$
\begin{equation*}
\begin{aligned}
A\times(B\times C)&=\hat{e_i}\epsilon_{ijk}A_j(B\times C)_k\\
&=\hat{e_i}\epsilon_{ijk}A_j\epsilon_{klm}B_lC_m\\
&=\hat{e_i}A_jB_lC_m\epsilon_{kij}\epsilon_{klm}\\
&=\hat{e_i}A_jB_lC_m(\delta_{il}\delta_{jm}-\delta_{im}\delta_{jl})\\
&=\hat{e_i}B_iA_jC_j-\hat{e_i}C_iA_jB_j\\
&=B(A\cdot C)-C(A\cdot B)
\end{aligned}
\end{equation*}
$$

## 矢量的微分运算
引入梯度算符(读作nabla)

$$
\begin{equation*}
\begin{aligned}
\nabla &=\frac{\partial}{\partial x}\hat{e_x}+\frac{\partial}{\partial y}\hat{e_y}+\frac{\partial}{\partial z}\hat{e_z}
&=\hat{e_i}\frac{\partial}{\partial i}
&=\hat{e_i}\partial_i
\end{aligned}
\end{equation*}
$$

矢量的散度反映矢量在所研究点附近的离散程度

$$
\begin{equation*}
\begin{aligned}
\nabla\cdot v&=\frac{\partial v_x}{\partial x}+\frac{\partial v_y}{\partial y}+\frac{\partial v_z}{\partial z}
&=\partial_i v_i
\end{aligned}
\end{equation*}
$$

矢量的旋度反映矢量场在所研究点的周围多大程度弯曲

$$\nabla\times v=\hat{e_i}\epsilon_{ijk}\partial_j v_k=\epsilon_(ijk)\partial_iv_j\hat{e_k}$$
