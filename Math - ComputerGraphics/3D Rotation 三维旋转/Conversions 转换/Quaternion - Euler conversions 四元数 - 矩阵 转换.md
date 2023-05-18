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

如果 w = 0, 无解，

如果 w 非常小，会存在数值稳定性问题。

因此，策略是决定四元数 (x, y, z or w) 存在绝对最大值(也就是无需计算平方根的) 并且永远选择那一个


<img width="800" alt="image" src="https://github.com/ChenxingWang93/Math/assets/31954987/24f1dbd9-bbf5-4f7b-9f24-c65be8ffb4b7">


``` C++
// Input matrix输入矩阵:
float m11,m12,m13;
float m21,m22,m23;
float m31,m32,m33;

// Output quaternion输出四元数
float w, x, y, z;

// Determine which of w, x, y, or z has the largest absolute value决定四元数中的哪个值存在最大绝对值
float fourWSquaredMinus1 = m11 + m22 + m33;
float fourXSquaredMinus1 = m11 − m22 − m33;
float fourYSquaredMinus1 = m22 − m11 − m33;
float fourZSquaredMinus1 = m33 − m11 − m22;

int biggestIndex = 0;
float fourBiggestSquaredMinus1 = fourWSquaredMinus1;

if(fourXSquaredMinus1 > fourBiggestSquaredMinus1) { 
        fourBigges tSquaredMinus1 = fourXSquaredMinus1;
        biggestIndex = 1;
}

if(fourYSquaredMinus1 > fourBiggestSquaredMinus1) { 
        fourBigges tSquaredMinus1 = fourYSquaredMinus1 ;
        biggestIndex = 2;
}

if(fourZSquaredMinus1 > fourBiggestSquaredMinus1) { 
        fourBiggestSquaredMinus1 = fourZSquaredMinus1 ;
        biggestIndex = 3;
}


// Perform square root and division执行平方根与除法计算
float biggestVal = sqrt(fourBiggestSquaredMinus1 + 1.0f) ∗ 0.5f;
float mult = 0.25f / biggestVal;

// Apply table to compute quaternion values计算四元数值
switch(biggestIndex) {
 
        case 0:
               w = biggestVal;
               x = (m23 − m32) ∗ mult;
               y = (m31 − m13) ∗ mult;
               z = (m12 − m21) ∗ mult;
        break;
 
        case 1:
               x = biggestVal;
               w = (m23 − m32) ∗ mult;
               y = (m12 + m21) ∗ mult;
               z = (m31 + m13) ∗ mult;
        break;
 
        case 2:
               y = biggestVal;
               w = (m31 − m13) ∗ mult;
               x = (m12 + m21) ∗ mult;
               z = (m23 + m32) ∗ mult;
        break;
 
        case 3:
               z = biggestVal;
               w = (m12 − m21) ∗ mult;
               x = (m31 + m13) ∗ mult;
               y = (m23 + m32) ∗ mult;
        break;
}
```
