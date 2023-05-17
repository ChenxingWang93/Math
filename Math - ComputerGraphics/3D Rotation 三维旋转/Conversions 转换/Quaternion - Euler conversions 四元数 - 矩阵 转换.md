四元数 - 矩阵 Quaternion to matrix 

四元数到旋转矩阵的方式有很多。many ways to convert a quaternion to a rotation matrix.

最常见的方法是对式 <img width="75" alt="76bcce7c8f3bc4322de3c64d96688d4" src="https://github.com/ChenxingWang93/Math/assets/31954987/3dc90198-31dd-442e-b2f1-0adab5e0946d"> 展开 

采用四元数部件的几何解释 use the geometric interpretation of the components of the quaternion

编码后的[Axis-angle form and exponential maps|axis-angle rotation], 是任意轴的旋转rotation around the arbitrary axis

创建矩阵沿着任意轴旋转create a matrix that makes a rotation around an arbitrary axis 是由随意四元数构造的 constructed from an arbitrary quaternion <img width="125" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/42c2a187-c8bd-43bb-9958-d9cfb6857c76">


矩阵是如此的，但实际上推导过程很复杂 the deduction is convoluted

