#### 矩阵的乘法 缩放/旋转/倾斜 一个几何平面 scales/rotates/skews a geometric plane
![image](https://user-images.githubusercontent.com/31954987/230701943-7295c984-409a-450f-a046-52aef55d178e.png)

#### 矩阵的乘法 组成线性运算 matrix multiplications composes linear operations
从技术正确的定义 the technically accurate definition: yes 新的矩阵由原有的函数构成 new matrix that composes the og function 然而被运算的矩阵并非线性运算 however the matrix being operated on is not a linear operation 而是一系列的向量或者点 but a set of vectors or data points 

#### 矩阵的乘法是有关信息流的 matrix multiplication is about information flow, converting data to code and back 

> ```
> 
>                               -    -
>                               |D  D|
>                               |a  a|
>                               |t  t|
>                               |a  a|
>                               -    -
>                             
> -    -      -         -     
> |    |      |Operation|
> |D  D|      |Operation|
> |a  a|      |Operation|
> |t  t|      |Operation|
> |a  a|      |Operation|
> |    |      |Operation|
> -    -      -         -
> 
> ```

把线性代数当作“数学电子表格” think of linear algebra as "math spreadsheets" 
- 我们存储信息在不同的电子表格中 store information in various spreadsheets("matrices")
- 一些数据被看作是函数来运用一些被当作数据点 some of the data are seens as functions to apply, others as data points to use
- 在理解为函数和理解为向量之间切换 swap between function & vector interpretation as needed
把数据作为几何向量，data as geometric vectors 矩阵作为构造函数 matrix as a composing functions 但本质上都是经过系统的信息流 information flowing thru a system.

#### 工程师的直觉：代码是数据是代码 Programmer‘s intuition: Code is Data is Code

#### 矩阵的移调 The Matrix Transpose

#### 矩阵的乘法与信息流相关 转换数据为代码而后转回 
