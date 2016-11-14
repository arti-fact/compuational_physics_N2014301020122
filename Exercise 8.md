# Exercise 8
## 3.4
### problem 3.18 3.19 3.20 3.21

### 公式分析

此次作业所需要的物理模型与上次作业几乎相同
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;无阻尼且摆角很小的情况下单摆的动力学方程近似为

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(1).gif?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这种情况下单摆近似地做简谐运动，有

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(3).gif?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;如果我们考虑阻尼，单摆的动力学方程会变为

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(2).gif?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;单摆将会做阻尼振动，有

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(4).gif?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;此时单摆将做振幅逐渐减小的周期性阻尼振动，经过较长时间后，振幅几乎为零，可以认为振动停止。
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;然而，如果有驱动力，单摆的运动学方程变为

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(5).gif?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;单摆做受迫振动，有

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(6).gif?raw=true" alt="" title="" />
</div>
其中<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(7).gif?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在摆角较大时，近似<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(8).gif?raw=true" alt="" title="" />不再成立，我们必须设法求解如下非线性方程

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(9).gif?raw=true" alt="" title="" />
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;我们如果依然采用欧拉法，将得到发散的解，显然这与实际不符，在此我们采用欧拉-克罗默方法求数值解，步骤如下

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(10).gif?raw=true" alt="" title="" />
</div>

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(11).gif?raw=true" alt="" title="" />
</div>

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(12).gif?raw=true" alt="" title="" />
</div>

注意，若<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(13).gif?raw=true" alt="" title="" />不在区间<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(14).gif?raw=true" alt="" title="" />内，我们须通过加或减<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(15).gif?raw=true" alt="" title="" />使其落入区间内。

### 庞加莱映射（以下来自于百科）

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在数学领域中，尤其是对动态系统的研究中，庞加莱映射，或第一次回归映射是连续动力系统的状态空间中的周期轨道与确定的低维子空间的横向交点，其中的低维子空间被称作庞加莱截面。更精确的说，对于具有初值位于庞加莱截面上的周期轨道，轨道第一次回到庞加莱截面上的交点就定义了初值的庞加莱映射，这就是第一次回归映射的由来。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;任何粒子在经历一个漫长的时间之后必然能回到其无限接近其初始位置的位置（但是不能回到原来位置，只能无限接近），尽管这个时间的长度远远超出我们所能想象，但是它必然会实现，这样一个周期就称为一个庞加莱回归。

<div align=center>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/84/Poincare_map.svg/771px-Poincare_map.svg.png" alt="" title="" />
</div>

<div align=center>
在庞加莱截面 S 上, 庞加莱映射 P 将 x 映射为 P(x).
</div>


# 老师很抱歉，我似乎在安装VPython时出现问题，请求下周补交，会在下周作业开头注明
