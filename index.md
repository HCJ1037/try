### [2]Electro-optic chaotic system based on the reverse-time chaos theory and a nonlinear hybrid feedback loop

[文章地址](https://www.osapublishing.org/oe/fulltext.cfm?uri=oe-24-25-28804&id=355797)

#### time delay signatures(TDS)指什么

However, distinct loop frequency peaks corresponding to the reciprocals of the delay times are often found in the chaos spectra generated with the optical feedback scheme. The periodicity and the associated time delay signatures (TDS) in the autocorrelation function and delayed mutual information deteriorate the performance of many potential applications.

#### electro-optical oscillator

光电振荡器，在微波以上频段产生超低相位噪声振荡信号。

#### Theory of reverse-time chaos

reverse-time chaos describes behaviour that differs from traditionalchaos by using the current state of the system to represent all of its paststates instead of all of its future states. Despite this difference, reverse-time chaos retains a positive Lyapunov exponent and a correspondingsensitivity to initial conditions that defines traditional chaotic systems.

### 摘要

>一种新型的光电混合混沌系统。  
移位寄存器-模拟输出，逆时混沌系统。  
隐藏延时特征。


### 1.简介


数字和模拟混沌系统优缺点。

有几种混合方案被提出并论证。

数字信号的加入减小了模拟系统的TDS，同时屏蔽数字信号的周期性。

基于混沌激光的安全通信方案，用伪二进制随机序列对相位进行调制的独立双环反馈系统。

混合混沌系统的应用。

lekda map。

光电振荡系统。

逆时混沌系统，但仍需要独立的随机或伪随机二进制源作为输入，相比传统光学混沌系统复杂度仍较低。

有文献将二进制反馈进行了集成。

本文提出了一种电光混合混沌源，结合逆时混沌和混沌反馈回路，获得高复杂度二进制序列和混沌光信号。


### 2.方案设置及原理


移位寄存器（SR）、逆时混沌发生器（RTCG：RF1+MPF））、非线性变换模块（NLTM：PD1+RF2+LD+PC+MZM）、采样量化模块（SQM）。

直接调制激光器（DML）、微波光子滤波器（MPF）。

便可产生逆时混沌信号，及其方程。

数字计算的成本可以和常规的移位寄存器一样低。

高复杂度的模拟信号与数字序列，低计算成本。

光域滤波和非线性变换都是确定过程，故模拟信号可以用已知的数字信号实现，鲁棒性。


### 3.混合系统的基本特征


MATLAB求解四阶龙格库塔。

增益G对系统进入混沌的影响，信号由双极性脉冲和本地振荡合成。

MZM的有界性，[0,γ2P2]。

X3的吸引子密度比x2大。

VPItransmissionMaker 9.0，光谱分析仪记录滤光片形状。

有效带宽


### 4.复杂度分析


Permutation entropy (PE) and Lempel-Ziv complexity (LZC)，[wiki中的LZC](https://en.wikipedia.org/wiki/Lempel-Ziv_complexity)

G>2，N增加，复杂度增加；G增大，复杂度增大；N足够大，饱和。

B增加，N饱和阈值增大，复杂度降低。

最低有效位序列的熵率更接近混沌系统的度量熵。

注意x2是数字信号，x3是模拟信号，x1为DSP输出信号.

x1的LZC可大于1；rabbit algorithm。


### 5.相关性


互相关函数（CCF），自相关函数（ACF，曲线横坐标是时间，啥子意思？）。

DMI：The method of "mutual information" is a way to determine useful delay coordinates for plotting attractors。[关于混沌与DMI](http://www.physics.emory.edu/faculty/weeks/research/tseries3.html)

SR初值的细微变化产生的序列是独立的。

关注输出序列的自相关特性。

利用TDS重建混沌载波，密钥空间维数减少；对多数光学混沌系统，固有自相关特性将导致该问题。

计算ACF与DMI，识别这种相关性。

在提出的系统中，延迟τ由SR和模拟设备的延时引起；为简化，仿真中忽略设备延时。

ACF曲线中的时间延迟点周围有一个凹陷区域，视为系统的TDS，虽然小但存在。

B大，TDS更明显。

ACF存在周期峰值，峰值间时间间隔代表单个SR信号时间偏移。

对DMI，未观察到明显的TDS。

提出了一些可行的方法消除TDS：
>数字部分：LFSR（线性反馈移位寄存器）与SR异或；异或为非线性，提高统计特征；此外从ACF图像，尽管移位寄存器带来的延迟仍存在，但TDS消失在背景中了（比较图11a与图8b，还有9，凹陷的变化，即TDS）。由于是对数字部分进行处理，未引入额外的模拟噪声，所以系统鲁棒性未受影响。

>模拟部分：两个NLTM，TDS几乎完全消失，但系统结构变复杂，且引入额外的模拟噪声。


### 6.总结


提出了集成了反转时间混沌源和混合反馈回路的混沌系统。

研究了混合系统的动力特征和参数对复杂度的影响，相关特性和TDS。

提出了两种掩盖TDS的方法。

可同时获得高度复杂的二进制序列和光学混沌信号，高动态复杂性的宽带鲁棒混沌信号。

超快光子模数转换器和光移位寄存器技术发展，该混合系统结构可以以全光方式建立，具有应用于雷达和光保密通信系统的潜力。


## HCJ
