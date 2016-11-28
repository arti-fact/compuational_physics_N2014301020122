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
<pre><code>
import math
import numpy as np
import pylab as pl
import time
import matplotlib.pyplot as plt
from matplotlib import animation

def cruisingx(beta,total_time,initvy):
    initx = 1
    inity = 0
    initvx = 0
    time_step = 0.0001
    x = [initx]
    y = [inity]
    vx = [initvx]
    vy = [initvy]
    dt = time_step
    tt = total_time
    r = 0.0
    cur_t = 0.0
    power = beta + 1
    while cur_t < tt:
        r = math.sqrt(x[-1] ** 2 + y[-1] ** 2)
        vx.append(vx[-1] - 4 * math.pi ** 2 * x[-1] * dt / r ** power)
        vy.append(vy[-1] - 4 * math.pi ** 2 * y[-1] * dt / r ** power)
        x.append(x[-1] + vx[-1] * dt)
        y.append(y[-1] + vy[-1] * dt)
        cur_t += dt
    return x

def cruisingy(beta,total_time,initvy):
    initx = 1
    inity = 0
    initvx = 0
    time_step = 0.0001
    x = [initx]
    y = [inity]
    vx = [initvx]
    vy = [initvy]
    dt = time_step
    tt = total_time
    r = 0.0
    cur_t = 0.0
    power = beta + 1
    while cur_t < tt:
        r = math.sqrt(x[-1] ** 2 + y[-1] ** 2)
        vx.append(vx[-1] - 4 * math.pi ** 2 * x[-1] * dt / r ** power)
        vy.append(vy[-1] - 4 * math.pi ** 2 * y[-1] * dt / r ** power)
        x.append(x[-1] + vx[-1] * dt)
        y.append(y[-1] + vy[-1] * dt)
        cur_t += dt
    return y

def exeTime(func):
    def newFunc(*args, **args2):
        t0 = time.time()
        print ("@%s, {%s} start" % (time.strftime("%X", time.localtime()), func.__name__))
        back = func(*args, **args2)
        print ("@%s, {%s} end" % (time.strftime("%X", time.localtime()), func.__name__))
        print ("@%.3fs taken for {%s}" % (time.time() - t0, func.__name__))
        return back
    return newFunc

class PlanetaryOrbit(object):
    # if no additional statement, use Astronomical Unit (AU):
    # time : year
    # distance : AU (ave distance between Sun and Earth)
    # G * M_Sun = v ** 2 * r
    # beta is the power of the distance in The Law of Attraction
    def __init__(self, initx = 1, inity = 0, initvx = 0, initvy = 1.6 * math.pi,
                 time_step = 0.0025, total_time = 1, beta = 2.5):
        self.x = []
        self.y = []
        self.dt = time_step
        self.tt = total_time
        self.vx = initvx
        self.vy = initvy
        self.r = 0.0
        self.cur_t = 0.0
        self.power = beta + 1
        self.beta = beta

    @exeTime
    def cruising(self):
        self.x = cruisingx(beta = self.power - 1,total_time = self.tt, initvy = self.vy)
        self.y = cruisingy(beta = self.power - 1,total_time = self.tt, initvy = self.vy)

    def insert_plot_data(self):
        pl.figure(figsize=(10,8), edgecolor='w')
        pl.subplots_adjust(left=0.20, right=0.83)
        pl.plot(self.x, self.y,'.',markersize=1)
        pl.plot([1.1,-1.1,-1.1,1.1],[1.1,1.1,-1.1,-1.1],'.',markersize=0.001)

    def show_plot(self):
        # pl.xlim(-1,1)
        # pl.ylim(-0.9,0.9)
        # l = []
        # for i in range(-15,20,5):
        #     l.append(i / 10)
        # pl.yticks(l)
        # pl.xticks(l)
        pl.title('Exact simulation of elliptical orbit\n$\\beta=%r , total\\_time = %r(yr), init\_vy = %r \\pi (AU/yr)$'
                 %(self.beta, self.tt, self.vy / math.pi))
        pl.axis('equal')
        pl.xlabel('x(AU)')
        pl.ylabel('y(AU)')
        pl.show()


def main2():
    planet = PlanetaryOrbit(total_time=3.27, initvy = 2* math.pi, beta = 3.1)
    planet.cruising()
    planet.insert_plot_data()
    planet.show_plot()

def main3():
    #两个球的动图
    planet = PlanetaryOrbit(total_time=3.27, initvy = 2* math.pi, beta = 3.1)
    planet.cruising()
    fig = plt.figure()
    ax = plt.axes(title=('Simulation of elliptical orbit\n$\\beta=%r , total\\_time = %r(yr), init\_vy = %r \\pi (AU/yr)$'
                  %(planet.beta, planet.tt, planet.vy / math.pi)),
                  aspect='equal', autoscale_on=False, xlim=(-1.2,1.2),ylim=(-1.2,1.2),xlabel=('x'),ylabel=('y'))
    line1=ax.plot([],[],'b:')#初始化数据，line是轨迹，point是轨迹的头部
    point1=ax.plot([],[],'bo',markersize=10)
    sun=ax.plot([],[],'ro',markersize=20)
    edge=ax.plot([],[],'.',markersize=1.01)
    images=[]

    def init():#该函数用于初始化动画

        line1=ax.plot([],[],'b:',markersize=8)
        point1=ax.plot([],[],'bo',markersize=10)
        sun=ax.plot([],[],'ro',markersize=20)
        edge=ax.plot([],[],'.',markersize=1.01)
        return line1,point1

    # change value of speed for velocity of animation
    speed = 100
    def anmi(i):
        ax.clear()
        plt.title('Simulation of elliptical orbit\n$\\beta=%r , total\\_time = %r(yr), init\_vy = %r \\pi (AU/yr)$'
                    %(planet.beta, planet.tt, planet.vy / math.pi))
        edge = ax.plot([1.2,-1.2,-1.2,1.2],[1.2,1.2,-1.2,-1.2],'.',markersize=0.001)
        line1=ax.plot(planet.x[0:speed*i],planet.y[0:speed*i], 'r:',markersize=8)
        point1 = ax.plot(planet.x[speed*i-1:speed*i],planet.y[speed*i-1:speed*i],'bo', markersize=10)
        sun=ax.plot([0],[0],'go',markersize=20)
        return line1,point1,edge

    anmi = animation.FuncAnimation(fig, anmi, init_func=init, frames=500, interval=1, blit=False,repeat=False,)
    plt.show()

if __name__ == '__main__':
    main2()
    main3()
</code></pre>

### 图像

下图为β=3.1时，小行星轨道不断被中心的星体吸引的轨道图：
![](https://github.com/arti-fact/compuational_physics_N2014301020122/blob/master/Ex10_1.png)
动态图：
![](https://github.com/arti-fact/compuational_physics_N2014301020122/blob/master/Ex10.gif)
进一步改变β值，行星有可能开始了各种奇形怪状的运行方式：

### 结论

对于平方反比定律而言
