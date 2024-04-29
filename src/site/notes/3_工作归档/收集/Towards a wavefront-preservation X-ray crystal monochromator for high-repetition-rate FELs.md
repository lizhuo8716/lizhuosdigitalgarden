---
{"dg-publish":true,"url":null,"tags":["同步辐射","同步辐射/光学元件/硅晶体","同步辐射/光学元件/热变形","同步辐射/光学测量/波前测量","同步辐射/光学测量/斯特雷尔比Strehlratio","同步辐射/自由电子激光"],"评分":5,"类型":["论文"],"发表年份":2023,"结束时间":"2023-12-19T00:00:00.000+08:00","简单评价":"非常详细非常良心，非常需要再读几次，关于热变形的解释非常好懂","permalink":"/3_工作归档/收集/Towards a wavefront-preservation X-ray crystal monochromator for high-repetition-rate FELs/","dgPassFrontmatter":true}
---


# 原文链接：
**标题**:  Towards a wavefront-preservation X-ray crystal monochromator for high-repetition-rate FELs  
**期刊**:  Journal of Synchrotron Radiation  
**DOI**:  [10.1107/S1600577523004216](https://doi.org/10.1107/S1600577523004216)  
**来源**:  ([📖ZhangLin等, 2023](zotero://open-pdf/library/items/SRWK4ZQ5?page=1))  
**记录时间**:  2023/12/18 10:06:06


# 纲要：

# 文章摘要的翻译

激光自由电子 X 射线的波前保持对 X 射线光学的质量和性能提出了前所未有的要求。Strehl 比可以用来量化这一要求。本文制定了 X 射线光学热变形的标准，特别是对于晶体单色器。为了保持 X 射线波前，
镜子的高度误差标准偏差应该在亚纳米级别，而晶体单色器应该小于 25 皮米。
冷却硅晶体结合两种技术可以用于实现单色器晶体的这一性能水平：(1)使用聚焦元件来补偿热变形的二阶分量；
(2)在冷却块和硅晶体之间引入冷却垫，并优化有效冷却温度。
这些技术中的每一种都可以将高度误差标准偏差的热变形降低一个数量级。
以 LCLS-II-HE 动态 X 射线散射仪为例，可以实现对高热负荷单色器晶体热变形的标准，适用于 100 W SASE FEL 光束。
波前传播模拟证实了反射光束的强度分布在峰值功率密度和聚焦光束尺寸上都是令人满意的。


## 摘要翻译的信心分数
95

# 文章的关键词列表
关键词: 见文件属性

# 设备和计算方法
文章中使用的设备和计算方法包括:
1. 
2. 
3. 硅晶体单色器
4. 有限元分析 (FEA)
5. 波前传播模拟
# 标题与主要内容

## 1. 导言  1. Introduction([ZhangLin等, 2023](zotero://open-pdf/library/items/SRWK4ZQ5?page=1&annotation=XAN7BMUV))


相干 X 射线光源出现, 波前保持提出更高要求。斯特雷尔比可用于量化这一要求。
XFEL 的峰值功率已达到太瓦级，而高重复率 XFEL 的平均功率可达数百瓦。
保持相干X射线光束波前的要求带来了X射线光学方面的新工程挑战。最小化承受数十甚至数百瓦功率负载的X射线光学的热变形需要越来越创新的方法。
自20世纪80年代末和90年代初第三代同步辐射光源的出现以来，光学上的 X 射线功率负载已达到数百瓦。光学的热变形可能导致光子通量减少，发散的 X 射线光束，最终导致 X 射线光束亮度显著降低。世界各地进行了许多工程努力和倡议，以最小化或补偿 X 射线光学的热变形。为了量化热变形，即由于热负荷而导致的形状变化，通常使用光学上的热斜率误差或高度误差来表示（Zhang 等人，2014；Zhang，2018）
- [ ] 论文两篇
![Pasted image 20231218112913.png](/img/user/%E9%99%84%E4%BB%B6/%E9%99%84%E4%BB%B6%201/Pasted%20image%2020231218112913.png)


The ratio of the real versus ideal peak intensity is widely known as the Strehl ratio (Strehl, 1895, 1902). When the quality of the optics is close to perfect, the Strehl ratio tends to 1. The Strehl ratio (SR) can also be calculated based on the root mean square of the phase error (’) introduced by the non-perfect optics, and can be written as([ZhangLin等, 2023](zotero://open-pdf/library/items/SRWK4ZQ5?page=2&annotation=J25R5NYE))  [✏️批注]: 真实峰值强度与理想峰值强度的比值被广泛称为斯特雷尔比（Strehl ratio）（Strehl, 1895, 1902）。当光学器件的质量接近完美时，斯特雷尔比趋向于1。斯特雷尔比（SR）也可以基于非完美光学器件引入的相位误差（’）的均方根来计算，可以写成
![Pasted image 20231218112619.png](/img/user/%E9%99%84%E4%BB%B6/%E9%99%84%E4%BB%B6%201/Pasted%20image%2020231218112619.png)

其中，，k 和分别代表基板材料的热膨胀系数、热导率和泊松比，fgeom 是一个几何函数，取决于光学和冷却几何形状以及功率分布。
有两种方法可以减小热变形：
(1)通过改进冷却设计和光学形状来减小几何函数fgeom，以及
(2)通过选择材料和/或温度范围来减小材料性能中的优点(1 + ) /k。
目前最先进的解决方案包括：
(1)使用同步辐射X射线白光镜来减小几何函数fgeom。使用水冷却镜子的顶部，完全照亮(过度填充)镜子长度，通过切口优化镜子横截面，使用镜子下游的次级缝隙来塑造期望的最终尺寸的光束(Zhang, 2010; Zhang et al., 2013a)。
这种镜子的热斜率误差，约为800 W的吸收光束功率，可以减小到0.018 mrad。这种技术广泛应用于ESRF升级波束线和APS-U波束线上的白光镜和大多数白光或粉红光多层光学器件(X. B. Shi, 私人通信)。
相比之下，在镜子底部(与镜子光学表面相对)冷却的情况下，RMS 热斜率误差可以达到200 mrad。此外，先前还提出了具有切口结构的镜子横截面的概念(Khounsary, 1999)。

(3) 主动补偿 X 射线镜（平面或可弯曲）：压电致动器动态可弯曲镜（Susini 等，1992）或（多电极）压电双形镜（Susini 等，1995）。这些主动光学器件可以被弯曲以进行可变聚焦，或者自适应弯曲以补偿热变形。对于 Linac 相干光源（LCLS）的波前保护 X 射线镜，提出了一种主动冷却和加热技术（Zhang 等，2015），并进行了测试（Cocco 等，2020）。
这是一种新颖的主动/自适应水冷却技术——称为 REAL（可调电阻元件长度）冷却，配合施加的辅助加热，可根据入射光束产生的热负荷的空间分布进行定制。使用这种技术，我们理论上可以在高重复频率 XFEL（如 LCLS-II 和 LCLS-II-HE）上，实现具有数百瓦平均入射光束功率的 X 射线镜的亚纳米表面形状误差。



(Zhang 等, 2023, p. 688) 高度误差的要求可以作为衡量热负荷引起的热变形、抛光、制造和安装误差以及光学元件的标准。为了减小受到入射角度为和光子能量为 eph（keV）的光子束作用的 X 射线镜子的热变形，我们可以使用以下准则（Zhang 等人，2015年）：  
当光子束热负荷引起的RMS高度误差（以纳米为单位）满足以下不等式时，热变形可以最小化：  
![Pasted image 20231219074809.png](/img/user/%E9%99%84%E4%BB%B6/%E9%99%84%E4%BB%B6%201/Pasted%20image%2020231219074809.png)
  
![Pasted image 20231219075001.png](/img/user/%E9%99%84%E4%BB%B6/%E9%99%84%E4%BB%B6%201/Pasted%20image%2020231219075001.png)
对于LCLS-II软X射线（SXR）镜子，入射角度在7到30 mrad之间。对于LCLS-II-HE硬X射线（HXR）镜子，入射角度在1.4到3 mrad之间。 
图2显示了LCLS-II X射线镜子的RMS高度误差要求 h。对于更高的Strehl比要求，阈值 h应该更小。由于镜子的入射角度较小，sin ffi ，阈值 h与入射角度 和光子能量eph成反比。与SXR镜子相比，LCLS HXR镜子的较小入射角度对 h要求的影响相当大，这抵消了HXR镜子具有更高光子能量的影响。对于SXR和HXR镜子，对高度误差的要求是相似的。X射线镜子的热变形应该限制在亚纳米级别的RMS高度误差范围内。


## 2. 波前保持的光学要求

给出 X 射线光学的高度误差标准偏差要求: 镜面亚纳米级, 晶体单色器小于 25 pm。
The power load on the X-ray optics for the new coherent X-ray light sources (high-repetition-rate FEL and MBA lattice DLSR) reaches a few hundred watts.([ZhangLin等, 2023](zotero://open-pdf/library/items/SRWK4ZQ5?page=4&annotation=YS6BYKSS))
新一代相干 X 射线光源（高重复率 FEL 和 MBA 晶格 DLSR）对 X 射线光学元件的功率负载达到几百瓦。最小化 X 射线光学元件的热变形对于保持相干光束所需的波前保持至关重要。

For the crystal monochromator, cryo-cooled silicon crystals have been widely used for the third-generation synchrotron light sources. LN2 is the typical coolant used due to its high cooling capacity and better stability compared with pulse tube cryocoolers.([ZhangLin等, 2023](zotero://open-pdf/library/items/SRWK4ZQ5?page=4&annotation=I2Z2EZSQ))  [✏️批注]: 对于晶体单色器，冷冻硅晶体已经广泛应用于第三代同步辐射光源。液氮（LN2）是常用的冷却剂，因为它具有较高的冷却能力和与脉冲管制冷机相比更好的稳定性。

X 射线光束功率负载引起的温度梯度是晶体热变形的驱动力。硅的热力学性质，如热导率和热膨胀系数，是与温度相关的。硅的热膨胀系数在125 K 左右为零。晶体的最佳温度应该使得光束足迹相邻区域的温度约为125 K；最高温度应高于125 K。优化的目标函数是热变形，例如光束足迹上高度误差的标准差。




## 3. 最小化热畸变

提出通过优化有效冷却温度和补偿二阶分量来最小化热畸变。

At those crystal dimensions, the thermal deformation of the crystal does not vary with crystal size. Thermal deformation of the crystal depends on the total absorbed power, on the power distribution (Gaussian parameters)([ZhangLin等, 2023](zotero://open-pdf/library/items/SRWK4ZQ5?page=5&annotation=6TPCMF9J))
在这些晶体尺寸下，晶体的热变形与晶体尺寸无关。
晶体的热变形取决于总吸收功率、功率分布（高斯参数）和布拉格角，而这些因素都与光子能量有关。

The minimized residual height error stddUy in the (beam) horizontal direction is plotted in Fig. 7 for both cases when the cryst([ZhangLin等, 2023](zotero://open-pdf/library/items/SRWK4ZQ5?page=6&annotation=HGVTHKJB))  [✏️批注]: 当晶体的最高温度接近125 K 或晶体的最高温度与冷却温度之间的温差较小时，热变形较小。图7显示了在晶体垂直或水平取向时，在（光束）水平方向上的最小化残余高度误差 stddUy。这些结果清楚地表明，垂直取向的晶体的热变形比水平取向的晶体小。这种差异可以通过光束足迹或功率分布来解释。
光子束在水平方向上的尺寸是一个恒定的2 FWHM = 2.5 mm，并且在光子能量从6到18 keV变化时，从2 FWHM = 2.08 mm减小到0.88 mm。两种晶体取向的总功率和峰值功率密度是相同的。但是足迹形状不同：水平取向的足迹形状比垂直取向的足迹形状更加椭圆形（参见图8的光束足迹尺寸）。在相同的总功率和峰值功率密度下，足迹长度越长，子午线方向上的热变形就越高。根据图7中显示的高度误差，可以使用方程（7）计算晶体的Strehl比。结果如图9所示。与图8中晶体的热变形一致，垂直取向的晶体的Strehl比在12 keV以下几乎等于1，并且高于水平取向的晶体。在18 keV时，Strehl比非常小。这是因为在18 keV时使用了更高阶的反射晶体Si(333)。在18 keV时，光束足迹最小，功率密度最高。因此，18 keV时的热变形最高。在实际应用中，当光子能量增加时，来自LCLS-II(-HE)的FEL功率会减小。通过将18 keV时的总FEL功率从100 W减小到70 W（或吸收功率从70 W减小到50 W），可以在18 keV时实现0.9的Strehl比。


## 4. 波前传播模拟  

模拟验证优化设计的有效性。

4.1. 波前传播模拟的方法

这里使用的波前传播方法受到了Synchrotron Radiation Workshop (SRW)软件（Chubar & Celestre, 2019）的启发。该方法在光学之间进行波前传播时，严重依赖于Fresnel缩放定理，通过在解析上跟踪波前的二次部分，避免了对强相位曲率进行适当采样的需要（Paganin, 2006）。使用混合光线追踪波光学方法处理波前与光学的相互作用，利用波前曲率的知识计算给定光学上每个点的“局部”入射角度以及随后的反射或衍射；这对于非对称晶体的色散反射以及基于入射角度计算复值晶体反射率非常重要。虽然这里考虑的晶体变形的斜率误差远小于10 keV下Si(111)的达尔文宽度，但值得注意的是，晶体反射率是使用XRayTracer (xrt)光线追踪软件包（Klementiev & Chernikov, 2014）的后端函数计算的。最后，通过对结果反射的斜率误差进行数值积分，计算纳米（和皮米）尺度变形对波前的影响。用于模拟的代码可以在网上免费获取

（ https://github.com/mseaberg/lcls_beamline_toolbox ）。

Considering the relevance of the thermal deformation requirement and the Strehl ratio, the ratio of the peak intensity of the reflected beam by the crystal with aberration related to the perfect crystal is close to the Strehl ratio when the ratio of the intensities is larger than the 10%. When the Strehl ratio is small (< 0.1), the ratio of the peak intensity is no longer relevant. The Strehl ratio is calculated with a global metric of thermal deformation – the RMS height error h. However, the local thermal deformation (slope or height error) over the footprint is variable; there is always a small region around the centre of the beam footprint where the local thermal deformation is very small.([ZhangLin等, 2023](zotero://open-pdf/library/items/SRWK4ZQ5?page=7&annotation=AWBKIJTC))
  

考虑到热变形要求和Strehl比的相关性，反射光束的峰值强度与完美晶体的峰值强度之比接近于Strehl比，当强度比大于10%时。

当Strehl比较小（<0.1）时，峰值强度的比值不再相关。Strehl比是使用热变形的全局度量 - 均方根高度误差 h计算的。

然而，足迹上的局部热变形（斜率或高度误差）是可变的；在光束足迹中心周围总是存在一个非常小的区域，局部热变形非常小。





## 5. 总结

总结方法和成果, 提出后续工作。


本文重新审视了最先进的解决方案，以最小化 X 射线光学元件的热变形，详细说明了波前保持的光学要求，并制定了 X 射线光学元件（尤其是晶体单色器）的热变形标准。
这些标准可以用来指导光机械工程设计决策。对于镜子（表面形状），高度误差标准差要求为亚纳米级别，对于晶体单色器（晶体平面），要求小于25 pm。
这种前所未有的要求推动了光机械工程的努力来应对这一挑战。我们已经证明，通过优化有效冷却温度，可以最小化液氮冷却的晶体单色器的热变形。
与标准液氮冷却相比，性能可以提高一个数量级。使用动态聚焦元件（例如聚焦镜）来补偿热变形的二阶分量，我们可以将残余高度误差再降低一个数量级。
例如，对于 LCLS-II-HE DXS 仪器，可以在100 W SASE FEL 功率负载下实现 HHLM 晶体的热变形标准。
波前传播模拟证实，反射光束的强度分布在峰值功率密度和聚焦光束尺寸方面都是令人满意的。
未来的发展包括详细的工程设计，以实施晶体单色器的提议解决方案：优化有效冷却温度，补偿热变形的二阶分量，以及最小化制造/安装/冷却引起的变形。



# 图注翻译

## Fig. 1 
![Pasted image 20231218113922.png](/img/user/%E9%99%84%E4%BB%B6/%E9%99%84%E4%BB%B6%201/Pasted%20image%2020231218113922.png)
X 射线镜面的高度误差示意图以及对 X 射线束相位误差的影响

## Fig. 2

LCLS X 射线镜面在不同入射角下的高度误差要求

## Fig. 3

(a) 晶体的高度误差要求与斯特雷尔比的关系图 (b) 三种硅晶体在不同光子能量下的布拉格角

## Fig. 4  

动态 X 射线散射光学布局示意图 (俯视)

## Fig. 5  

第一块晶体的有限元模型, 加载高斯功率分布 

## Fig. 6  

四个典型光子能量情况下, 残余高度误差随有效冷却温度的变化曲线图

## Fig. 7  

优化有效冷却温度后, 晶体在水平方向的最小残余高度误差

## Fig. 8

垂直和水平定向晶体的光束足迹参数 

## Fig. 9  

晶体在垂直和水平定向下的斯特雷尔比值

## Fig. 10  

四种情况下的光栅衍射波前在焦点位置的归一化强度分布图



