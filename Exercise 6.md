
# Exercise 6
## 2.2
### problem 2.10

### 公式分析
利用之前作业中的Euler法解二阶微分方程，将方程进行微调，加入空气阻力与绝热方程的影响 <br/>
则可以把方程组降为四元一阶常微分方程组 <br/>
 ![](http://latex.codecogs.com/gif.latex?x_%7Bi&plus;1%7D%3Dx_%7Bi%7D&plus;v_%7Bx%2Ci%7D%5CDelta%20t) （1） <br/>
 ![](http://latex.codecogs.com/gif.latex?v_%7Bx%2Ci&plus;1%7D%3Dv_%7Bx%7D-%5Cfrac%7BB_%7B2%7Dvv_%7Bx%2Ci%7D%7D%7Bm%7D%5Cleft%20%28%201-%5Cfrac%7Bay%7D%7BT_%7B0%7D%7D%20%5Cright%20%29%5E%7B%5Calpha%20%7D%5CDelta%20t) （2） <br/>

 ![](http://latex.codecogs.com/gif.latex?y_%7Bi&plus;1%7D%3Dy_%7Bi%7D&plus;v_%7By%2Ci%7D%5CDelta%20t) （3） <br/>
 ![](http://latex.codecogs.com/gif.latex?v_%7By%2Ci&plus;1%7D%3Dv_%7By%7D-%5Cfrac%7BB_%7B2%7Dvv_%7By%2Ci%7D%7D%7Bm%7D%5Cleft%20%28%201-%5Cfrac%7Bay%7D%7BT_%7B0%7D%7D%20%5Cright%20%29%5E%7B%5Calpha%20%7D%5CDelta%20t-g%5CDelta%20t) （4） <br/>
之后只需同样用Euler法解此方程组即可


### 代码（请查看raw）
import matplotlib.pyplot as plt
import math
theta_proper=[]
#t=0
vx=[]
vy=[]
dt=0.05
v=[]
x=[]
y=[]
v_ini=700
bm=4e-5
T=200
a=6.5e-3
c=2.5
g=9.80665
target1=10000
target2_list=[-300,0,4000]
for theta in range(0,90):
    v.append(v_ini)
    vx.append(v_ini*math.cos(theta*math.pi/180)),vy.append(v_ini*math.sin(theta*math.pi/180))
    x.append(0),y.append(0)
    while x[-1]<=22000:
        vx.append(vx[-1]-bm*dt*v[-1]*vx[-1]*(1-a*y[-1]/T)**c)
        vy.append(vy[-1]-g*dt-bm*dt*v[-1]*vy[-1]*(1-a*y[-1]/T)**c)
        x.append(x[-1]+vx[-1]*dt)
        y.append(y[-1]+vy[-1]*dt)
        v.append(math.sqrt(vx[-1]**2+vy[-1]**2))
        for i in range(3):
            if math.sqrt((x[-1]-target1)**2+(y[-1]-target2_list[i]*             *2)<=50:
                print"the altitude,the proper theta:",target2_list[i],theta
                theta_proper.append(theta)
                break
