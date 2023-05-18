## 四元数 - 矩阵 Quaternion to matrix 

四元数到旋转矩阵的方式有很多。many ways to convert a quaternion to a rotation matrix.

最常见的方法是对式 <img width="75" alt="76bcce7c8f3bc4322de3c64d96688d4" src="https://github.com/ChenxingWang93/Math/assets/31954987/3dc90198-31dd-442e-b2f1-0adab5e0946d"> 展开 

采用四元数部件的几何解释 use the geometric interpretation of the components of the quaternion

编码后的[Axis-angle form and exponential maps|axis-angle rotation], 是任意轴的旋转rotation around the arbitrary axis

创建矩阵沿着任意轴旋转create a matrix that makes a rotation around an arbitrary axis 是由随意四元数构造的 constructed from an arbitrary quaternion <img width="125" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/42c2a187-c8bd-43bb-9958-d9cfb6857c76">


矩阵是如此的，但实际上推导过程很复杂 the deduction is convoluted
<img width="1600" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/0232cd1a-8f40-4b0d-8c0b-565fbfca3d15">

## 矩阵 - 四元数 Matrix to quaternion
从矩阵中提取四元数 extract a quaternion out of a matrix,

对上述步骤逆向工程 reverse - engineer the previous step. 得到等式

<img width="300" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/fff9f47b-3748-4917-ae87-dde5526769fd">

问题在于：如何知道取正值还是负值？因为对于四元数 <img width="70" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/14ddca63-035e-4c16-9192-bf483bc0244a">

选择四元数中的其中1个 取正值，解剩下3个，使用以下等式
<img width="150" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/5dfcb529-b0eb-42ce-9934-3caf49991a9c">

应该使用哪一个？换句话说，哪个部分应该先解？我们可以选择一个随意的(e.g. use the equation for w and then use the other 6 equations to solve for the rest),

但❕ 这个不work
