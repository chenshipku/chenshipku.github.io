---
layout:     post
title:      "量子不可克隆定理"
subtitle:   ""
date:       2017-09-11 20:40:00
author:     "陈实"
header-img: ""
catalog: true
tags:
    - QM  
---

&emsp;&emsp;量子不可克隆定理(Quantum Non-cloned Theorem)：未知量子态不可能被完全精确地复制。

&emsp;&emsp;所谓复制，指的是$$\left \vert A \right \rangle\left \vert \varphi \right \rangle \rightarrow \left \vert A_\varphi \right \rangle\left \vert \varphi \right \rangle\left \vert \varphi \right \rangle$$。其中箭头左边的$$\left \vert A \right \rangle$$是复制前的量子装置（复印机），$$\left \vert \varphi \right \rangle$$是复制前的量子态；箭头右边的$$\left \vert A_\varphi \right \rangle$$是复制后的量子装置，第一个$$\left \vert \varphi \right \rangle$$是复制后的原来量子态，第二个$$\left \vert \varphi \right \rangle$$是复制出来的量子态，完全精确复制就是这两个$$\left \vert \varphi \right \rangle$$一样。

&emsp;&emsp;下面我们以最简单的二能级体系来说明量子不可克隆定理。记态空间基矢为$$\left \vert 0 \right \rangle,\left \vert 1 \right \rangle$$
，满足正交归一性。要复制的量子态$$\left \vert \varphi \right \rangle=a\left \vert 0 \right \rangle+b\left \vert 1 \right \rangle$$,其中$$\vert a\vert^2+\vert b\vert ^2=1$$。假定两基矢能够精确复制，即$$\left \vert A \right \rangle\left \vert 0 \right \rangle\rightarrow\left \vert A_0 \right \rangle\left \vert 0 \right \rangle\left \vert 0 \right \rangle,\left \vert A \right \rangle\left \vert 1 \right \rangle\rightarrow\left \vert A_1 \right \rangle\left \vert 1 \right \rangle\left \vert 1 \right \rangle$$，所以有$$\left \vert A \right \rangle\left \vert \varphi \right \rangle=\left \vert A \right \rangle[a\left \vert 0 \right \rangle+b\left \vert 1 \right \rangle]=a\left \vert A \right \rangle\left \vert 0 \right \rangle+b\left \vert A \right \rangle\left \vert 1 \right \rangle=a\left \vert A_0 \right \rangle\left \vert 0 \right \rangle\left \vert 0 \right \rangle+b\left \vert A_1 \right \rangle\left \vert 1 \right \rangle\left \vert 1 \right \rangle$$。需要说明，第二个等号说明我们认为量子克隆为线性变换，量子不可克隆定理是建立在克隆是线性变换的基础上。

&emsp;&emsp;若$$\left \vert A_0 \right \rangle\neq\left \vert A_1 \right \rangle$$，则复制后的状态为纠缠态，无法写成$$\left \vert \varphi \right \rangle\left \vert \varphi \right \rangle$$的形式；若$$\left \vert A_0 \right \rangle=\left \vert A_1 \right \rangle$$,则$$\left \vert A \right \rangle\left \vert \varphi \right \rangle=\left \vert A_0 \right \rangle[a\left \vert 0 \right \rangle\left \vert 0 \right \rangle+b\left \vert 1 \right \rangle\left \vert 1 \right \rangle]\neq \left \vert A_0 \right \rangle[a\left \vert 0 \right \rangle+b\left \vert 1 \right \rangle] [a\left \vert 0 \right \rangle+b\left \vert 1 \right \rangle]$$。量子不可克隆定理得证。
