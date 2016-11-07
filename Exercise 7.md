# Exercise 7
## 3.3
### problem 3.12 3.13 3.14

### 公式分析
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


###代码
<pre><code>
import pylab as pl
import math  as mt
g=9.8
l=9.8
q=0.5
ou_d=1/3

'''
print('The l ->')
l=float(input())
print('The q ->')
q=float(input())
print('The ou_d ->')
ou_d=float(input())
print('F_D->')
F_D=float(input())
print('theta->')
theta=float(input())
'''

class pendulum:
    def __init__(self,F_D,theta):
        self.theta=[theta]
        self.omiga=[0]
        self.t=[0]
        self.dt=0.02
        self.F_D=F_D
    def run(self):

        while self.t[-1]<60:
            omiga_new=self.omiga[-1]-((g/l)*mt.sin(self.theta[-1])+q*self.omiga[-1]-self.F_D*mt.sin(ou_d*self.t[-1]))*self.dt
            self.omiga.append(omiga_new)
            theta_new=(self.theta[-1]+self.omiga[-1]*self.dt)
            if theta_new>mt.pi:
                theta_new=theta_new-2*mt.pi
            if theta_new<-(mt.pi):
                theta_new=theta_new+2*mt.pi
            self.theta.append(theta_new)
            t_new=self.t[-1]+self.dt
            self.t.append(t_new)



sub1=pl.subplot(251)
A=pendulum(0,0.2)
A.run()
sub1.plot(A.t,A.theta,'b',label='$F_D=0$')
sub1.set_title('$θ$ versus time')
sub1.legend(loc="upper right",frameon=False)
pl.ylabel('$θ$(radians)')
pl.xlabel('time(s)')

sub2=pl.subplot(252)
A=pendulum(0.5,0.2)
A.run()
sub2.plot(A.t,A.theta,'b',label='$F_D=0.5$')
sub2.set_title('$θ$ versus time')
sub2.legend(loc="upper right",frameon=False)
pl.ylabel('$θ$(radians)')
pl.xlabel('time(s)')

sub3=pl.subplot(253)
A=pendulum(1.0,0.2)
A.run()
sub3.plot(A.t,A.theta,'b',label='$F_D=1.0$')
sub3.set_title('$θ$ versus time')
sub3.legend(loc="upper right",frameon=False)
pl.ylabel('$θ$(radians)')
pl.xlabel('time(s)')

sub4=pl.subplot(254)
A=pendulum(1.5,0.2)
A.run()
sub4.plot(A.t,A.theta,'b',label='$F_D=1.5$')
sub4.set_title('$θ$ versus time')
sub4.legend(loc="upper right",frameon=False)
pl.ylabel('$θ$(radians)')
pl.xlabel('time(s)')

sub5=pl.subplot(255)
A=pendulum(2.0,0.2)
A.run()
sub5.plot(A.t,A.theta,'b',label='$F_D=2.0$')
sub5.set_title('$θ$ versus time')
sub5.legend(loc="upper right",frameon=False)
pl.ylabel('$θ$(radians)')
pl.xlabel('time(s)')

sub6=pl.subplot(256)
A=pendulum(0,0.2)
A.run()
sub6.plot(A.t,A.omiga,'r',label='$F_D=0$')
sub6.set_title('$θ$ versus time')
sub6.legend(loc="upper right",frameon=False)
pl.ylabel('$θ$(radians)')
pl.xlabel('time(s)')

sub7=pl.subplot(257)
A=pendulum(0.5,0.2)
A.run()
sub7.plot(A.t,A.omiga,'r',label='$F_D=0.5$')
sub7.set_title('$θ$ versus time')
sub7.legend(loc="upper right",frameon=False)
pl.ylabel('$θ$(radians)')
pl.xlabel('time(s)')

sub8=pl.subplot(258)
A=pendulum(1.0,0.2)
A.run()
sub8.plot(A.t,A.omiga,'r',label='$F_D=1.0$')
sub8.set_title('$θ$ versus time')
sub8.legend(loc="upper right",frameon=False)
pl.ylabel('$θ$(radians)')
pl.xlabel('time(s)')

sub9=pl.subplot(259)
A=pendulum(1.5,0.2)
A.run()
sub9.plot(A.t,A.omiga,'r',label='$F_D=1.5$')
sub9.set_title('$θ$ versus time')
sub9.legend(loc="upper right",frameon=False)
pl.ylabel('$θ$(radians)')
pl.xlabel('time(s)')

sub10=pl.subplot(2,5,10)
A=pendulum(2.0,0.2)
A.run()
sub10.plot(A.t,A.omiga,'r',label='$F_D=2.0$')
sub10.set_title('$θ$ versus time')
sub10.legend(loc="upper right",frameon=False)
pl.ylabel('$θ$(radians)')
pl.xlabel('time(s)')

pl.show()
</code></pre>

###图像
![](https://github.com/arti-fact/compuational_physics_N2014301020122/blob/master/figure_1.png)

##3.12
首先，我们画出一般的庞加莱截面图


###代码
<pre><code>
import pylab as pl
import math  as mt
g=9.8
l=9.8
q=0.5
ou_d=2/3
class pendulum:
    def __init__(self,F_D,theta):
        self.theta=[theta]
        self.omiga=[0]
        self.t=[0]
        self.dt=0.04
        self.F_D=F_D
    def run(self):
        while self.t[-1]<60:
            omiga_new=self.omiga[-1]-((g/l)*mt.sin(self.theta[-1])+q*self.omiga[-1]-self.F_D*mt.sin(ou_d*self.t[-1]))*self.dt
            self.omiga.append(omiga_new)
            theta_new=(self.theta[-1]+self.omiga[-1]*self.dt)
            if theta_new>mt.pi:
                theta_new=theta_new-2*mt.pi
            if theta_new<-(mt.pi):
                theta_new=theta_new+2*mt.pi
            self.theta.append(theta_new)
            t_new=self.t[-1]+self.dt
            self.t.append(t_new)


pl.subplot(121)
A = pendulum(0.5, 0.2)
A.run()
pl.plot(A.theta, A.omiga, 'y.', label='$F_D=0.5$')
pl.title('$ω$ versus $θ$')
pl.legend(loc="upper right", frameon=False)
pl.xlabel('$θ$(radians)')
pl.ylabel('$ω$(radians/s)')

pl.subplot(122)
A = pendulum(1.1, 0.2)
A.run()
pl.plot(A.theta, A.omiga, 'y.', label='$F_D=1.1$')
pl.title('$ω$ versus $θ$')
pl.legend(loc="upper right", frameon=False)
pl.xlabel('$θ$(radians)')
pl.ylabel('$ω$(radians/s)')

pl.show()
</code></pre>

###图像
![](https://github.com/arti-fact/compuational_physics_N2014301020122/blob/master/e7——figure_2.png)

###当FD=0.5时，庞加莱界面上大致是一封闭曲线，可以认为运动是准周期的
###当FD=1.1时，庞加莱截面上是一些成片的具有分形结构的密集点，运动变为混沌的

按题目要求，我们选取特定相位附近，得到
<pre><code>
import math
import matplotlib.pyplot as py

g = 9.8
l = 9.8
q = 0.5
ou_D = 2 / 3


class pendulum0:
    def __init__(self, F_D, sita):
        self.sita = [sita]
        self.omiga = [0]
        self.t = [0]
        self.dt = 0.04
        self.F_D = F_D
        self.omiga2 = []
        self.sita2 = []

    def calculate(self):
        while self.t[-1] < 5000:
            omiga_new = self.omiga[-1] - (
                                         (g / l) * (math.sin(self.sita[-1])) + q * self.omiga[-1] - self.F_D * math.sin(
                                             ou_D * self.t[-1])) * self.dt
            self.omiga.append(omiga_new)
            sita_new = self.sita[-1] + self.omiga[-1] * self.dt
            t_new = self.t[-1] + self.dt

            while sita_new > math.pi:
                sita_new -= 2 * (math.pi)
            while sita_new < -math.pi:
                sita_new += 2 * (math.pi)
            self.sita.append(sita_new)
            self.t.append(t_new)


sub1 = py.subplot(221)
A = pendulum0(1.2, 0.2)
A.calculate()
for i in range(len(A.sita)):
    a = ((2 / 3) * (A.t[i])) % (2 * (math.pi))
    if a < 0.04:
        A.sita2.append(A.sita[i])
        A.omiga2.append(A.omiga[i])
sub1.plot(A.sita2, A.omiga2, '.', label='$\Omega _{D}t≈2\pi n$')
sub1.set_title('$Ω$ versus $θ$')
sub1.legend(loc="upper right", frameon=False)
py.xlabel('$θ$(radians)')
py.ylabel('$Ω$(radians/s)')

sub2 = py.subplot(222)
A = pendulum0(1.2, 0.2)
A.calculate()
for i in range(len(A.sita)):
    a = ((2 / 3) * (A.t[i] - (3 / 8) * (math.pi))) % (2 * (math.pi))
    if a < 0.04:
        A.sita2.append(A.sita[i])
        A.omiga2.append(A.omiga[i])
sub2.plot(A.sita2, A.omiga2, '.', label='$\Omega _{D}t≈2\pi n+\pi /4$')
sub2.set_title('$Ω$ versus $θ$')
sub2.legend(loc="upper right", frameon=False)
py.xlabel('$θ$(radians)')
py.ylabel('$Ω$(radians/s)')

sub3 = py.subplot(223)
A = pendulum0(1.2, 0.2)
A.calculate()
for i in range(len(A.sita)):
    a = ((2 / 3) * (A.t[i] - (3 / 4) * (math.pi))) % (2 * (math.pi))
    if a < 0.04:
        A.sita2.append(A.sita[i])
        A.omiga2.append(A.omiga[i])
sub3.plot(A.sita2, A.omiga2, '.', label='$\Omega _{D}t≈2\pi n+\pi /2$')
sub3.set_title('$Ω$ versus $θ$')
sub3.legend(loc="upper right", frameon=False)
py.xlabel('$θ$(radians)')
py.ylabel('$Ω$(radians/s)')

sub4 = py.subplot(224)
A = pendulum0(1.2, 0.2)
A.calculate()
for i in range(len(A.sita)):
    a = ((2 / 3) * (A.t[i] - (9 / 8) * (math.pi))) % (2 * (math.pi))
    if a < 0.04:
        A.sita2.append(A.sita[i])
        A.omiga2.append(A.omiga[i])
sub4.plot(A.sita2, A.omiga2, '.', label='$\Omega _{D}t≈2\pi n+3\pi /4$')
sub4.set_title('$Ω$ versus $θ$')
sub4.legend(loc="upper right", frameon=False)
py.xlabel('$θ$(radians)')
py.ylabel('$Ω$(radians/s)')

py.show()
</code></pre>

###此时得到图像
![](https://github.com/arti-fact/compuational_physics_N2014301020122/blob/master/e7_figure_2.png)

这几张图中都能见到奇异吸引子。

##3.13 3.14
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;在此我们研究两个单摆系统，参数与之前相同，但它们的初始摆角相差0.001rad

这里我们采用龙格-库塔法
<pre><code>
import math
import matplotlib.pyplot as plt

class physical_pendulum_changing_initial_angle:
    def __init__(self, FD, total_time, time_interval, angle):
        self.FD = FD
        self.dt = time_interval
        self.steps = int(total_time // time_interval) + 1 
        self.t = [0]
        self.omega = [0]
        self.initial_theta = angle
        self.theta = [self.initial_theta]
        self.energy = [1.9144]
    def calculate(self):
        for i in range(self.steps):
            midpoint_omega = self.omega[i] + 0.5 * (-math.sin(self.theta[i]) - 0.5 * self.omega[i] + self.FD * math.sin(0.66666666667 * self.t[i])) * self.dt
            midpoint_time = self.t[i] + 0.5 * self.dt
            midpoint_theta = self.theta[i] + 0.5 * self.dt
            temporary_theta = self.theta[i] + midpoint_omega * self.dt
            temporary_omega = self.omega[i] + (-math.sin(midpoint_theta) - 0.5 * midpoint_omega + self.FD * math.sin(0.66666666667 * midpoint_time)) * self.dt
            self.theta.append(temporary_theta)
            self.omega.append(temporary_omega)
            self.t.append(self.t[i] + self.dt)
            self.energy.append(0.5 * 9.8 ** 2 * (temporary_omega) ** 2 + 9.8 * 9.8 * (1 - math.cos(temporary_theta))) 

class physical_pendulum_changing_initial_angle_2(physical_pendulum_changing_initial_angle):
    def calculate(self):
        for i in range(self.steps):
            midpoint_omega = self.omega[i] + 0.5 * (-math.sin(self.theta[i]) - 0.56 * self.omega[i] + self.FD * math.sin(0.66666666667 * self.t[i])) * self.dt
            midpoint_time = self.t[i] + 0.5 * self.dt
            midpoint_theta = self.theta[i] + 0.5 * self.dt
            temporary_theta = self.theta[i] + midpoint_omega * self.dt
            temporary_omega = self.omega[i] + (-math.sin(midpoint_theta) - 0.56 * midpoint_omega + self.FD * math.sin(0.66666666667 * midpoint_time)) * self.dt
            self.theta.append(temporary_theta)
            self.omega.append(temporary_omega)
            self.t.append(self.t[i] + self.dt)
            self.energy.append(0.5 * 9.8 ** 2 * (temporary_omega) ** 2 + 9.8 * 9.8 * (1 - math.cos(temporary_theta)))

plt.rc('text', usetex=True)
plt.rc('font', family='serif')

p1_low_drive = physical_pendulum_changing_initial_angle(FD = 0.5, total_time = 50, time_interval = 0.01, angle = 0.2)
p2_low_drive = physical_pendulum_changing_initial_angle(FD = 0.5, total_time = 50, time_interval = 0.01, angle = 0.201)

p1_low_drive.calculate()
p2_low_drive.calculate()

angle_difference_1 =[]

for i in range(len(p2_low_drive.theta)):
    angle_difference_1.append(math.log(math.fabs(p2_low_drive.theta[i] - p1_low_drive.theta[i])))

plt.subplot(221)
plt.plot(p1_low_drive.t, angle_difference_1)
plt.title((r'$\ln \left (\Delta \theta   \right )$ versus time $F_D =0.5$ $q=0.5$'))
plt.ylabel(r'$\ln \left (\Delta \theta   \right )$ (radian)')
plt.xlabel("time (s)")
plt.xlim(0, 50)

p1_high_drive = physical_pendulum_changing_initial_angle(FD = 1.2, total_time = 150, time_interval = 0.01, angle = 0.2)
p2_high_drive = physical_pendulum_changing_initial_angle(FD = 1.2, total_time = 150, time_interval = 0.01, angle = 0.201)

p1_high_drive.calculate()
p2_high_drive.calculate()

angle_difference_2 = []

for i in range(len(p1_high_drive.theta)):
    angle_difference_2.append(math.log(math.fabs(p2_high_drive.theta[i] - p1_high_drive.theta[i])))

plt.subplot(222)
plt.plot(p1_high_drive.t, angle_difference_2)
plt.title((r'$\ln \left (\Delta \theta   \right )$ versus time $F_D =1.2$ $q=0.5$'))
plt.ylabel(r'$\ln \left (\Delta \theta   \right )$ (radian)')
plt.xlabel("time (s)")
plt.xlim(0, 150)


p1_low_drive_2 = physical_pendulum_changing_initial_angle_2(FD = 0.5, total_time = 50, time_interval = 0.01, angle = 0.2)
p2_low_drive_2 = physical_pendulum_changing_initial_angle_2(FD = 0.5, total_time = 50, time_interval = 0.01, angle = 0.201)

p1_low_drive_2.calculate()
p2_low_drive_2.calculate()

angle_difference_1_2 =[]

for i in range(len(p2_low_drive_2.theta)):
    angle_difference_1_2.append(math.log(math.fabs(p2_low_drive_2.theta[i] - p1_low_drive_2.theta[i])))

plt.subplot(223)
plt.plot(p1_low_drive_2.t, angle_difference_1_2)
plt.title((r'$\ln \left (\Delta \theta   \right )$ versus time $F_D =0.5$ $q=0.56$'))
plt.ylabel(r'$\ln \left (\Delta \theta   \right )$ (radian)')
plt.xlabel("time (s)")
plt.xlim(0, 50)

p1_high_drive_2 = physical_pendulum_changing_initial_angle_2(FD = 1.2, total_time = 150, time_interval = 0.01, angle = 0.2)
p2_high_drive_2 = physical_pendulum_changing_initial_angle_2(FD = 1.2, total_time = 150, time_interval = 0.01, angle = 0.201)

p1_high_drive_2.calculate()
p2_high_drive_2.calculate()

angle_difference_2_2 = []

for i in range(len(p1_high_drive_2.theta)):
    angle_difference_2_2.append(math.log(math.fabs(p2_high_drive_2.theta[i] - p1_high_drive_2.theta[i])))

plt.subplot(224)
plt.plot(p1_high_drive_2.t, angle_difference_2_2)
plt.title((r'$\ln \left (\Delta \theta   \right )$ versus time $F_D =1.2$ $q=0.56$'))
plt.ylabel(r'$\ln \left (\Delta \theta   \right )$ (radian)')
plt.xlabel("time (s)")
plt.xlim(0, 150)

plt.show()
</code></pre>
它们的摆角差取常用对数随时间的变化如下
![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/figure_1-2.png?raw=true)

根据![image](https://github.com/ACGNnsj/compuational_physics_N2014301020001/blob/master/Excercise_07/CodeCogsEqn%20(17).gif?raw=true)，观察得q=0.5时， 不同驱动力下对应的李雅普诺夫指数分别约为-0.25和0.1

而q=0.56时，不同驱动力下对应的李雅普诺夫指数均减小

##心得
混沌普遍存在于众多系统中，而且并非完全无法研究；它对初值十分敏感，如果需要研究混沌情况，应该特别注意初值问题。

#Acknowledgements
得到了倪世杰同学的指导
