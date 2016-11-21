# Exercise 9
##problem 3.30

### 公式分析

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;洛伦茨吸引子是洛伦茨振子（Lorenz oscillator）的长期行为对应的分形结构，以爱德华·诺顿·洛伦茨的姓氏命名。洛伦茨振子是能产生混沌流的三维动力系统，是一种吸引子，以其双纽线形状而著称。映射展示出动力系统（三维系统的三个变量）的状态是如何以一种复杂且不重复的模式，随时间的推移而演变的。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;洛伦茨吸引子及其导出的方程组是由爱德华·诺顿·洛伦茨于1963年发表，最初是发表在《大气科学杂志》（Journal of the Atmospheric Sciences）杂志的论文《Deterministic Nonperiodic Flow》中提出的，是由大气方程中出现的对流卷方程简化得到的。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这一洛伦茨模型不只对非线性数学有重要性，对于气候和天气预报来说也有着重要的含义。行星和恒星大气可能会表现出多种不同的准周期状态，这些准周期状态虽然是完全确定的，但却容易发生突变，看起来似乎是随机变化的，而模型对此现象有明确的表述。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;从技术角度看来，洛伦茨振子具有非线性、三维性和确定性。2001年，沃里克·塔克尔（Warwick Tucker）证明出在一组确定的参数下，系统会表现出混沌行为，显示出人们今天所知的奇异吸引子。这样的奇异吸引子是豪斯多夫维数在2与3之间的分形。彼得·格拉斯伯格（Peter Grassberger）已于1983年估算出豪斯多夫维数为2.06 ± 0.01，而关联维数为2.05 ± 0.01。

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/1.gif?raw=true" alt="" title="" />
</div>

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/Free-Converter.com-lorenz_attractor_boxed-12480943.png?raw=true" alt="" title="" />
</div>

<div align=center>
洛伦茨方程的一条轨迹的三维结构
</div>

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/1.jpg?raw=true" alt="" title="" />
</div>

<div align=center>
Paul Bourke作出的洛伦兹吸引子的3D图象
</div>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;台球动力系统是一个粒子沿直线匀速运动并在边界发生镜面反射的动力系统。当粒子击中边界发生反射时它不会损失动能。台球动力系统是哈密顿理想化的台球游戏，但其边界可以是矩形等其他形状，甚至可以是多维的。台球动力系统也可以被用于研究非欧几何。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;台球动力系统拥有哈密顿系统从可积性到混沌运动的所有复杂性，无须对运动方程进行困难的积分就可确定其庞加莱截面。乔治·大卫·比尔霍夫证明一个椭圆边界的台球动力系统是可积的。

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/maxresdefault.jpg?raw=true" alt="" title="" />
</div>

<div align=center>
 台球动力系统示意图
</div>

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/longorbit.jpg" alt="" title="" />
</div>

<div align=center>
一个混沌台球动力系统中粒子的轨迹
</div>

<div align=center>
<img src="https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/4-Figure4-1.png?raw=true" alt="" title="" />
</div>

<div align=center>
 其它形状边界的台球动力系统
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;我们对速度进行分解可得

<div align=center>
<a href="http://www.codecogs.com/eqnedit.php?latex=\vec{v}_{i,\perp&space;}=\left&space;(&space;\vec{v}_{i}\cdot&space;\hat{n}&space;\right&space;)&space;\hat{n}" target="_blank"><img src="http://latex.codecogs.com/gif.latex?\vec{v}_{i,\perp&space;}=\left&space;(&space;\vec{v}_{i}\cdot&space;\hat{n}&space;\right&space;)&space;\hat{n}" title="\vec{v}_{i,\perp }=\left ( \vec{v}_{i}\cdot \hat{n} \right ) \hat{n}" /></a>
</div>


<div align=center>
<a href="http://www.codecogs.com/eqnedit.php?latex=\vec{v}_{i,\parallel&space;}=\vec{v}_{i}-\vec{v}_{i,\perp&space;}" target="_blank"><img src="http://latex.codecogs.com/gif.latex?\vec{v}_{i,\parallel&space;}=\vec{v}_{i}-\vec{v}_{i,\perp&space;}" title="\vec{v}_{i,\parallel }=\vec{v}_{i}-\vec{v}_{i,\perp }" /></a>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;当粒子撞击边界时有

<div align=center>
<a href="http://www.codecogs.com/eqnedit.php?latex=\vec{v}_{f,\perp&space;}=-\vec{v}_{f,\perp&space;}" target="_blank"><img src="http://latex.codecogs.com/gif.latex?\vec{v}_{f,\perp&space;}=-\vec{v}_{f,\perp&space;}" title="\vec{v}_{f,\perp }=-\vec{v}_{f,\perp }" /></a>
</div>

<div align=center>
<a href="http://www.codecogs.com/eqnedit.php?latex=\vec{v}_{f,\parallel&space;}=\vec{v}_{f,\parallel&space;}" target="_blank"><img src="http://latex.codecogs.com/gif.latex?\vec{v}_{f,\parallel&space;}=\vec{v}_{f,\parallel&space;}" title="\vec{v}_{f,\parallel }=\vec{v}_{f,\parallel }" /></a>
</div>

### 代码

<pre><code>
import math

class stadium_billiard:
    def __init__(self, vx_initial, vy_initial, x_initial, y_initial, time_interval, total_time, alpha):
        self.vx = [vx_initial]
        self.vy = [vy_initial]
        self.x = [x_initial]
        self.y = [y_initial]
        self.t = [0]
        self.dt = time_interval
        self.alpha = alpha
        self.steps = int(total_time // time_interval) + 1
    def calculate(self):
        for i in range(self.steps):
            new_y = self.y[i] + self.vy[i] * self.dt
            new_x = self.x[i] + self.vx[i] * self.dt
            if new_y <= self.alpha and new_y >= -self.alpha:
                if new_x > 1 :
                    new_x = self.x[i] + self.vx[i] * self.dt / 100
                    new_y = self.y[i] + self.vy[i] * self.dt / 100
                    time_interval_revised = self.dt / 100
                    while new_x < 1:
                        new_x = new_x + self.vx[i] * self.dt / 100
                        new_y = new_y + self.vy[i] * self.dt / 100
                        time_interval_revised = time_interval_revised + self.dt / 100
                    v_vertical_in_x = self.vx[i]
                    v_vertical_in_y = 0
                    v_parallel_in_x = 0
                    v_parallel_in_y = self.vy[i]
                    v_vertical_out_x = -self.vx[i]
                    v_vertical_out_y = 0
                    v_parallel_out_x = 0
                    v_parallel_out_y = self.vy[i]
                    self.x.append(new_x)
                    self.y.append(new_y)
                    self.vx.append(v_vertical_out_x + v_parallel_out_x)
                    self.vy.append(v_vertical_out_y + v_parallel_out_y)
                    self.t.append(self.t[i] + time_interval_revised)
                elif new_x < -1:
                    new_x = self.x[i] + self.vx[i] * self.dt / 100
                    new_y = self.y[i] + self.vy[i] * self.dt / 100
                    time_interval_revised = self.dt / 100
                    while new_x > -1:
                        new_x = new_x + self.vx[i] * self.dt / 100
                        new_y = new_y + self.vy[i] * self.dt / 100
                        time_interval_revised = time_interval_revised + self.dt / 100
                    v_vertical_in_x = self.vx[i]
                    v_vertical_in_y = 0
                    v_parallel_in_x = 0
                    v_parallel_in_y = self.vy[i]
                    v_vertical_out_x = -self.vx[i]
                    v_vertical_out_y = 0
                    v_parallel_out_x = 0
                    v_parallel_out_y = self.vy[i]
                    self.x.append(new_x)
                    self.y.append(new_y)
                    self.vx.append(v_vertical_out_x + v_parallel_out_x)
                    self.vy.append(v_vertical_out_y + v_parallel_out_y)
                    self.t.append(self.t[i] + time_interval_revised)
                else:
                    self.x.append(new_x)
                    self.y.append(new_y)
                    self.vx.append(self.vx[i])
                    self.vy.append(self.vy[i])
                    self.t.append(self.t[i] + self.dt)
            elif new_y > self.alpha:
                if (new_x ** 2 + (new_y - self.alpha) ** 2) > 1:
                    new_x = self.x[i] + self.vx[i] * self.dt / 100
                    new_y = self.y[i] + self.vy[i] * self.dt / 100
                    time_interval_revised = self.dt / 100
                    while (new_x) ** 2 + (new_y - self.alpha) ** 2 < 1:
                        new_x = new_x + self.vx[i] * self.dt / 100
                        new_y = new_y + self.vy[i] * self.dt / 100
                        time_interval_revised = time_interval_revised + self.dt / 100
                    r = math.sqrt((new_x) ** 2 + (new_y - self.alpha) ** 2)
                    dot_product = self.vx[i] * (-new_x / r) + self.vy[i] * (self.alpha - new_y) / r
                    v_vertical_in_x = dot_product * (-new_x) / r
                    v_vertical_in_y = dot_product * (self.alpha - new_y) / r
                    v_parallel_in_x = self.vx[i] - v_vertical_in_x
                    v_parallel_in_y = self.vy[i] - v_vertical_in_y
                    v_vertical_out_x = -v_vertical_in_x
                    v_vertical_out_y = -v_vertical_in_y
                    v_parallel_out_x = v_parallel_in_x
                    v_parallel_out_y = v_parallel_in_y
                    self.x.append(new_x)
                    self.y.append(new_y)
                    self.vx.append(v_vertical_out_x + v_parallel_out_x)
                    self.vy.append(v_vertical_out_y + v_parallel_out_y)
                    self.t.append(self.t[i] + time_interval_revised)
                else:
                    self.x.append(new_x)
                    self.y.append(new_y)
                    self.vx.append(self.vx[i])
                    self.vy.append(self.vy[i])
                    self.t.append(self.t[i] + self.dt)
            elif new_y < -self.alpha:
                if (new_x ** 2 + (new_y - self.alpha) ** 2) > 1:
                    new_x = self.x[i] + self.vx[i] * self.dt / 100
                    new_y = self.y[i] + self.vy[i] * self.dt / 100
                    time_interval_revised = self.dt / 100
                    while new_x ** 2 + (new_y - self.alpha) ** 2 < 1:
                        new_x = new_x + self.vx[i] * self.dt / 100
                        new_y = new_y + self.vy[i] * self.dt / 100
                        time_interval_revised = time_interval_revised + self.dt / 100
                    r = math.sqrt((new_x) ** 2 + (new_y - self.alpha) ** 2)
                    dot_product = self.vx[i] * (-new_x / r) + self.vy[i] * (-self.alpha - new_y) / r
                    v_vertical_in_x = dot_product * (-new_x) / r
                    v_vertical_in_y = dot_product * (-self.alpha - new_y) / r
                    v_parallel_in_x = self.vx[i] - v_vertical_in_x
                    v_parallel_in_y = self.vy[i] - v_vertical_in_y
                    v_vertical_out_x = -v_vertical_in_x
                    v_vertical_out_y = -v_vertical_in_y
                    v_parallel_out_x = v_parallel_in_x
                    v_parallel_out_y = v_parallel_in_y
                    self.x.append(new_x)
                    self.y.append(new_y)
                    self.vx.append(v_vertical_out_x + v_parallel_out_x)
                    self.vy.append(v_vertical_out_y + v_parallel_out_y)
                    self.t.append(self.t[i] + time_interval_revised)
                else:
                    self.x.append(new_x)
                    self.y.append(new_y)
                    self.vx.append(self.vx[i])
                    self.vy.append(self.vy[i])
                    self.t.append(self.t[i] + self.dt)


t1 = stadium_billiard(vx_initial = 0.1, vy_initial = 0.2, x_initial = 0.01, y_initial = 0.02, time_interval = 0.01, total_time = 1500, alpha = 0.05)
t2 = stadium_billiard(vx_initial = 0.1, vy_initial = 0.2, x_initial = 0.01006, y_initial = 0.02, time_interval = 0.01, total_time = 1500, alpha = 0.05)
t1.calculate()
t2.calculate()

d = []
for i in range(len(t1.x)):
    d.append(math.sqrt((t1.x[i]-t2.x[i]) ** 2) + (t1.y[i] - t2.y[i]) ** 2)

d_log = []
for i in range(len(t1.x)):
    d_log.append(math.log(d[i]))
</code></pre>

<a href="http://www.codecogs.com/eqnedit.php?latex=\odot&space;\alpha&space;=0.05,\lambda&space;\approx&space;0.01\sim&space;0.015" target="_blank"><img src="http://latex.codecogs.com/gif.latex?\odot&space;\alpha&space;=0.05,\lambda&space;\approx&space;0.01\sim&space;0.015" title="\odot \alpha =0.05,\lambda \approx 0.01\sim 0.015" /></a>

![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure3-1.png?raw=true)
![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure3-2.png?raw=true)
![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure3-3.png?raw=true)
![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure3-4.png?raw=true)

<a href="http://www.codecogs.com/eqnedit.php?latex=\odot&space;\alpha&space;=0.01,\lambda&space;\approx&space;0.006\sim&space;0.012" target="_blank"><img src="http://latex.codecogs.com/gif.latex?\odot&space;\alpha&space;=0.01,\lambda&space;\approx&space;0.006\sim&space;0.012" title="\odot \alpha =0.01,\lambda \approx 0.006\sim 0.012" /></a>

![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure1-1.png?raw=true)
![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure1-2.png?raw=true)
![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure1-3.png?raw=true)
![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure1-4.png?raw=true)

<a href="http://www.codecogs.com/eqnedit.php?latex=\odot&space;\alpha&space;=0.001,\lambda&space;\approx&space;0.004\sim&space;0.006" target="_blank"><img src="http://latex.codecogs.com/gif.latex?\odot&space;\alpha&space;=0.001,\lambda&space;\approx&space;0.004\sim&space;0.006" title="\odot \alpha =0.001,\lambda \approx 0.004\sim 0.006" /></a>

![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure2-1.png?raw=true)
![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure2-2.png?raw=true)
![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure2-3.png?raw=true)
![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_09/figure2-4.png?raw=true)

* **结果讨论**

1.可以看出α不同时，李雅普诺夫指数截然不同；相同α下，不同的初始距离d可能导致李雅普诺夫指数的些微不同

2.α越小曲线越密集，这说明系统经历了更多状态，可以预见，当α足够大即台球桌足够长时混沌现象可能会消失
