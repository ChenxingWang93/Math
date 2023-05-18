## Euler to matrix 欧拉到矩阵
[[Euler angles]] 定义了围绕轴进行三次简单旋转的序列 a sequence of three simple rotations around the axis. 

因此从欧拉到矩阵的转换[[Linear transformation#Rotation|basic rotations as matrices]] 然后将这三个步骤组合为一个单一的矩阵concatenate them into a single matrix

## Matrix to Euler 矩阵到欧拉
如果我们应用欧拉角，旋转应用到本地空间 **Local space** 这样一来，每个旋转都会影响下一个

为防止类似的事情发生，我们只使用[[Euler angles|fixed axes]] doing the rotations in the reverse order: 

而不是使用 **heading**, **pitch**, **bank**, 

**bank**, **pitch**, **heading**.

matrix rotations -> Eular angles 使用 2 个假设作为出发点：

```
infinite Euler angles 代表一个给定的 angular displacement


```
