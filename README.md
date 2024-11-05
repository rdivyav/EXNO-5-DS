# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
plt.plot(x,y)
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('My first graph')
plt.show()
```
![image](https://github.com/user-attachments/assets/cd181963-6164-48d6-9c24-42d6dfa8b0b6)
```
import matplotlib.pyplot as plt
x1 = [1,2,3]
y1 = [2,4,1]
plt.plot (x1,y1,label="line 1")
x2 = [1,2,3]
y2 = [4,1,3]
plt.plot(x2,y2,label="line 2")
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('Two lines on same graph')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/2e29bb20-8de7-4fbd-967e-019a59dce958)
```
import matplotlib.pyplot as plt
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]
plt.plot(x,y,color='green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='blue',markersize=12)
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('Customised plot')
plt.show()
```
![image](https://github.com/user-attachments/assets/e7024e05-673a-4127-bdea-917f8348abda)


```
import matplotlib.pyplot as plt
x_values=[0,1,2,3,4,5]
y_values=[0,1,4,9,16,25]
plt.scatter(x_values,y_values,s=30,color="blue")
plt.show()
```
![image](https://github.com/user-attachments/assets/5c0a0ca4-3199-4d3d-8450-dd278318b5ee)
```
import matplotlib.pyplot as plt
x=[1,2,3,4,5,6,7,8,9,10]
y=[2,4,5,7,6,8,9,11,12,12]
plt.scatter(x,y,label='stars',color='green',s=30,marker='*')
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('My Scatter plot')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/22e4d8f4-4e84-4dad-901c-21049e2581e2)

```
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
x=np.arange(0,10)
y=np.arange(11,21)
plt.scatter(x,y,c='r')
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.title('Gaph in 2D')
plt.savefig('Test.png')
```
![image](https://github.com/user-attachments/assets/4998d3a1-bab3-478b-b9d3-ff2128e9b957)



```
y= x*x
y
```
array([ 0,  1,  4,  9, 16, 25, 36, 49, 64, 81])
```
plt.plot(x,y,'g*',linestyle='dashed',linewidth=2,markersize=12)
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.title('2D Diagram')
plt.show()
```
![image](https://github.com/user-attachments/assets/8d2e06a9-ab46-4ab8-9594-e3de3f70c3de)

```
plt.subplot(2,2,1)
plt.plot(x,y,'r--')
plt.subplot(2,2,2)
plt.plot(x,y,'g*--')
plt.subplot(2,2,3)
plt.plot(x,y,'bo')
plt.subplot(2,2,4)
plt.plot(x,y,'go')
```
![image](https://github.com/user-attachments/assets/9af4abf1-4b03-4952-8377-9b6202f9478a)


```
x=np.arange(0,4*np.pi,0.1)
y=np.sin(x)
plt.title("sine wave form")
plt.plot(x,y)
plt.show()
```
![image](https://github.com/user-attachments/assets/e14ca029-d30b-4413-9905-e05836392773)

```
import matplotlib.pyplot as plt
import numpy as np
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='blue')
plt.fill_between(x,y2,color='green')
plt.plot(x,y1,color='red')
plt.plot(x,y2,color='black')
plt.legend(['y1:y2'])
plt.show()
```
![image](https://github.com/user-attachments/assets/c6cd71b0-3d31-4d59-903d-c0aab607931a)

```
plt.stackplot(x,y1,y2,y3,labels=['Line 1','Line 2','Line 3'])
plt.legend(loc='upper left')
plt.title('Stacked Line Chart')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```
![image](https://github.com/user-attachments/assets/afc0f766-cd9b-4496-97e5-6e7e86ac7cc3)

```
import numpy as np
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline
x=np.array([1,2,3,4,5,6,7,8,9,10])
y=np.array([2,4,5,7,8,8,9,10,11,12])
spl=make_interp_spline(x,y)
x_smooth=np.linspace(x.min(),x.max(),100)
y_smooth=spl(x_smooth)
plt.plot(x,y,'o',label='data')
plt.plot(x_smooth,y_smooth,'-',label='spline')
plt.legend()
plt.show()
```
![image](https://github.com/user-attachments/assets/8bd08b5f-193e-4d17-8183-049533588ed7)

```
values=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.bar(names,values,color="green")
plt.show()
```
![image](https://github.com/user-attachments/assets/7933483e-946f-46da-8b1f-2a9e69610c9e)

```
values=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.barh(names,values,color="yellowgreen")
plt.show()
```

![image](https://github.com/user-attachments/assets/3d4d2fce-7acd-4dd5-995b-32184833dabc)

```



```





 

# Result:
 Include your result here
