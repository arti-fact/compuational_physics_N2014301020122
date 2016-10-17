# Exercise 5
## 2.2
### problem 2.6

###公式分析
Euler法解二阶微分方程 <br/>
 ![](http://latex.codecogs.com/gif.latex?%5Cfrac%7B%5Cpartial%5E2x%20%7D%7B%5Cpartial%20t%5E2%7D%3D0) <br/>
 ![](http://latex.codecogs.com/gif.latex?%5Cfrac%7B%5Cpartial%5E2y%20%7D%7B%5Cpartial%20t%5E2%7D%3D-g)<br/>
利用 <br/>
 ![](http://latex.codecogs.com/gif.latex?%5Cfrac%7B%5Cmathrm%7Bd%7Dx%20%7D%7B%5Cmathrm%7Bd%7D%20t%7D%3Dv_%7Bx%7D) （1） <br/>
 ![](http://latex.codecogs.com/gif.latex?%5Cfrac%7B%5Cmathrm%7Bd%7Dy%20%7D%7B%5Cmathrm%7Bd%7D%20t%7D%3Dv_%7By%7D) （2） <br/>
则可以把方程组降为四元一阶常微分方程组 <br/>
 ![](http://latex.codecogs.com/gif.latex?%5Cfrac%7B%5Cmathrm%7Bd%7Dv_%7By%7D%20%7D%7B%5Cmathrm%7Bd%7D%20t%7D%3Dg) （3） <br/>
 ![](http://latex.codecogs.com/gif.latex?%5Cfrac%7B%5Cmathrm%7Bd%7Dv_%7Bx%7D%20%7D%7B%5Cmathrm%7Bd%7D%20t%7D%3D0) （4） <br/>
之后只需用Euler法解此方程组即可

###代码（请查看raw）
import math
import matplotlib.pyplot as plt
class trajectory(object):
    def __init__(self,initial_speed):
        self.x = [[]]
        self.y = [[]]
        self.v_0 = initial_speed
        self.v_x = [[]]
        self.v_y = [[]]
        self.initial_angle = [30,35,40,45,50,55,60]
        self.delta_t = 0.1
    def calculate(self):
        g = 0.0098
        for i in self.initial_angle:
            self.x[-1].append([0])
            self.y[-1].append([0])
            self.v_x[-1].append([self.v_0 * math.cos((float(i) / 180) * math.pi)])
            self.v_y[-1].append([self.v_0 * math.sin((float(i) / 180) * math.pi)])
            while (self.y[-1][-1][-1] > 0) or (self.x[-1][-1][-1] == 0):
                self.x[-1][-1].append(self.x[-1][-1][-1] + self.v_x[-1][-1][-1] * self.delta_t)
                self.y[-1][-1].append(self.y[-1][-1][-1] + self.v_y[-1][-1][-1] * self.delta_t)
                self.v_x[-1][-1].append(self.v_x[-1][-1][-1])
                self.v_y[-1][-1].append(self.v_y[-1][-1][-1] - g * self.delta_t)
            if self.y[-1][-1][-1] < 0:
                r = - (self.y[-1][-1][-2] / self.y[-1][-1][-1])
                self.x[-1][-1][-1] = (self.x[-1][-1][-2] + r * self.x[-1][-1][-1]) / (r + 1)    
    def show_results(self):
        for i in range(len(self.initial_angle)):
            plt.plot(self.x[0][i], self.y[0][i])
            plt.annotate('%d'%self.initial_angle[i],xy=(25,6 + 2 * i))
        plt.title('Trajectory of cannon shell')
        plt.xlabel('x (km)')
        plt.ylabel('y (km)')
        plt.ylim(0,)
        plt.show()

###结果显示
![](http://latex.codecogs.com/gif.latex?v_%7Bo%7D) = 0.7km/s
![](https://github.com/arti-fact/compuational_physics_N2014301020122/blob/master/1.png)
