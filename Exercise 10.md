#Exercise 10
## 4.2 4.3
### problem 4.9

### 公式分析
#### 背景
nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1687年，物理泰斗艾萨克·牛顿在巨著《自然哲学的数学原理》里发表的万有引力定律，解释了为什么行星绕着太阳的公转运动会遵守开普勒定律。在这之后，许多科学家开始研究，当行星的运动稍许偏离了这轨道的时候，可能会发生的状况？其中一个问题为：轨道是否仍旧是闭合的？但是，经过多年的探讨，科学家都无法给出合理的解答。一直要等到1873年，法国数学家约瑟·伯特兰发表伯特兰定理，才正确地解析这问题。对于经典天体力学研究，这定理非常的重要；在宇宙遥远的那一边，万有引力的性质是否仍旧保持不变？伯特兰定理给予实验者一个精确的方法，来测试万有引力的平方反比性质。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在现代物理学里，理论物理学家发现，由于广义相对论效应，引力势轨道是非闭合的。天文学家作实验观测到，水星绕着太阳公转的椭圆轨道，其近拱点呈缓慢进动状态。所以，当涉及广义相对论的领域，伯特兰定理不成立。

* **进动**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;进动（precession）是自转物体之自转轴又绕着另一轴旋转的现象，又可称作旋进。在天文学上，又称为“岁差现象”。

常见的例子为陀螺。当其自转轴的轴线不再呈铅直时，即自转轴与对称轴不重合不平行时，会发现自转轴会沿着铅直线作旋转，此即“旋进”现象。另外的例子是地球的自转。
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;典型的岁差例子是在公元前若干世纪，3月份的平分点（即春分点）落在白羊宫与双鱼宫的交界处，于是30°的白羊宫便大致与白羊座恒星重合。但是这个框架会经历日积月累的微小变化，这种变化就物理学上称为进动，而天文学上称为岁差，它的一个中等长度的周期是25,868年，在这个时间里，地球极绕黄道极（像陀螺仪那样）缓慢旋转。每年，当太阳返回0°白羊宫时，它相对于背后群星的位置将后移约50弧秒，即约71年移动1°。

<div align=center>
<img src="https://upload.wikimedia.org/wikipedia/commons/b/bb/Precession_and_seasons_%28zh%29.jpg" alt="" title="" />
</div>

**②行星轨道的进动** 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;行星在轨道上绕行太阳的公转运动也是一种旋转的运动现象，（在这些事件中，行星和太阳结合的系统也是在旋转的。）所以行星轨道平面的转轴会随着时间产生进动。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;每颗行星椭圆轨道的长轴在他的轨道平面内也会发生进动，以回应其他行星的引力改变所施加的摄动，这称为近日点进动或是拱点进动。观察到的水星近日点进动与古典力学理论预测的数值不能吻合，每百年差了43" ，突显了爱因斯坦相对论的正确，消除了观测与理论上的歧异。

#### 公式推导
* **理论推导**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;根据牛顿万有引力定律，我们有

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_10/1111.png?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;由牛顿第二定律，可得

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_10/2.png?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在坐标(x,y)处，我们有

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_10/3.png?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;我们将行星受力分解到x方向和y方向上，从而(2)式变为

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_10/4.png?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在太阳系中，我们可得

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_10/5.png?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;我们将上述方程写成以下形式，以便进行数值求解

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_10/6.png?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;实际在太阳系中，行星轨道为椭圆轨道，我们有

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_10/7.png?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;从而半长轴a为

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_10/8.png?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在近日点和远日点分别有

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_10/9.png?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;广义相对论下万有引力公式近似为

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_10/10.png?raw=true" alt="" title="" />
</div>

### 代码

