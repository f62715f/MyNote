```python
# 牛顿迭代法是从曲线中的随机一点开始求导，导线与x轴的交点对应原曲线的点作为下一次要求导的点，依次类推。

# 实现代码：(求x**2-6对应的零点）

def fun():
    num = 0
    x = 2
    while True:
        f = x**2-6
        f1 = 2*x
        x = x - f/f1
        num += 1
        print(num, x)
        if abs(f) < 0.001 or num >= 100 :
            break

fun()```

```python
# e.g. 求解x**2+6*x-3的根
from sympy import *

# 首先要定義變量

x = symbols("x")
print(diff(x**2+6*x-3))

# 牛頓迭代法

x1 = float(input("你輸入一個猜測值: "))
x2 = 0
x_accuate = 0
x2 = x1 - (x1**2+6*x1-3)/(2*x1+6)
while True :
    x_accuate = x2
    x2 = x2 - (x2**2+6*x2-3)/(2*x2+6)
    print(x_accuate)
    if abs(x_accuate - x2) <= 0.000000001 :
        break
```